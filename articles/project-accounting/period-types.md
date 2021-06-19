---
title: Tipos de período
description: Este tópico fornece informações sobre como configurar tipos de período para estimativas de receitas.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 07cc9cde5fab10accb1fd6efede58926918f614c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013500"
---
# <a name="period-types"></a>Tipos de período

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Um tipo de período define a frequência com que as receitas de um projeto são estimadas. Este tópico fornece informações sobre como configurar tipos de período para estimativas de receitas. 

## <a name="create-and-work-with-period-types"></a>Criar e trabalhar com tipos de períodos
Para criar e trabalhar com tipos de períodos, complete os seguintes passos:

1. No seu ambiente do Dynamics 365 Finance, aceda a **Gestão de projetos e contabilística** > **Configurar** > **Estimativas** > **Tipos de períodos**.
2. Selecione **Novo** para criar um novo tipo de período. Introduza um nome e descrição.
3. No campo **Frequência**, selecione um valor:

    - Se selecionar **Semana**, **Quinzenal**, **Semi-mensal**, **Mês**, **Dia**, **Trimestre** ou **Ano**, o calendário será utilizado para gerar os períodos. 
    - Se selecionar o **Período do livro razão**, serão utilizados períodos de contabilidade a partir da configuração do livro razão geral para gerar períodos.
    - Se selecionar **Ilimitado**, pode especificar os períodos personalizados.
4. Selecione o registo do tipo de período e, em seguida, selecione **Gerar períodos** para criar períodos para o tipo de período. Com base na frequência de período que selecionou, poderá ter a opção de especificar uma data de início ou o número de períodos a gerar.
5. Selecione **Períodos** para rever os períodos gerados.



[!INCLUDE[footer-include](../includes/footer-banner.md)]