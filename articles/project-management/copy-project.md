---
title: Copiar um projeto
description: Este tópico fornece informações sobre copiar projetos no Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 02/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: af1942e81691d9e13fdcbbf68599c1a8a4004582
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/04/2021
ms.locfileid: "5479533"
---
# <a name="copy-a-project"></a>Copiar um projeto

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Com Dynamics 365 Project Operations, pode rapidamente construir novos projetos selecionando **Copiar projeto** no formulário **Projetos**. Para copiar um projeto, abra o projeto que pretende copiar e, em seguida, selecione **Copiar projeto**. A ação copiará:

- Propriedades do projeto (A data de início estimada é copiada do projeto fonte)
- A Estrutura Hierárquica do Trabalho
- Membros da equipa do projeto
- Estimativas do projeto
- Estimativas de despesa do projeto

## <a name="project-properties"></a>Propriedades do projeto

Quando o projeto é copiado, são copiados os valores nos seguintes campos:

- Nome
- Descrição
- Cliente
- Modelo de Calendário
- Moeda
- Unidade de Contratação
- Gestor de Projeto
- Estado
- Estado Geral do Projeto
- Comentários
- Estimativas
- Data de Início Estimada
- Data de Conclusão
- Esforço (Horas)
- Custo Estimado da Mão-de-Obra
- Custo Estimado da Despesa

## <a name="work-breakdown-structure"></a>Estrutura Hierárquica do Trabalho

Quando o projeto é copiado, é copiada toda a estrutura hierárquica do trabalho carregada pelos recursos. Os recursos nomeados são substituídos por recursos genéricos. Se os recursos nomeados não tiverem as mesmas horas de trabalho que o recurso genérico, a agenda será recalculada e as durações das tarefas poderão mudar.

## <a name="project-team-members"></a>Membros da equipa do projeto

Quando uma equipa do projeto é copiada a partir do projeto de origem, são copiados os recursos genéricos. As atribuições de recursos genéricos também são mantidas como no projeto de origem. Os recursos nomeados serão convertidos para membros genéricos da equipa.

## <a name="estimates"></a>Estimativas

Quando o projeto é copiado, são copiadas as linhas de estimativa de recursos e despesas a partir do projeto de origem. 

Para obter informações sobre como aceder programaticamente a Copiar Projeto, consulte [Programar modelos de projeto com Copiar Projeto](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
