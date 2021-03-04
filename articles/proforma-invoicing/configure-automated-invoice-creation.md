---
title: Configurar a criação automática de faturas
description: Este tópico fornece informações sobre como configurar o sistema para gerar faturas automaticamente.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 295c3b099c9670c930fb2ba2fd208be63a77217f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122447"
---
# <a name="configure-automatic-invoice-creation"></a>Configurar a criação automática de faturas

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_


Complete os seguintes passos para configurar a execução de uma fatura automatizada no Dynamics 365 Project Operations.

1. Aceda a **Definições** > **Tarefas de lote**.
2. Crie uma tarefa de lote e atribua-lhe o nome **Criar faturas nas operações do Projeto**. O nome da tarefa de lote tem de incluir as palavras "criar faturas".
3. No campo **Tipo de Tarefa**, selecione **Nenhum**. Por predefinição, as opções **Frequência Diária** e **Está Ativo** estão definidas como **Sim**.
4. Selecione **Executar Fluxo de Trabalho**. Na caixa de diálogo **Pesquisar Registo**, verá três fluxos de trabalho:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Selecione **ProcessRunCaller** e, em seguida, selecione **Adicionar**.
6. Na caixa de diálogo seguinte, selecione **OK**. Um fluxo de trabalho de **Suspensão** é seguido por um fluxo de trabalho do **Processo**.

  > [!NOTE]
  > Também pode selecionar **ProcessRunner** no passo 5. Em seguida, quando selecionar **OK**, um fluxo de trabalho do **Processo** é seguido por um fluxo de trabalho de **Suspensão**.

Os fluxos de trabalho **ProcessRunCaller** e **ProcessRunner** criam faturas. O **ProcessRunCaller** chama o **ProcessRunner**. **ProcessRunner** é o fluxo de trabalho que, na realidade, cria as faturas. Passa por todos os itens de contrato para os quais é necessário criar faturas e cria faturas para essas linhas. Para determinar os itens de contrato para os quais devem ser criadas faturas, a tarefa examina as datas de execução da fatura para os itens de contrato. Se os itens de contrato que pertencem a um contrato tiverem a mesma data de execução da fatura, as transações são combinadas numa fatura que tem duas linhas de fatura. Se não houver transações para as quais criar faturas, a tarefa ignorará a criação da fatura.

Depois de **ProcessRunner** ter terminado a execução, chama o **ProcessRunCaller**, fornece a hora de fim e é fechado. **ProcessRunCaller** em seguida, inicia um temporizador que funciona durante 24 horas a partir da hora de fim especificada. No final do temporizador, o **ProcessRunCaller** é fechado.

A tarefa de processamento em lote para criar faturas é uma tarefa recorrente. Se este processamento em lote for executado muitas vezes, são criadas várias instâncias da tarefa e causam erros. Consequentemente, deverá iniciar o processamento em lote apenas uma vez, e só deverá reiniciá-lo se parar de ser executado.

> [!NOTE]
> A faturação do lote só funciona para itens de contrato do projeto que são configurados por horários da fatura. Uma linha de contrato com um método de faturação de preço fixo tem de ter marcos configurados. Uma linha de contrato de projeto com um método de faturação de tempo e material necessitará de uma configuração de agenda de faturamento baseado em datas. O mesmo se aplica a uma linha de contratos baseada em projetos.     


[!INCLUDE[footer-include](../includes/footer-banner.md)]