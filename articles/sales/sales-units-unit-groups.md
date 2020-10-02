---
title: Unidades e grupos de unidades
description: Este tópico fornece informações sobre como criar unidades e grupos unitários no Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: ea5399368214a293ca7c10fabf21d82407b5c76f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898770"
---
# <a name="units-and-unit-groups"></a>Unidades e grupos de unidades

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

As unidades são as quantidades ou medidas em que vende os produtos ou serviços. Por exemplo, se vender artigos de jardinagem, poderá vender sementes em unidades de pacotes, caixas e paletes. Um grupo de unidades é uma coleção destas unidades diferentes.

Para completar os passos deste tópico, certifique-se de que lhe foi atribuída a função de Administrador do Sistema ou de Gestor Sales Professional ou que tem permissões equivalentes.

## <a name="create-a-unit-group"></a>Criar um grupo de unidades

1. No mapa do site, selecione **Unidades**.
2. Selecione **Novo**, e na caixa de diálogo **Criar grupo de unidades**, introduza o nome da unidade.
3. No campo **Unidade primária**, introduza a unidade de medida comum mais baixa na qual o produto será vendido. Por exemplo, pode introduzir "peça" ou "onça".
4. Selecione **OK**.

## <a name="add-units-to-a-unit-group"></a>Adicionar unidades a um grupo de unidades

1. Abra um grupo de unidades e, no separador **Relacionado**, selecione **Unidades**. Verá que a unidade primária já foi adicionada.
2. Selecione **Adicionar Nova Unidade**, e na página **Criar rápido: Unidade**, no campo **Nome**, introduza o nome da unidade.
3. No campo **Quantidade**, introduza a quantidade que a unidade irá conter. Por exemplo, se uma caixa contém dois artigos, introduza "2". 
4. No campo **unidade base**, selecione uma unidade base para estabelecer a unidade de medição mais baixa para a unidade. Por exemplo, pode selecionar "Peça".
5. Selecione **Guardar**:
