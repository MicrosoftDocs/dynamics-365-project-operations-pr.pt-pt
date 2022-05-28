---
title: Gerir contratos de projeto
description: Este tópico fornece informações sobre a visualização de contratos baseados em projetos.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 64e81593065d97272af6261e17175c76bd8dca7a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590514"
---
# <a name="manage-project-contracts"></a>Gerir contratos de projeto

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Os contratos de projeto no Dynamics 365 Project Operations capturam e gerem a alocações contratualmente acordadas e detalhes de faturação de um projeto. A estrutura de um contrato do projeto no Project Operations está ajustado a trabalho baseado em projetos com os seguintes componentes:

- Os itens de contrato que identificam os componentes discretos do trabalho que serão apresentados como componentes de alto nível numa fatura de projeto.
- Os detalhes do item de contrato que identificam e estimam o trabalho para cada componente de alto nível ou item de contrato. A estimativa inclui a agenda e os aspetos financeiros do trabalho estão ligados ao item de contrato.
- São criados modelos de contratação e componentes faturáveis para cada item de contrato que detenha o acordo de faturação de cada item de contrato e o contrato global.

## <a name="view-all-project-based-contracts"></a>Ver todos os contratos baseados em projetos

Uma lista de todos os contratos do projeto pode ser vista na página de lista **Contratos**. 

1. Aceda a **Vendas** > **Contratos**. Uma lista de todas os seus Contratos do projeto no sistema são mostrados. 
2. Selecione o **Alternador de vistas** (a seta pendente ao lado do nome da vista) para selecionar outras vistas filtradas. Pode criar as suas próprias vistas com critérios de filtro personalizados.

Os contratos podem ser criados ou eliminados a partir desta página de lista ou páginas de detalhes.

> [!NOTE]
> Os contratos que têm projetos, tarefas, estimativas, diários e/ou valores reais associados não podem ser eliminados. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
