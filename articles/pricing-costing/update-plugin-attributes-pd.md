---
title: Atualizar atributos de plug-in com novas dimensões de preços
description: Este artigo fornece informações sobre como atualizar atributos de plug-in para dimensões de preços.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2ae502fea533d9f199ef5ee1cc85b623f08cbd84
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920028"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>Atualizar atributos de plug-in com novas dimensões de preços

Este artigo fornece informações sobre como atualizar atributos de plug-in para dimensões de preços.

> [!NOTE]
> Este artigo só é aplicável às funcionalidades de proposta e de contrato no Dynamics 365 Project Operations.

## <a name="prerequisites"></a>Pré-requisitos
Antes de concluir os passos descritos neste artigo, tem de ter concluído os procedimentos nos seguintes artigos:

  - [Criar campos e entidades personalizados](create-custom-fields-entities-pricing-dimensions.md) 
  - [Adicionar campos personalizados às entidades de configuração de preços e transacionais](add-custom-fields-price-setup-transactional-entities.md)
  - [Configurar campos personalizados como dimensões de preços](set-up-custom-fields-pricing-dimensions.md). 
  
Se não tiver concluído esses procedimentos, conclua-os e, em seguida, volte a este artigo.

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