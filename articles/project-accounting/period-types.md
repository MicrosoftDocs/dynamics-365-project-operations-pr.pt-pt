---
title: Tipos de período
description: Este artigo fornece informações sobre como configurar tipos de períodos para a estimativas de receitas.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5bbf2dcb4758611aa9d0591ddfec42869f4438c0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930976"
---
# <a name="period-types"></a>Tipos de período

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Um tipo de período define a frequência com que as receitas de um projeto são estimadas. Este artigo fornece informações sobre como configurar tipos de períodos para a estimativas de receitas. 

## <a name="create-and-work-with-period-types"></a>Criar e trabalhar com tipos de períodos
Para criar e trabalhar com tipos de períodos, complete os seguintes passos:

1. No ambiente do Dynamics 365 Finance, aceda a **Gestão de projeto e contabilidade** > **Configuração** > **Estimativas** > **Tipos de período**.
2. Selecione **Novo** para criar um novo tipo de período. Introduza um nome e descrição.
3. No campo **Frequência**, selecione um valor:

    - Se selecionar **Semana**, **Quinzenal**, **Semi-mensal**, **Mês**, **Dia**, **Trimestre** ou **Ano**, o calendário será utilizado para gerar os períodos. 
    - Se selecionar o **Período do livro razão**, serão utilizados períodos de contabilidade a partir da configuração do livro razão geral para gerar períodos.
    - Se selecionar **Ilimitado**, pode especificar os períodos personalizados.
4. Selecione o registo do tipo de período e, em seguida, selecione **Gerar períodos** para criar períodos para o tipo de período. Com base na frequência de período que selecionou, poderá ter a opção de especificar uma data de início ou o número de períodos a gerar.
5. Selecione **Períodos** para rever os períodos gerados.



[!INCLUDE[footer-include](../includes/footer-banner.md)]