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
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="bed4a-103">Notas do programador para Aprovações</span><span class="sxs-lookup"><span data-stu-id="bed4a-103">Developer notes for Approvals</span></span>

<span data-ttu-id="bed4a-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="bed4a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bed4a-105">O Dynamics 365 Project Operations inclui uma lógica de validação que garante a correta transição de registo através das fases de aprovação.</span><span class="sxs-lookup"><span data-stu-id="bed4a-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="bed4a-106">As transições de registo corretas asseguram que:</span><span class="sxs-lookup"><span data-stu-id="bed4a-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="bed4a-107">Todas as linhas de suporte são criadas em tabelas relacionadas, tais como diários e valores reais.</span><span class="sxs-lookup"><span data-stu-id="bed4a-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="bed4a-108">O aprovador é marcado como um **Aprovador de Projeto** no projeto antes de prosseguir.</span><span class="sxs-lookup"><span data-stu-id="bed4a-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>