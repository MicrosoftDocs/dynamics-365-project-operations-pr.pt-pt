---
title: Inscreva-se nas subscrições de pré-visualização do Project Operations para os cenários de recursos/não armazenados
description: Este tópico fornece informações sobre como subscrever e implementar o Project Operations para cenários baseados em recursos/não armazenados.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949022"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Inscreva-se nas subscrições de pré-visualização do Project Operations para os cenários de recursos/não armazenados

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Este tópico explica como subscrever a oferta pré-visualizar/parceiro e implementar o ambiente do Project Operations para os cenários baseados em recursos/não armazenados.

## <a name="prerequisites"></a>Pré-requisitos

- Receberá um e-mail a convidá-lo para participar na pré-visualização. Pode solicitar uma pré-visualização no [Web site do Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- O utilizador que implementar a pré-visualização tem de ter direitos de administrator global do inquilino do Azure.
- A implementação de um ambiente do Finance requer uma subscrição válida do Azure que será faturada por ambiente. Poderá utilizar subscrição existente das suas organizações ou utilizar uma [Avaliação do Azure](https://azure.microsoft.com/en-us/free/) para começar. O ambiente do CDS será disponibilizado gratuitamente durante um período limitado de 30 dias.

## <a name="subscribe"></a>Subscrever

Quando o seu [pedido de pré-visualização](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) for aprovado, receberá duas ofertas da Microsoft por e-mail. Estas ofertas permitem implementar a Pré-visualização do Project Operations:

- Dynamics 365 Project Operations – Avaliação da Pré-visualização
- Avaliação da Pré-visualização do Dynamics 365 for Finance and Operations.

> [!IMPORTANT]
> Só uma pessoa, o administrador inquilino, numa organização precisa de executar esta tarefa. Se não for subscritor desta versão, aguarde até a sua organização estar inscrita e receber as suas credenciais de utilizador.

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations – Avaliação da pré-visualização

1. Resgate a primeira oferta, **Avaliação do Dynamics 365 Project Operations**, com o URL fornecido no seu e-mail de boas-vindas.

![Primeira Oferta](./media/1FirstOffer.png)

2. Verifique se tem sessão iniciada como o utilizador que pertence à organização que irá subscrever o serviço.
3. Prossiga com o resgate da oferta. 
4. Selecione **Sim, adicioná-la à minha conta**.

![Resgatar Oferta](./media/2RedeemFirstOffer.png)

![Confirmar Oferta](./media/3ConfirmFirstOffer.png)

![Oferta Resgatada](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a>Avaliação da pré-visualização do Dynamics 365 Finance

Repita os mesmos passos com a segunda oferta do e-mail de boas-vindas.

## <a name="assign-licenses"></a>Atribuir Licenças

> [!IMPORTANT]
> Necessitará de acesso administrativo ao Portal Office 365 da sua organização para concluir os seguintes passos.

1. Vá para o [Centro de administração do Microsoft 365](https://portal.office.com/) para atribuir licenças aos seus utilizadores.

![Portal de Administração do Office](./media/5OfficeAdminPortal.png)

2. Na página **Utilizadores ativos**, selecione os utilizadores aos quais pretende atribuir uma licença.

![Atribuir Licenças](./media/6AssignLicenses.png)

3. Verifique se a licença do Project Operations foi selecionada e selecione **Guardar alterações**. 

> [!NOTE]
> A oferta de avaliação do Finance não precisa de ser atribuída a um utilizador.

## <a name="start-a-new-project-in-lcs"></a>Iniciar um novo projeto no LCS

Criar um novo projeto LCS conforme descrito no tópico [Iniciar um novo projeto no LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Adicionar uma subscrição do Azure a um projeto LCS

Para concluir esta tarefa, siga os passos na tópico, [Adicionar uma subscrição do Azure ao projeto LCS](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Implementar o ambiente de demonstração do Finance com o Project Operations para cenários de recursos/non armazenados

Siga as orientações no tópico [Aprovisionar um novo ambiente](resource-provision-new-environment.md) para concluir a implementação. Utilize o tipo de implementação do [ambiente de demonstração](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) para pré-visualização.

## <a name="install-cds-setup-and-configuration-data"></a>Instalar dados de configuração do CDS

Instale os dados de configuração do CDS descritos no tópico [Configurar e aplicar dados de configuração no Common Data Service](resource-apply-pro-setup-config-data.md).

