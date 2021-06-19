---
title: Copiar um projeto
description: Este tópico fornece informações sobre copiar projetos no Dynamics 365 Project Operations.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c3055ab5b8c07faa2bc9167956d283e2a66029dd
ms.sourcegitcommit: 173f2b1f4e063c440a5f78d76d456c62aadbd89e
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/24/2021
ms.locfileid: "6091268"
---
# <a name="copy-a-project"></a>Copiar um projeto

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Com Dynamics 365 Project Operations, pode rapidamente construir novos projetos selecionando **Copiar projeto** no formulário **Projetos**. Para copiar um projeto, abra o projeto que pretende copiar e, em seguida, selecione **Copiar projeto**. A ação copiará o seguinte:

- Propriedades do projeto 
- Estrutura Hierárquica do Trabalho
- Membros da equipa do projeto
- Estimativas do projeto
- Estimativas de despesa do projeto
- Estimativas de material do projeto

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
- Data de Início Estimada: Esta é a data em que o projeto é criado a partir da cópia.
- Data de Conclusão Estimada: Esta data é ajustada com base na data de início do novo projeto que foi feito a partir da cópia.
- Esforço (Horas)
- Custo Estimado da Mão-de-Obra
- Custo Estimado da Despesa
- Custo Estimado do Material

> [!NOTE]
> Copiar projeto é uma operação de execução prolongada. Os registos do projeto, os seus atributos relevantes e muitas entidades relacionadas também são copiados. Devido à natureza de execução prolongada da operação, após o início da cópia, a página de destino do projecto está bloqueada para edição até que a operação da cópia esteja concluída.

## <a name="work-breakdown-structure"></a>Estrutura Hierárquica do Trabalho

Quando o projeto é copiado, é copiada toda a estrutura hierárquica do trabalho carregada pelos recursos. Os recursos nomeados são substituídos por recursos genéricos. Se os recursos nomeados não tiverem as mesmas horas de trabalho que o recurso genérico, a agenda será recalculada e as durações das tarefas poderão mudar.

## <a name="project-team-members"></a>Membros da equipa do projeto

Quando uma equipa do projeto é copiada a partir do projeto de origem, são copiados os recursos genéricos. As atribuições de recursos genéricos também são mantidas como no projeto de origem. Os recursos nomeados serão convertidos para membros genéricos da equipa.

## <a name="estimates"></a>Estimativas

Quando o projeto é copiado, as linhas de estimativa de recursos, despesas e materiais são copiadas do projeto de origem. 

Para obter informações sobre como aceder programaticamente a Copiar Projeto, consulte [Programar modelos de projeto com Copiar Projeto](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
