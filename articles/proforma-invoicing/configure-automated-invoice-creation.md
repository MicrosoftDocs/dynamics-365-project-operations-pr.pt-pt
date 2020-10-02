---
title: Configurar uma criação automatizada de faturas
description: Este tópico fornece informações sobre como configurar o sistema para gerar faturas automaticamente.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 764fd4568619e4f5676ee3cbf7fce14ffb069548
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898140"
---
# <a name="configure-automated-invoice-creation"></a>Configurar uma criação automatizada de faturas

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Complete os seguintes passos para configurar a execução de uma fatura automatizada nas operações do Projeto.

1. Aceda a **Definições** \> **Tarefas de lote**.
2. Crie uma tarefa de lote e atribua-lhe o nome **Criar faturas nas operações do Projeto**. O nome da tarefa de lote tem de incluir o termo "criar faturas."
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
> A faturação do lote só funciona para itens de contrato do projeto que são configurados por horários da fatura. Uma linha de contrato com um método de faturação de preço fixo tem de ter marcos configurados. Uma linha de contrato de projeto com um método de faturação de tempo e material necessitará de uma configuração de agenda de faturamento baseado em datas. O mesmo se aplica a uma linha de contratos baseada em projetos.     
