---
title: Copiar um projeto
description: Este tópico fornece informações sobre copiar projetos no Dynamics 365 Project Operations.
author: ruhercul
ms.date: 03/07/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: e9b637d2d282d123dfacb8a295292ea06549aa1e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574444"
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
- Listas de verificação do projeto
- Registos do projeto

## <a name="project-properties"></a>Propriedades do projeto

Quando o projeto é copiado, são copiados os valores nos seguintes campos.

| Campo | Materiais sem stock no Project Operations | Project Operations Lite | Project for the Web |
|-------|------------------------------------------|-------------------------|---------------------|
| Name | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Description | :heavy_check_mark: | :heavy_check_mark: | |
| Cliente | :heavy_check_mark: | :heavy_check_mark: | |
| Modelo de Calendário | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Moeda | :heavy_check_mark: | :heavy_check_mark: | |
| Unidade de Contratação | :heavy_check_mark: | :heavy_check_mark: | |
| Empresa Proprietária | :heavy_check_mark: | | |
| Gestor de Projeto | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Status | :heavy_check_mark: | :heavy_check_mark: | |
| Estado Geral do Projeto | :heavy_check_mark: | :heavy_check_mark: | |
| Comentários | :heavy_check_mark: | :heavy_check_mark: | |
| Estimativas | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Data de Início Estimada</p><p><strong>Nota:</strong> este campo especifica a data de criação do projeto a partir da cópia. | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Data de Conclusão Estimada</p><p><strong>Nota:</strong> a data neste campo é ajustada com base na data de início do novo projeto que foi feito a partir da cópia.</p> | :heavy_check_mark: | :heavy_check_mark: | |
| Esforço (Horas) | :heavy_check_mark: | :heavy_check_mark: | |
| Custo Estimado da Mão-de-Obra | :heavy_check_mark: | :heavy_check_mark: | |
| Custo Estimado da Despesa | :heavy_check_mark: | :heavy_check_mark: | |
| Custo Estimado do Material | | :heavy_check_mark: | |

> [!NOTE]
> Copiar projeto é uma operação de execução prolongada. Os registos do projeto, os seus atributos relevantes e muitas entidades relacionadas também são copiados. Devido à natureza de execução prolongada da operação, após o início da cópia, a página de destino do projecto está bloqueada para edição até que a operação da cópia esteja concluída.

## <a name="work-breakdown-structure"></a>Estrutura Hierárquica do Trabalho

Quando o projeto é copiado, é copiada toda a estrutura hierárquica do trabalho carregada pelos recursos. Os recursos nomeados são substituídos por recursos genéricos. Se os recursos nomeados não têm as mesmas horas de trabalho que o recurso genérico, a agenda será recalculada e a duração das tarefas poderá ser mudada.

## <a name="project-team-members"></a>Membros da equipa do projeto

Quando uma equipa do projeto é copiada a partir do projeto de origem, são copiados os recursos genéricos. As atribuições de recursos genéricos também são mantidas como no projeto de origem. Os recursos nomeados serão convertidos para membros genéricos da equipa.

> [!NOTE]
> Os membros da equipa e as atribuições não são copiados no Project for the Web.

## <a name="estimates"></a>Estimativas

Quando o projeto é copiado, as linhas de estimativa de recursos, despesas e materiais são copiadas do projeto de origem. 

Para obter informações sobre como aceder programaticamente a Copiar Projeto, consulte [Programar modelos de projeto com Copiar Projeto](dev-copy-project.md).

## <a name="quotes-and-contracts"></a>Propostas e contratos

As propostas e os contratos não estão associados ao projeto de destino.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
