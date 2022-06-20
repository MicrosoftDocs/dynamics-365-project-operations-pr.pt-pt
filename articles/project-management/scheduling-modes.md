---
title: Modos de agendamento
description: Este artigo fornece informações sobre os modos de agendamento.
author: ruhercul
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 3cbe14f8d458c5d9631e0595912afa8cbb87b9de
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923662"
---
# <a name="scheduling-modes"></a>Modos de agendamento

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_


Dynamics 365 Project Operations fornece a capacidade para as organizações definirem como gerem as alterações às variáveis-chave nas tarefas dentro da estrutura hierárquica de trabalho. Com base nas necessidades específicas da organização, os gestores de projeto podem fazer alterações ao modo de agendamento quando um projeto é criado.

Existem três modos de agendamento disponíveis no Project Operations:

  - Duração fixa (este é o modo predefinido)
  - Esforço fixo (*Trabalho*)
  - Unidades fixas

Os valores impactados pela definição de um modo de programação específico são determinados pela seguinte fórmula:

  Esforço = Duração x Unidades

Quando se define o modo de agendamento de um projeto, está a definir um destes valores, que depois não pode ser alterado. Manter este valor como uma constante coloca uma prioridade nesse valor, o que notifica o sistema de não o alterar quando os outros dois valores mudam. A tabela seguinte fornece informações sobre os impactos da seleção de um modo específico.

| **Nesta tarefa**             | **Se rever as unidades**   | **Se rever a duração** | **Se rever o esforço**  |
|----------------------|---------------------------|----------------------------|---------------------------|
| Tarefa de unidades fixas     | A duração é recalculada. | O esforço é recalculado.    | A duração é recalculada. |
| Tarefa de esforço fixo    | A duração é recalculada. | As unidades são recalculadas.    | A duração é recalculada. |
| Tarefa de duração fixa  | O esforço é recalculado.   | O esforço é recalculado.    | As unidades são recalculadas.   |

Para obter mais informações sobre as implicações de um determinado modo, consulte [Alterar o tipo de tarefa para agendamento mais preciso](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72). No artigo, o termo **Trabalho** é utilizado em vez de **Esforço**.

## <a name="change-the-organizations-scheduling-mode"></a>Alterar o modo de agendamento da organização

Complete os seguintes passos para definir o modo de agendamento de uma organização.

1. Vá a **Definições** \> **Geral** \> **Parâmetros** e, em seguida, selecione o parâmetro do projeto. 
2. Na página **Parâmetros do projeto**, selecione o modo de agendamento predefinido para a organização e, em seguida, defina a capacidade para o gestor do Projeto sobrepor a definição ao criar um novo projeto.

## <a name="change-the-scheduling-mode-setting-on-a-project"></a>Alterar a definição do modo de agendamento num projeto

Se uma organização permitir que o gestor do projeto substitua o modo de agendamento predefinido, o gestor do projeto pode fazer essa alteração quando criar um novo projeto. No entanto, depois de o projeto ter sido salvo, o modo de agendamento não pode ser alterado.

## <a name="copied-projects"></a>Projetos copiados

Como um projeto é criado quando a ação do projeto copiar é tomada, o gestor do projeto não pode definir o modo de agendamento. O projeto de destino irá sempre estar predefinido no modo definido a nível organizacional.

## <a name="copied-tasks"></a>Tarefas copiadas

Quando uma tarefa é copiada de um projeto para outro, a tarefa herda o modo de agendamento do projeto de destino.
