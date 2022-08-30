---
title: Transições de estado numa fatura de fornecedor
description: Este artigo explica as transições de estado numa fatura de fornecedor no Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e25e4d63d4c9098112a7f40abe60c7184018d582
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261058"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Transições de estado numa fatura de fornecedor

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

Este artigo explica as transições de estado numa fatura de fornecedor no Microsoft Dynamics 365 Project Operations. São utilizados os seguintes estados: **Rascunho**, **Em revisão**, **Confirmado**, **Em espera** e **Cancelado**.

As seguintes ilustrações mostram as transições de estado.

![Modelo de transição de estado de subcontrato.](../media/VI_State_Model.jpg)

A tabela a seguir explica o que cada estado representa no ciclo de vida de uma fatura de fornecedor no Project Operations.

| Estado | Description | Transições permitidas |
| --- | --- | --- |
| Rascunho | Este estado é o estado inicial de uma fatura de fornecedor. As linhas e os preços estão sujeitos a modificação. Uma fatura de fornecedor neste estado não podem ser editada nem eliminada. | Em processamento |
| Em revisão | Este estado representa o estado de processamento de uma fatura de fornecedor. Pelo menos uma linha de fatura de fornecedor tem o estado de verificação **Em progresso**. | Confirmado, Em espera |
| Confirmada | Este estado representa a fase de uma fatura de fornecedor na qual a aplicação criou os valores reais de custo para cada linha de fatura do fornecedor. Os valores reais de custo associados que tenham sido associados às linhas de fatura do fornecedor foram revertidos e substituídos pelo custo real dessas linhas de fatura do fornecedor. Uma fatura de fornecedor neste estado não pode ser editada ou eliminada. Pode utilizar o botão **Cancelar** para cancelar uma fatura de fornecedor confirmada. A ação Cancelar reverte o impacto da ação Confirmar. | Cancelada |
| Em espera | <p>Este estado representa uma fase da fatura de um fornecedor onde a fatura do fornecedor não se pode mover devido a um problema na fatura ou no estado do fornecedor. Uma fatura de fornecedor neste estado não pode ser confirmada, cancelada, editada ou eliminada.</p><p>Pode utilizar a ação Reabrir para mover a fatura do fornecedor para o estado **Rascunho** ou **Em revisão**. Se pelo menos uma linha na fatura do fornecedor tiver um estado de verificação **Em progresso** ou **Concluído**, a fatura do fornecedor será reaberta no estado **Em revisão**. Se todas as linhas na fatura do fornecedor tiver um estado de verificação **Não iniciado**, a fatura do fornecedor será reaberta no estado **Rascunho**.</p> | Rascunho, Em revisão |
| Cancelada | Este estado representa a fase de um subcontrato em que a entrega efetiva de materiais e/ou trabalho por recursos subcontratados já não é obrigatória. Um subcontrato neste estado não pode ser utilizado para estimar e dotar de requisitos de projeto para recursos e materiais e também não pode fazer referência a tempo, despesas e utilização de material num projeto. Um subcontrato neste estado não pode ser editado ou eliminado. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
