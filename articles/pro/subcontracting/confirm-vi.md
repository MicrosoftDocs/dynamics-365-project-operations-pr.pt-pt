---
title: Confirmar uma fatura de fornecedor do projeto
description: Este artigo explica como confirmar a fatura de um fornecedor do projeto no Microsoft Dynamics 365 Project Operations e o impacto financeiro da confirmação da fatura de um fornecedor do projeto.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4dafbe64e0727957068d68f510202a12871b62aa
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261527"
---
# <a name="confirm-a-project-vendor-invoice"></a>Confirmar uma fatura de fornecedor do projeto

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
