---
title: Configurar gestão contabilística para projetos faturáveis
description: Este tópico fornece informações sobre as opções contabilísticas para os projetos faturáveis.
author: sigitac
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 413c9821f251fa37f5cfa082281be662d6be670a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012600"
---
# <a name="configure-accounting-for-billable-projects"></a>Configurar gestão contabilística para projetos faturáveis

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Dynamics 365 Project Operations apoia várias opções contabilísticas para projetos faturáveis que incluem transações de tempo e material e preço fixo.

- **Transações de tempo e material**: estas transações são faturadas à medida que o trabalho progride com base no consumo de horas, despesas, itens ou tarifas do projeto. Estes custos de transação podem ser comparados com as receitas em cada transação e o projeto é faturado à medida que o trabalho progride. As receitas do projeto também podem ser acumuladas no momento em que a transação ocorre. Durante a faturação, as receitas são reconhecidas e, se aplicável, as receitas acumuladas são estornadas.
- **Transações de preço fixo**: estas transações são faturadas de acordo com uma agenda de faturação que se baseia no contrato de projeto. As receitas por transações por preço fixo podem ser reconhecidas na faturação ou calculadas e lançadas periodicamente, de acordo com os métodos **Contrato concluído** ou **Percentagem concluída**.

Um projeto é considerado faturável quando está associado a um ou mais itens de contrato. Um item de contrato do projeto define por si próprio qual o método de faturação e os tipos de transações permitidos.

Como exemplo, a Fabrikam Robotics ganhou um contrato de projeto com a Adatum Corporation para a otimização dos equipamentos. A Adatum pagará um montante fixo de 10.000 USD para cobrir as despesas incorridas no projeto. Este é um método de faturação de preço fixo. O tempo e as tarifas do projeto serão faturados por utilização. Teste é o método de faturação por tempo e material. Todo o trabalho será monitorizado num único projeto denominado Otimização de equipamentos Adatum.

Um membro da equipa do projeto submete oito horas de trabalho no projeto Otimização de equipamentos Adatum. Quando o gestor de projeto aprova este tempo, o sistema utiliza o método de faturação de tempo e material para criar transações de valores reais, uma fatura e uma conta. Esta transação não será incluída no cálculo da estimativa de receitas de preço fixo.

Outro membro da equipa do projeto submete uma despesa de viagem de 2000 USD para o projeto Otimização de equipamentos Adatum. Quando o gestor de projeto aprova esta submissão, o sistema utiliza um método de faturação de preço fixo para criar transações de valores reais e uma conta para esta despesa do projeto. O cliente não será faturado com base nesta transação. Em vez disso, serão faturados através de marcos de faturação configurados separadamente. Esta transação de despesa, a par das estimativas de despesa, será incluída no cálculo da estimativa de receitas de preço fixo.

Os princípios contabilísticos das transações do projeto são definidos nos perfis de custos e receitas do projeto. Para cada transação do projeto, o sistema determina o perfil adequado de custos e receitas do projeto através das regras do perfil de custos e receitas do projeto que foram configuradas.

## <a name="define-project-cost-and-revenue-profiles"></a>Definir perfis de custos e receitas do projeto 

Os perfis de custos e receitas do projeto determinam as regras contabilísticas das transações do projeto. Estes perfis são configurados em Gestão de projetos e contabilística. 

Conclua os seguintes passos para criar um novo perfil de custos e receitas do projeto. 

1. Vá para **Gestão de projetos e contabilística** > **Configurar** > **Lançar** > **Perfis de custos e receitas do projeto**. 
2. Selecione **Novo** para criar um novo perfil de custos e receitas do projeto.
3. No campo **Nome**, introduza o nome e uma breve descrição do perfil.
4. No campo **Método de faturação**, selecione **Tempo e material** ou **Preço fixo**.
5. Expanda o FastTab **Livro Razão**. Os campos neste separador definem os princípios contabilísticos que são utilizados quando as transações do projeto são registadas no diário através do Diário de integração do Project Operations e, em seguida, faturadas através das Propostas de faturas do projeto.
6. Selecione as informações adequadas nos campos seguintes no FastTab **Livro Razão**:

    - **Lançar custos – hora**:

       - *Sem Livro Razão*: o custo das transações de tempo não será lançado no Livro Razão quando o diário de integração do Project Operations for lançado. No entanto, o contabilista pode lançar os custos através da função Lançar custos mais tarde.
       - **Saldo**: o custo das transações de tempo será debitado ao tipo de conta Livro Razão, *WIP - Valor de custo* e creditado na conta na *Conta de locação de vencimentos* na configuração de lançamento no Livro Razão. O contabilista utilizará a função Lançar custos para mover este custo de uma Conta de saldo para uma Conta de resultados periodicamente.
       - **Resultados**: ao lançar no diário de integração do Project Operations, o custo da transação de tempo será debitado no tipo de conta Livro Razão *Custo* e creditado na *Conta de locação de vencimentos* definida no separador **Custo** na página **Configuração do lançamento no livro razão** (**Gestão de projetos e contabilística** \> **Configurar** \> **Lançar** \> **Configuração do lançamento no livro razão**). Esta é a configuração mais comum para as transações de tempo e material.
        - *Nunca o Livro Razão*: o custo das transações a tempo nunca será lançado no Livro Razão.

    - **Lançar custos – despesas**:

         - **Saldo**: ao lançar o diário de integração do Project Operations, o custo da transação de despesas será debitado no tipo de conta Livro Razão *WIP - Valor do custo* tal como definido no separador **Custo** na página **Configuração do lançamento no livro razão** e creditado na conta de compensação na linha do diário. As contas de compensação predefinidas para despesas são definidas em **Gestão de projetos e contabilística** > **Configurar** \> **Lançar** \> **Conta de compensação predefinida para despesas**. O contabilista utilizará a função **Lançar custos** para mover este custo de uma conta de saldo para a conta de resultados periodicamente.
        - **Resultados**: ao lançar o diário de integração do Project Operations, o custo da transação de despesas será debitado no tipo de conta Livro Razão *Custo* tal como definido no separador **Custo** na página **Configuração do lançamento no livro razão** e creditado na conta de compensação na linha do diário. As contas de compensação predefinidas para despesas são definidas em **Gestão de projetos e contabilística** \> **Configurar** \> **Lançar** \> **Conta de compensação predefinida para despesas**.
      
    - **Custos de publicação - item**:

         - **Saldo**: Ao publicar o diário de integração de operações de projeto, o custo de transação de produto será debitado para a conta do livro razão tipo *WIP - Valor de custo - item* tal como definido no separador **Custo** na página de **Configuração de publicação de livro razão** e creditado no seguinte:
    
              - Para utilização do tipo de documento: conta **Custo - item** na **Configuração de publicação de livro razão**.  
              - Para a aquisição do tipo de documento: **Conta de integração de aquisições** nos **Parâmetros de gestão de projetos e contabilística**.
           O contabilista utilizará a função **Lançar custos** para mover este custo de uma conta de saldo para a conta de resultados periodicamente.
        - **Lucro e perda**: Ao publicar o diário de integração de operações de projeto, o custo de transação de produto será debitado para a conta do livro razão tipo *Custo* tal como definido no separador **Custo** na página de **Configuração de publicação de livro razão** e creditado no seguinte:
         
             - Para utilização do tipo de documento: conta **Custo - item** na **Configuração de publicação de livro razão**.  
             - Para a aquisição do tipo de documento: **Conta de integração de aquisições** nos **Parâmetros de gestão de projetos e contabilística**.
       
    - **Faturação na conta**:

        - **Saldo**: ao lançar a Proposta de fatura do projeto, uma transação na conta (marco de faturação) será creditada no tipo de conta do Livro Razão *WIP Faturado - na conta*, tal como definido no separador **Receitas** na página **Configuração do lançamento no livro razão**, e debitada na Conta de saldo do cliente.
         - **Resultados**: ao lançar a Proposta de fatura do projeto, uma transação na conta (marco de faturação) será creditada no tipo de conta do Livro Razão *Receitas faturadas - na conta*, tal como definido no separador **Receitas** na página **Configuração do lançamento no livro razão**, e debitada na Conta de saldo do cliente. As contas de saldo do cliente são definidas em **Contas a receber** \> **Configurar** \> **Perfis de lançamento do cliente**.

   Ao definir os perfis de publicação para métodos de tempo e faturação material, tem a opção de acumular receitas por tipo de transação (hora, despesa, item e taxa). Se a opção **Acumular receitas** for definida como **Sim**, as transações de vendas não faturadas no diário de Integração do Project Operations serão registadas no razão geral. O valor de venda é debitado em **WIP - conta de valor de vendas** e creditado na conta **Receitas acumuladas - valor de vendas** que foi configurada na página **Configuração do lançamento no livro razão** no separador **Receitas**. 
  
  > [!NOTE]
  > A opção **Acumular receitas** está disponível apenas quando o tipo de transação respetivo **Custo** é lançado na conta de resultados.
    
7. Expanda o FastTab **Estimar**. Os campos neste separador definem as definições de cálculo para as estimativas de receitas de preço fixo. Os campos neste separador são aplicáveis apenas aos perfis de custos e receitas do Projeto com um método de faturação de **Preço fixo**.
8. Selecione as informações adequadas nos campos seguintes no FastTab **Estimar**:

    - **Princípio utilizado para os cálculos de conclusão do projeto**:

        - **Contrato concluído**: a correspondência de custos e o reconhecimento de receitas só ocorrem no final do projeto. Os custos refletem-se como WIP no saldo até o projeto ser concluído.
        - **Percentagem concluída**: as receitas acumuladas são calculadas e lançadas no livro razão em cada período com base na percentagem de conclusão do projeto. Estão disponíveis vários métodos de cálculo da percentagem de conclusão. Estes métodos podem ser automáticos, baseados na configuração, ou manuais.
        - **Sem WIP**: esta configuração é utilizada nos projetos de preço fixo com um curto período e onde a fatura e os custos ocorrem no mesmo período. Neste caso, o valor do campo **Faturação na conta** no FastTab **Livro Razão** é definido automaticamente como **Resultados** para assegurar que as receitas são reconhecidas na faturação. O Processo de estimativa de receitas não será utilizado para este perfil de custos e receitas do projeto.

    - **Princípio de correspondência**: este campo determina como o valor de vendas calculado (receitas acumuladas) será lançado no livro razão.

        - Ao utilizar o princípio do **Valor de vendas**, o sistema calculará o valor das vendas ao fazer corresponder os custos e as receitas e, em seguida, publicá-los como um único montante.
        - Ao utilizar o princípio **Produção e lucros**, o sistema dividirá o valor das vendas em custos realizados e lucros calculados. Estes valores são lançados separadamente.

    - **Modelos de custos**: permitir que as transações do projeto sejam agrupadas com base no tipo de transação e na categoria do projeto, e defina as regras de cálculo da percentagem de conclusão para estes grupos.
    - **Códigos de período**: defina a frequência com que as estimativas de receitas são calculadas para um determinado perfil de custos e receitas do Projeto.
    - **Categorias para estimativa**: utilizado para o lançamento do valor de vendas (receitas acumuladas) nas transações do Projeto. Primeiro, configure a categoria de projeto dedicada para um tipo de transação **Tarifa** e, em seguida, definir o sinalizador **Estimar** para esta categoria de projeto. Em seguida, consoante o princípio de correspondência selecionado, escolha esta categoria de projeto no valor **Vendas** ou no campo **Lucros** no perfil de custos e receitas do Projeto.

### <a name="sample-configurations-for-project-cost-and-revenue-profiles"></a>Configurações de amostra para os perfis de custos e receitas do Projeto

Tempo e materiais - sem WIP

![Perfil de custos e receitas: Tempo e materiais - sem WIP](media/time-material-no-wip.png)

Tempo e materiais – WIP (receitas)

![Perfil de custos e receitas: Tempo e materiais - WIP](media/time-material-with-wip.png)

Preço Fixo - Sem WIP

![Perfil de custos e receitas: Preço fixo - sem WIP](media/fixed-price-no-wip.png)

Preço Fixo – contrato concluído

![Perfil de custos e receitas: Preço fixo - contrato concluído](media/fixed-price-completed-contract.png)

Preço Fixo – percentagem de conclusão

![Perfil de custos e receitas: Preço fixo - percentagem de conclusão](media/fixed-price-completed-percentage.png)


## <a name="accounting-event-examples-for-sample-project-cost-and-revenue-profiles"></a>Exemplos de eventos de contabilidade para os perfis de custos e receitas do Projeto de exemplo.

| Evento de Contabilidade                  | Tempo e material - Sem WIP                       | Tempo e Material - WIP                                                                                           | Preço fixo - sem WIP                                            | Preço fixo – Contrato concluído                                                                            | Preço Fixo – Percentagem de Conclusão                             |
|-----------------------------------|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| Registo no diário das transações de tempo    | Débito – Custo <br>Crédito – Alocação de vencimentos          | Débito - Custo <br>Crédito – Alocação de Vencimentos <br>Débito – Valor de Vendas WIP <br>Crédito - Valor de Vendas de Receitas Acumuladas                | Débito – Custo <br>Crédito – Alocação de vencimentos                         | Débito – Custo <br>Crédito – Alocação de vencimentos                                                                    | Débito – Custo <br>Crédito – Alocação de vencimentos                       |
| Registo no diário das transações de despesas | Débito – Custo <br>Crédito – Conta de compensação para despesas | Débito – Custo <br>Crédito – Conta de compensação para despesas <br>Débito – Valor de Vendas WIP <br>Crédito - Valor de Vendas de Receitas Acumuladas      | Débito - Custo <br>Crédito – Conta de compensação para despesas                 | Débito – Custo<br> Crédito – Conta de compensação para despesas                                                            | Débito – Custo <br>Crédito – Conta de compensação para despesas               |
| Cliente de faturação                | Débito – Saldo do cliente <br>Crédito – Receitas faturadas | Débito – Saldo do cliente <br>Crédito – Receitas faturadas <br>Crédito – Débito do Valor de Vendas WIP – Valor de Vendas de Receitas Acumuladas | Débito – Saldo do cliente <br>Crédito – Receitas faturadas - na conta | Débito – Saldo do cliente <br>Crédito – WIP – Faturado na conta                                                  | Débito – Saldo do cliente <br>Crédito – WIP – Faturado na conta    |
| Estimativa de Lançamento de Receitas             | Não aplicável                                   | Não aplicável                                                                                                    | Não Aplicável                                                  | Débito – Valor do Custo WIP <br>Crédito – Custo                                                                         | Débito – WIP - Valor de Vendas <br>Crédito – Valor de Vendas de Receitas Acumuladas |
| Eliminar                         | Não aplicável                                   | Não aplicável                                                                                                    | Não Aplicável                                                  | Crédito – Valor do Custo WIP <br>Débito – Custo <br>Crédito – Receitas Acumuladas - Valor das vendas <br>Débito – Faturado na conta WIP | Débito – WIP - Faturado na conta <br>Crédito – Valor de Vendas WIP     |

## <a name="configure-project-cost-and-revenue-profile-rules"></a>Configurar regras de perfis de custos e receitas do projeto

As regras de perfis de custos e receitas do projeto determinam o perfil de custos e receitas do Projeto que tem de ser usado ao processar quaisquer transações de projetos faturáveis. Defina as regras em **Gestão de projetos e contabilística** \> **Configurar** \> **Lançar** \> **Regras de perfis de custos e receitas do projeto**.

As regras podem ser definidas por contrato de projeto, grupo de projetos ou por um projeto específico. O sistema escolherá sempre primeiro a regra de maior granularidade.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
