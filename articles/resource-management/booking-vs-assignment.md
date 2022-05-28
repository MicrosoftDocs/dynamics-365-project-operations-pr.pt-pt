---
title: Reservas versus atribuições
description: Este tópico fornece informações sobre as diferenças entre as reservas de recursos e as atribuições de recursos.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: b06555ec48e50f88c11872336539ca88c5cef34a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591281"
---
# <a name="bookings-vs-assignments"></a>Reservas versus atribuições

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

As reservas são a alocação fixa ou flexível de recursos a um projeto. As reservas fixas consomem a capacidade de um recurso. As reservas representam conceitos organizacionais para as equipas, para que possam compreender como os recursos serão envolvidos em vários projetos. Dynamics 365 Project Operations considera as reservas um conceito de nível de projeto. 

Ao contrários das reservas, as atribuições são a alocação de recursos às tarefas de projeto na agenda do projeto. Os recursos podem ser nomeados ou genéricos.  Quando um requisito de recursos é derivado das atribuições de tarefas do projeto, o Project Operations usa os contornos de esforço da atribuição de recursos para construir os contornos dos detalhes dos requisitos de recursos. No entanto, não é mantida uma referência para as atribuições de recursos. As atualizações às reservas derivadas do requisito de recursos não atualizam nenhuma atribuição de recursos.

Normalmente, a soma das reservas para um recurso será igual à soma das atribuições do recurso numa ou muitas tarefas. No entanto, o Project Operations não impõe este contrato. A vista de **Reconciliação** mostra o Gestor de projeto em que as reservas e as atribuições de um recurso não concordam.




[!INCLUDE[footer-include](../includes/footer-banner.md)]