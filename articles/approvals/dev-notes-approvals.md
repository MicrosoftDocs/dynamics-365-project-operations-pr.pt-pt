---
title: Notas do programador para Aprovações
description: Este artigo fornece informações adicionais sobre como trabalhar com aprovações.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: df3e27f95bffb9c169644fa3e42ff1e9b2b6ff54
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924766"
---
# <a name="developer-notes-for-approvals"></a>Notas do programador para Aprovações

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

O Dynamics 365 Project Operations inclui uma lógica de validação que garante a correta transição de registo através das fases de aprovação. As transições de registo corretas asseguram que: 

  - Todas as linhas de suporte são criadas em tabelas relacionadas, tais como diários e valores reais.
  - O aprovador é marcado como um **Aprovador de Projeto** no projeto antes de prosseguir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]