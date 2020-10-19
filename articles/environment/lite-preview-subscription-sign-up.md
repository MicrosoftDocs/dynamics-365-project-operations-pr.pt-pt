---
title: Inscrever-se para obter uma subscrição de pré-visualização
description: Este tópico fornece informações sobre como subscrever e implementar o Project Operations lite - oportunidade potencial para fatura pró-forma.
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a9c1432e8971eeb7918e23e00be9989294335f49
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949019"
---
# <a name="sign-up-for-a-preview-subscription-for-lite-deployment--deal-to-proforma-invoicing"></a>Inscreva-se numa subscrição de pré-visualização para implementação leve – oportunidade potencial para fatura pró-forma

Este tópico explica como subscrever a oferta de parceiros de pré-visualização e implementar a Implementação leve do Dynamics 365 Project Operations - oportunidade potencial para fatura pró-forma.

> [!NOTE]
> Este processo será alterado nas próximas versões do Project Operations.

## <a name="prerequisites"></a>Pré-requisitos

- Receberá um e-mail a convidá-lo para participar na pré-visualização. Pode solicitar uma pré-visualização no [Web site do Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- O utilizador que implementar a pré-visualização tem de ter direitos de administrator global do inquilino do Azure.
- O utilizador que implementar a pré-visualização precisará de um número de telefone e de um cartão de crédito válido. Durante a inscrição, não haverá encargos no cartão durante seis meses. Após seis meses, terá de cancelar a subscrição. 
- Reveja todos os termos e condições.

## <a name="subscribe"></a>Subscrever

Quando receber uma aprovação de [pedido de pré-visualização](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), receberá duas ofertas da Microsoft por e-mail. Estas ofertas permitem implementar a Pré-visualização do Project Operations:

- Avaliação da pré-visualização do Dynamics 365 Customer Service – código de utilização única
- Dynamics 365 Project Operations – avaliação da pré-visualização

### <a name="dynamics-365-customer-service-paid-offer"></a>Oferta paga do Dynamics 365 Customer Service

1. Através de uma janela de browser InPrivate/Incognito, troque o primeiro código de oferta pelo Dynamics 365 Customer Service. Para se inscrever no Customer Service, vai precisar do seguinte:

- Um número de telefone
- Um cartão de crédito. Quando se inscrever, não haverá encargos no cartão durante seis meses. Após seis meses, terá de cancelar a subscrição.
- Reveja todos os termos e condições.

2. Forneça as suas informação de contacto.

![Informações de Contacto](./media/1ContactInformation.png)

3. Forneça os novos detalhes do inquilino.

![Criar ID de Utilizador](./media/2CreateUserID.png)

4. Verifique a sua identidade, guarde o seu novo ID do utilizador e, em seguida, selecione **Configurar**.

![Guardar Informações](./media/3SaveInfo.png)

5. Conclua a inscrição do cartão de crédito e reveja todos os termos e condições. 

![Concluir Cartão de Crédito](./media/4CompleteCreditCard.png)

![Finalização da Compra com o Cartão de Crédito](./media/5CreditCardCheckout.png)

![Guardar Encomenda](./media/6SaveOrder.png)

![Confirmação do cartão de crédito](./media/7Confirmation.png)

## <a name="cancel-the-dynamics-365-customer-service-enterprise-offer"></a>Cancelar a oferta empresarial do Dynamics 365 Customer Service

A Oferta Empresarial do Dynamics 365 Customer Service é fornecida gratuitamente durante seis meses. A oferta será renovada à taxa total no final do período de seis meses. Para cancelar antes da data de renovação, preencha as seguintes instruções. 

> [!NOTE]
> Depois de concluir estes passos, deixará de poder utilizar o ambiente de pré-visualização pública do Project Operations.

1. Vá para o [Portal de administração](https://admin.microsoft.com/) e, em **Faturação**, selecione **Os Seus Produtos**.

![Portal de Administração, página Os Seus Produtos](./media/8AdminPortal.png)

2. Selecione a **Oferta Empresarial do Dynamics 365 Customer Service**.

![Cancelar Subscrição](./media/9CancelSubscription.png)

3. Selecione **Definições** > **Ações** > **Cancelar Subscrição**.
4. No formulário **Cancelamento da subscrição**, introduza as informações nos campos obrigatórios.
5. Selecione **Cancelar** > **Subscrição**.

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations – Avaliação da pré-visualização

1. Resgate a segunda oferta, Avaliação do Dynamics 365 Project Operations, com o URL fornecido no seu e-mail de boas-vindas.

![Resgatar Oferta 2](./media/10RedeemOffer2.png)

2. Verifique se tem sessão iniciada como o utilizador que pertence à mesma organização que foi subscrita através do código da primeira oferta e, em seguida, avance para o resgate da oferta. 
3. Selecione **Sim, adicioná-la à minha conta**.

![Adicionar à Conta](./media/11AddToAccount.png)

![Experimentar Novo Ecrã](./media/12TryNow.png)

![Detalhes da encomenda](./media/13Confirmation.png)

## <a name="assign-licenses"></a>Atribuir licenças

> [!IMPORTANT]
> Necessitará de acesso administrativo ao Portal Office 365 da sua organização para concluir os seguintes passos.

1. Vá para o [Centro de administração do Microsoft 365](https://portal.office.com/) para atribuir as licenças aos seus utilizadores.

![Home page do centro de administração](./media/14AdminPortal.png)

2. Na página **Utilizadores ativos**, selecione os utilizadores aos quais pretende atribuir uma licença.

![Atribuir Licenças](./media/15AssignLicenses.png)

3. Verifique se as licenças **Customer Service Enterprise** e **Project Operations** foram selecionadas e selecione **Guardar alterações**.

## <a name="create-a-new-cds-environment"></a>Criar um novo ambiente de CDS

Aprovisione um novo ambiente de implementação de CDS do Project Operations ao seguir as instruções no tópico [Modelo de implementação CDS](lite-deployment.md).

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Instalar uma configuração CDS e dados de demonstração da configuração

Instale a configuração CDS e configure os dados de demonstração da configuração ao seguir as instruções no tópico [Aplicar dados de configuração da demonstração](lite-apply-demo-setup-config-data.md).
