---
title: Fases do projeto
description: Este tópico fornece informações sobre as fases do projeto que estão disponíveis em Operações de Projeto Microsoft Dynamics.
author: ruhercul
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 079c3d2d16cf802d2b9ecc779577e6e390d92ddc
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996940"
---
# <a name="project-stages"></a>Fases do projeto

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

As fases de um projeto são concebidas para refletir o estado do projeto à medida que o mesmo progride. As personalizações podem ser usadas para atualizar automaticamente as fases com fluxos do processo de negócio, Power Automate ou extensões de plug-in.

As fases seguintes são definidas no fluxo do processo de negócio predefinido:

- Nova
- Proposta
- Plano
- Entregar
- Concluir
- Fechar 

## <a name="new"></a>Nova

Quando cria um projeto, a fase do projeto é definida como **Novo**. Se o projeto tiver sido criado a partir de um modelo, este poderá ter dados de agendas, estimativas e da equipa. Caso contrário, é um contorno do projeto e os componentes restantes têm de ser introduzidos.

## <a name="quote"></a>Proposta

Quando associa um projeto a uma proposta ou quando cria um projeto a partir de uma proposta, a fase de projeto é definida como **Proposta** e as datas de início e de fim estimadas também são atualizadas. Quando o projeto está na fase **Proposta**, o separador **Vendas** na página **Entidade do Projeto** mostra os detalhes da proposta.

## <a name="plan"></a>Planear

Quando ganha uma proposta associada a um projeto e quando o projeto é movido para a fase **Contrato**, a fase do projeto é atualizada para **Plano**. Quando o projeto está na fase **Plano**, a página **Entidade do Projeto** mostra os detalhes do contrato.

## <a name="deliver"></a>Entregar

Quando o plano do projeto estiver concluído, e estiver pronto para iniciar o projeto, o gestor de projeto deverá atualizar a fase do projeto **Entregar** para mostrar que o projeto foi iniciado.

## <a name="complete"></a>Concluído 

Quando o trabalho do projeto estiver concluído, o gestor de projeto poderá atualizar a fase para **Concluído**. Ao atualizar a fase do projeto para **Concluído**, o gestor de projeto indica que o trabalho está 100% concluído, mas que o projeto está a ser mantido aberto para que qualquer entrada de tempo ou despesa pendente possa ser registada.

## <a name="close"></a>Fechar

Quando todas as transações são registadas para o projeto, o gestor de projeto pode atualizar a fase para **Fechar**. Nesta altura, não é possível registar nenhuma transação e o projeto está definido como só de leitura.



[!INCLUDE[footer-include](../includes/footer-banner.md)]