---
title: Projetos de estimativa de receitas de preço fixo
description: Este tópico fornece informações sobre a receita de preço fixo em projetos.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 290608e5663f9c953212c156771bbf1ad6b1e901
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578722"
---
# <a name="fixed-price-revenue-estimate-projects"></a>Projetos de estimativa de receitas de preço fixo 

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Quando cria um item de contrato de projeto com os seguintes atributos no Dynamics 365 Project Operations no Microsoft Dataverse, o sistema cria automaticamente um projeto de estimativa de receitas de preço fixo. As informações neste projeto baseiam-se no seguinte:

  - Um método de faturação de preço fixo.
  - Um projeto associado.
  - Pelo menos, um marco definido no separador **Agenda de faturas** na página **Item de contrato do projeto**.

## <a name="review-fixed-price-revenue-estimates-projects"></a>Reveja projetos de estimativas de receitas de preço fixo
Para rever os projetos de estimativas de receitas de preços fixos, complete os seguintes passos:

1. No ambiente Dynamics 365 Finance, aceda a **Gestão de projetos e contabilidade** > **Projetos** > **Projetos de estimativa de receitas de preço fixo**.
2. Selecione o projeto que pretende visualizar e clique duas vezes em **ID do projeto de estimativa** para abrir o registo e rever os detalhes do projeto.
3. Expanda o separador **Projeto**. Verá um projeto na grelha **Projetos selecionados**. O sistema usa isto como o projeto predefinido porque é o projeto associado ao item de contrato do projeto. 
4. Para alterar a associação, selecione projetos adicionais e adicione-os à grelha **Projetos selecionados**. Se vários projetos forem selecionados nesta grelha, a percentagem de conclusão do projeto e as estimativas de receitas são calculadas em conjunto para todos os projetos selecionados.

  O custo do projeto, o perfil da receita, o modelo de custos e o código de período podem ser definidos manualmente. Se não forem definidos manualmente, os valores assumem a predefinição durante o primeiro cálculo de estimativa para o projeto utilizando as regras configuradas para o custo do projeto e perfis de receitas.



[!INCLUDE[footer-include](../includes/footer-banner.md)]