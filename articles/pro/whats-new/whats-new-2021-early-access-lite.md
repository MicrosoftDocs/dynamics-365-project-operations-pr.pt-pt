---
title: Novidades do acesso antecipado da edição 2 de 2021 - Implementação leve do Project Operations
description: Este tópico fornece informações sobre as funcionalidades disponíveis na versão de acesso antecipado da edição 2 de 2021 da implementação leve do Project Operations.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a201e3e4333b8892eea72387222d64e18b74d71b
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323925"
---
# <a name="whats-new-2021-wave-2-early-access---project-operations-lite-deployment"></a>Novidades do acesso antecipado da edição 2 de 2021 - Implementação leve do Project Operations

_Aplica-se a: Implementação lite – negócio para faturação pró-forma_

Este tópico aplica-se aos seguintes componentes e versões do Dynamics 365 Project Operations:

  - Project Operations na versão 4.23.0.4 do ambiente Dataverse

A versão só é aplicada quando um ambiente tiver [optado pelo Acesso Antecipado](/power-platform/admin/opt-in-early-access-updates#how-to-enable-early-access-updates).

## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versão

[Gestão de subcontratos](../subcontracting/subcontracting_EA_scope.md) - Esta funcionalidade permite uma melhor visibilidade e controlo de todos os aspetos relacionados com o trabalho num projeto. A pré-visualização da gestão de subcontratos inclui as seguintes capacidades:

  - Um gestor de projeto pode criar um subcontrato com um fornecedor. Por predefinição, as listas de preços anexadas ao registo do fornecedor são utilizadas para o subcontrato. A conta do fornecedor tem um tipo de relação de **Fornecedor** ou **Prestador**.
  - Um gestor de projeto pode discriminar todas as compras como itens de linha no subcontrato. Os itens de subcontrato podem ser para tempo, despesas ou produtos. A classe de transação do item de subcontrato determina a finalidade do item.
  - O gestor de conta do fornecedor e o gestor de projeto podem iterar sobre o subcontrato. Os preços podem ser ajustados nas listas de preços das compras que estão anexadas ao subcontrato.
  - Durante o processo, se o item do subcontrato for para tempo, o gestor de conta do fornecedor pode associar os contactos do fornecedor a cada item de subcontrato. Esta associação fornece informações ao gestor do projeto que está a trabalhar no subcontrato. Quando um contacto do fornecedor é associado a um item de subcontrato, o sistema cria automaticamente um recurso reservável a partir do contacto, se ainda não existir um recurso reservável.
  - O método de faturação em cada item de subcontrato pode ser de preço fixo ou tempo e material. Para itens de subcontrato de preço fixo, é configurada uma agenda de faturação baseada em marcos.
