---
title: FAQ de gestão de recursos
description: Este tópico fornece respostas às perguntas mais frequentes sobre a gestão de recursos.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: fdf7f1e2-e4a2-4c68-aa03-4a41c7b10531
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 87da759b3b30ed6d38866c045194cde79837c209
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754587"
---
# <a name="resource-management-faq"></a>FAQ de gestão de recursos

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a>Qual é a diferença entre um membro da equipa e um requisito de recurso?

Um membro da equipa do projeto pode ser atribuído a tarefas, reservado ou reservado em excesso e definido como aprovador. Um requisito de recurso pode existir sem um membro da equipa do projeto, como uma nota de procura de rascunho. 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a>Qual é a diferença entre as horas propostas e as horas reservadas de forma flexível?

As horas propostas e as horas reservadas de forma flexível diferem em visibilidade. As horas propostas são visíveis apenas para os gestores de recursos e o gestor de projeto que iniciaram a procura utilizando um pedido de recurso. As horas reservadas de forma flexível são visíveis a qualquer pessoa que tenha acesso ao Quadro da Agenda.

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a>Como posso ver as horas reservadas de forma flexível para os recursos numa equipa?

As reservas flexíveis podem ser efetuadas quando reserva um requisito de recurso. Os recursos que são reservados de forma flexível numa equipa do projeto aparecem como membros da equipa que possuem horas reservadas de forma flexível. Também aparecem no Quadro da Agenda.

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a>Como posso alterar as horas necessárias e as datas de início e de fim, para um recurso (genérico ou nomeado) que reservei?

Depois de os recursos serem reservados, selecione **Manter Reservas** para efetuar as alterações necessárias.

## <a name="what-resources-types-does-project-service-automation-support"></a>Que tipos de recursos suporta o Project Service Automation?

O **Utilizador** e o **Contacto** são os únicos tipos de recursos suportados no Dynamics 365 Project Service Automation. Apesar de poder criar outros tipos de recursos (por exemplo, **Equipamento** e **Grupo**), nenhum caso de utilização completo é suportado por eles.

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a>Qual é a diferença entre uma atribuição e uma reserva?

As atribuições são a atribuição de recursos às tarefas de projeto na agenda do projeto. Os recursos podem ser recursos reais ou genéricos. As reservas são a alocação fixa ou flexível de recursos a um projeto. As reservas fixas consomem a capacidade de um recurso. Idealmente, no caso dos recursos reais, as reservas e atribuições devem concordar, porque não diferem. No entanto, o PSA não impõe este contrato. A vista de Reconciliação mostra um gestor de projeto em que as reservas e as atribuições de um recurso não concordam.
