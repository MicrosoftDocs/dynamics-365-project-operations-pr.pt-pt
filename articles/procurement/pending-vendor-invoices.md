---
title: Comprar materiais não armazenados utilizando uma fatura pendente do fornecedor
description: Este tópico explica como registar faturas pendentes do fornecedor.
author: sigitac
manager: tfehr
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7a706f419443dcdf92ce3b247d719943272907d0
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880674"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a><span data-ttu-id="8027c-103">Comprar materiais não armazenados utilizando uma fatura pendente do fornecedor</span><span class="sxs-lookup"><span data-stu-id="8027c-103">Purchase non-stocked materials using a pending vendor invoice</span></span>

<span data-ttu-id="8027c-104">_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_</span><span class="sxs-lookup"><span data-stu-id="8027c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="8027c-105">À medida que uma empresa adquire materiais não armazenados para um projeto, os custos podem ser imediatamente registados contra o projeto.</span><span class="sxs-lookup"><span data-stu-id="8027c-105">As a company procures non-stocked materials for a project, the costs can be immediately recorded against the project.</span></span> 

<span data-ttu-id="8027c-106">Por exemplo, a Contoso Robotics US está a realizar um projeto de renovação de equipamentos e precisa de licenças de software.</span><span class="sxs-lookup"><span data-stu-id="8027c-106">For example, Contoso Robotics US is performing an equipment renewal project and needs software licenses.</span></span> <span data-ttu-id="8027c-107">Estas licenças são obtidas a partir de um fornecedor terceiro.</span><span class="sxs-lookup"><span data-stu-id="8027c-107">These licenses are procured from a third-party vendor.</span></span>  <span data-ttu-id="8027c-108">Utilizando Dynamics 365 Finance, o escriturário das Contas a pagar regista um documento de fatura do fornecedor pendente e atribui os custos da licença diretamente contra o projeto de renovação do equipamento.</span><span class="sxs-lookup"><span data-stu-id="8027c-108">Using Dynamics 365 Finance, the Accounts payable clerk records a pending vendor invoice document and attributes the license costs directly against the equipment renewal project.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="8027c-109">Antes de utilizar a funcionalidade descrita neste tópico, reveja e aplique as configurações necessárias.</span><span class="sxs-lookup"><span data-stu-id="8027c-109">Before you use the functionality described in this topic, review and apply the required configurations.</span></span> <span data-ttu-id="8027c-110">Para obter mais informações, consulte [Ativar materiais não armazenados e faturas pendentes do fornecedor](configure-materials-nonstocked.md).</span><span class="sxs-lookup"><span data-stu-id="8027c-110">For more information, see [Enable non-stocked materials and pending vendor invoices](configure-materials-nonstocked.md).</span></span> 

## <a name="post-a-project-related-pending-vendor-invoice"></a><span data-ttu-id="8027c-111">Publicar uma fatura pendente do fornecedor relacionada com o projeto</span><span class="sxs-lookup"><span data-stu-id="8027c-111">Post a project-related pending vendor invoice</span></span> 

<span data-ttu-id="8027c-112">As faturas pendentes do fornecedor podem ser registadas na página de **faturas pendentes do fornecedor** (**Contas a pagar** > **Faturas** > **Pendentes do fornecedor**).</span><span class="sxs-lookup"><span data-stu-id="8027c-112">Pending vendor invoices can be recorded on the **Pending vendor invoices** page (**Accounts payable** > **Invoices** > **Pending vendor invoices**).</span></span> <span data-ttu-id="8027c-113">Complete os seguintes passos para publicar uma fatura pendente do fornecedor relacionada com o projeto:</span><span class="sxs-lookup"><span data-stu-id="8027c-113">Complete the following steps to post a project-related pending vendor invoice:</span></span>

1. <span data-ttu-id="8027c-114">Vá a **Contas a pagar** > **Faturas** e selecione **Nova**.</span><span class="sxs-lookup"><span data-stu-id="8027c-114">Go to **Accounts payable** > **Invoices** and select **New**.</span></span> 
2. <span data-ttu-id="8027c-115">No campo **Conta da fatura**, selecione um fornecedor e no campo **Número**, introduza a identificação da fatura do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="8027c-115">In the **Invoice account** field, select a vendor and in the **Number** field, enter the vendor invoice identification.</span></span>
3. <span data-ttu-id="8027c-116">Adicione uma linha à fatura do fornecedor e no campo **número do artigo**, selecione o artigo não armazenado comprado ao fornecedor.</span><span class="sxs-lookup"><span data-stu-id="8027c-116">Add a line to the vendor invoice and in the **Item number** field, select the non-stocked item purchased from the vendor.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="8027c-117">As linhas de fatura do fornecedor que se baseiam numa categoria de compras não podem ser registadas contra o projeto.</span><span class="sxs-lookup"><span data-stu-id="8027c-117">Vendor invoice lines that are based on a procurement category can't be recorded against the project.</span></span> 
    
5. <span data-ttu-id="8027c-118">Adicionar a quantidade comprada.</span><span class="sxs-lookup"><span data-stu-id="8027c-118">Add the quantity purchased.</span></span> <span data-ttu-id="8027c-119">O sistema preencherá o preço unitário com base na configuração do preço do artigo não armazenado.</span><span class="sxs-lookup"><span data-stu-id="8027c-119">The system will populate the unit price based on the non-stocked item price configuration.</span></span> 
6. <span data-ttu-id="8027c-120">Verifique o valor total e outros detalhes obrigatórios na linha.</span><span class="sxs-lookup"><span data-stu-id="8027c-120">Verify the total amount and other required details on the line.</span></span>
7. <span data-ttu-id="8027c-121">Nos detalhes da linha, no separador **Projeto**, selecione o ID do projeto para o quais este artigo será gravado.</span><span class="sxs-lookup"><span data-stu-id="8027c-121">On the line details, on the **Project** tab, select the ID of the project that this item will be recorded to.</span></span>
8. <span data-ttu-id="8027c-122">Opcionalmente, selecione o número de atividade e atualize a categoria de projeto e propriedade de linha.</span><span class="sxs-lookup"><span data-stu-id="8027c-122">Optionally, select the activity number, and update the project category and line property.</span></span>
9. <span data-ttu-id="8027c-123">Publique a fatura pendente do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="8027c-123">Post pending vendor invoice.</span></span> <span data-ttu-id="8027c-124">Quando a fatura é publicada, o sistema regista:</span><span class="sxs-lookup"><span data-stu-id="8027c-124">When the invoice is posted, the system records:</span></span>
    
    - <span data-ttu-id="8027c-125">O valor do saldo do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="8027c-125">The vendor balance amount.</span></span>
    - <span data-ttu-id="8027c-126">O valor do imposto sobre vendas.</span><span class="sxs-lookup"><span data-stu-id="8027c-126">The sales tax amount.</span></span>
    - <span data-ttu-id="8027c-127">O custo contra o projeto é registado na conta de integração de contratos públicos.</span><span class="sxs-lookup"><span data-stu-id="8027c-127">The cost against the project is recorded to the procurement integration account.</span></span>
    - <span data-ttu-id="8027c-128">A transação real do projeto em Dataverse.</span><span class="sxs-lookup"><span data-stu-id="8027c-128">The project actual transaction in Dataverse.</span></span> <span data-ttu-id="8027c-129">Esta transação é ainda processada através do [diário de Integração do Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="8027c-129">This transaction is further processed using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="8027c-130">A publicação deste diário transfere o montante da conta de integração de aquisições para a conta de custos do projeto.</span><span class="sxs-lookup"><span data-stu-id="8027c-130">Posting this journal moves the amount from the procurement integration account to the project cost account.</span></span>
