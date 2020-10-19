---
title: Definir calendários de recursos
description: Este tópico fornece informações sobre como definir os calendários de horas de trabalho para os recursos no Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ab39d7e5dc2d8c01ed49ca0f1a4d1691aaf15637
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961924"
---
# <a name="define-resource-calendars"></a>Definir calendários de recursos

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Cada recurso reservável que trabalhe num projeto tem de ter um calendário de horas de trabalho para definir a sua disponibilidade. As horas de trabalho para um recurso podem ser definidas de duas formas: 

   - Definir regras de calendário individuais para um recurso
   - Aplicar um modelo de calendário existente para o recurso

## <a name="define-a-resources-working-hours"></a>Definir as horas de trabalho de um recurso

1. No menu **Recursos**, selecione **Recursos**.
2. A partir da vista de grelha, selecione o **Recurso Reservável** aplicável.
3. Na página **Detalhes do Recurso**, selecione o separador **Horas de Trabalho**. Por predefinição, o calendário de recursos reservados assume por predefinição as horas de trabalho do modelo de horas de trabalho predefinido que é definido para a organização.
4. Para atualizar as horas de trabalho, clique com o botão direito na data de início da regra de calendário proposta a definir. Utilize o menu de regras do calendário para definir uma regra de calendário para um dia específico, o restante da série ou todo o calendário.
5. Após a seleção da opção, pode definir:

    - O dia da semana em que se aplicarão as horas de trabalho.
    - As horas de trabalho em cada dia.
    - O fuso horário para a regra de calendário.
    - Se aplicável, o tempo não dedicado ao trabalho também pode ser especificado para a regra.

## <a name="applying-a-calendar-template-to-a-resource"></a>Aplicar um modelo de calendário para um recurso

1. No menu **Recursos**, selecione **Recursos**.
2. A partir da vista da grelha, selecione até 25 **Recursos Reserváveis** para atualizar.
3. Ao selecionar **Definir Calendário**, é aberta uma caixa de diálogo que apresenta uma lista dos modelos de horas de trabalho disponíveis.
4. Selecione o modelo que pretende utilizar e, em seguida, selecione **Aplicar**.
