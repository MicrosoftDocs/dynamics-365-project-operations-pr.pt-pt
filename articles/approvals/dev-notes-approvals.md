---
title: Notas do programador para Aprovações
description: Este tópico fornece informações adicionais do programador sobre o trabalho aprovações.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cfa4928eda286bee298a2c33f4e9c25b576f495795fc2deda33b393e372465b1
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991680"
---
# <a name="developer-notes-for-approvals"></a>Notas do programador para Aprovações

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

O Dynamics 365 Project Operations inclui uma lógica de validação que garante a correta transição de registo através das fases de aprovação. As transições de registo corretas asseguram que: 

  - Todas as linhas de suporte são criadas em tabelas relacionadas, tais como diários e valores reais.
  - O aprovador é marcado como um **Aprovador de Projeto** no projeto antes de prosseguir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]