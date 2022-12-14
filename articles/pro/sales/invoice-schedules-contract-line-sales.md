---
title: Criar agendas de faturação num item de contrato do projeto
description: Este artigo fornece informações sobre a criação de agendas de faturas e marcos.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1a6d0647ee012212a74a674cfa4e995d0e375b77
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824735"
---
# <a name="create-invoice-schedules-on-a-project-contract-line"></a>Criar agendas de faturação num item de contrato do projeto

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

Pode anexar uma agenda de faturação num item de contrato baseado no projeto. A faturação só é permitida após o contrato ser ganho para criar um contrato de Projeto. As agendas de faturação permitem a criação automática de faturas de rascunho para um item de contrato baseado em projetos. Se planeia criar sempre faturas manualmente, pode ignorar a criação de agendas de faturação num item de contrato baseado em projetos ou um item de contrato.

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-contract-line"></a>Criar uma agenda de faturação de tempo e material para um item de contrato baseado em projetos

Quando um item de contrato baseado em projetos tiver um método de faturação de tempo e material, pode criar uma agenda de faturação baseada na data. Para gerar automaticamente uma agenda de faturação baseada na data, conclua os seguintes passos.

1. Aceda a **Definições** > **Frequências de Fatura** para configurar a frequência da fatura.
2. Abra o contrato do projeto e no separador **Resumo**, defina a data de entrega solicitada.
3. Abra o item de contrato de tempo e material para o qual pretende criar uma agenda de faturação baseada em datas. 
4. No separador **Agenda de Faturação**, selecione uma data de início de faturação e a frequência da fatura. 
5. Na subgrelha, selecione **Gerar Agenda de Faturação**.

    O sistema gera a agenda de faturação com as seguintes informações de campo:

    - A **Data de Execução da Fatura** está marcada para a data com base na frequência da fatura.
    - A **Data Limite da Transação** está definida para o dia anterior à **Data de Execução da Fatura**.
    - O **Estado da Execução** é definido automaticamente como **Não Executar**. Quando a tarefa de criação automática de faturas é executada para uma determinada **Data de Execução da Fatura**, este campo é atualizado para **Execução com Êxito** ou **Falha na Execução**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-contract-line"></a>Criar uma agenda de faturação de preço fixo para um item de contrato baseado em projetos

Quando um item de contrato baseado em projetos tem um método de faturação de preço fixo, pode criar uma agenda de faturação baseada em marcos. Complete os seguintes passos para gerar automaticamente uma agenda de faturação baseada em marcos para um conjunto fixo de marcos que distribuem igualmente para o período de calendário.

1. Aceda a **Definições** > **Frequências de Fatura** para configurar a frequência da fatura.
2. Abra o contrato do projeto e no separador **Resumo**, defina a data de entrega solicitada.
3. Abra o item de contrato de preço fixo no qual precisa de criar uma agenda de marcos. 
4. No separador **Agenda de Faturação (Marcos de Faturação)**, selecione a data de início de faturação e a frequência da fatura. 
5. Na subgrelha, selecione **Gerar Marcos Periódicos**.

    O sistema gera a agenda de faturação com as seguintes informações de marco.

    - O **Nome do Marco** está definido para a data que é ditada com base na frequência de faturação.
    - A **Data do Marco** está definido para a data que é ditada com base na frequência de faturação.
    - O **Montante do Marco** é calculado dividindo o valor do contrato no item de contrato baseado em projetos pelo número de marcos ditados pela frequência, início da faturação e datas de entrega solicitadas.
    - Se o item de contrato tiver um valor no campo **Montante Estimado do Imposto**, este campo também é repartido para cada marco igualmente ao gerar marcos periódicos.

Os marcos de faturação devem ser iguais ao valor contratado do item de contrato baseado em projetos. Se não forem iguais, ocorre um erro. Pode corrigir esse erro verificando se os marcos de faturação totalizam o valor contratado do item através da criação, edição ou eliminação de marcos. Depois de efetuadas as alterações, atualize a página.

### <a name="manually-create-milestones"></a>Criar marcos manualmente

Os marcos de preço fixo podem ser gerados manualmente quando não são divididos periodicamente. Para criar um marco manualmente, complete os seguintes passos.

1. Abra o item de contrato de preço fixo no qual pretende criar um marco. 
2. No separador **Agenda de Faturação**, na subgrelha, selecione **+ Criar novo marco do Item de contrato**.
3. No formulário **Criação do Marco**, insira as informações necessárias com base na tabela seguinte. 

| Campo | Localização | Descrição | Impacto a jusante |
| --- | --- | --- | --- |
| Nome do Marco | Criação Rápida | Campo de texto para o nome do marco. | Este campo está incluído no marco do item de contrato do projeto e na fatura. |
| Tarefa de Projeto | Criação Rápida | Se o marco estiver ligado a uma tarefa do projeto, utilize esta referência para adicionar lógica personalizada e defina um marco com base no estado da tarefa. | Não há qualquer impacto a jusante desta referência para uma tarefa. |
| Data do Marco | Criação Rápida | A data em que o processo automático de criação de faturas deve procurar o estado deste marco para considerá-lo para faturação. | Este está incluído no marco do item de contrato do projeto e na fatura. |
| Estado da Fatura | Criação Rápida | Quando o marco é criado, este estado está sempre definido para **Não está pronto para faturação** ou **Não iniciado**. | Este está incluído no marco do item de contrato do projeto e na fatura. |
| Montante de Linha | Criação Rápida | O montante ou valor do marco que será faturado ao cliente. | Este campo está incluído no marco do item de contrato do projeto e na fatura. |
| Imposto | Criação Rápida | O valor do imposto aplicado ao marco. | Este está incluído no marco do item de contrato do projeto e na fatura. |

4. Selecione **Guardar e Fechar**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
