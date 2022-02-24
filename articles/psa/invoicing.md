---
title: Faturação do Project Service Automation
description: Este tópico fornece informações sobre a faturação.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 0855e85c1f09d29d3ecb49ba517fd3043ae11140
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151402"
---
# <a name="invoicing-in-project-service-automation"></a>Faturação do Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

A faturação do Dynamics 365 Project Service Automation é útil porque fornece aos gestores de projeto um segundo nível de aprovação antes de criarem faturas para os clientes. O primeiro nível de aprovação é concluído quando as entradas de tempo e de despesa que os membros da equipa do projeto submetem são aprovadas.

O PSA não foi concebido para gerar faturas direcionadas para o cliente, pelas seguintes razões:

- Não contém informações sobre impostos.
- Não consegue converter outras moedas na moeda de faturação utilizando as taxas de câmbio configuradas corretamente.
- Não é possível formatar corretamente as faturas para que possam ser impressas.

Em vez disso, pode utilizar um sistema financeiro ou de contabilidade para criar faturas direcionadas para o cliente que utilizem as informações das propostas de fatura geradas no PSA.

## <a name="creating-project-invoices-in-psa"></a>Criar faturas do projeto no PSA

É possível criar uma fatura do projeto de cada vez ou em massa. Pode criá-las manualmente ou podem ser configuradas para que sejam geradas em execuções automatizadas.

### <a name="manually-create-project-invoices-in-psa"></a>Criar manualmente faturas do projeto no PSA

A partir da página da lista de **Contratos do Projeto**, pode criar faturas do projeto separadamente para cada contrato do projeto ou pode criar faturas em massa para vários contratos do projeto.

Siga este passo para criar uma fatura para um contrato do projeto específico.

- Na página da lista de **Contratos do Projeto**, abra um contrato do projeto e, em seguida, selecione **Criar Fatura**.

    ![Criar faturas do projeto para um contrato do projeto específico](media/CreateProjectInvoicesOneByOne.png)

    É gerada uma fatura para todas as transações referentes ao contrato do projeto selecionado que têm um estado de **Pronto para Faturar**. Estas transações incluem o tempo, as despesas, os marcos e os itens de contrato baseados no produto.

Siga estes passos para criar faturas em massa.

1. Na página da lista de **Contratos do Projeto**, selecione um ou mais contratos do projeto para os quais tem de criar uma fatura e, em seguida, selecione **Criar Faturas do Projeto**.

    ![Criar faturas do projeto em massa](media/CreateProjectInvoicesBulk.png)

    Uma mensagem de aviso informa-o de que poderá haver um atraso antes da criação das faturas. O processo também é mostrado.

2. Selecione **OK** para fechar a caixa de mensagem.

    É gerada uma fatura para todas as transações num item de contrato que têm um estado de **Pronto para Faturar**. Estas transações incluem o tempo, as despesas, os marcos e os itens de contrato baseados no produto.

3. Para ver as faturas geradas, aceda a **Vendas** \> **Faturação** \> **Faturas**. Verá uma fatura para cada contrato do projeto.

### <a name="set-up-automated-creation-of-project-invoices-in-psa"></a>Configurar a criação automatizada de faturas do projeto no PSA

Siga estes passos para configurar uma fatura automatizada executada no PSA.

1. Aceda a **Project Service** \> **Definições** \> **Tarefas de lote**.
2. Crie uma tarefa de lote e atribua-lhe o nome **Criação de Faturas no PSA**. O nome da tarefa de lote tem de incluir o termo "Criar Faturas."
3. No campo **Tipo de tarefa**, selecione **Nenhum**. Por predefinição, as opções **Frequência Diária** e **Está Ativo** estão definidas como **Sim**.
4. Selecione **Executar Fluxo de Trabalho**. Na caixa de diálogo **Pesquisar Registo**, verá três fluxos de trabalho:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Selecione **ProcessRunCaller** e, em seguida, selecione **Adicionar**.
6. Na caixa de diálogo seguinte, selecione **OK**. Um fluxo de trabalho de **Suspensão** é seguido por um fluxo de trabalho do **Processo**.

    Também pode selecionar **ProcessRunner** no passo 5. Em seguida, quando selecionar **OK**, um fluxo de trabalho do **Processo** é seguido por um fluxo de trabalho de **Suspensão**.

Os fluxos de trabalho **ProcessRunCaller** e **ProcessRunner** criam faturas. O **ProcessRunCaller** chama o **ProcessRunner**. **ProcessRunner** é o fluxo de trabalho que, na realidade, cria as faturas. Passa por todos os itens de contrato para os quais é necessário criar faturas e cria faturas para essas linhas. Para determinar os itens de contrato para os quais devem ser criadas faturas, a tarefa examina as datas de execução da fatura para os itens de contrato. Se os itens de contrato que pertencem a um contrato tiverem a mesma data de execução da fatura, as transações são combinadas numa fatura que tem duas linhas de fatura. Se não houver transações para as quais criar faturas, a tarefa ignorará a criação da fatura.

Depois de **ProcessRunner** ter terminado a execução, chama o **ProcessRunCaller**, fornece a hora de fim e é fechado. **ProcessRunCaller** em seguida, inicia um temporizador que funciona durante 24 horas a partir da hora de fim especificada. No final do temporizador, o **ProcessRunCaller** é fechado.

A tarefa de processamento em lote para criar faturas é uma tarefa recorrente. Se este processamento em lote for executado muitas vezes, são criadas várias instâncias da tarefa e causam erros. Consequentemente, deverá iniciar o processamento em lote apenas uma vez, e só deverá reiniciá-lo se parar de ser executado.

> [!NOTE]
> A faturação em lote no Project Service Automation só funciona para linhas de contrato de projeto que são configuradas por agendas de fatura. Uma linha de contrato com um método de faturação de preço fixo tem de ter marcos configurados. Uma linha de contrato de projeto com um método de faturação de tempo e material necessitará de uma configuração de agenda de faturamento baseado em datas. As informações sobre a criação de frequências de faturação no contexto de um projeto que se baseia numa linha de proposta, são fornecidas no tópico [Propostas e linhas de propostas](basic-quote-lines.md#invoice-schedule). O mesmo se aplica a uma linha de contratos baseada em projetos.      
 
### <a name="edit-a-draft-psa-invoice"></a>Editar um rascunho da fatura do PSA

Quando cria um rascunho da fatura do projeto, todas as transações de vendas não faturadas criadas quando as entradas de tempo e despesa foram aprovadas são reunidas na fatura. Pode efetuar os seguintes ajustes enquanto a fatura ainda está numa fase de rascunho:

- Elimine ou edite os detalhes de linha de fatura.
- Edite e ajuste a quantidade e o tipo de faturação.
- Adicione diretamente o tempo, a despesa e as taxas como transações na fatura. Pode utilizar esta funcionalidade se a linha da fatura estiver mapeada para um item de contrato que permita estas classes de transação.

Selecione **Confirmar** para confirmar uma fatura. A ação de Confirmação é uma ação unilateral. Quando seleciona **Confirmar**, o sistema efetua a faturação só de leitura e cria valores reais de vendas faturadas a partir de cada detalhe de linha de fatura para cada linha de fatura. Se o detalhe de linha de fatura referenciar um valor real de vendas não faturadas, o sistema também reverte o valor real de vendas não faturadas. (Qualquer detalhe de linha de fatura que tenha sido criado a partir de uma entrada de tempo ou despesa irá referenciar um valor real de vendas não faturadas.) Os sistemas de integração do razão geral podem utilizar esta reversão para reverter o trabalho do projeto em curso (WIP) para fins de contabilidade.

### <a name="correct-a-confirmed-psa-invoice"></a>Corrigir uma fatura do PSA confirmada

As faturas do PSA confirmadas podem ser editadas (corrigidas). Quando corrige uma fatura confirmada, uma nova fatura corretiva de rascunho é criada. Dado que a pressuposição é que pretende reverter todas as transações e quantidades da fatura original, esta fatura corretiva inclui todas as transações da fatura original e todas as quantidades são 0 (zero).

Se alguma transação não necessitar de correção, pode removê-la da fatura corretiva de rascunho. Se pretender reverter ou devolver apenas uma quantidade parcial, pode editar o campo **Quantidade** no detalhe de linha. Se abrir o detalhe de linha de fatura, poderá ver a quantidade original da fatura. Em seguida, pode editar a quantidade da fatura atual para que seja inferior ou superior à quantidade original da fatura.

Quando confirma uma fatura corretiva, o valor real de vendas faturadas originais é revertido e é criado um novo valor real de vendas faturadas. Se a quantidade tiver sido reduzida, a diferença causará a criação de um novo valor real de vendas não faturadas. Por exemplo, se as vendas faturadas originais eram de oito horas e o detalhe de linha de fatura corretiva tiver uma quantidade reduzida de seis horas, o PSA reverte a linha de vendas faturadas originais e cria dois novos valores reais:

- Um valor real de vendas faturadas durante seis horas.
- Uma valor real de vendas não faturadas para as duas horas restantes. Esta transação pode ser faturada mais tarde ou marcada como não faturável, dependendo das negociações com o cliente.
