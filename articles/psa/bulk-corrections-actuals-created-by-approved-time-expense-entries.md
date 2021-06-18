---
title: Correções em massa dos valores reais criados pelas entradas de tempo e despesa aprovadas
description: Este tópico explica como um administrador pode fazer correções individuais ou em massa às entradas de tempo ou despesa aprovadas anteriormente se a faturação não for concluída.
author: rumant
ms.date: 04/02/2020
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: c6d849e4be9e3687396cd6a0c4158d92f25c7879
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012060"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a><span data-ttu-id="36fe8-103">Correções em massa dos valores reais criados pelas entradas de tempo e despesa aprovadas</span><span class="sxs-lookup"><span data-stu-id="36fe8-103">Bulk corrections of actuals created by approved time and expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="36fe8-104">Ocasionalmente, uma entrada de hora ou despesa pode ser introduzida incorretamente.</span><span class="sxs-lookup"><span data-stu-id="36fe8-104">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="36fe8-105">Por exemplo, um consultor pode selecionar a data errada ao criar uma entrada de hora ou transpor os números ao introduzir uma despesa.</span><span class="sxs-lookup"><span data-stu-id="36fe8-105">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="36fe8-106">Se um consultor não conseguir efetuar as atualizações às entradas submetidas, um administrador pode corrigir diretamente a entrada para um projeto.</span><span class="sxs-lookup"><span data-stu-id="36fe8-106">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="36fe8-107">Para concluir os procedimentos neste tópico, precisará de permissões de Administrador.</span><span class="sxs-lookup"><span data-stu-id="36fe8-107">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="36fe8-108">Corrigir entradas de tempo aprovadas</span><span class="sxs-lookup"><span data-stu-id="36fe8-108">Correct approved time entries</span></span>     

<span data-ttu-id="36fe8-109">Conclua os passos seguintes para corrigir entradas individuais ou múltiplas para um projeto.</span><span class="sxs-lookup"><span data-stu-id="36fe8-109">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="36fe8-110">Na área **Vendas**, selecione **Transações** e selecione **Tempo Aprovado**.</span><span class="sxs-lookup"><span data-stu-id="36fe8-110">In the **Sales** area, select **Transactions**, and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="36fe8-111">Na lista **Tempo Aprovado**, localize e selecione uma ou mais entradas de tempo aprovadas para correção.</span><span class="sxs-lookup"><span data-stu-id="36fe8-111">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="36fe8-112">Pode utilizar o filtro para localizar as entradas relacionadas.</span><span class="sxs-lookup"><span data-stu-id="36fe8-112">You can use the filter to locate related entries.</span></span> <span data-ttu-id="36fe8-113">Por exemplo, poderá filtrar por um ID de projeto e selecionar todas as entradas de tempo aprovadas com esse ID de projeto.</span><span class="sxs-lookup"><span data-stu-id="36fe8-113">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="36fe8-114">Selecione **Entradas corretas**.</span><span class="sxs-lookup"><span data-stu-id="36fe8-114">Select **Correct entries**.</span></span> <span data-ttu-id="36fe8-115">É criado automaticamente um novo diário de correções, com o tipo atribuído de **Correção de Hora**.</span><span class="sxs-lookup"><span data-stu-id="36fe8-115">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="36fe8-116">As entradas selecionadas são adicionadas ao diário.</span><span class="sxs-lookup"><span data-stu-id="36fe8-116">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="36fe8-117">Na página **Novo Diário**, introduza uma **Descrição** para o diário de correções e selecione o separador **Correções de Entrada de Hora**.</span><span class="sxs-lookup"><span data-stu-id="36fe8-117">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  
5. <span data-ttu-id="36fe8-118">Na secção **Novos Valores para Entradas de Hora**, atualize os campos com as informações corretas, conforme seja necessário.</span><span class="sxs-lookup"><span data-stu-id="36fe8-118">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="36fe8-119">Por exemplo, poderá alterar o projeto atribuído ou o recurso reservável.</span><span class="sxs-lookup"><span data-stu-id="36fe8-119">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="36fe8-120">Selecione **Pré-visualizar**.</span><span class="sxs-lookup"><span data-stu-id="36fe8-120">Select **Preview**.</span></span> <span data-ttu-id="36fe8-121">Na caixa de diálogo, selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="36fe8-121">In the dialog box, select **OK**.</span></span> <span data-ttu-id="36fe8-122">No separador **Linhas do diário**, pode ver uma lista dos valores reais originais que estão relacionados com as entradas de tempo selecionadas que foram revertidas e as linhas correspondentes corrigidas que foram criadas.</span><span class="sxs-lookup"><span data-stu-id="36fe8-122">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="36fe8-123">Se forem necessárias correções adicionais, repita os passos 5 e 6.</span><span class="sxs-lookup"><span data-stu-id="36fe8-123">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="36fe8-124">Todos os valores reais corrigidos terão os mesmos valores selecionados na secção **Novos Valores para Entradas de Hora**.</span><span class="sxs-lookup"><span data-stu-id="36fe8-124">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="36fe8-125">Se as correções aparecerem conforme esperado, selecione **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="36fe8-125">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="36fe8-126">Na caixa de diálogo, selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="36fe8-126">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="36fe8-127">Regresse à área **Vendas**, selecione **Projetos** e, em seguida, abra o projeto para o qual acabou de atualizar as entradas de hora.</span><span class="sxs-lookup"><span data-stu-id="36fe8-127">Return to the **Sales** area, select **Projects**, and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="36fe8-128">Na página **Projetos**, no separador **Valores Reais**, veja as alterações que efetuou.</span><span class="sxs-lookup"><span data-stu-id="36fe8-128">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="36fe8-129">Se o separador **Valores Reais** não for visível, selecione **Relacionados** > **Valores Reais**.</span><span class="sxs-lookup"><span data-stu-id="36fe8-129">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="36fe8-130">Na lista **Vista Associada de Valor Real**, poderá ver que as entradas de tempo originais que foram revertidas continuam a ser listadas, tal como são as entradas de tempo corrigidas correspondentes.</span><span class="sxs-lookup"><span data-stu-id="36fe8-130">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="36fe8-131">Por exemplo, no gráfico seguinte existem dois itens com a quantidade de 8 com débitos listados na coluna Montante.</span><span class="sxs-lookup"><span data-stu-id="36fe8-131">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="36fe8-132">Além disso, existem dois itens com a quantidade -8 que mostram montantes creditados na coluna Montante.</span><span class="sxs-lookup"><span data-stu-id="36fe8-132">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="36fe8-133">Estas correções repõem a quantidade para zero.</span><span class="sxs-lookup"><span data-stu-id="36fe8-133">These corrections bring the quantity to zero.</span></span>

![Lista de vistas associadas de valor real](https://github.com/MicrosoftDocs/dynamics-365-customer-engagement-pr/blob/bulk-corrections-actuals-created-by-approved-time-expense-entries.md/time-actuals.png)
 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="36fe8-135">Corrigir entradas de despesa aprovadas</span><span class="sxs-lookup"><span data-stu-id="36fe8-135">Correct approved expense entries</span></span>

<span data-ttu-id="36fe8-136">Conclua os seguintes passos para corrigir uma ou mais entradas de despesa.</span><span class="sxs-lookup"><span data-stu-id="36fe8-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="36fe8-137">Na área **Vendas**, no painel de navegação esquerdo, em **Transações**, selecione **Despesas Aprovadas**.</span><span class="sxs-lookup"><span data-stu-id="36fe8-137">In the **Sales** area, in the left navigation pane, under **Transactions**, select **Approved Expenses**.</span></span>

2. <span data-ttu-id="36fe8-138">Na lista **Despesas Aprovadas**, selecione o projeto que pretende corrigir e selecione **Entradas corretas**.</span><span class="sxs-lookup"><span data-stu-id="36fe8-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="36fe8-139">Será criado automaticamente um novo diário de correções, com o tipo atribuído de **Correção de Despesa**.</span><span class="sxs-lookup"><span data-stu-id="36fe8-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="36fe8-140">Na página **Novo Diário**, introduza uma **Descrição** para a correção e, no separador **Correção de Despesa**, na secção **Novos Valores para Despesas**, selecione os campos de dados que pretende corrigir para os itens de despesa selecionados.</span><span class="sxs-lookup"><span data-stu-id="36fe8-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="36fe8-141">Por exemplo, pode atribuir a despesa a outro **Projeto** ou corrigir a **Categoria de Despesa**, **Data da Despesa** ou **Recurso Reservável**.</span><span class="sxs-lookup"><span data-stu-id="36fe8-141">For example, you can assign the expense to another **Project**, or correct the **Expense Category**, **Expense Date**, or **Bookable Resource**.</span></span>

4. <span data-ttu-id="36fe8-142">Selecione **Pré-visualizar**.</span><span class="sxs-lookup"><span data-stu-id="36fe8-142">Select **Preview**.</span></span> <span data-ttu-id="36fe8-143">Na caixa de diálogo, selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="36fe8-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="36fe8-144">Verifique as correções no separador **Linhas do diário**. Pode ver uma lista dos valores reais originais que estão relacionados com as entradas de despesa selecionadas que foram revertidas e as linhas correspondentes corrigidas que foram criadas.</span><span class="sxs-lookup"><span data-stu-id="36fe8-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="36fe8-145">Se os valores corrigidos aparecerem conforme esperado, selecione **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="36fe8-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="36fe8-146">Na caixa de diálogo, selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="36fe8-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="36fe8-147">Se os valores não forem mostrados conforme esperado, selecione **Cancelar** para voltar à lista **Despesas Aprovadas**.</span><span class="sxs-lookup"><span data-stu-id="36fe8-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="36fe8-148">Repita os passos 2 a 5.</span><span class="sxs-lookup"><span data-stu-id="36fe8-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="36fe8-149">Os valores reais corrigidos terão os mesmos valores selecionados na secção **Novos Valores para Despesas**.</span><span class="sxs-lookup"><span data-stu-id="36fe8-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="36fe8-150">Depois de confirmar o diário de correção, volte ao projeto ou projetos atualizados para ver as alterações.</span><span class="sxs-lookup"><span data-stu-id="36fe8-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="36fe8-151">Na página do projeto, no separador **Valores Reais**, reveja a **Vista Associada de Valor Real**.</span><span class="sxs-lookup"><span data-stu-id="36fe8-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="36fe8-152">São listadas as entradas originais e as entradas corrigidas.</span><span class="sxs-lookup"><span data-stu-id="36fe8-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="36fe8-153">O gráfico seguinte mostra os montantes de entrada de despesa originais e os montantes de entrada de despesa corrigidos correspondentes.</span><span class="sxs-lookup"><span data-stu-id="36fe8-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 

![Valores reais de despesa](https://user-images.githubusercontent.com/60806505/77122219-4cd52900-69fa-11ea-8349-ccd2ffebf640.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]