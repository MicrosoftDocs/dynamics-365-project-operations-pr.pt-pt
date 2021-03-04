---
title: Tipos de fases do projeto
description: Este tópico fornece informações sobre as fases do projeto.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 61db23e19614f5c3be5c8b46fbf72463705e409c
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148117"
---
# <a name="project-stage-types"></a>Tipos de fases do projeto 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

As fases de um projeto são concebidas para refletir o estado do projeto à medida que o mesmo progride. As personalizações podem ser usadas para atualizar automaticamente as fases com fluxos do processo de negócio, Power Automate ou extensões de plug-in.

As fases seguintes são definidas no BPF predefinido:

- Nova
- Proposta
- Planear
- Entregar
- Concluído
- Fechar 

## <a name="new"></a>Novo

Quando cria um projeto, a fase do projeto é definida como **Novo**. Se o projeto tiver sido criado a partir de um modelo, este poderá ter dados de agendas, estimativas e da equipa. Caso contrário, é apenas um contorno do projeto e os componentes restantes têm de ser introduzidos.

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