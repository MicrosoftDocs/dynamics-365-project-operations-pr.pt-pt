---
title: Compreender o estado do projeto
description: Esta tópico fornece informações sobre o estado atribuído a projetos no Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 47d71b945a2d5e7aa41d2ac3731ac4a5d3051ce279229794e31c9673f688130e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997035"
---
# <a name="understand-project-status"></a>Compreender o estado do projeto

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_


A secção **Estado** na página **Entidade do Projeto** fornece um resumo o estado de funcionamento de um projeto baseado no custo e no esforço.


## <a name="status-summary-fields"></a>Campos Resumo do estado

- O campo **Estado Geral do Projeto** é um campo editável que mostra o estado geral do projeto. Este campo utiliza a codificação de cores, tal como verde, amarela e vermelha, para indicar um risco de aumento. 
- O campo **Comentários** permite que o gestor de projeto introduza comentários específicos sobre o estado. 
- O campo **Estado atualizado em** não é editável. O valor neste campo é um carimbo de data/hora que indica quando o estado foi atualizado pela última vez.
- Os campos **Desempenho de Agendamento** e **Desempenho de Custos** são definidos a partir da grelha de monitorização. Quando os desvios da agenda e de custo do nó raiz na vista **Controlo do esforço** são positivos, estes campos são atualizados para **Adiantado**. Quando a variação da agenda e do custo para o nó raiz é negativa, estes campos são definidos como **Atrasado**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]