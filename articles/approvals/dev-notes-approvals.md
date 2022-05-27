---
title: Notas do programador para Aprovações
description: Este tópico fornece informações adicionais do programador sobre o trabalho aprovações.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: c02778c4ed79a8750d207b5870300ebf0f479be7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579734"
---
# <a name="developer-notes-for-approvals"></a>Notas do programador para Aprovações

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

O Dynamics 365 Project Operations inclui uma lógica de validação que garante a correta transição de registo através das fases de aprovação. As transições de registo corretas asseguram que: 

  - Todas as linhas de suporte são criadas em tabelas relacionadas, tais como diários e valores reais.
  - O aprovador é marcado como um **Aprovador de Projeto** no projeto antes de prosseguir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]