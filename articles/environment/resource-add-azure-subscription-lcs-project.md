---
title: Adicionar uma subscrição do Azure ao projeto LCS
description: Este tópico fornece informações sobre como ligar a sua subscrição do Azure a um projeto LCS.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0b5703542ac58adcc710890d9676dd0090a82f25
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082275"
---
# <a name="add-an-azure-subscription-to-lcs-project"></a>Adicionar uma subscrição do Azure ao projeto LCS

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Os ambientes alojados na cloud têm de ser implementados através de uma subscrição do Azure existente. Este tópico explica como ligar a sua subscrição do Azure existente a um projeto LCS. 

## <a name="grant-admin-consent"></a>Conceder consentimento do administrador

1. No seu projeto LCS, na secção **Ambientes** , selecione **Definições do Microsoft Azure**.

![Definições do Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. Na página **Definições do projeto** , no separador **Conectores do Azure** , selecione **Autorizar**. Isto permite que os ambientes sejam implementados neste projeto.

![Conectores do Azure](./media/2AzureConnectors.png)

3. Selecione **Autorizar** novamente para fornecer o consentimento do administrador.

![Conceder Consentimento do Administrador](./media/3GrantAdminConsent.png)

4. Aceite o pedido de permissões.

![Aceitar o Pedido de Permissão.](./media/4AcceptPermissionRequest.png)

A autorização está agora concluída. 

![Autorização Com Êxito](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a>Fornecer acesso dos Serviços de Implementação do Dynamics à sua subscrição do Azure

1. Vá para to [Faturação do Microsoft Azure](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) e selecione a sua subscrição. Os Serviços de Implementação do Dynamics precisam de acesso a esta subscrição para conseguirem implementar ambientes.

![Detalhes da Subscrição do Azure](./media/6AzureSubscription.png)

2. Selecione **Controlo de acesso (IAM)** no painel de navegação e selecione **Adicionar Atribuição de Função**.
3. No controlo de deslize no lado direito, selecione **Função de contribuidor** e, na lista fornecida, localize e selecione **Serviços de Implementação do Dynamics**. 
4. Selecione **Guardar**.

![Acesso à Subscrição](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a>Adicionar um conector de subscrição a um projeto LCS

1. No seu projeto LCS, na página **Definições do Microsoft Azure** , selecione **Adicionar** para adicionar um novo conector.
2. Introduza o seu ID de subscrição do Azure. Poderá localizar o seu ID de subscrição do Azure no [Portal do Azure](https://ms.portal.azure.com/), em  **Definições** na parte inferior esquerda do ecrã.
3. No campo **Configurar para utilizar o Azure Resource Manager** , selecione **Sim**.
4. Certifique-se de que o Domínio do Inquilino do AAD da Subscrição do Azure corresponde à subscrição do Azure proprietária do domínio que está utilizar e selecione **Seguinte**.
5. No ecrã **Configuração do Microsoft Azure** , selecione **Seguinte** para confirmar. Se receber um erro neste ecrã, volte à secção [Fornecer acesso aos Serviços de Implementação do Dynamics à subscrição do Azure](#provide) neste tópico e certifique-se de que concluiu todos os passos.
6. Transfira o Certificado de Gestão do Azure para uma pasta local no seu computador e, em seguida, carregue-a para o Portal de Gestão do Azure em **Definições** > **Certificados de Gestão**. Este certificado permitirá que o LCS comunique com a Azure em seu nome. Pode ignorar este passo se o seu utilizador tiver acesso à subscrição.
7. Selecione **Seguinte**.
8. Selecione a região do Azure onde fazer a implementação e selecione um centro de dados que esteja perto de onde planeia utilizar este sistema.
9.  Selecione **Ligar**.

Ligou com êxito a sua subscrição do Azure. Pode agora implementar os ambientes alojados na cloud do Dynamics 365 Finance.


