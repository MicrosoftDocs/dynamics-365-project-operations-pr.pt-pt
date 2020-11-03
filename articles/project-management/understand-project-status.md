---
title: Compreender o estado do projeto
description: Este tópico fornece informações sobre o estado atribuído aos projetos no Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 336e479ad39653af14cca7930fe63e906b7de489
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082276"
---
# <a name="understand-project-status"></a>Compreender o estado do projeto

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_


A secção **Estado** na página **Entidade do Projeto** fornece um resumo o estado de funcionamento de um projeto baseado no custo e no esforço.


## <a name="status-summary-fields"></a>Campos Resumo do estado

- O campo  **Estado Geral do Projeto** é um campo editável que mostra o estado geral do projeto. Este campo utiliza a codificação de cores, tal como verde, amarela e vermelha, para indicar um risco de aumento. 
- O campo  **Comentários** permite que o gestor de projeto introduza comentários específicos sobre o estado. 
- O campo **Estado atualizado em** não é editável. O valor neste campo é um carimbo de data/hora que indica quando o estado foi atualizado pela última vez.
- Os campos  **Desempenho de Agendamento** e **Desempenho de Custos** são definidos a partir da grelha de monitorização. Quando os desvios da agenda e de custo do nó raiz na vista **Monitorização do esforço** são positivos, é possível definir estes campos como **Adiantado**. Quando a variação da agenda e do custo para o nó raiz é negativa, estes campos são definidos como **Atrasado**.
