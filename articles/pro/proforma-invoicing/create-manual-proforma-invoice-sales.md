---
title: Criar uma fatura pró-forma manual – lite
description: Este tópico fornece informações sobre a criação de uma fatura pró-forma manual no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 87ef090454b2a7ab997e7c21d8d10badc31c8235
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176400"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="6c041-103">Criar uma fatura pró-forma manual – lite</span><span class="sxs-lookup"><span data-stu-id="6c041-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="6c041-104">_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_</span><span class="sxs-lookup"><span data-stu-id="6c041-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6c041-105">No Dynamics 365 Project Operations, as faturas pró-forma podem ser criadas manualmente, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="6c041-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="6c041-106">Pode criar manualmente uma fatura pró-forma a partir da página da lista **Contratos do Projeto** ou na página de detalhes **Contrato do Projeto**.</span><span class="sxs-lookup"><span data-stu-id="6c041-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="6c041-107">Página de lista Contratos do Projeto</span><span class="sxs-lookup"><span data-stu-id="6c041-107">Project Contracts list page</span></span>

<span data-ttu-id="6c041-108">A partir da página da lista **Contratos do Projeto**, selecione um ou mais contratos de projeto e crie faturas para todos os registos selecionados.</span><span class="sxs-lookup"><span data-stu-id="6c041-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="6c041-109">O sistema verifica qual dos contratos de projeto selecionados tem uma tarefa pendente de **Pronto a Faturar** datado anterior à data de hoje.</span><span class="sxs-lookup"><span data-stu-id="6c041-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog  dated before today's date.</span></span> <span data-ttu-id="6c041-110">A partir desses contratos, o sistema cria faturas pró-forma de rascunho.</span><span class="sxs-lookup"><span data-stu-id="6c041-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="6c041-111">Se um contrato de projeto tiver vários clientes, pode haver uma fatura criada por cliente, e várias faturas por contrato de projeto.</span><span class="sxs-lookup"><span data-stu-id="6c041-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="6c041-112">Todas as faturas do projeto criadas estão disponíveis na página **Fatura** na secção **Faturação** da área de **Vendas**.</span><span class="sxs-lookup"><span data-stu-id="6c041-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="6c041-113">Página de detalhes Contrato do Projeto</span><span class="sxs-lookup"><span data-stu-id="6c041-113">Project Contract details page</span></span>

<span data-ttu-id="6c041-114">Uma fatura pró-forma também pode ser criada a partir da página de detalhes **Contrato do Projeto**, que cria a fatura para esse contrato específico do projeto.</span><span class="sxs-lookup"><span data-stu-id="6c041-114">A proforma invoice can also be created from the **Project Contract** details page, which creates the invoice for that specific project contract.</span></span> <span data-ttu-id="6c041-115">O sistema verifica se o contrato de projeto tem uma tarefa pendente de **Pronto a Faturar** que esteja com data anterior à de hoje.</span><span class="sxs-lookup"><span data-stu-id="6c041-115">The system verifies that the project contract has a **Ready to Invoice** backlog that is dated before today's date.</span></span> <span data-ttu-id="6c041-116">A partir destes contratos, o sistema cria faturas pró-forma de rascunho com base no número de clientes em cada item de contrato.</span><span class="sxs-lookup"><span data-stu-id="6c041-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="6c041-117">Quando há uma única fatura pró-forma criada, a página **Fatura** abre.</span><span class="sxs-lookup"><span data-stu-id="6c041-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="6c041-118">Se houver várias faturas criadas para esse contrato de projeto, então a página da lista **Faturas** abre para mostrar todas as faturas criadas.</span><span class="sxs-lookup"><span data-stu-id="6c041-118">If there are multiple invoices created for that project contract, then the **Invoices** list page opens to show all of the created invoices.</span></span>
