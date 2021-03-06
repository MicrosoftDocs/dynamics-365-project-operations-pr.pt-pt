---
title: Configurar categorias do projeto
description: Este tópico fornece informações sobre como configurar categorias de projetos.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 84033182ce047d230724409eef9bc6afcaefd2b4
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3895980"
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

O Dynamics 365 utiliza o conceito de Categorias partilhadas para categorizar as despesas em diferentes aplicações, como o Dynamics 365 Finance, Dynamics 365 Supply Chain e Dynamics 365 Project Operations. Para cada Categoria de transação criada, o Project Operations cria automaticamente quatro Categorias partilhadas relacionadas: Horas, Despesa, Taxas e Item. Pode rever e ajustar as categorias partilhadas em **Gestão de projetos e contabilística** \> **Configurar** \> **Categorias** \> **Categorias Partilhadas**.

## <a name="project-categories"></a>Categorias do projeto

As categorias de projetos representam o nível mais granular de configuração de categorias e têm de ser configuradas separadamente, e para cada empresa, por um Contabilista de projetos.

1. Vá para **Gestão de projetos e contabilística** \> **Configurar** \> **Categorias** \> **Categorias do projeto**.
2. Selecione **Novo**.
3. Selecione o **ID da Categoria** da Categoria partilhada que criou na secção anterior. O Project Operations permite utilizar apenas as categorias partilhadas que estão associadas às categorias de transações.
4. Selecione um grupo de categorias.

## <a name="category-groups"></a>Grupos de categorias

Os grupos de categorias são utilizados para partilhar as propriedades, principalmente perfis de lançamento, entre Categorias de projetos relacionadas. Tem de haver pelo menos um grupo de categorias para cada tipo de transação e cada categoria de projeto é atribuída a um grupo.

As especificações de lançamento no Project Operations são definidas pelas regras do perfil de custos e receitas, pelas categorias de projetos e pelos grupos de categorias. Pode configurar grupos de categorias em **Gestão de projetos e contabilística** \> **Configurar** \> **Categorias** \> **Grupos de categorias**.
