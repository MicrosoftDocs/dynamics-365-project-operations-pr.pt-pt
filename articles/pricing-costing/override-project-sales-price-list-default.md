---
title: Substituir listas de preços de vendas do projeto
description: Este tópico fornece informações sobre a criação de listas de preços de venda personalizadas.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: af9baca540d89f4e5e616bdfdd6111bef29abe28
ms.sourcegitcommit: 656a9d03f260c29e988e2ff05b6e07ae0365d6d0
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 12/04/2020
ms.locfileid: "4672245"
---
# <a name="override-project-sales-price-lists"></a><span data-ttu-id="0b407-103">Substituir listas de preços de vendas do projeto</span><span class="sxs-lookup"><span data-stu-id="0b407-103">Override project sales price lists</span></span>

<span data-ttu-id="0b407-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="0b407-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="customer-specific-project-price-lists"></a><span data-ttu-id="0b407-105">Listas de preços de projeto específicas do cliente</span><span class="sxs-lookup"><span data-stu-id="0b407-105">Customer-specific project price lists</span></span>

<span data-ttu-id="0b407-106">Os contratos de preços específicos do cliente podem ser configurados como listas de preços do projeto num registo de conta no Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="0b407-106">Customer-specific price agreements can be set up as project price lists on an account record in Dynamics 365 Project Operations.</span></span>

<span data-ttu-id="0b407-107">Para configurar uma lista de preços de projeto específica do cliente, na área **Vendas**, navegue para o registo da conta.</span><span class="sxs-lookup"><span data-stu-id="0b407-107">To set up a customer-specific project price list, in the **Sales** area, navigate to the account record.</span></span>

1. <span data-ttu-id="0b407-108">Abra a página de lista **Contas**.</span><span class="sxs-lookup"><span data-stu-id="0b407-108">Open the **Accounts** list page.</span></span>
2. <span data-ttu-id="0b407-109">Localize e clique duas vezes num registo de cliente para abrir a página de detalhes da **Conta**.</span><span class="sxs-lookup"><span data-stu-id="0b407-109">Locate and double-click a customer record to open the **Account** details page.</span></span>
3. <span data-ttu-id="0b407-110">No separador **Listas de preços do Projeto**, selecione **+ Nova Lista de preços do Projeto**.</span><span class="sxs-lookup"><span data-stu-id="0b407-110">On the **Project Price lists** tab, select **+ New Project Price List**.</span></span>
4. <span data-ttu-id="0b407-111">Na página **Nova Lista de Preços do Projeto**, selecione uma lista de preços a partir da lista pendente.</span><span class="sxs-lookup"><span data-stu-id="0b407-111">On the **New Project Price List** page, select a price list from the drop-down.</span></span> <span data-ttu-id="0b407-112">Apenas listas de preços que tenham o contexto definido para **Vendas** e cuja moeda corresponda à moeda da conta estão incluídas.</span><span class="sxs-lookup"><span data-stu-id="0b407-112">Only price lists that have the context set to **Sales** and whose currency matches the account currency are included.</span></span>
5. <span data-ttu-id="0b407-113">Nomeie a associação e, em seguida, selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="0b407-113">Name the association, and then select **Save**.</span></span> <span data-ttu-id="0b407-114">É criada uma lista de preços de projeto específica do cliente.</span><span class="sxs-lookup"><span data-stu-id="0b407-114">A customer-specific project price list is created.</span></span> <span data-ttu-id="0b407-115">Esta lista de preços será utilizada para os preços de projeto predefinidos em propostas de projetos ou contratos criados para este cliente, sempre que a data criada do contrato de proposta ou projeto se insere na data da efetividade da lista de preços.</span><span class="sxs-lookup"><span data-stu-id="0b407-115">This price list will be used to default project prices on project quotes or contracts created for this customer where the created date of the quote or project contract falls within the date effectivity of the price list.</span></span>

## <a name="custom-pricing-on-project-quotes"></a><span data-ttu-id="0b407-116">Preços personalizados em propostas de projeto</span><span class="sxs-lookup"><span data-stu-id="0b407-116">Custom pricing on project quotes</span></span>

<span data-ttu-id="0b407-117">Nas propostas de projeto, pode ter preços de projeto que começam com uma lista de preços padrão predefinida que assume a predefinição do cliente ou dos parâmetros do projeto.</span><span class="sxs-lookup"><span data-stu-id="0b407-117">On project quotes, you can have project pricing that starts with a default standard price list that defaults from the customer or from the project parameters.</span></span>

<span data-ttu-id="0b407-118">Quando precisa de preços personalizados para trabalhos relacionados com projetos numa determinada proposta, pode obtê-los a partir da entidade associada às listas de preços de projeto.</span><span class="sxs-lookup"><span data-stu-id="0b407-118">When you need custom pricing for project-related work on a particular quote, you can get that from the project price lists associated entity.</span></span>

<span data-ttu-id="0b407-119">Complete os seguintes passos para configurar preços de projeto específicos da proposta.</span><span class="sxs-lookup"><span data-stu-id="0b407-119">Complete the following steps to set up quote-specific project pricing.</span></span>

1. <span data-ttu-id="0b407-120">Abra a proposta do projeto e selecione o separador **Listas de Preços do Projeto**.</span><span class="sxs-lookup"><span data-stu-id="0b407-120">Open the project quote and select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="0b407-121">Na subgrelha, selecione **Criar preços personalizados**.</span><span class="sxs-lookup"><span data-stu-id="0b407-121">In the subgrid, select **Create custom pricing**.</span></span>

<span data-ttu-id="0b407-122">Todas as listas de preços do projeto que estão anexadas à proposta são copiadas para novas listas de preços.</span><span class="sxs-lookup"><span data-stu-id="0b407-122">All the project price lists that are attached to the quote are copied to new price lists.</span></span> <span data-ttu-id="0b407-123">Os nomes das novas listas de preços refletem o nome da proposta com um carimbo de data/hora para quando estas listas de preços foram criadas.</span><span class="sxs-lookup"><span data-stu-id="0b407-123">The names of the new price lists reflect the name of quote with a date-time stamp for when these price lists were created.</span></span>

<span data-ttu-id="0b407-124">Pode utilizar cada uma dessas listas de preços e atualizar os preços de mão de obra (preço de função) e despesas (preço de categoria).</span><span class="sxs-lookup"><span data-stu-id="0b407-124">You can use each of those price lists and make updates to labor (role price) and expense (category price) prices.</span></span> <span data-ttu-id="0b407-125">Estes preços só serão aplicáveis a esta proposta de projeto.</span><span class="sxs-lookup"><span data-stu-id="0b407-125">These prices will only be applicable to this project quote.</span></span>

## <a name="price-lists-on-a-project-contract"></a><span data-ttu-id="0b407-126">Listas de preços num contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="0b407-126">Price lists on a project contract</span></span>

<span data-ttu-id="0b407-127">Num contrato do projeto, os preços do projeto assumem sempre a predefinição de uma lista de preços personalizada com o nome do contrato e o carimbo de data/hora criado anexado ao nome.</span><span class="sxs-lookup"><span data-stu-id="0b407-127">On a project contract, project pricing always defaults as a custom price list with the name of contract and the created date time stamp appended to the name.</span></span> <span data-ttu-id="0b407-128">Isto é verdade se o contrato foi criado quando a proposta foi ganha ou se o contrato foi criado de raiz.</span><span class="sxs-lookup"><span data-stu-id="0b407-128">This is true whether the contract was created when the quote was won or if the contract was created from scratch.</span></span> <span data-ttu-id="0b407-129">Se necessário, pode remover esta associação à lista de preços personalizada e associar uma lista de preços padrão ao contrato do projeto.</span><span class="sxs-lookup"><span data-stu-id="0b407-129">If needed, you can remove this association to the custom price list and associate a standard price list to the project contract instead.</span></span>

<span data-ttu-id="0b407-130">Quando associar uma lista de preços padrão às listas de preços do projeto na proposta ou no contrato, quaisquer alterações efetuadas aos preços na lista de preços terão impacto em todas as propostas e contratos que utilizem a lista de preços.</span><span class="sxs-lookup"><span data-stu-id="0b407-130">When you associate a standard price list to the project price lists on quote or contract, any changes made to the prices in the price list will impact all quotes and contracts that use the price list.</span></span>
