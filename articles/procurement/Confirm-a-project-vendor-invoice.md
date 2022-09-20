---
title: Confirmar faturas de fornecedor do projeto
description: Este artigo explica como confirmar a fatura de um fornecedor do projeto no Microsoft Dynamics 365 Project Operations e descreve o impacto financeiro da confirmação da fatura de um fornecedor do projeto.
author: suvaidya
ms.date: 8/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 9739b15753aa34c51a0aa1e6dfeb7f590655ca7a
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475448"
---
# <a name="confirm-project-vendor-invoices"></a>Confirmar faturas de fornecedor do projeto

_ **Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados

Quando o parâmetro **É necessária confirmação manual pelo PM** está ativado, as faturas de fornecedor criadas no Microsoft Dataverse têm o estado **Rascunho**. As faturas dos fornecedores que são criadas desta forma têm de ser revistas e confirmadas manualmente. Quando o parâmetro **É necessária confirmação manual pelo PM** está desativado, as faturas de fornecedor que são criadas no Dataverse são confirmadas automaticamente. Não é necessária qualquer ação adicional. 

Depois de verificar todas as linhas de uma fatura de fornecedor no Dynamics 365 Project Operations, selecione **Confirmar** para confirmar a fatura do fornecedor.

Quando seleciona **Confirmar** numa fatura do fornecedor, ocorre o seguinte comportamento:

1. O estado da fatura do fornecedor é atualizado para **Confirmado**.
1. A fatura do fornecedor confirmada e os seus dados relacionados tornam-se só de leitura e não podem ser editados nem eliminados.
1. Se os valores reais de custo se referem a uma linha de fatura do fornecedor como parte do processo de correspondência, todos os valores de custo reais associados à linha de fatura do fornecedor referenciada são revertidos.
1. Os novos valores de custo são criados utilizando as informações do fornecedor na linha de fatura.
1. Já não pode criar diários de correção, processar revocações de entrada de tempo ou cancelar a aprovação do tempo, despesas ou valores reais de materiais originais que foram revertidos.
1. No Dynamics 365 Finance, o valor de **Custo do Projeto** é atualizado utilizando o diário de integração de projeto e a conta de integração de aquisição é *revertida* após a publicação no diário de integração do projeto.

> [!NOTE]
> Se alguma linha numa fatura de fornecedor tiver outro estado de verificação que não **Concluído**, a fatura de fornecedor não pode ser confirmada.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
