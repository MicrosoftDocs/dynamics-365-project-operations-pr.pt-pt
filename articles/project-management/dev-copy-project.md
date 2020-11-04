---
title: Desenvolver modelos de projeto com Copiar Projeto
description: Este tópico fornece informações sobre como criar modelos de projeto usando a ação personalizada de Copiar Projeto.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cb49109e8c199bc4569702ae844a19985534294d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082344"
---
# <a name="develop-project-templates-with-copy-project"></a>Desenvolver modelos de projeto com Copiar Projeto

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

O Dynamics 365 Project Operations suporta a capacidade de copiar um projeto e reverter quaisquer atribuições para aos recursos genéricos que representam a função. Os clientes podem usar esta funcionalidade para criar modelos básicos de projeto.

Quando selecionar **Copiar Projeto** , o estado do projeto-alvo é atualizado. Utilize **Razão do Estado** para determinar quando a ação da cópia está concluída. Selecionar **Copiar Projeto** também atualiza a data de início do projeto para a data de início atual se não for detetada nenhuma data-alvo na entidade-alvo do projeto.

## <a name="copy-project-custom-action"></a>Ação personalizada Copiar Projeto 

### <a name="name"></a>Nome 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>Parâmetros de entrada
Existem três parâmetros de entrada:

| Parâmetro          | Tipo   | Valores                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | Cadeia (de carateres) | **{"removeNamedResources":true}** ou **{"clearTeamsAndAssignments":true}** |
| SourceProject      | Referência de Entidade | Projeto de Origem |
| Destino             | Referência de Entidade | Projeto de Destino |


- **{"clearTeamsAndAssignments":true}** : o comportamento predefinido do Projeto para a Web, e removerá todas as atribuições e membros da equipa.
- **{"removeNamedResources":true}** : o comportamento predefinido do Project Operations, e reverterá as atribuições a recursos genéricos.

Para mais predefinições sobre ações, consulte [Utilizar ações API Web](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Especificar campos a copiar 
Quando a ação for convocada, **Copiar Projeto** irá analisar **Copiar Colunas do Projeto** da vista do projeto para determinar quais os campos a copiar quando o projeto é copiado.