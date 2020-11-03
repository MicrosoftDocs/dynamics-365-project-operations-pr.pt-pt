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
ms.openlocfilehash: 1ea1ca002a8f68f86808831b398e452244471322
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082458"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="6f9d7-103">Implementar campos personalizados para a aplicação móvel do Microsoft Dynamics 365 Project Timesheet em iOS e Android</span><span class="sxs-lookup"><span data-stu-id="6f9d7-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6f9d7-104">Este tópico fornece padrões comuns para utilizar extensões para implementar campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="6f9d7-105">São abordados os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="6f9d7-105">The following topics are covered:</span></span>

- <span data-ttu-id="6f9d7-106">Os vários tipos de dados suportados pela arquitetura de campos personalizados</span><span class="sxs-lookup"><span data-stu-id="6f9d7-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="6f9d7-107">Como mostrar os campos só de leitura ou editáveis nas entradas da folha de horas, e guardar os valores fornecidos pelo utilizador na base de dados</span><span class="sxs-lookup"><span data-stu-id="6f9d7-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="6f9d7-108">Como mostrar campos só de leitura no cabeçalho da folha de horas</span><span class="sxs-lookup"><span data-stu-id="6f9d7-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="6f9d7-109">Como integrar outra lógica de negócio personalizada para introduzir valores predefinidos nos campos e fazer uma validação adicional</span><span class="sxs-lookup"><span data-stu-id="6f9d7-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="6f9d7-110">Audiência</span><span class="sxs-lookup"><span data-stu-id="6f9d7-110">Audience</span></span>

<span data-ttu-id="6f9d7-111">Este tópico destina-se aos programadores que estão a integrar os seus campos personalizados na aplicação móvel do Microsoft Dynamics 365 Project Timesheet que está disponível para Apple iOS e Google Android.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="6f9d7-112">O pressuposto é que os leitores estejam familiarizados com a programação em X++ e a funcionalidade de folha de horas do projeto.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="6f9d7-113">Contrato de dados: classe TSTimesheetCustomField X++</span><span class="sxs-lookup"><span data-stu-id="6f9d7-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="6f9d7-114">A classe **TSTimesheetCustomField** é a classe de contrato de dados X++ que representa as informações sobre um campo personalizado para a funcionalidade da folha de horas.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="6f9d7-115">As listas dos objetos de campo personalizados são transmitidas no contrato de dados TSTimesheetDetails e no contrato de dados TSTimesheetEntry para mostrar os campos personalizados na aplicação móvel.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="6f9d7-116">**TSTimesheetDetails** : o contrato do cabeçalho da folha de horas.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="6f9d7-117">**TSTimesheetEntry** : o contrato de transação da folha de horas.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="6f9d7-118">Os grupos destes objetos que têm a mesma informação do projeto e o valor **timesheetLineRecId** constituem uma linha.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="6f9d7-119">fieldBaseType (Tipos)</span><span class="sxs-lookup"><span data-stu-id="6f9d7-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="6f9d7-120">A propriedade **FieldBaseType** no objeto **TsTimesheetCustom** determina o tipo de campo que aparece na aplicação.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="6f9d7-121">São suportados os seguintes valores **Tipos**.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="6f9d7-122">Valor Tipos</span><span class="sxs-lookup"><span data-stu-id="6f9d7-122">Types value</span></span> | <span data-ttu-id="6f9d7-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="6f9d7-123">Type</span></span>              | <span data-ttu-id="6f9d7-124">Notas</span><span class="sxs-lookup"><span data-stu-id="6f9d7-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="6f9d7-125">0</span><span class="sxs-lookup"><span data-stu-id="6f9d7-125">0</span></span>           | <span data-ttu-id="6f9d7-126">Cadeia (e Enumeração)</span><span class="sxs-lookup"><span data-stu-id="6f9d7-126">String (and Enum)</span></span> | <span data-ttu-id="6f9d7-127">O campo aparece como um campo de texto.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="6f9d7-128">5</span><span class="sxs-lookup"><span data-stu-id="6f9d7-128">1</span></span>           | <span data-ttu-id="6f9d7-129">Integer</span><span class="sxs-lookup"><span data-stu-id="6f9d7-129">Integer</span></span>           | <span data-ttu-id="6f9d7-130">O valor é mostrado como um número sem casas decimais.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="6f9d7-131">2</span><span class="sxs-lookup"><span data-stu-id="6f9d7-131">2</span></span>           | <span data-ttu-id="6f9d7-132">Real</span><span class="sxs-lookup"><span data-stu-id="6f9d7-132">Real</span></span>              | <span data-ttu-id="6f9d7-133">O valor é mostrado como um número com casas decimais.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="6f9d7-134">Para mostrar o valor real como uma moeda na aplicação, utilize a propriedade **fieldExtenededType**.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="6f9d7-135">Pode utilizar a propriedade **numberOfDecimals** para definir o número de casas decimais que são mostradas.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="6f9d7-136">3</span><span class="sxs-lookup"><span data-stu-id="6f9d7-136">3</span></span>           | <span data-ttu-id="6f9d7-137">Date</span><span class="sxs-lookup"><span data-stu-id="6f9d7-137">Date</span></span>              | <span data-ttu-id="6f9d7-138">Os formatos de data são determinados pela definição **Formato de data, horas e número** do utilizador especificada em **Preferência de idioma e país/região** em **Opções do utilizador**.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="6f9d7-139">4</span><span class="sxs-lookup"><span data-stu-id="6f9d7-139">4</span></span>           | <span data-ttu-id="6f9d7-140">Boolean</span><span class="sxs-lookup"><span data-stu-id="6f9d7-140">Boolean</span></span>           | |
| <span data-ttu-id="6f9d7-141">15</span><span class="sxs-lookup"><span data-stu-id="6f9d7-141">15</span></span>          | <span data-ttu-id="6f9d7-142">GUID</span><span class="sxs-lookup"><span data-stu-id="6f9d7-142">GUID</span></span>              | |
| <span data-ttu-id="6f9d7-143">17</span><span class="sxs-lookup"><span data-stu-id="6f9d7-143">16</span></span>          | <span data-ttu-id="6f9d7-144">Int64</span><span class="sxs-lookup"><span data-stu-id="6f9d7-144">Int64</span></span>             | |

- <span data-ttu-id="6f9d7-145">Se a propriedade **stringOptions** não for fornecida no objeto **TSTimesheetCustomField** , será fornecido um campo de texto livre ao utilizador.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="6f9d7-146">A propriedade **stringLength** pode ser utilizada para definir o comprimento máximo da cadeia de caracteres que os utilizadores podem introduzir.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="6f9d7-147">Se a propriedade **stringOptions** for fornecida no objeto **TSTimesheetCustomField** , esses elementos de lista são os únicos valores que os utilizadores podem selecionar através dos botões de opção.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="6f9d7-148">Neste caso, o campo de cadeia de caracteres pode funcionar como um valor de enumeração para efeitos de introdução do utilizador.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="6f9d7-149">Para guardar o valor na base de dados como uma enumeração, mapeie manualmente o valor da cadeia de caracteres para o valor de enumeração antes de guardar na base de dados através da cadeia de comando (consulte a secção "Utilizar a cadeia do comando na classe TSTimesheetEntryService para guardar uma entrada na folha de horas da aplicação de volta à base de dados" mais à frente neste tópico para ver um exemplo).</span><span class="sxs-lookup"><span data-stu-id="6f9d7-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="6f9d7-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="6f9d7-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="6f9d7-151">Pode utilizar esta propriedade para formatar os valores reais como moeda.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="6f9d7-152">Esta abordagem é aplicável apenas quando o valor **fieldBaseType** for **Real**.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="6f9d7-153">**TSCustomFieldExtendedType:None** – Não é aplicada qualquer formatação.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="6f9d7-154">**TSCustomFieldExtendedType::Currency** – Formatar o valor como moeda.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="6f9d7-155">Quando a formatação da moeda estiver ativa, o campo **stringValue** poderá ser utilizado para transmitir o código de moeda que deve ser mostrado na aplicação.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="6f9d7-156">O valor é um valor só de leitura.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-156">The value is a read-only value.</span></span>

    <span data-ttu-id="6f9d7-157">O campo **realValue** contém o montante em dinheiro que deve ser guardado na base de dados.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="6f9d7-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="6f9d7-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="6f9d7-159">Pode utilizar esta propriedade para especificar onde o campo personalizado deve aparecer na aplicação.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="6f9d7-160">**TSCustomFieldSection::Header** – O campo aparecerá na secção na secção **Ver mais detalhes** na aplicação.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="6f9d7-161">Estes campos são sempre só de leitura.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-161">These fields are always read-only.</span></span>
- <span data-ttu-id="6f9d7-162">**TSCustomFieldSection::Line** – O campo aparecerá depois de todos os campos de linha de configuração inicial nas entradas da folha de horas.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="6f9d7-163">Estes campos podem ser editáveis ou só de leitura.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="6f9d7-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="6f9d7-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="6f9d7-165">Esta propriedade identifica o campo quando os valores que a aplicação fornece são guardados de volta na base de dados.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="6f9d7-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="6f9d7-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="6f9d7-167">Esta propriedade identifica o campo quando os valores que a aplicação fornece são guardados de volta na base de dados.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="6f9d7-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="6f9d7-168">isEditable (NoYes)</span></span>

<span data-ttu-id="6f9d7-169">Defina esta propriedade como **Sim** para especificar que o campo na secção de entrada da folha de horas deve ser editável pelos utilizadores.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="6f9d7-170">Defina a propriedade como **Não** para tornar o campo só de leitura.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="6f9d7-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="6f9d7-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="6f9d7-172">Defina esta propriedade como **Sim** para especificar que o campo na secção de entrada da folha de horas deve ser obrigatório.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="6f9d7-173">label (str)</span><span class="sxs-lookup"><span data-stu-id="6f9d7-173">label (str)</span></span>

<span data-ttu-id="6f9d7-174">Esta propriedade especifica a etiqueta que é mostrada junto ao campo na aplicação.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="6f9d7-175">stringOptions (List of Strings)</span><span class="sxs-lookup"><span data-stu-id="6f9d7-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="6f9d7-176">Esta propriedade só é aplicável quando **fieldBaseType** estiver definido como **String**.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="6f9d7-177">Se **stringOptions** estiver definido, os valores da cadeia de caracteres que estão disponíveis para seleção através dos botões de opção são especificados pelas cadeias de caracteres na lista.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="6f9d7-178">Se não forem fornecidas cadeias de caracteres, é permitida a introdução de texto livre no campo de cadeia de caracteres (consulte a secção "Utilizar a cadeia de comando na classe TSTimesheetEntryService para guardar uma entrada da folha de horas da aplicação de volta na base de dados" mais à frente neste tópico para ver um exemplo).</span><span class="sxs-lookup"><span data-stu-id="6f9d7-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="6f9d7-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="6f9d7-179">stringLength (int)</span></span>

<span data-ttu-id="6f9d7-180">Esta propriedade especifica o comprimento máximo de um campo de cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="6f9d7-181">Aplicável apenas quando **fieldBaseType** estiver definido como **String**.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="6f9d7-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="6f9d7-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="6f9d7-183">Esta propriedade especifica o número de casas decimais que são mostradas para um campo real.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="6f9d7-184">Aplicável apenas quando **fieldBaseType** estiver definido como **Real**.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="6f9d7-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="6f9d7-185">orderSequence (int)</span></span>

<span data-ttu-id="6f9d7-186">Esta propriedade controla a ordem em que os campos personalizados são mostrados na aplicação quando é especificado mais de um campo personalizado.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="6f9d7-187">Os campos que têm números mais baixos são mostrados primeiro.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="6f9d7-188">booleanValue (boolean)</span><span class="sxs-lookup"><span data-stu-id="6f9d7-188">booleanValue (boolean)</span></span>

<span data-ttu-id="6f9d7-189">Para os campos do tipo **Booleano** , esta propriedade transmite o valor Booleano do campo entre o servidor e a aplicação.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="6f9d7-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="6f9d7-190">guidValue (guid)</span></span>

<span data-ttu-id="6f9d7-191">Para os campos do tipo **GUID** , esta propriedade transmite o valor GUID (identificador exclusivo global) do campo entre o servidor e a aplicação.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="6f9d7-192">int64Value (int64)</span><span class="sxs-lookup"><span data-stu-id="6f9d7-192">int64Value (int64)</span></span>

<span data-ttu-id="6f9d7-193">Para os campos do tipo **Int64** , esta propriedade transmite o valor int64 do campo entre o servidor e a aplicação.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="6f9d7-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="6f9d7-194">intValue (int)</span></span>

<span data-ttu-id="6f9d7-195">Para os campos do tipo **Int** , esta propriedade transmite o valor int do campo entre o servidor e a aplicação.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="6f9d7-196">realValue (real)</span><span class="sxs-lookup"><span data-stu-id="6f9d7-196">realValue (real)</span></span>

<span data-ttu-id="6f9d7-197">Para os campos do tipo **Real** , esta propriedade transmite o valor real do campo entre o servidor e a aplicação.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="6f9d7-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="6f9d7-198">stringValue (str)</span></span>

<span data-ttu-id="6f9d7-199">Para os campos do tipo **Cadeia de caracteres** , esta propriedade transmite o valor de cadeia de caracteres do campo entre o servidor e a aplicação.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="6f9d7-200">Também é utilizada para os campos do **Real** que são formatados como moeda.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="6f9d7-201">Para estes campos, a propriedade é utilizada para transmitir o código de moeda para a aplicação.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="6f9d7-202">dateValue (date)</span><span class="sxs-lookup"><span data-stu-id="6f9d7-202">dateValue (date)</span></span>

<span data-ttu-id="6f9d7-203">Para os campos do tipo **Data** , esta propriedade transmite o valor de data do campo entre o servidor e a aplicação.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="6f9d7-204">Mostrar e guardar um campo personalizado na secção de entrada na folha de horas</span><span class="sxs-lookup"><span data-stu-id="6f9d7-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="6f9d7-205">Segue-se uma captura de ecrã de uma criação de entrada na folha de horas na aplicação móvel.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="6f9d7-206">Mostra os campos de configuração inicial e um campo personalizado na secção "Entrada de hora" denominada "Cadeia de teste" com um valor de enumeração de "Segunda opção" já definido.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![Campo personalizado da cadeia de teste na aplicação](media/timesheet-entry.jpg)



<span data-ttu-id="6f9d7-208">Segue-se uma captura de ecrã do utilizador a selecionar uma das opções de enumeração disponíveis para o campo personalizado "Cadeia de teste" na aplicação móvel.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="6f9d7-209">As duas opções são "Primeira opção" e "Segunda opção" mostradas como botões de opção.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="6f9d7-210">A segunda opção está atualmente selecionada.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-210">The second option is currently selected.</span></span>

![Botões de opção para o campo personalizado da Cadeia de teste](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="6f9d7-212">Expandir a tabela TSTimesheetLine para ter um campo personalizado</span><span class="sxs-lookup"><span data-stu-id="6f9d7-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="6f9d7-213">Nos cenários típicos, é provável que os dados para um campo personalizado na secção de entrada na folha de horas sejam guardados na tabela TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="6f9d7-214">No entanto, podem ser utilizadas outras tabelas se os dados puderem ser obtidos com base num registo TSTimesheetTrans fornecido, ou se não tiver um contexto de registo específico (por exemplo, se o campo estiver definido como só de leitura nos parâmetros do projeto).</span><span class="sxs-lookup"><span data-stu-id="6f9d7-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="6f9d7-215">Note que os campos personalizados não têm de ter registos de base de dados de segurança.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="6f9d7-216">Podem ser gerados dinamicamente com base na lógica X++.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="6f9d7-217">Esta abordagem pode ser útil nos cenários só de leitura (consulte a secção “Utilizar a cadeia de comando na classe TSTimesheetDetails, método buildCustomFieldListForHeader para preencher os detalhes da folha de cálculo” para ver um exemplo de valores de campos personalizados gerados dinamicamente.)</span><span class="sxs-lookup"><span data-stu-id="6f9d7-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="6f9d7-218">Segue-se uma imagem do Visual Studio da Árvore de Objetos da Aplicação.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="6f9d7-219">Mostra uma extensão da tabela TSTimesheetLine com o campo TestLineString adicionado como campo personalizado.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![Cadeia de linha](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="6f9d7-221">Utilizar a cadeia de comando no método buildCustomFieldList da classe TSTimesheetSettings para mostrar um campo na secção de entrada na folha de horas</span><span class="sxs-lookup"><span data-stu-id="6f9d7-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="6f9d7-222">Este código controla as definições de visualização para o campo na aplicação.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="6f9d7-223">Por exemplo, controla o tipo de campo, a etiqueta, se o campo é obrigatório e em que secção o campo aparece.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="6f9d7-224">O exemplo seguinte mostra um campo de cadeia nas entradas de horas.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="6f9d7-225">Este campo tem duas opções, **Primeira opção** e **Segunda opção** , que estão disponíveis através de botões de opção.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-225">This field has two options, **First option** and **Second option** , that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="6f9d7-226">O campo na aplicação está associado ao campo **TestLineString** que é adicionado à tabela TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="6f9d7-227">Tenha em conta que a utilização do método **TSTimesheetCustomField::newFromMetatdata()** para simplificar a inicialização das propriedades do campo personalizado: **fieldBaseType** , **tableName** , **fieldname** , **label** , **isEditable** , **isMandatory** , **stringLength** e **numberOfDecimals**.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType** , **tableName** , **fieldname** , **label** , **isEditable** , **isMandatory** , **stringLength** , and **numberOfDecimals**.</span></span> <span data-ttu-id="6f9d7-228">Também pode definir estes parâmetros manualmente, como preferir.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-228">You can also set these parameters manually, as you prefer.</span></span>

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="6f9d7-229">Utilizar a cadeia de comando no método buildCustomFieldListForEntry da classe TSTimesheetEntry para introduzir valores numa entrada na folha de horas</span><span class="sxs-lookup"><span data-stu-id="6f9d7-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="6f9d7-230">O método **buildCustomFieldListForEntry** é utilizado para introduzir valores nas linhas da folha de horas guardadas na aplicação móvel.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="6f9d7-231">Assume um registo TSTimesheetTrans como parâmetro.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="6f9d7-232">Os campos desse registo podem ser utilizados para preencher o valor de campo personalizado na aplicação.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

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

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="6f9d7-233">Utilizar a cadeia de comando na classe TSTimesheetEntryService para guardar a entrada na folha de horas da aplicação na base de dados</span><span class="sxs-lookup"><span data-stu-id="6f9d7-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="6f9d7-234">Para guardar um campo personalizado de volta na base de dados em utilização típica, tem de expandir vários métodos:</span><span class="sxs-lookup"><span data-stu-id="6f9d7-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="6f9d7-235">O método **timesheetLineNeedsUpdating** é utilizado para determinar se o registo de linha foi alterado pelo utilizador na aplicação e tem de ser guardado na base de dados.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="6f9d7-236">Se o desempenho não for uma preocupação, este método poderá ser simplificado para devolver sempre **verdadeiro**.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="6f9d7-237">Os métodos **populateTimesheetLineFromEntryDuringCreate** e **populateTimesheetLineFromEntryDuringUpdate** podem ser expandidos para introduzirem valores no registo TSTimesheetLine database a partir do registo de contrato de dados TSTimesheetEntry fornecido.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="6f9d7-238">No exemplo seguinte, note como o mapeamento entre o campo de base de dados e o campo de introdução é feito manualmente através do código X++.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="6f9d7-239">O método **populateTimesheetWeekFromEntry** também pode ser expandido se o campo personalizado que está mapeado para o objeto **TSTimesheetEntry** tem de ser escrito de volta na tabela de base de dados TSTimesheetLineweek.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="6f9d7-240">O exemplo seguinte guarda o valor **firstOption** ou **secondOption** que o utilizador seleciona para a base de dados como um valor de cadeia sem formato.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="6f9d7-241">Se o campo da base de dados for um campo do tipo **Enumeração** , esses valores podem ser mapeados manualmente para um valor de enumeração e, depois, guardados para um campo de enumeração na tabela de base de dados.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

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

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="6f9d7-242">Mostrar um campo personalizado na secção de cabeçalho da folha de horas</span><span class="sxs-lookup"><span data-stu-id="6f9d7-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="6f9d7-243">Segue-se uma captura de ecrã de um utilizador a ver uma folha de horas na aplicação móvel.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="6f9d7-244">O botão "Mais informações" foi selecionado no canto superior direito para mostrar a opção "Ver mais detalhes".</span><span class="sxs-lookup"><span data-stu-id="6f9d7-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![Comando Ver mais detalhes](media/show-more.png)

<span data-ttu-id="6f9d7-246">Segue-se uma captura de ecrã da aplicação móvel a mostrar a secção "Mais".</span><span class="sxs-lookup"><span data-stu-id="6f9d7-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="6f9d7-247">Um campo personalizado denominado "Taxa de utilização desta folha de horas (campo personalizado calculado)" foi adicionado à secção de cabeçalho da folha de horas.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="6f9d7-248">Um valor só de leitura de "0,667" é definido no campo personalizado.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-248">A read-only value of "0.667" is set on the custom field.</span></span>

![Secção Mais](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="6f9d7-250">Expandir a tabela TSTimesheetTable para ter um campo personalizado</span><span class="sxs-lookup"><span data-stu-id="6f9d7-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="6f9d7-251">Nos cenários típicos, é provável que os dados para um campo personalizado na secção de cabeçalho sejam retirados da tabela TSTimesheetHeader.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="6f9d7-252">No entanto, podem ser utilizadas outras tabelas se os dados puderem ser obtidos com base num registo TSTimesheetTable fornecido, ou se não tiver um contexto de registo específico (por exemplo, se o campo estiver definido como só de leitura nos parâmetros do projeto).</span><span class="sxs-lookup"><span data-stu-id="6f9d7-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="6f9d7-253">Note que os campos personalizados não têm de ter registos de base de dados de segurança.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="6f9d7-254">Podem ser gerados dinamicamente com base na lógica X++.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="6f9d7-255">O exemplo que se segue mostra esta abordagem.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="6f9d7-256">Os campos na secção de cabeçalho são sempre só de leitura na aplicação.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="6f9d7-257">Utilizar a cadeia de comando no método buildCustomFieldList da classe TSTimesheetSettings para mostrar um campo na secção de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6f9d7-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="6f9d7-258">Este código controla as definições de visualização para o campo na aplicação.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="6f9d7-259">Por exemplo, controla o tipo de campo, a etiqueta, se o campo é obrigatório e em que secção o campo aparece.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="6f9d7-260">O exemplo seguinte mostra um valor calculado na secção de cabeçalho na aplicação.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-260">The following example shows a computed value in the header section in the app.</span></span>

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="6f9d7-261">Utilizar a cadeia de comando no método buildCustomFieldListForHeader da classe TSTimesheetDetails para preencher os detalhes da folha de horas</span><span class="sxs-lookup"><span data-stu-id="6f9d7-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="6f9d7-262">O método **buildCustomFieldListForHeader** é utilizado para preencher os detalhes do cabeçalho da folha de horas na aplicação móvel.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="6f9d7-263">Assume um registo TSTimesheetTable como parâmetro.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="6f9d7-264">Os campos desse registo podem ser utilizados para preencher o valor de campo personalizado na aplicação.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="6f9d7-265">O exemplo seguinte não lê quaisquer valores da base de dados.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="6f9d7-266">Em vez disso, utiliza a lógica X++ para gerar um valor calculado que depois é mostrado na aplicação.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


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

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="6f9d7-267">Outras oportunidades de configurabilidade/extensibilidade</span><span class="sxs-lookup"><span data-stu-id="6f9d7-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="6f9d7-268">Adicionar validação adicional para a aplicação</span><span class="sxs-lookup"><span data-stu-id="6f9d7-268">Adding additional validation for the app</span></span>

<span data-ttu-id="6f9d7-269">A lógica existente para a funcionalidade de folha de horas a nível da base de dados continuará a funcionar conforme esperado.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="6f9d7-270">Para interromper a conclusão das operações de guardar ou submeter e mostrar uma mensagem de erro específica, pode adicionar **throw error("mensagem para o utilizador")** ao código através de uma extensão da cadeia de comando.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="6f9d7-271">Seguem-se três exemplos de métodos extensíveis úteis:</span><span class="sxs-lookup"><span data-stu-id="6f9d7-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="6f9d7-272">Se **validateWrite** na tabela TSTimesheetLine devolver **falso** durante uma operação de guardar para uma linha da folha de horas, é mostrada uma mensagem de erro na aplicação móvel.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="6f9d7-273">Se **validateSubmit** na tabela TSTimesheetTable devolver **falso** durante a submissão da folha de horas na aplicação, é mostrada uma mensagem de erro ao utilizador.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="6f9d7-274">A lógica que preenche os campos (por exemplo, **Propriedade de Linha** ) durante o método **insert** na tabela TSTimesheetLine continuará a ser executada.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-274">Logic that fills in fields (for example, **Line Property** ) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="6f9d7-275">Ocultar e marcar os campos de configuração inicial como só de leitura através da configuração</span><span class="sxs-lookup"><span data-stu-id="6f9d7-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="6f9d7-276">A partir dos parâmetros do projeto, pode tornar os campos de configuração inicial só de leitura ou ocultos na aplicação móvel.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="6f9d7-277">Defina as opções na secção **Folhas de horas móveis** no separador **Folha de Horas** da página **Parâmetros de gestão de projetos e contabilística**.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![Parâmetros do projeto](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="6f9d7-279">Alterar as atividades que estão disponíveis para seleção através das extensões</span><span class="sxs-lookup"><span data-stu-id="6f9d7-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="6f9d7-280">As atividades disponíveis para seleção para um projeto são preenchidas através dos métodos **getActivitiesForProject()** e **getActivityQuery()** na classe **TsTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="6f9d7-281">Pode utilizar a cadeia de comando para alterar este comportamento para corresponder ao seu cenário de negócio para as atividades que estão disponíveis para seleção para um projeto específico.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="6f9d7-282">Introduzir uma categoria de projeto predefinida nas entradas da folha de horas</span><span class="sxs-lookup"><span data-stu-id="6f9d7-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="6f9d7-283">A entrada de uma categoria de projeto predefinida nas entradas da folha de horas ocorre em três níveis.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="6f9d7-284">Pode utilizar a cadeia de comando para expandir o comportamento em qualquer um ou em todos estes níveis para alcançar o comportamento pretendido.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="6f9d7-285">É utilizada a seguinte hierarquia:</span><span class="sxs-lookup"><span data-stu-id="6f9d7-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="6f9d7-286">A aplicação tenta colocar a categoria predefinida a partir do recurso do projeto.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="6f9d7-287">Esta categoria predefinida é definida nos métodos **getCurrentUserResource** e **getDelegatedResourcesForCurrentUser** na classe **TSTimesheetSettingsService**.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="6f9d7-288">Se a categoria predefinida não for fornecida a nível do recurso do projeto, a aplicação tenta obtê-la a partir da atividade do projeto.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="6f9d7-289">Esta categoria predefinida é definida no método **getActivitiesForProject** na classe **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="6f9d7-290">Se a categoria predefinida não for fornecida a nível da atividade do projeto, a categoria predefinida é obtida a partir dos parâmetros do projeto.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="6f9d7-291">Esta categoria predefinida é definida no método **getProjectDetailsbyRule** na classe **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>
