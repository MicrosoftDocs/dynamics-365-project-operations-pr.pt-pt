---
title: Notas do programador para Aprovações
description: Este tópico fornece informações adicionais do programador sobre o trabalho aprovações.
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 9e4e910d0ff0a5f2603148fcc5daa0d423a4d174
ms.sourcegitcommit: a9dbcd3aff4c6ae495412e4980e105ae160fd1ec
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 11/10/2020
ms.locfileid: "4483962"
---
# <a name="developer-notes-for-approvals"></a>Notas do programador para Aprovações

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

O Dynamics 365 Project Operations inclui uma lógica de validação que garante a correta transição de registo através das fases de aprovação. As transições de registo corretas asseguram que: 

  - Todas as linhas de suporte são criadas em tabelas relacionadas, tais como diários e valores reais.
  - O aprovador é marcado como um **Aprovador de Projeto** no projeto antes de prosseguir.
