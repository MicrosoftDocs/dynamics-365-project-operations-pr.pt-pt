---
title: Cancelar uma fatura de fornecedor do projeto
description: Este artigo explica como cancelar a fatura de um fornecedor do projeto no Microsoft Dynamics 365 Project Operations e o impacto financeiro do cancelamento da fatura de um fornecedor do projeto.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 79d00a91f9ab2d66eab2f80349d6f1fba1934f94
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261105"
---
# <a name="cancel-a-project-vendor-invoice"></a>Cancelar uma fatura de fornecedor do projeto

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

Depois de uma fatura de fornecedor ser confirmada, não pode ser editada ou eliminada. Se tiver sido confirmado um erro na fatura de um fornecedor, poderá utilizar a ação Cancelar para reverter o impacto na fatura do fornecedor e criar uma nova fatura de fornecedor.

Quando seleciona **Cancelar** numa fatura do fornecedor, ocorre o seguinte comportamento:

1. O estado da fatura do fornecedor é atualizado para **Cancelado**.
2. A fatura do fornecedor cancelada e os seus dados relacionados tornam-se só de leitura e não podem ser editados nem eliminados.
3. Todos os valores de custo reais que foram criados com base em linhas de fatura do fornecedor como parte da confirmação da fatura do fornecedor são revertidos.
4. Se os valores reais de custo foram associados às linhas de fatura do fornecedor como parte do processo de correspondência, a confirmação da fatura do fornecedor original reverteu-as. Durante o cancelamento da fatura do fornecedor, esses custos reais são criados de novo. As origens apontam para as entradas de hora, despesas ou utilização de material.
5. Depois de a fatura do fornecedor ser cancelada, já pode criar novamente diários de correção, processar revocações de entrada de tempo e cancelar a aprovação do tempo, despesas ou materiais reais originais que foram revertidos.

> [!NOTE]
> Apenas as faturas de fornecedor de projeto confirmadas podem ser canceladas. As faturas de fornecedores noutros estados não podem ser canceladas.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
