---
title: Transições de estado num subcontrato
description: Este artigo explica as transições de estado num subcontrato no Microsoft Dynamics 365 Project Operations à medida que o subcontrato é criado, executado e fechado.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b41e3d44a17c51778dd850c7d4a48351a5d44554
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919752"
---
# <a name="state-transitions-on-a-subcontract"></a>Transições de estado num subcontrato 

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

Este artigo explica as transições de estado num subcontrato no Microsoft Dynamics 365 Project Operations. Cada estado é representado como rascunho, confirmado, fechado ou cancelado. A imagem a seguir representa as transições de estado.

![Modelo do estado do subcontrato](../media/SubconStates.png)  

A tabela a seguir apresenta uma descrição do que cada estado representa no ciclo de vida de um subcontrato no Project Operations.

| Estado | Description | Transições permitidas |
| --- | --- | --- |
| Rascunho | Isto representa o estado inicial de um subcontrato. As negociações com o fornecedor estão em curso. Os itens e os preços estão sujeitos a modificações. Um subcontrato neste estado pode ser usado para estimar e dotar de requisitos de projeto para recursos e materiais. Também pode ser referenciado em tempo, despesas e utilização de material num projeto. Um subcontrato neste estado pode ser editado e eliminado. | Confirmada |
| Confirmada | Isto representa a fase de um subcontrato após as negociações com o fornecedor sobre preços e itens de linha que estão a ser comprados ser concluída. No entanto, a entrega efetiva de materiais e/ou trabalho por recursos subcontratados ainda está em curso. Um subcontrato neste estado pode ser usado para estimar e dotar de requisitos de projeto para recursos e materiais. Também pode ser referenciado em tempo, despesas e utilização de material num projeto. Um subcontrato neste estado não pode ser editado ou eliminado. O botão **Cancelar** permite-lhe cancelar um subcontrato confirmado. O botão **Reabrir** permite-lhe reabrir o subcontrato para o trazer de volta ao estado de **Rascunho**. Utilize o botão **Fechar** para fechar um subcontrato confirmado. | Fechadas <br> Cancelada <br> Rascunho |
| Fechadas | Isto representa a fase de um subcontrato quando a entrega efetiva de materiais e/ou trabalho por recursos subcontratados é concluída. Um subcontrato neste estado já não pode ser usado para estimar e dotar de requisitos de projeto para recursos e materiais. Além disso, já não pode ser referenciado em tempo, despesas e utilização de material num projeto. Um subcontrato neste estado não pode ser editado ou eliminado. | None |
| Cancelada | Isto representa a fase de um subcontrato quando a entrega efetiva de materiais e/ou trabalho por recursos subcontratados já não é necessária. Um subcontrato neste estado não pode ser utilizado para estimar e dotar de requisitos de projeto para recursos e materiais nem pode ser referenciado em tempo, despesas e utilização de material num projeto. Um subcontrato neste estado não pode ser editado ou eliminado. | None |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
