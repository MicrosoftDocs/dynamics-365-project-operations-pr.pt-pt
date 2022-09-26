---
title: Segurança e aprovações
description: Este artigo fornece informações sobre a configuração de segurança para trabalhar com aprovações no Microsoft Dynamics 365 Project Operations.
author: stsporen
ms.date: 08/29/2022
ms.topic: security
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: bc33f63f66bdcf1470e5d9386cfc3661774436fd
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/16/2022
ms.locfileid: "9525369"
---
# <a name="security-and-approvals"></a>Segurança e aprovações

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

O Microsoft Dynamics 365 Project Operations utiliza dois direitos de acesso para permitir a aprovação de entradas de tempo, despesas e materiais:

- Aprovador do Projeto
- Admin de Aprovador do Projeto

## <a name="project-approver"></a>Aprovador do Projeto

Tem de ter o direito de acesso de **Aprovador do Projeto** para aprovar entradas de tempo, despesas e materiais do projeto. Também tem de ter acesso às entidades relacionadas relevantes, tais como **Projeto**. Esse acesso pode ser atribuído por alguém que tenha a função **Gestor de Projetos**. Além disso, tem de ser membro da equipa do projeto e de estar marcado como aprovador.

Para aprovar entradas que não sejam do projeto, tem de ser o gestor do submissor.

## <a name="project-approver-admin"></a>Admin de Aprovador do Projeto

> [!NOTE]
> A caraterística de [Conjuntos de aprovação](approval-sets.md) tem de estar ativada antes de poder utilizar a funcionalidade de Admin do Aprovador de Projetos.

O direito de acesso **Admin do Aprovador de Projetos** permite que os utilizadores ignorem políticas e permite a aprovação de entradas em todos os projetos. A atribuição desta função irá ignorar a lógica de validação que necessita de associação à equipa e que está marcada como aprovador. Tem de ter acesso às entidades relacionadas relevantes, tais como **Projeto**. Esse acesso pode ser atribuído por alguém que tenha a função **Gestor de Projetos**.

O contexto de utilizador do SISTEMA ignora validações da mesma forma que o direito de acesso de Admin do Aprovador de Projetos.
