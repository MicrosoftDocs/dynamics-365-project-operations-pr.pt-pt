---
title: Inscrever-se para obter uma subscrição de pré-visualização
description: Este tópico fornece informações sobre como subscrever e implementar o Project Operations lite - oportunidade potencial para fatura pró-forma.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5342466f308ab62a9f73a85fbd838d7c33bb1f47
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082267"
---
# <a name="sign-up-for-a-preview-subscription-for-lite-deployment--deal-to-proforma-invoicing"></a>Inscreva-se numa subscrição de pré-visualização para implementação leve – oportunidade potencial para fatura pró-forma

Este tópico explica como subscrever a oferta de parceiros de pré-visualização e implementar a Implementação leve do Dynamics 365 Project Operations - oportunidade potencial para fatura pró-forma.

> [!NOTE]
> Este processo será alterado nas próximas versões do Project Operations.

## <a name="prerequisites"></a>Pré-requisitos

- Receberá um e-mail a convidá-lo para participar na pré-visualização. Pode solicitar uma pré-visualização no [Web site do Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- O utilizador que implementar a pré-visualização tem de ter direitos de administrator global do inquilino do Azure.
- Reveja todos os termos e condições.

## <a name="subscribe"></a>Subscrever

Quando receber uma aprovação de [pedido de pré-visualização](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), receberá duas ofertas da Microsoft por e-mail. Estas ofertas permitem implementar a Pré-visualização do Project Operations:

- Dynamics 365 Project Operations (CRM) – Avaliação da Pré-visualização
- Office 365 Project Operations – Avaliação da Pré-visualização

> [!IMPORTANT]
> Só uma pessoa, o administrador inquilino, numa organização precisa de executar esta tarefa. Se não for subscritor desta versão, aguarde até a sua organização estar inscrita e receber as suas credenciais de utilizador.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM) – Avaliação da Pré-visualização 

Antes de começar, certifique-se de que está a iniciar sessão num browser com a conta de profissional de utilizador no inquilino onde pretende a pré-visualização do Project Operations.

1. Resgate o primeiro código de oferta, **Dynamics 365 Project Operations (CRM) - Pré-visualização da Avaliação** , colando-o no URL do browser.

![Resgatar Oferta](./media/16RedeemFirstOfferNew.png)

2. Confirme a encomenda.
![Confirme a encomenda](./media/17ConfirmOrderNew.png)

Verá que a oferta de confirmação foi resgatada com sucesso.

![Confirmação](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Project Operations – Avaliação da Pré-visualização

Repita os mesmos passos que com o primeiro código de oferta. Certifique-se de que adiciona o segundo código de oferta usando a mesma conta de utilizador que foi usada com o código da primeira oferta.

## <a name="assign-licenses"></a>Atribuir licenças

> [!IMPORTANT]
> Necessitará de acesso administrativo ao Portal Microsoft 365 da sua organização do para concluir os seguintes passos.


1. Vá para o [Centro de administração do Microsoft 365](https://portal.office.com/) para atribuir as licenças aos seus utilizadores.

![Home page do centro de administração](./media/14AdminPortal.png)

2. Na página **Utilizadores ativos** , selecione os utilizadores aos quais pretende atribuir uma licença.

![Atribuir Licenças](./media/15AssignLicenses.png)

3. Verifique se as licenças **Pré-visualização do Dynamics 365 Project Operations (CRM)** e **Office 365 Project Operations – Pré-visualização** estão selecionadas. 
4. Selecione **Guardar alterações**.

## <a name="create-a-new-cds-environment"></a>Criar um novo ambiente de CDS

1. Aprovisione um novo ambiente de implementação de CDS do Project Operations ao seguir as instruções no tópico [Modelo de implementação CDS](lite-deployment.md). Ao selecionar o tipo de ambiente, certifique-se de que utiliza **Avaliação (baseado em Subscrição)**.
![Novo ambiente](./media/19CreateEnvironment.png)

2. Selecione a definição **Ativar aplicações do Dynamics 365** e deixe **Implementar automaticamente estas aplicações** em branco.  
3. Selecione **Guardar** para criar o ambiente.

![Adicionar base de dados](./media/20CreateEnvironment1.png)

4. Após a criação do ambiente, instale a solução **Microsoft Dynamics 365 Project Operations**. 

![Instalar Solução](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Instalar uma configuração CDS e dados de demonstração da configuração

Instale a configuração CDS e configure os dados de demonstração da configuração ao seguir as instruções no tópico [Aplicar dados de configuração da demonstração](lite-apply-demo-setup-config-data.md).