---
title: Confirmar uma fatura de fornecedor do projeto
description: Este tópico explica como confirmar a fatura de um fornecedor do projeto no Microsoft Dynamics 365 Project Operations e o impacto financeiro da confirmação da fatura de um fornecedor do projeto.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c248b3baec6d3f14a020e4fa93f3dad50c65b263
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595742"
---
# <a name="confirm-a-project-vendor-invoice"></a>Confirmar uma fatura de fornecedor do projeto

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

Depois de verificar todas as linhas de uma fatura de fornecedor no Microsoft Dynamics 365 Project Operations, pode utilizar a ação Confirmar para confirmar a fatura do fornecedor.

Quando seleciona **Confirmar** numa fatura do fornecedor, ocorre o seguinte comportamento:

1. O estado da fatura do fornecedor é atualizado para **Confirmado**.
2. A fatura do fornecedor confirmada e os seus dados relacionados tornam-se só de leitura e não podem ser editados nem eliminados.
3. Se os valores reais de custo se referem a uma linha de fatura do fornecedor como parte do processo de correspondência, todos os valores de custo reais associados à linha de fatura do fornecedor referenciada são revertidos.
4. Os novos valores de custo são criados utilizando as informações do fornecedor na linha de fatura.
5. Depois de a fatura do fornecedor ser confirmada, já não pode criar diários de correção, processar revocações de entrada de tempo ou cancelar a aprovação do tempo, despesas ou materiais reais originais que foram revertidos.

> [!NOTE]
> Se alguma linha numa fatura de fornecedor tiver outro estado de verificação que não **Concluído**, a fatura de fornecedor não pode ser confirmada.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
