---
title: Inscreva-se nas subscrições de pré-visualização do Project Operations para os cenários de recursos/não armazenados
description: Este tópico fornece informações sobre como subscrever e implementar o Project Operations para cenários baseados em recursos/não armazenados.
author: sigitac
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 1b8c8982ede83191ce346e76718322d47abf0dd8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000450"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Inscreva-se nas subscrições de pré-visualização do Project Operations para os cenários de recursos/não armazenados

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Este tópico explica como subscrever a oferta pré-visualizar/parceiro e implementar o ambiente do Project Operations para os cenários baseados em recursos/não armazenados.

## <a name="prerequisites"></a>Pré-requisitos

- Receberá um e-mail a convidá-lo para participar na pré-visualização. Pode solicitar uma pré-visualização no [Web site do Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- O utilizador que implementar a pré-visualização tem de ter direitos de administrator global do inquilino do Azure.
- A implementação de um ambiente do Finance requer uma subscrição válida do Azure que será faturada por ambiente. Poderá utilizar subscrição existente das suas organizações ou utilizar uma [Avaliação do Azure](https://azure.microsoft.com/en-us/free/) para começar. O ambiente do CDS será disponibilizado gratuitamente durante um período limitado de 30 dias.

## <a name="subscribe"></a>Subscrever

Quando o seu [pedido de pré-visualização](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) for aprovado, receberá três ofertas da Microsoft por e-mail. Estas ofertas permitem implementar a Pré-visualização do Project Operations:

- Dynamics 365 Project Operations (CRM) – Avaliação da Pré-visualização
- Office 365 Project Operations – Avaliação da Pré-visualização
- Dynamics 365 Finance – Avaliação da Pré-visualização

> [!IMPORTANT]
> Só uma pessoa, o administrador inquilino, numa organização precisa de executar esta tarefa. Se não for subscritor desta versão, aguarde até a sua organização estar inscrita e receber as suas credenciais de utilizador.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM) – Avaliação da Pré-visualização 

Antes de começar, certifique-se de que está a iniciar sessão num browser com a conta de profissional de utilizador no inquilino onde pretende a pré-visualização do Project Operations.

1. Resgate o primeiro código de oferta, **Dynamics 365 Project Operations (CRM) – Avaliação da Pré-visualização**, colando-o no URL do browser.

![Resgatar Oferta](./media/16RedeemFirstOfferNew.png)

2. Confirme a encomenda.

![Confirme a encomenda](./media/17ConfirmOrderNew.png)

Verá que a oferta de confirmação foi resgatada com sucesso.

![Confirmação](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Project Operations – Avaliação da Pré-visualização

Repita os mesmos passos que com o primeiro código de oferta. Certifique-se de que adiciona o segundo código de oferta usando a mesma conta de utilizador que foi usada com o código da primeira oferta.

### <a name="dynamics-365-finance-preview-trial"></a>Avaliação da pré-visualização do Dynamics 365 Finance

Repita os mesmos passos com a última oferta do e-mail de boas-vindas.

## <a name="assign-licenses"></a>Atribuir licenças

> [!IMPORTANT]
> Necessitará de acesso administrativo ao Portal Microsoft 365 da sua organização do para concluir os seguintes passos.

1. Vá para o [Centro de administração do Microsoft 365](https://portal.office.com/) para atribuir as licenças aos seus utilizadores.

![Home page do centro de administração](./media/14AdminPortal.png)

2. Na página **Utilizadores ativos**, selecione os utilizadores aos quais pretende atribuir uma licença.

![Atribuir Licenças](./media/15AssignLicenses.png)

3. Verifique se as licenças **Pré-visualização do Dynamics 365 Project Operations (CRM)** e **Office 365 Project Operations – Pré-visualização** foram selecionadas e selecione **Guardar alterações**.

> [!NOTE]
> A oferta de avaliação do Finance não precisa de ser atribuída a um utilizador.

## <a name="start-a-new-project-in-lcs"></a>Iniciar um novo projeto no LCS

Criar um novo projeto LCS conforme descrito no tópico [Iniciar um novo projeto no LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Adicionar uma subscrição do Azure a um projeto LCS

Para concluir esta tarefa, siga os passos na tópico, [Adicionar uma subscrição do Azure ao projeto LCS](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Implementar o ambiente de demonstração do Finance com o Project Operations para cenários de recursos/non armazenados

Siga as orientações no tópico [Aprovisionar um novo ambiente](resource-provision-new-environment.md) para concluir a implementação. Utilize o tipo de implementação do [ambiente de demonstração](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) para pré-visualização. 

## <a name="install-cds-setup-and-configuration-data"></a>Instalar dados de configuração do CDS

Instale os dados de configuração do CDS descritos no tópico [Configurar e aplicar dados de configuração no Common Data Service](resource-apply-pro-setup-config-data.md).
Complete este passo apenas após a implementação do ambiente de demonstração do Finance e os dados de demonstração no FO estarem prontos.


[!INCLUDE[footer-include](../includes/footer-banner.md)]