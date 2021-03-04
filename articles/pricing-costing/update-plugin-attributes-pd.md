---
title: Atualizar atributos de plug-in com novas dimensões de preços
description: Este tópico fornece informações sobre como atualizar atributos de plug-in para dimensões de preços.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9b0cf48318d0b9e94c4be0d3775b54e83832c1b7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643232"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>Atualizar atributos de plug-in com novas dimensões de preços

Este tópico fornece informações sobre como atualizar atributos de plug-in para dimensões de preços.

> [!NOTE]
> Este tópico só é aplicável às funcionalidades de proposta e de contrato no Dynamics 365 Project Operations.

## <a name="prerequisites"></a>Pré-requisitos
Antes de completar os passos deste tópico, deve ter concluído os procedimentos nos seguintes tópicos:

  - [Criar campos e entidades personalizados](create-custom-fields-entities-pricing-dimensions.md) 
  - [Adicionar campos personalizados às entidades de configuração de preços e transacionais](add-custom-fields-price-setup-transactional-entities.md)
  - [Configurar campos personalizados como dimensões de preços](set-up-custom-fields-pricing-dimensions.md). 
  
Se não tiver concluído esses procedimentos, conclua-os e, em seguida, volte a este tópico.

## <a name="register-a-plug-in"></a>Registar um plug-in
Quando um detalhe da linha de proposta é criado na página **Linha de proposta** para uma linha de proposta do projeto, o sistema cria duas linhas de estimativa. Uma linha é para o lado do custo da estimativa e a outra linha é para o lado das vendas. É o mesmo para os itens de contrato do projeto.

Quando altera uma quantidade ou um campo no lado do custo, essa alteração é também efetuada no lado das vendas. Isto é possível porque os plug-ins PreOperation na Quotelinedetail e as entidades de detalhes do item de contrato ligam atributos específicos do lado do custo ao lado das vendas da transação. Se necessitar de alterar os valores de dimensão dos preços do lado das vendas, a fim de ser feita também do lado dos custos, os seguintes plug-ins devem ser registados novamente após a alteração de uma dimensão de preços.

Estes são os plug-ins a atualizar e a registar novamente:

- PreOperationContractLineDetailUpdate – **Atualizar msdyn_orderlinetransaction**
- PreOperationQuoteLineDetailUpdate – **Atualiza msdyn_quotelinetransaction**

Preencha os seguintes passos para atualizar e voltar a registar os plug-ins.

1. Abra **PluginRegistrationTool** e ligue-se ao ambiente do Dataverse do Project Operations.
2. Selecione **Pesquisar** e digite as primeiras letras do plug-in a atualizar.
3. Depois do plug-in ser encontrado, selecione-o e, em seguida, selecione **Selecionar no Formulário Principal**.
4. Selecione o passo **Atualizar msdyn_orderlinetransaction**, clique com o botão direito do rato e, em seguida, selecione **Atualizar**.
5. Na página de diálogo **Atualizar**, selecione as reticências (**...**) nos atributos de filtragem.
6. A janela de atributos de filtragem abre-se e fornece uma lista de todos os atributos na entidade e nas dimensões dos preços. Selecione as caixas de verificação para os atributos da dimensão dos preços.
7. Selecione **OK** para fechar a página e, em seguida, selecione **Atualizar Passo**.
8. Repita os passos 2-7 para o segundo plug-in, **PreOperationQuoteLineDetail**. Para este plug-in, precisa de atualizar o passo **Atualizar msdyn_quotelinetransaction**.
9. Feche **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]