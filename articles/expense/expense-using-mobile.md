---
title: Aplicação de despesas móvel
description: Este tópico fornece informações sobre a área de trabalho móvel da gestão de despesas.
author: suvaidya
ms.date: 11/15/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 14bd76df5f058d2af9f77990471a0a173fe8c15d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588934"
---
# <a name="mobile-expense-app"></a>Aplicação de despesas móvel

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Este tópico fornece informações sobre a área de trabalho móvel da **gestão de despesas**. Esta área de trabalho permite que os utilizadores recolham e carreguem um recibo, para que possam anexá-lo a um relatório de despesas mais tarde. Os utilizadores também podem criar rapidamente uma linha de despesas usando um recibo anexo, e criar e gerir os seus relatórios de despesas. Além disso, os aprovadores podem usar a área de trabalho móvel da **gestão de despesas** para visualizar relatórios de despesas que lhes são atribuídos, e aprovar ou rejeitar esses relatórios de despesas.

Esta área de trabalho móvel destina-se a ser utilizada com a aplicação móvel Dynamics 365 Unified Ops.

Muitas organizações exigem que uma cópia de um recibo seja anexada a um relatório de despesas relacionado com viagens ou com negócios que um funcionário submete para reembolso. A área de trabalho móvel da **gestão de despesas** permite aos utilizadores criar rapidamente novas linhas de despesas no dispositivo móvel à sua escolha, utilizando uma foto anexa de um recibo. Em alternativa, os utilizadores podem recolher uma foto de um recibo e depois anexá-la a um relatório de despesas mais tarde. Os colaboradores também podem criar e gerir os seus relatórios de despesas e, em seguida, submetê-los para aprovação e reembolso utilizando o seu dispositivo móvel.

Especificamente, a área de trabalho móvel da **gestão de despesas** permite que os utilizadores executem estas tarefas:

- Tirar uma foto a um recibo. Carregar a foto do recibo e anexá-la a um relatório de despesas mais tarde.
- Carregar um ficheiro como recibo fotografado. Em seguida, pode anexar esse ficheiro a um relatório de despesas mais tarde.
- Criar uma nova linha de despesas utilizando um recibo anexo. Em seguida, pode adicionar o item da linha a um relatório de despesas mais tarde, e submetê-lo para aprovação e reembolso.

Também poderá utilizar estas características:

- Criar um novo relatório de despesas.
- Anexar transações de cartões de crédito e outras despesas previamente criadas a um relatório de despesas.
- Criar novas despesas para um relatório de despesas.
- Anexar um recibo a qualquer despesa para um relatório de despesas, quer tirando uma foto ao recibo, quer enviando um ficheiro como recibo fotografado.
- Dependendo da política de despesas da empresa, adicione a lista de convidados a uma despesa.
- Dependendo da política de despesas da empresa, discrimine as despesas.
- Apresente um relatório de despesas para aprovação e reembolso.
- Aprove ou rejeite relatórios de despesas para os quais é um aprovador atribuído.

## <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Pré-requisitos se utilizar o Dynamics 365 Finance

Se o Finance foi implementado para a sua organização, o administrador de sistema tem de publicar a área de trabalho móvel da **gestão de despesas**. 

## <a name="download-and-install-the-dynamics-365-unified-ops-mobile-app"></a>Descarregue e instale a aplicação móvel Dynamics 365 Unified Ops
Descarregue e instale a aplicação móvel Dynamics 365 Unified Ops:

- [Para telemóveis Android](https://go.microsoft.com/fwlink/?linkid=850662)
- [Para iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Iniciar sessão na aplicação móvel
1. Inicie a aplicação no seu dispositivo móvel.
2. Introduza o seu URL do Dynamics 365.
4. Quando iniciar sessão pela primeira vez, ser-lhe-á solicitado o nome de utilizador e a palavra-passe. Introduza as suas credenciais.
5. Depois de iniciar sessão, são mostradas as áreas de trabalho disponíveis para a sua empresa. Se o seu administrador de sistema publicar uma nova área de trabalho mais tarde, terá de atualizar a lista de áreas de trabalho móveis.

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Recolha um recibo utilizando a área de trabalho móvel de gestão de despesas

1. No seu dispositivo móvel, abra a área de trabalho da **gestão de despesas**.
2. Selecione **Recolha de recibo**.
3. Selecione **Tirar fotografia** ou **Escolher imagem**.
4. Siga um destes passos:

    - Se selecionar **Tirar fotografia**, siga estes passos:

        1. É levado para a câmara do seu dispositivo móvel, para que possa tirar uma fotografia ao recibo. 
        2. Quando terminar de tirar uma fotografia, selecione **OK** para aceitar a foto.
        3. Opcional: Introduza um nome para a fotografia e introduza quaisquer notas.

    - Se selecionar **Escolher fotografia**, siga estes passos:

        1. Selecione uma imagem na lista.
        2. Opcional: Introduza um nome para a imagem e introduza quaisquer notas.

5. Selecione **Concluído**.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Introduzir rapidamente as despesas utilizando a área de trabalho móvel de gestão de despesas

1. No seu dispositivo móvel, abra a área de trabalho da **gestão de despesas**.
2. Selecione **Entrada rápida de despesas**.
3. Selecione a categoria da despesa. Vê uma lista de categorias de despesas que são carregadas na sua aplicação para utilização offline. Por predefinição, são carregados 50 itens, mas um programador pode alterar este número. Para mais informações, os programadores deveriam consultar [Plataforma móvel](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Se a sua categoria não estiver na lista, selecione **Procurar** para fazer uma pesquisa online. Procure por categoria de despesa ou mude para a pesquisa por tipo de despesa.
4. Insira a data de transação da despesa.
5. Opcional: Insira o comerciante para as despesas.
6. Introduza o montante da despesa.
7. Selecionar a moeda da despesa. Vê uma lista dos códigos de moeda que são carregadas na sua aplicação para utilização offline. Por predefinição, são carregados 400 moedas, mas um programador pode alterar este número. Para mais informações, os programadores deveriam consultar [Plataforma móvel](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Se a sua moeda não estiver na lista, selecione **Procurar** para fazer uma pesquisa online. Procure por moeda ou mude para a pesquisa por nome de categoria.
8. Selecione **Tirar fotografia** ou **Escolher imagem**.
9. Siga um destes passos:

    - Se selecionou **Tirar fotografia**, é levado para a câmara do seu dispositivo móvel, para que possa tirar uma fotografia ao recibo. Quando terminar de tirar uma fotografia, selecione **OK** para aceitar a foto.
    - Se selecionou **Escolher a imagem**, selecione uma imagem na lista.

10. Selecione **Concluído**.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace"></a>Aprovar um relatório de despesas utilizando a Área de trabalho móvel da gestão de despesas

1. No seu dispositivo móvel, abra a área de trabalho da **gestão de despesas**.
2. A **aprovação das despesas** mostra o número de relatórios de despesas que lhe são atribuídos para aprovação. O número é atualizado aproximadamente a cada 30 minutos. Selecione **aprovações de despesas**.

    A lista de relatórios de despesas que lhe são atribuídos para aprovação é apresentada.

3. Selecione um relatório de despesas para ver os detalhes das despesas para o mesmo.
4. Selecione uma despesa para ver os detalhes da mesma. A informação que é mostrada para uma despesa inclui qualquer recibo, convidado e detalhes de discriminação.
5. De volta à página do **relatório de despesas**, selecione para aprovar ou rejeitar o relatório de despesas.
6. Insira quaisquer comentários para a ação de aprovação.
7. Selecione **Concluído**.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace"></a>Criar um novo relatório de despesas e submeta-o para aprovação utilizando a Área de trabalho móvel de gestão de despesas

1. No seu dispositivo móvel, abra a área de trabalho da **gestão de despesas**.
2. Selecione **Entrada de despesas**.
3. Selecione **Novo relatório** ou selecione um relatório de despesas na lista.
4. Para novos relatórios de despesas, insira o objetivo e qualquer informação adicional disponível. Esta informação varia, dependendo da forma que a gestão de despesas estiver configurada para a sua empresa.
5. Selecione **Concluído**.
6. Para adicionar as despesas existentes, como transações de cartões de crédito, ao relatório de despesas, selecione **Anexar**.
7. Selecionar uma ou mais despesas na lista.
8. Selecione **Concluído**.
9. Para adicionar uma nova despesa ao relatório de despesas, selecione **Novas despesas**.
10. Selecione a categoria para a despesa. Vê uma lista de categorias de despesas que são carregadas na sua aplicação para utilização offline. Por predefinição, são carregados 50 itens, mas um programador pode alterar este número. Para mais informações, os programadores deveriam consultar [Plataforma móvel](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Se a sua categoria não estiver na lista, selecione **Procurar** para fazer uma pesquisa online. Procure por categoria de despesa ou mude para a pesquisa por tipo de despesa.
11. Opcional: Insira o comerciante para as despesas.
12. Insira a data de transação da despesa.
13. Introduza o montante da despesa.
14. Selecionar a moeda da despesa. Vê uma lista dos códigos de moeda que são carregadas na sua aplicação para utilização offline. Por predefinição, são carregados 400 moedas, mas um programador pode alterar este número. Para mais informações, os programadores deveriam consultar [Plataforma móvel](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Se a sua moeda não estiver na lista, selecione **Procurar** para fazer uma pesquisa online. Procure por moeda ou mude para a pesquisa por nome de categoria.
15. Selecione **Concluído**.
16. Para adicionar mais detalhes à despesa, selecione **Adicionar mais detalhes**. Os campos disponíveis dependem da configuração da gestão de despesas para a sua empresa.
17. Se a política da empresa exigir um recibo para as despesas, selecione **Recibos**, e siga estes passos:

    1. Selecione o **recibo de recolha** ou **Anexar recibo**.
    2. Siga um destes passos:

        - Se selecionar **Recibo de recolha**, siga estes passos:

            1. Selecione **Tirar fotografia** ou **Escolher imagem**.
            2. Siga um destes passos:

                - Se selecionar **Tirar fotografia**, siga estes passos:

                    1. É levado para a câmara do seu dispositivo móvel, para que possa tirar uma fotografia ao recibo. Quando terminar de tirar uma fotografia, selecione **OK** para aceitar a foto.
                    2. Opcional: Introduza um nome para a fotografia e introduza quaisquer notas.

                - Se selecionar **Escolher fotografia**, siga estes passos:

                    1. Selecione uma imagem na lista.
                    2. Opcional: Introduza um nome para a imagem e introduza quaisquer notas.

            3. Selecione **Concluído**.

        - Se selecionar **Anexar recibo**, siga estes passos:

            1. Selecione uma ou mais imagens na lista.
            2. Selecione **Concluído**.

    3. Selecione o botão **Anterior** para voltar aos detalhes das despesas.

18. Se a política da empresa exigir convidados para as despesas, selecione **Convidados**, e siga estes passos:

    1. Selecione **Convidado**, **Convidados anteriores** ou **Colegas de trabalho**.
    2. Siga um destes passos:

        - Se selecionou **Convidado**, siga estes passos:

            1. Introduza o nome do convidado.
            2. Opcional: Insira a organização e/ou o país do convidado.
            3. Opcional: Introduzir o cargo do convidado.
            4. Selecione **Concluído**.

        - Se selecionar **Convidados anteriores**, siga estes passos:

            1. Selecione um ou mais convidados anteriores na lista. Vê uma lista de convidados anteriores que adicionou aos relatórios de despesas anteriores que são carregados na sua aplicação para uso offline. Por predefinição, são carregados 50 itens, mas um programador pode alterar este número. Para mais informações, os programadores deveriam consultar [Plataforma móvel](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Se o seu convidado anterior não estiver na lista, selecione **Procurar** para fazer uma pesquisa online. Procure por nome ou mude para a pesquisa por organização, país, ou cargo.
            2. Selecione **Concluído**.

        - Se selecionou **Colega de trabalho**, siga estes passos:

            1. Selecione um ou mais colegas de trabalho na lista. Vê uma lista de colegas de trabalho que são carregados na sua aplicação para utilização offline. Por predefinição, são carregados 50 itens, mas um programador pode alterar este número. Para mais informações, os programadores deveriam consultar [Plataforma móvel](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Se o seu colega de trabalho não estiver na lista, selecione **Procurar** para fazer uma pesquisa online. Procure por nome ou mude para a pesquisa por empresa ou cargo.
            2. Selecione **Concluído**.

    3. Selecione o botão **Anterior** para voltar aos detalhes das despesas.

19. Se a política da empresa exigir que a despesa seja discriminada, selecione **Discriminar**, e siga estes passos:

    1. Selecione a primeira data para discriminar.
    2. Selecione **Adicionar discriminação**.
    3. Selecione a subcategoria para a discriminação das despesas. Vê uma lista de subcategorias de despesas que são carregadas na sua aplicação para utilização offline. Por predefinição, são carregados 50 itens, mas um programador pode alterar este número. Para mais informações, os programadores deveriam consultar [Plataforma móvel](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Se a sua subcategoria não estiver na lista, selecione **Procurar** para fazer uma pesquisa online. Procure por nome da subcategoria de despesas.
    4. Introduza o valor da transação para a discriminação.
    5. Edite a data de transação, se necessário.
    6. Selecione **Concluído**.
    7. Repita os passos anteriores até terminar de adicionar todas as discriminações para a data selecionada.
    8. Para dias adicionais, pode selecionar **Copiar para o dia seguinte** para copiar as discriminações para o dia seguinte. Em alternativa, pode selecionar a data para discriminar e, em seguida, adicionar itens como fez na primeira data.
    9. Depois de ter terminado de item a despesa, selecione o botão **Anterior** para voltar aos detalhes das despesas.

20. Selecione o botão **Anterior** para voltar à página **Relatório de despesas**.
21. Repita os passos anteriores até terminar de adicionar todas as despesas.
22. Selecione **Submeter**.
23. Insira quaisquer comentários para o aprovador.
24. Selecionar **Concluído**.

## <a name="frequently-asked-questions"></a>Perguntas mais frequentes

### <a name="why-doesnt-the-expense-mobile-app-enter-the-payment-method-by-default"></a>Porque é que a aplicação móvel Despesas não introduz o método de pagamento por predefinição?

As organizações podem personalizar a definição **Método de pagamento predefinido** para cada categoria de despesas à medida que são criadas. Além disso, ao configurar métodos de pagamento, pode definir o campo **Método de pagamento predefinido** para **Apenas importar**.

Quando **Apenas importar** estiver ativada para um método de pagamento, o método de pagamento não é introduzido por predefinição. Ficará em branco nas categorias de despesas em que este método de pagamento está configurado. Este comportamento é consistente tanto na experiência Web como na experiência móvel.
    
Quando **Apenas importar** não estiver ativada para um método de pagamento, o valor definido é introduzido por predefinição para categorias de despesas em que este método de pagamento está configurado. No entanto, existe um problema conhecido em que o valor predefinido não é introduzido na aplicação móvel Despesas. Para contornar este problema, selecione manualmente um método de pagamento antes de guardar o relatório de despesas. 

### <a name="why-cant-i-add-or-edit-financial-dimensions-in-the-expense-mobile-app"></a>Por que não posso adicionar ou editar dimensões financeiras na aplicação móvel Despesas?

A entrada de dimensões e distribuições não é suportada. Para contornar esta limitação, pode predefinir estes campos na aplicação móvel definindo as dimensões financeiras predefinidas por projeto ou colaborador.

### <a name="why-do-i-sometimes-see-a-synchronization-error-in-the-expense-mobile-app"></a>Por que é que às vezes vejo um erro de sincronização na aplicação móvel Despesas?

Se as linhas de despesas não satisfizerem os requisitos da política, e o utilizador submeter o relatório de despesas sem tratar do aviso de política, os dados móveis não são sincronizados com o servidor e ocorre uma falha de sincronização. Todos os relatórios de despesas que são submetidos após a falha de sincronização permanecerão num estado falhado e causarão mais falhas de sincronização. A única forma de corrigir esta situação é eliminar manualmente as notificações de sincronização. Este problema foi abordado ao impedir a submissão de relatórios de despesas quando os avisos de política não foram abordados, de modo a evitar os erros de sincronização.

### <a name="why-isnt-project-and-category-validation-correctly-reflected-in-the-expense-mobile-app"></a>Porque é que a validação do projeto e da categoria não se reflete corretamente na aplicação móvel Despesas?

Atualmente, esta validação não é suportada. No entanto, poderá ser adicionado suporte no futuro. 

### <a name="what-document-types-are-supported-in-the-expense-mobile-app"></a>Que tipos de documentos são suportados na aplicação móvel Despesas?

A aplicação móvel Despesas suporta apenas imagens. Atualmente não suporta PDFs ou outros documentos.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
