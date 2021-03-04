---
title: Projetos de estimativa de receitas de preço fixo
description: Este tópico fornece informações sobre a receita de preço fixo em projetos.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 80fe1d4171d80ca39e8b7ebb1eefaa524a4f2b07
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531522"
---
# <a name="fixed-price-revenue-estimate-projects"></a>Projetos de estimativa de receitas de preço fixo 

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Quando cria um item de contrato de projeto com os seguintes atributos no Dynamics 365 Project Operations no Microsoft Dataverse, o sistema cria automaticamente um projeto de estimativa de receitas de preço fixo. As informações neste projeto baseiam-se no seguinte:

  - Um método de faturação de preço fixo.
  - Um projeto associado.
  - Pelo menos, um marco definido no separador **Agenda de faturas** na página **Item de contrato do projeto**.

## <a name="review-fixed-price-revenue-estimates-projects"></a>Reveja projetos de estimativas de receitas de preço fixo
Para rever os projetos de estimativas de receitas de preços fixos, complete os seguintes passos:

1. No ambiente do Dynamics 365 Finance, vá a **Gestão de projetos e contabilística** > **Projetos** > **Projetos de estimativa de receitas de preço fixo**.
2. Selecione o projeto que pretende visualizar e clique duas vezes em **ID do projeto de estimativa** para abrir o registo e rever os detalhes do projeto.
3. Expanda o separador **Projeto**. Verá um projeto na grelha **Projetos selecionados**. O sistema usa isto como o projeto predefinido porque é o projeto associado ao item de contrato do projeto. 
4. Para alterar a associação, selecione projetos adicionais e adicione-os à grelha **Projetos selecionados**. Se vários projetos forem selecionados nesta grelha, a percentagem de conclusão do projeto e as estimativas de receitas são calculadas em conjunto para todos os projetos selecionados.

  O custo do projeto, o perfil da receita, o modelo de custos e o código de período podem ser definidos manualmente. Se não forem definidos manualmente, os valores assumem a predefinição durante o primeiro cálculo de estimativa para o projeto utilizando as regras configuradas para o custo do projeto e perfis de receitas.



[!INCLUDE[footer-include](../includes/footer-banner.md)]