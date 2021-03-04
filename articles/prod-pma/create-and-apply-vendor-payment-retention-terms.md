---
title: Criar e aplicar os termos de retenção de pagamento do fornecedor
description: Este tópico fornece informações sobre como configurar e manter termos de retenção para pagamentos a fornecedores.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 1970a24a5073de6af43db1f1c068332c9ba9c8fe
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082541"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a>Criar e aplicar os termos de retenção de pagamento do fornecedor

[!include [banner](../includes/banner.md)] 

A configuração dos termos de retenção de pagamento a fornecedores para um projeto é útil quando a sua organização quer reter parte dos pagamentos feitos a um fornecedor. Por exemplo, quando pretender reter o pagamento a um fornecedor até que os produtos entregues correspondam às suas expetativas. As condições de retenção de pagamento do fornecedor podem ser especificadas quando negoceia um contrato de fornecedor.

## <a name="create-vendor-payment-retention-terms"></a>Criar os termos de retenção de pagamento do fornecedor

Pode introduzir a percentagem de pagamento do fornecedor pela retenção e a percentagem dos montantes anteriormente retidos a serem libertados. Os valores são automaticamente retidos nas faturas do fornecedor até que o contrato atinja o estado de conclusão especificado. Depois de configurar os termos de retenção, pode aplicá-los a qualquer projeto para esse fornecedor.

Utilize os seguintes passos para configurar e manter termos de retenção para os pagamentos do fornecedor. 

1. Aceda a **Gestão de projetos e contabilística** > **Retenção** > **Termos de retenção de pagamento do fornecedor**.
2. Selecione **Novo** para adicionar um novo termo de retenção do fornecedor. O valor **ID da Regra** para o novo termo é automaticamente introduzido. 
3. Introduza uma breve descrição no campo **Descrição** e, no Separador Rápido **Termos** , selecione **Adicionar linha** para introduzir valores de prazo para os seguintes valores:

   - **Percentagem de unidades entregues** : Insira uma percentagem de conclusão para o termo. Os valores são automaticamente retidos nas faturas do fornecedor até que a fase de conclusão do projeto seja igual à percentagem especificada. Por exemplo, se introduzir 50,00, os valores são retidos até que o projeto esteja 50 por cento concluído.
   - **Percentagem a reter** : Introduza uma percentagem do valor da fatura do fornecedor a reter. Por exemplo, se introduzir 10,00, então 10 por cento do valor numa fatura de fornecedor é mantido até que o projeto atinja a percentagem de conclusão tal como definido no campo **Percentagem de unidades entregues**.
   - **Percentagem a libertar** : Selecione **Adicionar linha** para introduzir uma percentagem de quaisquer montantes previamente retidos a serem libertados para o nível de conclusão do projeto selecionado.

> [!NOTE]
> Se tiver mais de um marco para diferentes níveis de conclusão do projeto, insira uma linha de fim de tempo de retenção separada para cada regra de retenção. Cada linha pode especificar uma percentagem de retenção diferente e uma percentagem de libertação diferente para cada nível de conclusão do projeto designado.

Depois de criar termos de retenção do fornecedor para um fornecedor, pode aplicá-los aos termos de um projeto.

## <a name="apply-vendor-retention-terms-to-a-project"></a>Aplicar termos de retenção de fornecedor a um projeto

1. Vá a **Gestão de projetos e contabilística** > **Projetos** > **Todos os projetos** e abra um projeto a partir da página da lista de projetos.
2. No Separador Rápido **Contratos de fornecedor** , selecione **Adicionar linha**.
3. No campo **Código da conta** , selecione uma das seguintes opções: 

   - **Tabela** : Os termos de retenção do fornecedor aplicam-se a um único fornecedor.
   - **Grupo** : Os termos de retenção do fornecedor aplicam-se a todos os fornecedores de um grupo de fornecedores.
   - **Todos** : Os termos de retenção do fornecedor aplicam-se a todos os fornecedores.

4. No campo **Fornecedor/Grupo de Fornecedores** , selecione o fornecedor ou grupo de fornecedores ao qual se aplicam os termos de retenção do fornecedor. Se selecionou **Todos** no passo anterior, este campo não está disponível.
5. No campo **Termos de retenção do fornecedor** , selecione os termos de retenção que criou no procedimento anterior.
6. Se o projeto também tiver termos paga quando pago (PWP) criados para o fornecedor, insira a percentagem de limiar para o projeto no campo **Percentagem de limiar PWP**.

Os termos de retenção do fornecedor também são apresentados em notas de encomenda que cria para o fornecedor.


[!INCLUDE[footer-include](../includes/footer-banner.md)]