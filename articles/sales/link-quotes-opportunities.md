---
title: Criar propostas do projeto a partir de oportunidades
description: Este tópico fornece informações sobre como criar uma proposta de projeto a partir de uma oportunidade.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 606098473db479d0015e3a7a3c01a3d3b6de9db1
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082316"
---
# <a name="create-project-quotes-from-opportunities"></a>Criar propostas do projeto a partir de oportunidades

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

As propostas podem ser criadas a partir de oportunidades do projeto das seguintes formas:

- A partir do separador **Propostas** na página **Oportunidade de Projeto**
- A partir do Fluxo do processo de vendas de oportunidade
- Ao atualizar a referência da oportunidade numa proposta existente

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a>A partir do separador Propostas da página Oportunidade de Projeto

Para criar uma proposta de projeto a partir de uma oportunidade, conclua os seguintes passos.

1. Abra a página **Oportunidade de Projeto** e selecione o separador **Propostas**. 
2. Na subgrelha **Propostas** , selecione **+** para criar uma nova proposta de projeto baseada na oportunidade. Todas as linhas de oportunidade e listas de preços do Projeto relacionadas são copiadas para a nova proposta a partir da oportunidade.

## <a name="from-the-opportunity-sales-process-flow"></a>A partir do Fluxo do processo de vendas de oportunidade

Para criar uma proposta a partir do Fluxo do processo de vendas de oportunidade, conclua os seguintes passos.

1. A partir do Fluxo do processo de vendas de oportunidade, abra a Oportunidade.
2. Selecione a fase **Qualificar**. 
3. Selecione **Seguinte** e, em seguida, selecione **+ Criar** para criar uma nova proposta. A maioria das informações no separador **Resumo** para esta nova proposta terão sido assumidas por predefinição a partir da oportunidade. 
4. Introduza todas as informações necessárias em falta ou atualize os valores predefinidos, conforme necessário no separador **Resumo**.
5. Selecione **Guardar**. A nova proposta é criada e associada à oportunidade. Pode agora ver as informações da proposta no separador **Propostas** da página **Oportunidade**. 

   O Processo de vendas da oportunidade avança para a fase seguinte, **Propor**.


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a>Ao atualizar a referência da oportunidade numa proposta existente

Uma proposta existente pode ser associada a uma Oportunidade. Conclua os seguintes passos para atualizar as Informações da oportunidade numa proposta existente.

1. Abra a página **Proposta** e selecione o separador **Resumo**.
2. No campo **Oportunidade** , selecione a oportunidade que pretende associar à proposta. Pode ver a proposta na grelha **Propostas** da Oportunidade. 
3. Ao utilizar o Processo de vendas da oportunidade, a oportunidade pode avançar para a fase seguinte, **Propor**. 

   Ao fazer uma oportunidade avançar para esta fase, pode selecionar esta proposta a partir de uma lista de propostas associadas a esta oportunidade. A seleção desta proposta indica que está a avançar com ela.

   Todas as outras propostas associadas à Oportunidade continuarão disponíveis e ativas até uma delas ser ganha. Pode fazer retroceder o processo de vendas para a fase anterior **Qualificar** e escolher outra proposta com a qual avançar.
