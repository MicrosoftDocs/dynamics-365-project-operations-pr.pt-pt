---
title: Gestão de subcontratos no Project Operations
description: Este tópico fornece uma visão geral do processo de gestão de subcontratos ponto a ponto no Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ffceb0886fdc841ea01a099243cf4eeb43e5374a18414576f3639a3e50857fd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994245"
---
# <a name="subcontract-management-in-project-operations"></a>Gestão de subcontratos no Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

A subcontratação no Microsoft Dynamics 365 Project Operations suporta o seguinte fluxo de processo empresarial.

![Fluxo de processo de subcontratação](../media/SubcontractingProcessFlow.png)

Aqui está uma descrição passo a passo do processo de subcontratação.

1. O gestor de projeto cria um subcontrato com um fornecedor. Por predefinição, as listas de preços anexadas ao registo do fornecedor são utilizadas para o subcontrato. A conta do fornecedor tem um tipo de relação de **Fornecedor** ou **Prestador**.
2. O gestor de projeto pode discriminar todas as compras como itens de linha no subcontrato. Os itens de subcontrato podem ser para tempo, despesas ou produtos. A classe de transação selecionada em cada item de subcontrato determina para que é o item.
3. O gestor de conta do fornecedor e o gestor de projeto podem iterar sobre o subcontrato. Os preços podem ser ajustados nas listas de preços das compras que estão anexadas ao subcontrato.
4. Neste momento ou mais tarde no processo, se o item do subcontrato for para tempo, o gestor de conta do fornecedor associa os contactos a cada item de subcontrato. Esta associação fornece informações ao gestor do projeto que está a trabalhar no subcontrato. Quando um contacto está associado a um item de subcontrato, o sistema cria automaticamente um recurso reservável a partir do contacto, se um recurso reservável já não existir.
5. O método de faturação em cada item de subcontrato pode ser **Preço Fixo** ou **Tempo e Material**. Para itens de subcontrato de preço fixo, pode configurar uma agenda de faturas baseada em marcos.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
