---
title: Implementar campos personalizados para a aplicação móvel do Microsoft Dynamics 365 Project Timesheet em iOS e Android
description: Este tópico fornece padrões comuns para utilizar extensões para implementar campos personalizados.
author: Yowelle
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 5dae571fce746b49281587f5349774a7f2c4111b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271007"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>Implementar campos personalizados para a aplicação móvel do Microsoft Dynamics 365 Project Timesheet em iOS e Android

[!include [banner](../includes/banner.md)]

Este tópico fornece padrões comuns para utilizar extensões para implementar campos personalizados. São abordados os seguintes tópicos:

- Os vários tipos de dados suportados pela arquitetura de campos personalizados
- Como mostrar os campos só de leitura ou editáveis nas entradas da folha de horas, e guardar os valores fornecidos pelo utilizador na base de dados
- Como mostrar campos só de leitura no cabeçalho da folha de horas
- Como integrar outra lógica de negócio personalizada para introduzir valores predefinidos nos campos e fazer uma validação adicional

## <a name="audience"></a>Audiência

Este tópico destina-se aos programadores que estão a integrar os seus campos personalizados na aplicação móvel do Microsoft Dynamics 365 Project Timesheet que está disponível para Apple iOS e Google Android. O pressuposto é que os leitores estejam familiarizados com a programação em X++ e a funcionalidade de folha de horas do projeto.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>Contrato de dados: classe TSTimesheetCustomField X++

A classe **TSTimesheetCustomField** é a classe de contrato de dados X++ que representa as informações sobre um campo personalizado para a funcionalidade da folha de horas. As listas dos objetos de campo personalizados são transmitidas no contrato de dados TSTimesheetDetails e no contrato de dados TSTimesheetEntry para mostrar os campos personalizados na aplicação móvel.

- **TSTimesheetDetails**: o contrato do cabeçalho da folha de horas.
- **TSTimesheetEntry**: o contrato de transação da folha de horas. Os grupos destes objetos que têm a mesma informação do projeto e o valor **timesheetLineRecId** constituem uma linha.

### <a name="fieldbasetype-types"></a>fieldBaseType (Tipos)

A propriedade **FieldBaseType** no objeto **TsTimesheetCustom** determina o tipo de campo que aparece na aplicação. São suportados os seguintes valores **Tipos**.

| Valor Tipos | Tipo              | Notas |
|-------------|-------------------|-------|
| 0           | Cadeia (e Enumeração) | O campo aparece como um campo de texto. |
| 5           | Integer           | O valor é mostrado como um número sem casas decimais. |
| 2           | Real              | O valor é mostrado como um número com casas decimais.<p>Para mostrar o valor real como uma moeda na aplicação, utilize a propriedade **fieldExtenededType**. Pode utilizar a propriedade **numberOfDecimals** para definir o número de casas decimais que são mostradas.</p> |
| 3           | Date              | Os formatos de data são determinados pela definição **Formato de data, horas e número** do utilizador especificada em **Preferência de idioma e país/região** em **Opções do utilizador**. |
| 4           | Boolean           | |
| 15          | GUID              | |
| 17          | Int64             | |

- Se a propriedade **stringOptions** não for fornecida no objeto **TSTimesheetCustomField**, será fornecido um campo de texto livre ao utilizador.

    A propriedade **stringLength** pode ser utilizada para definir o comprimento máximo da cadeia de caracteres que os utilizadores podem introduzir.

- Se a propriedade **stringOptions** for fornecida no objeto **TSTimesheetCustomField**, esses elementos de lista são os únicos valores que os utilizadores podem selecionar através dos botões de opção.

    Neste caso, o campo de cadeia de caracteres pode funcionar como um valor de enumeração para efeitos de introdução do utilizador. Para guardar o valor na base de dados como uma enumeração, mapeie manualmente o valor da cadeia de caracteres para o valor de enumeração antes de guardar na base de dados através da cadeia de comando (consulte a secção "Utilizar a cadeia do comando na classe TSTimesheetEntryService para guardar uma entrada na folha de horas da aplicação de volta à base de dados" mais à frente neste tópico para ver um exemplo).

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

Pode utilizar esta propriedade para formatar os valores reais como moeda. Esta abordagem é aplicável apenas quando o valor **fieldBaseType** for **Real**.

- **TSCustomFieldExtendedType:None** – Não é aplicada qualquer formatação.
- **TSCustomFieldExtendedType::Currency** – Formatar o valor como moeda.

    Quando a formatação da moeda estiver ativa, o campo **stringValue** poderá ser utilizado para transmitir o código de moeda que deve ser mostrado na aplicação. O valor é um valor só de leitura.

    O campo **realValue** contém o montante em dinheiro que deve ser guardado na base de dados.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

Pode utilizar esta propriedade para especificar onde o campo personalizado deve aparecer na aplicação.

- **TSCustomFieldSection::Header** – O campo aparecerá na secção na secção **Ver mais detalhes** na aplicação. Estes campos são sempre só de leitura.
- **TSCustomFieldSection::Line** – O campo aparecerá depois de todos os campos de linha de configuração inicial nas entradas da folha de horas. Estes campos podem ser editáveis ou só de leitura.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

Esta propriedade identifica o campo quando os valores que a aplicação fornece são guardados de volta na base de dados.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

Esta propriedade identifica o campo quando os valores que a aplicação fornece são guardados de volta na base de dados.

### <a name="iseditable-noyes"></a>isEditable (NoYes)

Defina esta propriedade como **Sim** para especificar que o campo na secção de entrada da folha de horas deve ser editável pelos utilizadores. Defina a propriedade como **Não** para tornar o campo só de leitura.

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

Defina esta propriedade como **Sim** para especificar que o campo na secção de entrada da folha de horas deve ser obrigatório.

### <a name="label-str"></a>label (str)

Esta propriedade especifica a etiqueta que é mostrada junto ao campo na aplicação.

### <a name="stringoptions-list-of-strings"></a>stringOptions (List of Strings)

Esta propriedade só é aplicável quando **fieldBaseType** estiver definido como **String**. Se **stringOptions** estiver definido, os valores da cadeia de caracteres que estão disponíveis para seleção através dos botões de opção são especificados pelas cadeias de caracteres na lista. Se não forem fornecidas cadeias de caracteres, é permitida a introdução de texto livre no campo de cadeia de caracteres (consulte a secção "Utilizar a cadeia de comando na classe TSTimesheetEntryService para guardar uma entrada da folha de horas da aplicação de volta na base de dados" mais à frente neste tópico para ver um exemplo).

### <a name="stringlength-int"></a>stringLength (int)

Esta propriedade especifica o comprimento máximo de um campo de cadeias de caracteres. Aplicável apenas quando **fieldBaseType** estiver definido como **String**.

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

Esta propriedade especifica o número de casas decimais que são mostradas para um campo real. Aplicável apenas quando **fieldBaseType** estiver definido como **Real**.

### <a name="ordersequence-int"></a>orderSequence (int)

Esta propriedade controla a ordem em que os campos personalizados são mostrados na aplicação quando é especificado mais de um campo personalizado. Os campos que têm números mais baixos são mostrados primeiro.

### <a name="booleanvalue-boolean"></a>booleanValue (boolean)

Para os campos do tipo **Booleano**, esta propriedade transmite o valor Booleano do campo entre o servidor e a aplicação.

### <a name="guidvalue-guid"></a>guidValue (guid)

Para os campos do tipo **GUID**, esta propriedade transmite o valor GUID (identificador exclusivo global) do campo entre o servidor e a aplicação.

### <a name="int64value-int64"></a>int64Value (int64)

Para os campos do tipo **Int64**, esta propriedade transmite o valor int64 do campo entre o servidor e a aplicação.

### <a name="intvalue-int"></a>intValue (int)

Para os campos do tipo **Int**, esta propriedade transmite o valor int do campo entre o servidor e a aplicação.

### <a name="realvalue-real"></a>realValue (real)

Para os campos do tipo **Real**, esta propriedade transmite o valor real do campo entre o servidor e a aplicação.

### <a name="stringvalue-str"></a>stringValue (str)

Para os campos do tipo **Cadeia de caracteres**, esta propriedade transmite o valor de cadeia de caracteres do campo entre o servidor e a aplicação. Também é utilizada para os campos do **Real** que são formatados como moeda. Para estes campos, a propriedade é utilizada para transmitir o código de moeda para a aplicação.

### <a name="datevalue-date"></a>dateValue (date)

Para os campos do tipo **Data**, esta propriedade transmite o valor de data do campo entre o servidor e a aplicação.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>Mostrar e guardar um campo personalizado na secção de entrada na folha de horas

Segue-se uma captura de ecrã de uma criação de entrada na folha de horas na aplicação móvel. Mostra os campos de configuração inicial e um campo personalizado na secção "Entrada de hora" denominada "Cadeia de teste" com um valor de enumeração de "Segunda opção" já definido.

![Campo personalizado da cadeia de teste na aplicação](media/timesheet-entry.jpg)



Segue-se uma captura de ecrã do utilizador a selecionar uma das opções de enumeração disponíveis para o campo personalizado "Cadeia de teste" na aplicação móvel.  As duas opções são "Primeira opção" e "Segunda opção" mostradas como botões de opção. A segunda opção está atualmente selecionada.

![Botões de opção para o campo personalizado da Cadeia de teste](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>Expandir a tabela TSTimesheetLine para ter um campo personalizado

Nos cenários típicos, é provável que os dados para um campo personalizado na secção de entrada na folha de horas sejam guardados na tabela TSTimesheetLine. No entanto, podem ser utilizadas outras tabelas se os dados puderem ser obtidos com base num registo TSTimesheetTrans fornecido, ou se não tiver um contexto de registo específico (por exemplo, se o campo estiver definido como só de leitura nos parâmetros do projeto).

Note que os campos personalizados não têm de ter registos de base de dados de segurança. Podem ser gerados dinamicamente com base na lógica X++. Esta abordagem pode ser útil nos cenários só de leitura (consulte a secção “Utilizar a cadeia de comando na classe TSTimesheetDetails, método buildCustomFieldListForHeader para preencher os detalhes da folha de cálculo” para ver um exemplo de valores de campos personalizados gerados dinamicamente.)

Segue-se uma imagem do Visual Studio da Árvore de Objetos da Aplicação. Mostra uma extensão da tabela TSTimesheetLine com o campo TestLineString adicionado como campo personalizado.

![Cadeia de linha](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>Utilizar a cadeia de comando no método buildCustomFieldList da classe TSTimesheetSettings para mostrar um campo na secção de entrada na folha de horas

Este código controla as definições de visualização para o campo na aplicação. Por exemplo, controla o tipo de campo, a etiqueta, se o campo é obrigatório e em que secção o campo aparece.

O exemplo seguinte mostra um campo de cadeia nas entradas de horas. Este campo tem duas opções, **Primeira opção** e **Segunda opção**, que estão disponíveis através de botões de opção. O campo na aplicação está associado ao campo **TestLineString** que é adicionado à tabela TSTimesheetLine.

Tenha em conta que a utilização do método **TSTimesheetCustomField::newFromMetatdata()** para simplificar a inicialização das propriedades do campo personalizado: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** e **numberOfDecimals**. Também pode definir estes parâmetros manualmente, como preferir.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>Utilizar a cadeia de comando no método buildCustomFieldListForEntry da classe TSTimesheetEntry para introduzir valores numa entrada na folha de horas

O método **buildCustomFieldListForEntry** é utilizado para introduzir valores nas linhas da folha de horas guardadas na aplicação móvel. Assume um registo TSTimesheetTrans como parâmetro. Os campos desse registo podem ser utilizados para preencher o valor de campo personalizado na aplicação.

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>Utilizar a cadeia de comando na classe TSTimesheetEntryService para guardar a entrada na folha de horas da aplicação na base de dados

Para guardar um campo personalizado de volta na base de dados em utilização típica, tem de expandir vários métodos:

- O método **timesheetLineNeedsUpdating** é utilizado para determinar se o registo de linha foi alterado pelo utilizador na aplicação e tem de ser guardado na base de dados. Se o desempenho não for uma preocupação, este método poderá ser simplificado para devolver sempre **verdadeiro**.
- Os métodos **populateTimesheetLineFromEntryDuringCreate** e **populateTimesheetLineFromEntryDuringUpdate** podem ser expandidos para introduzirem valores no registo TSTimesheetLine database a partir do registo de contrato de dados TSTimesheetEntry fornecido. No exemplo seguinte, note como o mapeamento entre o campo de base de dados e o campo de introdução é feito manualmente através do código X++.
- O método **populateTimesheetWeekFromEntry** também pode ser expandido se o campo personalizado que está mapeado para o objeto **TSTimesheetEntry** tem de ser escrito de volta na tabela de base de dados TSTimesheetLineweek.

> [!NOTE]
> O exemplo seguinte guarda o valor **firstOption** ou **secondOption** que o utilizador seleciona para a base de dados como um valor de cadeia sem formato. Se o campo da base de dados for um campo do tipo **Enumeração**, esses valores podem ser mapeados manualmente para um valor de enumeração e, depois, guardados para um campo de enumeração na tabela de base de dados.

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>Mostrar um campo personalizado na secção de cabeçalho da folha de horas

Segue-se uma captura de ecrã de um utilizador a ver uma folha de horas na aplicação móvel. O botão "Mais informações" foi selecionado no canto superior direito para mostrar a opção "Ver mais detalhes".  

![Comando Ver mais detalhes](media/show-more.png)

Segue-se uma captura de ecrã da aplicação móvel a mostrar a secção "Mais". Um campo personalizado denominado "Taxa de utilização desta folha de horas (campo personalizado calculado)" foi adicionado à secção de cabeçalho da folha de horas. Um valor só de leitura de "0,667" é definido no campo personalizado.

![Secção Mais](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>Expandir a tabela TSTimesheetTable para ter um campo personalizado

Nos cenários típicos, é provável que os dados para um campo personalizado na secção de cabeçalho sejam retirados da tabela TSTimesheetHeader. No entanto, podem ser utilizadas outras tabelas se os dados puderem ser obtidos com base num registo TSTimesheetTable fornecido, ou se não tiver um contexto de registo específico (por exemplo, se o campo estiver definido como só de leitura nos parâmetros do projeto).

Note que os campos personalizados não têm de ter registos de base de dados de segurança. Podem ser gerados dinamicamente com base na lógica X++. O exemplo que se segue mostra esta abordagem.

Os campos na secção de cabeçalho são sempre só de leitura na aplicação.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>Utilizar a cadeia de comando no método buildCustomFieldList da classe TSTimesheetSettings para mostrar um campo na secção de cabeçalho

Este código controla as definições de visualização para o campo na aplicação. Por exemplo, controla o tipo de campo, a etiqueta, se o campo é obrigatório e em que secção o campo aparece.

O exemplo seguinte mostra um valor calculado na secção de cabeçalho na aplicação.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>Utilizar a cadeia de comando no método buildCustomFieldListForHeader da classe TSTimesheetDetails para preencher os detalhes da folha de horas

O método **buildCustomFieldListForHeader** é utilizado para preencher os detalhes do cabeçalho da folha de horas na aplicação móvel. Assume um registo TSTimesheetTable como parâmetro. Os campos desse registo podem ser utilizados para preencher o valor de campo personalizado na aplicação. O exemplo seguinte não lê quaisquer valores da base de dados. Em vez disso, utiliza a lógica X++ para gerar um valor calculado que depois é mostrado na aplicação.


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a>Outras oportunidades de configurabilidade/extensibilidade

### <a name="adding-additional-validation-for-the-app"></a>Adicionar validação adicional para a aplicação

A lógica existente para a funcionalidade de folha de horas a nível da base de dados continuará a funcionar conforme esperado. Para interromper a conclusão das operações de guardar ou submeter e mostrar uma mensagem de erro específica, pode adicionar **throw error("mensagem para o utilizador")** ao código através de uma extensão da cadeia de comando. Seguem-se três exemplos de métodos extensíveis úteis:

- Se **validateWrite** na tabela TSTimesheetLine devolver **falso** durante uma operação de guardar para uma linha da folha de horas, é mostrada uma mensagem de erro na aplicação móvel.
- Se **validateSubmit** na tabela TSTimesheetTable devolver **falso** durante a submissão da folha de horas na aplicação, é mostrada uma mensagem de erro ao utilizador.
- A lógica que preenche os campos (por exemplo, **Propriedade de Linha**) durante o método **insert** na tabela TSTimesheetLine continuará a ser executada.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>Ocultar e marcar os campos de configuração inicial como só de leitura através da configuração

A partir dos parâmetros do projeto, pode tornar os campos de configuração inicial só de leitura ou ocultos na aplicação móvel. Defina as opções na secção **Folhas de horas móveis** no separador **Folha de Horas** da página **Parâmetros de gestão de projetos e contabilística**.

![Parâmetros do projeto](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>Alterar as atividades que estão disponíveis para seleção através das extensões

As atividades disponíveis para seleção para um projeto são preenchidas através dos métodos **getActivitiesForProject()** e **getActivityQuery()** na classe **TsTimesheetProjectService**. Pode utilizar a cadeia de comando para alterar este comportamento para corresponder ao seu cenário de negócio para as atividades que estão disponíveis para seleção para um projeto específico.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>Introduzir uma categoria de projeto predefinida nas entradas da folha de horas

A entrada de uma categoria de projeto predefinida nas entradas da folha de horas ocorre em três níveis. Pode utilizar a cadeia de comando para expandir o comportamento em qualquer um ou em todos estes níveis para alcançar o comportamento pretendido. É utilizada a seguinte hierarquia:

1. A aplicação tenta colocar a categoria predefinida a partir do recurso do projeto. Esta categoria predefinida é definida nos métodos **getCurrentUserResource** e **getDelegatedResourcesForCurrentUser** na classe **TSTimesheetSettingsService**.
2. Se a categoria predefinida não for fornecida a nível do recurso do projeto, a aplicação tenta obtê-la a partir da atividade do projeto. Esta categoria predefinida é definida no método **getActivitiesForProject** na classe **TSTimesheetProjectService**.
3. Se a categoria predefinida não for fornecida a nível da atividade do projeto, a categoria predefinida é obtida a partir dos parâmetros do projeto. Esta categoria predefinida é definida no método **getProjectDetailsbyRule** na classe **TSTimesheetProjectService**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]