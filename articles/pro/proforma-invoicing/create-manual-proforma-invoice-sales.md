---
title: Faturas pró-forma de projeto
description: Esta tópico fornece informações sobre faturas pró-forma de projetos no Project Operations.
author: rumant
ms.date: 04/06/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f2ce672a412f7ad73b072854590cd423a3499fc1
ms.sourcegitcommit: 650a84add65588defdd2ac2c4524806baab070e0
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/21/2022
ms.locfileid: "8628868"
---
# <a name="proforma-project-invoices"></a>Faturas pró-forma de projeto

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

A faturação pró-forma de projeto fornece aos gestores de projeto um segundo nível de aprovação antes de criarem faturas para os clientes. O primeiro nível de aprovação é concluído quando as entradas de tempo, despesa e material que os membros da equipa do projeto submetem são aprovadas.

Dynamics 365 Project Operations A implementação leve não foi concebida para gerar faturas viradas para o cliente. A lista que se segue mostra por que razão as faturas não podem ser geradas:

- Não contém informações sobre impostos.
- Não é possível converter outras moedas como moeda de faturação.
- Não é possível formatar corretamente as faturas para impressão.

Em vez disso, pode utilizar um sistema financeiro ou contabilística para criar faturas direcionadas para o cliente que utilizem as informações em propostas de fatura geradas.

## <a name="creating-project-invoices"></a>Criar faturas do projeto

É possível criar uma fatura do projeto de cada vez ou em massa. Pode criá-las manualmente ou podem ser configuradas para que sejam geradas em execuções automatizadas.

### <a name="manually-create-project-invoices"></a>Criar manualmente faturas do projeto 

Na página da lista de **Contratos do Projeto**, pode criar faturas do projeto separadamente para cada contrato do projeto ou pode criar faturas em massa para vários contratos do projeto.

   - Para criar uma fatura para um contrato de projeto específico, na página da lista de **Contratos do Projeto**, abra um contrato de projeto e, em seguida, selecione **Criar fatura**.

   É gerada uma fatura para todas as transações referentes ao contrato do projeto selecionado que têm um estado de **Pronto para Faturar**. Estas transações incluem tempo, despesas, materiais, marcos, itens de contrato baseadas em produtos e outras linhas do diário de vendas não faturadas que possam ter sido confirmadas.

Para criar faturas de forma automática:

1. Na página da lista de **Contratos do Projeto**, selecione um ou mais contratos do projeto para os quais pretende criar uma fatura e, em seguida, selecione **Criar Faturas do Projeto**.
2. Uma mensagem de aviso informa-o de que poderá haver um atraso antes da criação das faturas. O processo também é mostrado. Selecione **OK** para fechar a caixa de mensagem.

   É gerada uma fatura para todas as transações num item de contrato que têm um estado de **Pronto para Faturar**. Estas transações incluem tempo, despesas, materiais, marcos, itens de contrato baseadas em produtos e outras linhas do diário de vendas não faturadas que possam ter sido confirmadas.

3. Veja as faturas geradas indo a **Vendas** \> **Faturação** \> **Faturas**. Verá uma fatura para cada contrato do projeto.

### <a name="set-up-automated-creation-of-project-invoices"></a>Configurar a criação automatizada de faturas do projeto 

Siga estes passos para configurar a execução de fatura automatizada.

1. Aceda a **Definições** \> **Tarefas de lote**.
2. Crie uma tarefa de lote e atribua-lhe o nome **Criar faturas nas operações do Projeto**. O nome da tarefa de lote tem de incluir o termo "Criar Faturas."
3. No campo **Tipo de tarefa**, selecione **Nenhum**. Por predefinição, as opções **Frequência Diária** e **Está Ativo** estão definidas como **Sim**.
4. Selecione **Executar Fluxo de Trabalho**. Na caixa de diálogo **Pesquisar registo** verá os seguintes fluxos de trabalho:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Selecione **ProcessRunCaller** e, em seguida, selecione **Adicionar**.
6. Na caixa de diálogo seguinte, selecione **OK**. Um fluxo de trabalho de **Suspensão** é seguido por um fluxo de trabalho do **Processo**.

    Também pode selecionar **ProcessRunner** no passo 5. Em seguida, quando selecionar **OK**, um fluxo de trabalho do **Processo** é seguido por um fluxo de trabalho de **Suspensão**.

Os fluxos de trabalho **ProcessRunCaller** e **ProcessRunner** criam faturas. O **ProcessRunCaller** chama o **ProcessRunner**. **ProcessRunner** é o fluxo de trabalho que cria as faturas. Este fluxo de trabalho passa por todos os itens de contrato para os quais é necessário criar faturas e cria as faturas. Para determinar os itens de contrato para os quais devem ser criadas faturas, o fluxo de trabalho examina as datas de execução da fatura para os itens de contrato. Se os itens de contrato que pertencem a um contrato tiverem a mesma data de execução da fatura, as transações são combinadas numa fatura que tem duas linhas de fatura. Se não houver transações para as quais criar faturas, não são criadas faturas.

Depois de **ProcessRunner** ter terminado a execução, chama o **ProcessRunCaller**, fornece a hora de fim e é fechado. **ProcessRunCaller** em seguida, inicia um temporizador que funciona durante 24 horas a partir da hora de fim especificada. No final do temporizador, o **ProcessRunCaller** é fechado.

A tarefa de processamento em lote para criar faturas é uma tarefa recorrente. Se este processamento em lote for executado muitas vezes, são criadas várias instâncias da tarefa e podem causar erros. Para trabalhar sobre este problema, iniciar o processamento em lote apenas uma vez e só reiniciá-lo se parar de ser executado.

> [!NOTE]
> A faturação do lote só funciona para itens de contrato do projeto que são configurados por horários da fatura. Uma linha de contrato com um método de faturação de preço fixo tem de ter marcos configurados. Uma linha de contrato de projeto com um método de faturação de tempo e material necessitará de uma configuração de agenda de faturamento baseado em datas. O mesmo se aplica a uma linha de contratos baseada em projetos.      
 
### <a name="edit-a-draft-invoice"></a>Editar um rascunho da fatura

Quando cria um rascunho da fatura do projeto, todas as transações de vendas não faturadas criadas quando as entradas de tempo e despesa foram aprovadas são reunidas na fatura. Pode efetuar os seguintes ajustes enquanto a fatura ainda está numa fase de rascunho:

- Elimine ou edite os detalhes de linha de fatura.
- Edite e ajuste a quantidade e o tipo de faturação.
- Adicione diretamente o tempo, a despesa, o material e as taxas como transações na fatura. Pode utilizar esta funcionalidade se a linha da fatura estiver mapeada para um item de contrato que permita estas classes de transação.

Selecione **Confirmar** para confirmar uma fatura. Esta ação é uma ação unilateral. Quando seleciona **Confirmar**, a fatura fica só de leitura e cria valores reais de vendas faturadas a partir de cada detalhe de linha de fatura para cada linha de fatura. Se o detalhe de linha de fatura referenciar um valor real de vendas não faturadas, o valor real de vendas não faturadas é revertido. Qualquer detalhe da linha de fatura que tenha sido criado a partir de um tempo, despesa ou entrada de utilização de material irá fazer referência a um valor real de vendas não faturado. Os sistemas gerais de integração de livro razão podem utilizar esta inversão para reverter os trabalhos de projeto em curso (WIP) para fins contabilísticos.

### <a name="correct-a-confirmed-invoice"></a>Corrigir uma fatura confirmada

As faturas corrigidas podem ser editadas. Quando corrige uma fatura confirmada, uma nova fatura corretiva de rascunho é criada. Dado que a pressuposição é que pretende reverter todas as transações e quantidades da fatura original, esta fatura corretiva inclui todas as transações da fatura original e todas as quantidades são zero.

Se houver alguma transação que não necessite de correção, pode removê-la da fatura corretiva de rascunho. Se pretender reverter ou devolver apenas uma quantidade parcial, pode editar o campo **Quantidade** no detalhe de linha. Se abrir o detalhe de linha de fatura, poderá ver a quantidade original da fatura. Em seguida, pode editar a quantidade da fatura atual para que seja inferior ou superior à quantidade original da fatura.

Quando confirma uma fatura corretiva, o valor real de vendas faturadas originais é revertido e é criado um novo valor real de vendas faturadas. Se a quantidade tiver sido reduzida, a diferença causará a criação de um novo valor real de vendas não faturado. Por exemplo, se a venda faturada original era de oito horas e o detalhe de linha de fatura corretiva tiver uma quantidade reduzida de seis horas, a linha de vendas faturadas originais é invertida e são criados dois novos valores reais:

- Um valor real de vendas faturadas durante seis horas.
- Uma valor real de vendas não faturadas para as duas horas restantes. Esta transação pode ser faturada mais tarde ou marcada como não faturável, dependendo das negociações com o cliente.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
