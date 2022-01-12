---
title: Inscrição para as avaliações do Project Operations
description: Este tópico fornece informações sobre como implementar uma avaliação do Dynamics 365 Project Operations.
author: ruhercul
ms.date: 12/08/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e40b4ac23241730f5c2db89f0dc674083f9e7abe
ms.sourcegitcommit: 8f970b46d0303dafaa75fc7d00567d232e1e600b
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 12/09/2021
ms.locfileid: "7901631"
---
# <a name="sign-up-for-project-operations-trials"></a>Inscrição para as avaliações do Project Operations 

_**Aplica-se a:** Project Operations para cenários baseados em Recursos/Não Stock, implementação Lite – negócio para faturação pró-forma, Project Operations para cenários baseados em Stock/Produção_ 

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Este tópico explica como subscrever a oferta de parceiro de pré-visualização e implementar um ambiente do Dynamics 365 Project Operations.

Com a nova avaliação do Project Operations, pode implementar automaticamente qualquer um dos três cenários de implementação suportados, bastando para isso responder a um questionário que recomenda a melhor abordagem de implementação. Este tópico fornece informações sobre como:

- Resgatar a oferta de avaliação.
- Iniciar o aprovisionamento.
- Configurar a escrita dupla.
- Saiba mais sobre o Project Operations. 

A tabela seguinte descreve os detalhes da nova oferta de avaliação.

| **Item de oferta**               | **Detalhes**                                  |
|------------------------------|----------------------------------------------|
| Tipo de oferta                   | Este tipo de oferta é uma oportunidade potencial de administrador, pelo que é necessário um administrador de inquilinos para efetuar o resgate. |
| Utilização da oferta                    | Uma vez por inquilino                          |
| Duração da oferta               | 30 dias                             |
| Resgates por inquilino       | 5                                            |
| Número de utilizadores              | 25                                           |
| Extensão                    | 1 extensão, 30 dias               |
| Número de ambientes de avaliação | 3                                            |


## <a name="admin-trial-details"></a>Detalhes da avaliação de administrador
A tabela seguinte lista os detalhes da avaliação e como se aplicam a cada tipo de implementação.

| **Item**                      | **Leve**                                     | **Materiais não existentes em stock** | **Materiais em stock** |
|-------------------------------|----------------------------------------------|---------------------------|-----------------------|
| Dados de configuração fornecidos           | Sim                                          | Sim                       | Sim (USSI)            |
| Dados transacionais            | No                                           | No                        | No                    |
| Tempo de aprovisionamento em minutos  | 15                                           | 90                        | 30                    |
 
## <a name="prerequisites"></a>Pré-requisitos
São necessários os seguintes pré-requisitos para implementar uma avaliação do Dynamics 365 Project Operations.

- Inscrever-se no [Dynamics 365 Project Operations - Avaliação de Pré-visualização](https://www.aka.ms/try-po).
- O utilizador que implementar a pré-visualização tem de ter direitos de administrator global do inquilino do Azure.

> [!IMPORTANT]
> Apenas uma pessoa numa organização, o administrador de inquilinos, necessita de realizar esta tarefa. Se não for subscritor desta versão, aguarde até a sua organização estar inscrita e receber as suas credenciais de utilizador.

### <a name="dynamics-365-project-operations---preview-trial"></a>Dynamics 365 Project Operations - Avaliação de pré-visualização 

Antes de começar, inicie sessão num browser com a conta profissional de utilizador no inquilino onde pretende instalar a pré-visualização do Project Operations.

1. Resgate o primeiro código de oferta, **Dynamics 365 Project Operations - Avaliação de Pré-visualização**, colando-o no URL do browser.

    ![Resgatar Oferta](./media/16RedeemFirstOfferNew.png)

2. Confirme a encomenda.

    ![Confirme a encomenda](./media/17ConfirmOrderNew.png)

  Verá que a oferta de confirmação foi resgatada com êxito.

   ![Confirmação](./media/18OrderConfirmationNew.png)

  Será redirecionado para o [centro de administração do Power Platform](https://admin.powerplatform.microsoft.com/projectoperationstrial).

## <a name="questionnaire-and-provisioning"></a>Questionário e aprovisionamento

1.  Aceda ao [centro de administração do Power Platform](https://admin.powerplatform.com/projectoperationstrial) e preencha o questionário.  
2.  Reveja o tipo de implementação recomendado e selecione **Iniciar Configuração** para iniciar o aprovisionamento.
3.  Reveja os termos e condições e, em seguida, selecione **Iniciar**.

   Após o início do aprovisionamento, é redirecionado para a lista de ambientes no centro de administração do Power Platform. Enquanto o aprovisionamento está em curso, o estado do ambiente é **PreparingInstance**.
 
  Quando o aprovisionamento ficar concluído, o estado do seu ambiente é **Pronto**. O aprovisionamento do ambiente inclui a implementação de dados de demonstração.
 
4.  Selecione o URL do Microsoft Dataverse e os URLs das aplicações Finance and Operations para validar a implementação.

## <a name="configuring-dual-write"></a>Configurar a escrita dupla
- Para configurar direitos de acesso para escrita dupla, consulte [Atualizar definições de segurança no Project Operations no Dataverse](resource-provision-new-environment.md).
- Para configurar mapas de escrita dupla, consulte [Executar mapas de escrita dupla do Project Operations](resource-provision-new-environment.md#run-project-operations-dual-write-maps).

## <a name="assign-licenses"></a>Atribuir licenças

Necessitará de acesso administrativo ao Portal Microsoft 365 da sua organização do para concluir os seguintes passos.

1. Aceda ao [centro de administração do Microsoft 365](https://portal.office.com/) para atribuir licenças aos utilizadores.

   ![Home page do centro de administração](./media/14AdminPortal.png)

2. Na página **Utilizadores ativos**, selecione os utilizadores aos quais pretende atribuir uma licença.

   ![Atribuir Licenças](./media/15AssignLicenses.png)

3. Verifique se a licença de **Pré-visualização do Dynamics 365 Project Operations** foi selecionada e, em seguida, selecione **Guardar alterações**.

## <a name="additional-resources"></a>Recursos adicionais

Os recursos seguintes fornecem orientações úteis para o ajudar a utilizar o Project Operations:

- [Série de vídeos -Descrição Geral do Project Operations, funcionalidades detalhadas e mapa de objetivos](https://youtube.com/playlist?list=PLcakwueIHoT_LJ3Fr1tHnkPk5lioqE6uH)
- [Dynamics 365 Project Operations](/learn/modules/examine-dynamics-365-project-operations/)
- [Determinar o tipo de implementação](determine-deployment-type.md)

## <a name="frequently-asked-questions"></a>Perguntas mais frequentes

### <a name="what-if-i-require-alm-or-elm-for-my-finance-and-operations-apps-environment"></a>E se eu necessitar do ALM ou ELM para o meu ambiente de aplicações do Finance and Operations?

- No caso de parceiros que necessitem de capacidades de gestão de ciclos de vida de ambiente completo, consulte o [Pedido de Licença de Sandbox de Parceiro](https://experience.dynamics.com/requestlicense) para rever a nova oferta de parceiro. 
- No caso de parceiros que pretendam obter mais informações sobre os Direitos de Utilização Interna, consulte [Benefícios do software e da cloud de Direitos de Utilização Interna (microsoft.com](https://partner.microsoft.com/membership/internal-use-software).

### <a name="can-i-extend-my-trial-beyond-30-days"></a>Posso prolongar a minha avaliação para além dos 30 dias?
Para prolongar a sua avaliação, conclua os seguintes passos.

1. No **centro de administração do Microsoft 365**, aceda a **Faturação** > **Os seus produtos**.
2. Selecione **Dynamics 365 Project Operations (CE) - Avaliação de Pré-visualização**.
3. Em **Data de Expiração**, selecione **Prolongar Data**.

### <a name="can-i-upgrade-from-the-lite-deployment-to-the-resourcenon-stocked-based-scenario-deployment"></a>Posso atualizar de uma implementação leve para a implementação de cenário baseada em recursos/não armazenados?
Atualmente, não há qualquer suporte para atualizar um ambiente de uma implementação leve para uma implementação baseada em materiais não armazenados.

### <a name="can-i-access-lifecycle-services-lcs-for-my-finance-environments"></a>Posso aceder ao Lifecycle Services (LCS) para os meus ambientes do Finance?  
N.º Para estas avaliações, a implementação é efetuada através do Centro de Administração do Power Platform. O acesso ao ambiente do Finance é restrito.

### <a name="can-i-install-my-trial-on-an-existing-environment"></a>Posso instalar a minha avaliação num ambiente existente?
Se tiver um ambiente existente, poderá instalar a implementação leve num ambiente de vendas existente do Dataverse a partir do Centro de administração do Power Platform.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
