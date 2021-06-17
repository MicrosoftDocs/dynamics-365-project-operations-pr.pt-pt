---
title: Descrição geral da despesa
description: Este tópico fornece informação sobre a funcionalidade Despesa no Project Operations.
author: stsporen
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2a26b321e15080cc6a4a6a3ed410be175e790a1b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995410"
---
# <a name="expense-home-page"></a><span data-ttu-id="b9f00-103">Home page das despesas</span><span class="sxs-lookup"><span data-stu-id="b9f00-103">Expense home page</span></span>

<span data-ttu-id="b9f00-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="b9f00-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="b9f00-105">Dynamics 365 Project Operations apoia a capacidade de processar despesas.</span><span class="sxs-lookup"><span data-stu-id="b9f00-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="b9f00-106">O processamento de despesas ocorre com ou sem projetos através de um fluxo de trabalho personalizável de políticas, categorias de transação e aprovações.</span><span class="sxs-lookup"><span data-stu-id="b9f00-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="b9f00-107">No Project Operations, existem dois modelos de implementação suportados para Despesas:</span><span class="sxs-lookup"><span data-stu-id="b9f00-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="b9f00-108">**Completo**: está disponível a implementação completa para o **Project Operations para cenários baseados em recursos/não armazenados** ou **Project Operations para cenários baseados em encomenda de produção**.</span><span class="sxs-lookup"><span data-stu-id="b9f00-108">**Full**: Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order-based scenarios**.</span></span>
- <span data-ttu-id="b9f00-109">**Básico**: a implementação básica está disponível para **Project Operations para cenários baseados em recursos/não armazenados** e **Implementação leve – oportunidade potencial para fatura pró-forma**.</span><span class="sxs-lookup"><span data-stu-id="b9f00-109">**Basic**: Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="b9f00-110">Total</span><span class="sxs-lookup"><span data-stu-id="b9f00-110">Full</span></span> 
<span data-ttu-id="b9f00-111">A implementação de Despesas Completas proporciona uma aplicação completa da política que inclui a capacidade de criar políticas, tais como:</span><span class="sxs-lookup"><span data-stu-id="b9f00-111">Full Expense deployment provides a complete policy enforcement that includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="b9f00-112">Limites da categoria de despesa</span><span class="sxs-lookup"><span data-stu-id="b9f00-112">Expense category limits</span></span>
  - <span data-ttu-id="b9f00-113">Viagens</span><span class="sxs-lookup"><span data-stu-id="b9f00-113">Travel</span></span>
  - <span data-ttu-id="b9f00-114">Diária</span><span class="sxs-lookup"><span data-stu-id="b9f00-114">Per diem</span></span>
  - <span data-ttu-id="b9f00-115">Importações de cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="b9f00-115">Credit card imports</span></span>
  - <span data-ttu-id="b9f00-116">Reconhecimento de caracteres óticos de recibos</span><span class="sxs-lookup"><span data-stu-id="b9f00-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="b9f00-117">Básica</span><span class="sxs-lookup"><span data-stu-id="b9f00-117">Basic</span></span> 
<span data-ttu-id="b9f00-118">O cenário de implementação Despesa Básica só permite registar as despesas básicas para um projeto.</span><span class="sxs-lookup"><span data-stu-id="b9f00-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="b9f00-119">Para mais informações, consulte [Entrada de despesas (lite)](basic-expense.md)</span><span class="sxs-lookup"><span data-stu-id="b9f00-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="b9f00-120">Determinar a Implementação de despesa</span><span class="sxs-lookup"><span data-stu-id="b9f00-120">Determine your Expense deployment</span></span>
<span data-ttu-id="b9f00-121">Para determinar se está a executar a implementação da gestão Despesa Básica, verifique se o URL do endereço termina com **.crm.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="b9f00-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]