---
title: Reservas versus atribuições
description: Este tópico fornece informações sobre as diferenças entre as reservas de recursos e as atribuições de recursos.
author: ruhercul
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8fe6937dfdfe137f28917c16da1d7dc6155284ae
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130232"
---
# <a name="bookings-vs-assignments"></a>Reservas versus atribuições

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

As reservas são a alocação fixa ou flexível de recursos a um projeto. As reservas fixas consomem a capacidade de um recurso. As reservas representam conceitos organizacionais para as equipas, para que possam compreender como os recursos serão envolvidos em vários projetos. O Dynamics 365 Project Operations considera as reservas um conceito ao nível do projeto. 

Ao contrários das reservas, as atribuições são a alocação de recursos às tarefas de projeto na agenda do projeto. Os recursos podem ser nomeados ou genéricos. 

Normalmente, a soma das reservas para um recurso será igual à soma das atribuições do recurso numa ou muitas tarefas. No entanto, o Project Operations não impõe este contrato. A vista de **Reconciliação** mostra o Gestor de projeto em que as reservas e as atribuições de um recurso não concordam.
