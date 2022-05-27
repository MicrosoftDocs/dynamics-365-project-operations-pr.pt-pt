---
title: Compreender o estado do projeto
description: Esta tópico fornece informações sobre o estado atribuído a projetos no Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 9efa6135bbaa98f8968e09fcf38c9dd4fde84fe4
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578906"
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