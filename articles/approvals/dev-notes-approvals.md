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
ms.openlocfilehash: d58c776b0341c08b0292e1b459a7d7ebac550bcc
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290283"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="970bd-103">Notas do programador para Aprovações</span><span class="sxs-lookup"><span data-stu-id="970bd-103">Developer notes for Approvals</span></span>

<span data-ttu-id="970bd-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="970bd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="970bd-105">O Dynamics 365 Project Operations inclui uma lógica de validação que garante a correta transição de registo através das fases de aprovação.</span><span class="sxs-lookup"><span data-stu-id="970bd-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="970bd-106">As transições de registo corretas asseguram que:</span><span class="sxs-lookup"><span data-stu-id="970bd-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="970bd-107">Todas as linhas de suporte são criadas em tabelas relacionadas, tais como diários e valores reais.</span><span class="sxs-lookup"><span data-stu-id="970bd-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="970bd-108">O aprovador é marcado como um **Aprovador de Projeto** no projeto antes de prosseguir.</span><span class="sxs-lookup"><span data-stu-id="970bd-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]