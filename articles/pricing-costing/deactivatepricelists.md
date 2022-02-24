---
title: Desativar listas de preços
description: Este tópico explica como desativar ou remover listas de preços não reutilizadas ou antigas.
author: rumant
manager: AnnBe
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3fa902e93815002be7d6915880cd7759dbbde5ef
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701962"
---
# <a name="deactivate-price-lists"></a>Desativar listas de preços 

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Para remover listas de preços antigos ou não reutilizados de Dynamics 365 Project Operations, há dois passos que deve realizar. 

1. Remova ou elimine a lista de preços de páginas específicas.
2. Desativar ou eliminar a lista de preços das listas de preços Ativos na página **Listas de preços**.

>[!IMPORTANT]
> Tem de completar ambos os passos para remover totalmente uma lista de preços. Apenas a realização do passo 2, que consiste em eliminar ou desativar diretamente a lista de preços da vista das Listas de Preços Ativos, não é suficiente. Deve também eliminar a associação desta lista de preços de todos os locais mencionados no passo 1.

## <a name="delete-the-price-list-from-specific-pages"></a>Elimine a lista de preços de páginas específicas
1. Para eliminar uma lista de preços do Project Operations, aceda às seguintes páginas:  

      - Página **Parâmetros de projeto** > separador **Listas de preços**
      - Página da **Unidade Organizacional** > grelha de **Listas de preços**
      - Página **Conta** > grelha **Listas de preço de projetos**
      - Página de **Propostas de projeto** > grelha de **Listas de preços do projeto**: isto aplica-se a todas as propostas de projetos ativas.
      - Página de **Contratos de projeto** > grelha de **Listas de preços do projeto**: isto aplica-se a todos os contratos de projetos ativos.

 2. Para cada página, tem de selecionar a lista de preços que pretende eliminar e, em seguida, selecionar **Eliminar**. 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a>Eliminar ou desativar a lista de preços da página Listas de preços
 
1. Para eliminar uma lista de preços das listas de preços ativas, vá a **Vendas** > **Clientes** > **Listas de preços**. 
2. Selecione a lista de preços que pretende eliminar e, em seguida, selecione **Eliminar**. Se a lista de preços for referenciada em quaisquer transações existentes, não poderá eliminá-la. Se isso acontecer, pode desativar a lista de preços para que não apareça em nenhuma opinião. 
3. Para desativar a lista de preços, selecione novamente a lista de preços e, em seguida, selecione **Desativar**.   
