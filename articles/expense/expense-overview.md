---
title: Descrição geral da despesa
description: Este tópico fornece informação sobre a funcionalidade Despesa no Project Operations.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 6da831fef5dba060b8019d7689645405c7ebdbed
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082284"
---
# <a name="expense-home-page"></a><span data-ttu-id="29008-103">Home page das despesas</span><span class="sxs-lookup"><span data-stu-id="29008-103">Expense home page</span></span>

<span data-ttu-id="29008-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="29008-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="29008-105">O Dynamics 365 Project Operations suporta a capacidade de processar despesas.</span><span class="sxs-lookup"><span data-stu-id="29008-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="29008-106">O processamento de despesas ocorre com ou sem projetos através de um fluxo de trabalho personalizável de políticas, categorias de transação e aprovações.</span><span class="sxs-lookup"><span data-stu-id="29008-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="29008-107">No Project Operations, existem dois modelos de implementação suportados para Despesas:</span><span class="sxs-lookup"><span data-stu-id="29008-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="29008-108">**Completo** : está disponível a implementação completa para o **Project Operations para cenários baseados em recursos/não armazenados** ou **Project Operations para cenários baseados em encomenda de produção**.</span><span class="sxs-lookup"><span data-stu-id="29008-108">**Full** : Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order based scenarios**.</span></span>
- <span data-ttu-id="29008-109">**Básico** : a implementação básica está disponível para **Project Operations para cenários baseados em recursos/não armazenados** e **Implementação leve – oportunidade potencial para fatura pró-forma**.</span><span class="sxs-lookup"><span data-stu-id="29008-109">**Basic** : Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="29008-110">Total</span><span class="sxs-lookup"><span data-stu-id="29008-110">Full</span></span> 
<span data-ttu-id="29008-111">A implementação Despesa Total fornece uma aplicação completa de políticas que inclui a capacidade de criar políticas, tais como:</span><span class="sxs-lookup"><span data-stu-id="29008-111">Full Expense deployment provides a complete policy enforcement which includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="29008-112">Limites da categoria de despesa</span><span class="sxs-lookup"><span data-stu-id="29008-112">Expense category limits</span></span>
  - <span data-ttu-id="29008-113">Viagens</span><span class="sxs-lookup"><span data-stu-id="29008-113">Travel</span></span>
  - <span data-ttu-id="29008-114">Diária</span><span class="sxs-lookup"><span data-stu-id="29008-114">Per diem</span></span>
  - <span data-ttu-id="29008-115">Importações de cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="29008-115">Credit card imports</span></span>
  - <span data-ttu-id="29008-116">Reconhecimento de caracteres óticos de recibos</span><span class="sxs-lookup"><span data-stu-id="29008-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="29008-117">Básica</span><span class="sxs-lookup"><span data-stu-id="29008-117">Basic</span></span> 
<span data-ttu-id="29008-118">O cenário de implementação Despesa Básica só permite registar as despesas básicas para um projeto.</span><span class="sxs-lookup"><span data-stu-id="29008-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="29008-119">Para mais informações, consulte [Entrada de despesas (lite)](basic-expense.md)</span><span class="sxs-lookup"><span data-stu-id="29008-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="29008-120">Determinar a Implementação de despesa</span><span class="sxs-lookup"><span data-stu-id="29008-120">Determine your Expense deployment</span></span>
<span data-ttu-id="29008-121">Para determinar se está a executar a implementação da gestão Despesa Básica, verifique se o URL do endereço termina com **.crm.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="29008-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 
