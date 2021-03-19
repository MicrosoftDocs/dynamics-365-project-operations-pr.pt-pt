---
title: Configurar categorias do projeto
description: Este tópico fornece informações sobre como configurar categorias de projetos.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b7adf61a82714a0148d9c8b1d2b2b37fd611c1cf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287522"
---
# <a name="configure-project-categories"></a>Configurar categorias do projeto

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

O Project Operations oferece funcionalidades robustas para categorizar as receitas e as despesas nos projetos. As categorias fornecem a capacidade de reportar e analisar transações de projetos, e impulsionar o lançamento no razão geral.

O diagrama seguinte ilustra a correlação entre categorias de transações, categorias partilhadas e categorias de projetos. 

As categorias de transações são o agrupamento básico para transações de projetos. Nesse agrupamento, existe um conjunto de categorias partilhadas que podem ser partilhadas entre aplicações e módulos. Entrando ainda mais nos detalhes, as categorias de projetos são o nível mais granular das categorias. As categorias de projetos são específicas da entidade jurídica, do módulo e da aplicação.

![Correlação entre categorias de transações, categorias partilhadas e categorias de projetos](media/project-categories.png)

## <a name="transaction-categories"></a>Categorias de transações

As categorias de transações representam o agrupamento básico para as transações de projetos e não são específicas da empresa ou do tipo de transação. Por exemplo, a Contoso Robotics utiliza as categorias Design, Viagem, Instalação e Transação de Serviços para agrupar as Transações do projeto.

As categorias de transações são definidas no módulo Project Operations. 
1. Vá para **Definições** \> **Categorias de Transação** para abrir o formulário. 
2. Crie uma nova categoria de transação ao selecionar **Novo** ou ao selecionar **Importar do Excel**.

## <a name="shared-categories"></a>Categorias partilhadas

A Dynamics 365 utiliza o conceito de categorias Partilhadas para categorizar despesas em diferentes aplicações, tais como Dynamics 365 Finance, Dynamics 365 Supply Chain e Dynamics 365 Project Operations. Para cada Categoria de transação criada, o Project Operations cria automaticamente quatro Categorias partilhadas relacionadas: Horas, Despesa, Taxas e Item. Pode rever e ajustar as categorias partilhadas em **Gestão de projetos e contabilística** \> **Configurar** \> **Categorias** \> **Categorias Partilhadas**.

## <a name="project-categories"></a>Categorias do projeto

As categorias de projetos representam o nível mais granular de configuração de categorias e têm de ser configuradas separadamente, e para cada empresa, por um Contabilista de projetos.

1. Vá para **Gestão de projetos e contabilística** \> **Configurar** \> **Categorias** \> **Categorias do projeto**.
2. Selecione **Novo**.
3. Selecione o **ID da Categoria** da Categoria partilhada que criou na secção anterior. O Project Operations permite utilizar apenas as categorias partilhadas que estão associadas às categorias de transações.
4. Selecione um grupo de categorias.

## <a name="category-groups"></a>Grupos de categorias

Os grupos de categorias são utilizados para partilhar as propriedades, principalmente perfis de lançamento, entre Categorias de projetos relacionadas. Tem de haver pelo menos um grupo de categorias para cada tipo de transação e cada categoria de projeto é atribuída a um grupo.

As especificações de lançamento no Project Operations são definidas pelas regras do perfil de custos e receitas, pelas categorias de projetos e pelos grupos de categorias. Pode configurar grupos de categorias em **Gestão de projetos e contabilística** \> **Configurar** \> **Categorias** \> **Grupos de categorias**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]