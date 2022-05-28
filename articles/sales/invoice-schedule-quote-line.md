---
title: Agendas de faturação nas linhas de proposta baseadas no projeto
description: Este tópico fornece informações sobre como criar marcos e agendas de faturação para linhas de proposta.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 6b443a353c98fe5c7475d8a95c99abe01cd00987
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601078"
---
# <a name="invoice-schedules-on-project-based-quote-lines"></a>Agendas de faturação nas linhas de proposta baseadas no projeto

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Uma linha de proposta baseada no projeto dá a capacidade de expressar uma agenda de faturação. Isto é opcional durante a fase de proposta porque a aplicação não suporta a faturação de um projeto quando está associado a uma linha Proposta. A faturação só é permitida depois de a proposta ser ganha. O único impacto a jusante da criação de uma agenda de faturação durante a fase de proposta reside no facto de esta agenda de faturação ser copiada para o item de contrato baseado no projeto. Se não criar uma agenda de faturação durante a fase de proposta, poderá fazê-lo no item de contrato baseado no projeto.

Globalmente, o objetivo das agendas de faturação consiste em permitir a criação automática de faturas de rascunho para um item de contrato baseado no projeto. 

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-quote-line"></a>Criar uma agenda de faturação Tempo e material para uma linha de proposta baseada no projeto

Quando o método de faturação para uma linha de proposta baseada no projeto for Tempo e material, o sistema gera uma agenda de faturação baseada na data. Para gerar automaticamente uma agenda de faturação baseada na data, conclua os seguintes passos.

1. Vá para **Definições** > **Frequências de faturação** e configure uma frequência de faturação.
2. Na página **Propostas**, abra a Proposta do projeto e, no separador **Resumo**, defina uma data de entrega pretendida.
3. Abra a linha de proposta de tempo e material para a qual precisa de criar uma agenda de faturação baseada na data. 
4. No separador **Agenda de Faturação**, selecione os valores nos campos **Início da faturação** e **Frequência da Faturação**. 
5. Na subgrelha, selecione **Gerar Agenda de Faturação**.
6. A aplicação gera a agenda de faturação com os campos **Data de Execução da Fatura**, **Data Limite da Transação** e **Estado da Execução** da seguinte forma:

    - A **Data de Execução da Fatura** está definida para a data ditada com base na frequência de faturação.
    - A **Data limite da transação** está definida para o dia anterior à **Data de Execução da Fatura**.
    - O **Estado da Execução** é definido automaticamente como **Não Executar**. Quando a tarefa de criação automática de faturas é executada para uma determinada data de execução da faturação, atualizará este campo para **Execução com Êxito** ou **Falha na Execução**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-quote-line"></a>Criar uma agenda de faturação de Preço fixo para uma linha de proposta baseada no projeto

Quando a linha de proposta baseada no projeto tem um método de faturação **Fixo**, o sistema cria uma agenda de faturação baseada em marcos. Conclua os seguintes passos para gerar automaticamente esta agenda para um conjunto fixo de marcos que são distribuídos igualmente para o período de calendário.

1. Vá para **Definições** > **Frequências de faturação** e configure uma frequência de faturação.
2. Na página **Propostas**, abra a Proposta do projeto e, no separador **Resumo**, defina uma data de entrega pretendida.
3. Abra a linha de proposta de preço fixo para a qual precisa de criar uma agenda de marcos. 
4. No separador **Agenda de Faturação**, selecione os valores nos campos **Início da faturação** e **Frequência da Faturação**. 
5. Na subgrelha, selecione **Gerar Marcos Periódicos**.
6. A aplicação gera a agenda de faturação com um nome, data e valor do marco.

    - O nome do marco está definido para a data ditada com base na frequência de faturação.
    - A data do marco está definida para a data ditada com base na frequência de faturação.
    - O valor do marco é calculado ao dividir o valor da proposta na linha de proposta baseada no projeto pelo número de marcos, conforme ditados pela frequência, e pelo início de faturação e as datas de entrega pretendidas.
    - Se a Linha de proposta também tiver como valor do imposto estimado, este valor é dividido entre cada marco equitativamente ao gerar marcos periódicos.

### <a name="manually-create-milestones"></a>Criar marcos manualmente

Também podem ser gerados manualmente marcos de preço fixo quando não são divididos periodicamente. Para criar um marco manualmente:

Abra a Linha de proposta de preço fixo onde precisa de criar um marco. No separador **Agenda de Fatura**, na subgrelha, selecione **+ Criar novo marco da linha de proposta** e introduza as informações necessárias com base na tabela seguinte.

| **Campo** | **Localização** | **Descrição** | **Impacto a jusante** |
| --- | --- | --- | --- |
| Nome do marco | Criação rápida | O nome do marco. | Isto é propagado para o marco do item de contrato do projeto e para a fatura |
| Tarefa de Projeto | Criação rápida | Se o marco estiver associado à tarefa do projeto, poderá utilizar esta referência para adicionar lógica personalizada e definir o estado do marco baseado no estado da tarefa. | A aplicação não tem qualquer impacto a jusante desta referência a uma tarefa. |
| Data do marco | Criação rápida | Defina a data em que o processo automático de criação de faturas deve procurar o estado deste marco para considerá-lo para faturação. | Isto é propagado para o marco do item de contrato do projeto e para a fatura. |
| Estado da fatura | Criação rápida | Quando um marco é criado, este estado está sempre definido como **Não pronto para faturação**. | Isto é propagado para o marco do item de contrato do projeto e para a fatura. |
| Montante de Linha | Criação rápida | Montante ou valor do marco que será faturado ao cliente. | Isto é propagado para o marco do item de contrato do projeto e para a fatura. |
| Imposto | Criação rápida | Montante de imposto que será aplicado ao marco. | Isto é propagado para o marco do item de contrato do projeto e para a fatura. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]