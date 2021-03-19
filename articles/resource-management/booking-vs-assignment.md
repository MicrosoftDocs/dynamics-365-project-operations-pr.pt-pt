---
title: Reservas versus atribuições
description: Este tópico fornece informações sobre as diferenças entre as reservas de recursos e as atribuições de recursos.
author: ruhercul
manager: Annbe
ms.date: 01/08/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3aaf8dcbae0a5762879c2b1223eba3bdc33af1a7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279917"
---
# <a name="bookings-vs-assignments"></a>Reservas versus atribuições

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

As reservas são a alocação fixa ou flexível de recursos a um projeto. As reservas fixas consomem a capacidade de um recurso. As reservas representam conceitos organizacionais para as equipas, para que possam compreender como os recursos serão envolvidos em vários projetos. Dynamics 365 Project Operations considera as reservas um conceito de nível de projeto. 

Ao contrários das reservas, as atribuições são a alocação de recursos às tarefas de projeto na agenda do projeto. Os recursos podem ser nomeados ou genéricos.  Quando um requisito de recursos é derivado das atribuições de tarefas do projeto, o Project Operations usa os contornos de esforço da atribuição de recursos para construir os contornos dos detalhes dos requisitos de recursos. No entanto, não é mantida uma referência para as atribuições de recursos. As atualizações às reservas derivadas do requisito de recursos não atualizam nenhuma atribuição de recursos.

Normalmente, a soma das reservas para um recurso será igual à soma das atribuições do recurso numa ou muitas tarefas. No entanto, o Project Operations não impõe este contrato. A vista de **Reconciliação** mostra o Gestor de projeto em que as reservas e as atribuições de um recurso não concordam.




[!INCLUDE[footer-include](../includes/footer-banner.md)]