---
title: Configurar gestão de despesas
description: Este artigo descreve as considerações e as decisões que deve tomar durante o processo de planeamento antes de configurar a gestão de Despesas no Microsoft Dynamics 365 Finance.
author: KimANelson
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 52538946c7260fad4076a64e8dc34fecf08b90cf
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005400"
---
# <a name="configure-expense-management"></a><span data-ttu-id="5edbe-103">Configurar gestão de despesas</span><span class="sxs-lookup"><span data-stu-id="5edbe-103">Configure expense management</span></span>

<span data-ttu-id="5edbe-104">Este tópico descreve as considerações e as decisões que deve tomar durante o processo de planeamento antes de configurar a gestão de Despesas.</span><span class="sxs-lookup"><span data-stu-id="5edbe-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management.</span></span> <span data-ttu-id="5edbe-105">Na gestão de Despesas, pode armazenar informações sobre métodos de pagamento, requisições de viagem, relatórios de despesas, políticas, e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="5edbe-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="5edbe-106">Porque muitas das decisões que toma quando planeia a sua configuração para a gestão de Despesas são baseadas na hierarquia e estrutura financeira da sua organização, deve consultar os documentos de planeamento dessas áreas.</span><span class="sxs-lookup"><span data-stu-id="5edbe-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="5edbe-107">Despesas entre empresas</span><span class="sxs-lookup"><span data-stu-id="5edbe-107">Intercompany expenses</span></span>

<span data-ttu-id="5edbe-108">Quando permite Despesas entre empresas, permite que entidades jurídicas e colaboradores incorram em despesas em nome de outra entidade legal, e cobrem o pagamento da entidade legal de trabalho dentro da sua organização.</span><span class="sxs-lookup"><span data-stu-id="5edbe-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="5edbe-109">Por exemplo, um colaborador na entidade legal A completa um projeto para a entidade legal B, e o projeto incorre em despesas relacionadas com viagens.</span><span class="sxs-lookup"><span data-stu-id="5edbe-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="5edbe-110">Se as Despesas entre empresas forem ativadas, o trabalhador pode então apresentar um relatório de despesas que irá registar a despesa para a entidade legal B, e as despesas devem então ser pagas pela entidade legal A. Se a sua organização não tem várias entidades jurídicas, não tem de ativar Despesas entre empresas.</span><span class="sxs-lookup"><span data-stu-id="5edbe-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="5edbe-111">**Decisão:** Deseja ativar Despesas entre empresas?</span><span class="sxs-lookup"><span data-stu-id="5edbe-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="5edbe-112">Gestão financeira</span><span class="sxs-lookup"><span data-stu-id="5edbe-112">Financial management</span></span>

<span data-ttu-id="5edbe-113">A gestão de despesas está fortemente integrada na gestão financeira da sua organização.</span><span class="sxs-lookup"><span data-stu-id="5edbe-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="5edbe-114">Muitas das suas configurações para a gestão de Despesas serão baseadas nas decisões que tomou sobre as finanças da sua organização.</span><span class="sxs-lookup"><span data-stu-id="5edbe-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="5edbe-115">As seguintes secções descrevem as várias áreas que requerem planeamento e decisões, com base nas decisões financeiras da sua organização e orientação da sua equipa de liderança.</span><span class="sxs-lookup"><span data-stu-id="5edbe-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="5edbe-116">Subsídios diários</span><span class="sxs-lookup"><span data-stu-id="5edbe-116">Per diems</span></span>

<span data-ttu-id="5edbe-117">Deve definir o funcionário por dias que a sua organização fornece.</span><span class="sxs-lookup"><span data-stu-id="5edbe-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="5edbe-118">Como os dias são normalmente usados para cobrir despesas como refeições, alojamento e outras despesas incidentais, pode criar regras para os subsídios por dia que a sua organização oferece.</span><span class="sxs-lookup"><span data-stu-id="5edbe-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="5edbe-119">as tarifas de subsídio diário podem basear-se na época do ano, na localização da viagem ou em ambas.</span><span class="sxs-lookup"><span data-stu-id="5edbe-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="5edbe-120">Ao definir uma regra de subsídio diário, pode especificar que uma percentagem da tarifa do subsídio diário será retida se um trabalhador receber refeições ou serviços gratuitos.</span><span class="sxs-lookup"><span data-stu-id="5edbe-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="5edbe-121">Também pode definir um níveis de tarifas diárias para definir o número mínimo e máximo de horas para as quais a tarifa do subsídio por dia pode ser aplicada à viagem de um trabalhador.</span><span class="sxs-lookup"><span data-stu-id="5edbe-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="5edbe-122">**Decisões:**</span><span class="sxs-lookup"><span data-stu-id="5edbe-122">**Decisions:**</span></span>

- <span data-ttu-id="5edbe-123">Regras diárias predefinidas para o primeiro e último dia:</span><span class="sxs-lookup"><span data-stu-id="5edbe-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="5edbe-124">Qual é o número mínimo de horas que um trabalhador pode solicitar por um dia e ainda receber um por dia?</span><span class="sxs-lookup"><span data-stu-id="5edbe-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="5edbe-125">Existe uma redução na quantidade que é oferecida para as refeições para o primeiro dia e último dia?</span><span class="sxs-lookup"><span data-stu-id="5edbe-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="5edbe-126">Se houver uma redução, qual é a percentagem da redução?</span><span class="sxs-lookup"><span data-stu-id="5edbe-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="5edbe-127">Existe uma redução na quantidade que é oferecida para um hotel para o primeiro dia e último dia?</span><span class="sxs-lookup"><span data-stu-id="5edbe-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="5edbe-128">Se houver uma redução, qual é a percentagem da redução?</span><span class="sxs-lookup"><span data-stu-id="5edbe-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="5edbe-129">Existe uma redução na quantidade que é oferecida para outras despesas incorridas no primeiro dia e último dia?</span><span class="sxs-lookup"><span data-stu-id="5edbe-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="5edbe-130">Se houver uma redução, qual é a percentagem da redução?</span><span class="sxs-lookup"><span data-stu-id="5edbe-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="5edbe-131">Regras por dia predefinidas:</span><span class="sxs-lookup"><span data-stu-id="5edbe-131">Default per diem rules:</span></span>

    - <span data-ttu-id="5edbe-132">Existe uma redução percentual do subsídio por dia por refeição se, por exemplo, a refeição for gratuita?</span><span class="sxs-lookup"><span data-stu-id="5edbe-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="5edbe-133">Se houver uma redução, qual é a percentagem da redução para cada refeição?</span><span class="sxs-lookup"><span data-stu-id="5edbe-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="5edbe-134">A redução da refeição é calculada por dia, por viagem ou pelo número de refeições por dia?</span><span class="sxs-lookup"><span data-stu-id="5edbe-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="5edbe-135">As quantidades por da devem ser arredondadas da forma regular ou arredondada?</span><span class="sxs-lookup"><span data-stu-id="5edbe-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="5edbe-136">Os diários são calculados num período de 24 horas ou num dia de calendário?</span><span class="sxs-lookup"><span data-stu-id="5edbe-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="5edbe-137">Regras por dia que são baseadas na localização:</span><span class="sxs-lookup"><span data-stu-id="5edbe-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="5edbe-138">As tarifas por dia variam de acordo com a localização?</span><span class="sxs-lookup"><span data-stu-id="5edbe-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="5edbe-139">Quais as localizações incluídas?</span><span class="sxs-lookup"><span data-stu-id="5edbe-139">What locations are included?</span></span>
    - <span data-ttu-id="5edbe-140">Se as tarifas por dia variarem em função da localização, para cada local, qual o montante percentual fornecido para os seguintes tipos de despesas:</span><span class="sxs-lookup"><span data-stu-id="5edbe-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="5edbe-141">Refeições</span><span class="sxs-lookup"><span data-stu-id="5edbe-141">Meals</span></span>
        - <span data-ttu-id="5edbe-142">Hotel</span><span class="sxs-lookup"><span data-stu-id="5edbe-142">Hotel</span></span>
        - <span data-ttu-id="5edbe-143">Outras despesas</span><span class="sxs-lookup"><span data-stu-id="5edbe-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="5edbe-144">Diários e contas de gestão de despesas</span><span class="sxs-lookup"><span data-stu-id="5edbe-144">Expense management journals and accounts</span></span>

<span data-ttu-id="5edbe-145">A gestão de despesas requer que utilize vários diários e contas.</span><span class="sxs-lookup"><span data-stu-id="5edbe-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="5edbe-146">Deve decidir, por exemplo, se a mesma conta é usada para adiantamentos de dinheiro e litígios com cartão de crédito.</span><span class="sxs-lookup"><span data-stu-id="5edbe-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="5edbe-147">**Decisões:**</span><span class="sxs-lookup"><span data-stu-id="5edbe-147">**Decisions:**</span></span>

- <span data-ttu-id="5edbe-148">Em que livro razão são publicados os relatórios de despesas aprovados?</span><span class="sxs-lookup"><span data-stu-id="5edbe-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="5edbe-149">Que conta é usada para adiantamentos de dinheiro?</span><span class="sxs-lookup"><span data-stu-id="5edbe-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="5edbe-150">Os adiantamentos em dinheiro devem ser publicados imediatamente?</span><span class="sxs-lookup"><span data-stu-id="5edbe-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="5edbe-151">Métodos de pagamento</span><span class="sxs-lookup"><span data-stu-id="5edbe-151">Payment methods</span></span>

<span data-ttu-id="5edbe-152">Quando permite que os colaboradores incorram em despesas em nome do seu negócio, tem de definir os métodos de pagamento que os colaboradores podem utilizar.</span><span class="sxs-lookup"><span data-stu-id="5edbe-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="5edbe-153">Por exemplo, pode permitir que os colaboradores utilizem dinheiro ou um cartão de crédito corporativo.</span><span class="sxs-lookup"><span data-stu-id="5edbe-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="5edbe-154">Também pode permitir que os colaboradores utilizem cartões de crédito pessoais e, em seguida, reembolsa os empregados.</span><span class="sxs-lookup"><span data-stu-id="5edbe-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="5edbe-155">Deve tomar as seguintes decisões por cada método de pagamento que permitir.</span><span class="sxs-lookup"><span data-stu-id="5edbe-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="5edbe-156">**Decisões:**</span><span class="sxs-lookup"><span data-stu-id="5edbe-156">**Decisions:**</span></span>

- <span data-ttu-id="5edbe-157">Que métodos de pagamento são permitidos?</span><span class="sxs-lookup"><span data-stu-id="5edbe-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="5edbe-158">Quem é o proprietário das despesas do método de pagamento?</span><span class="sxs-lookup"><span data-stu-id="5edbe-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="5edbe-159">Existe um tipo de conta compensada?</span><span class="sxs-lookup"><span data-stu-id="5edbe-159">Is there an offset account type?</span></span> <span data-ttu-id="5edbe-160">Se houver um tipo de conta de compensação, o que é?</span><span class="sxs-lookup"><span data-stu-id="5edbe-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="5edbe-161">Se houver um tipo de conta de compensação, o que é a conta?</span><span class="sxs-lookup"><span data-stu-id="5edbe-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="5edbe-162">Se o método de pagamento for um cartão de crédito, o método de pagamento deve ser utilizado apenas com transações importadas?</span><span class="sxs-lookup"><span data-stu-id="5edbe-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="5edbe-163">Categorias de despesas e categorias partilhadas</span><span class="sxs-lookup"><span data-stu-id="5edbe-163">Expense categories and shared categories</span></span>

<span data-ttu-id="5edbe-164">Quando os colaboradores criam um relatório de despesas, cada despesa que registam tem de ser associada a uma categoria de despesas.</span><span class="sxs-lookup"><span data-stu-id="5edbe-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="5edbe-165">As categorias de despesas são derivadas das categorias partilhadas que podem ser partilhadas pelas entidades legais na sua organização.</span><span class="sxs-lookup"><span data-stu-id="5edbe-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="5edbe-166">Estas categorias também podem ser partilhadas na gestão e contabilidade do Projeto, dependendo da forma como a sua organização é definida.</span><span class="sxs-lookup"><span data-stu-id="5edbe-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="5edbe-167">Com base na definição da sua organização e na orientação da equipa de implementação, tem de determinar se as categorias que são utilizadas na Gestão de despesas serão utilizadas apenas na gestão de Despesas ou se devem ser partilhadas entre a gestão do Projeto e a contabilidade e gestão de Despesas.</span><span class="sxs-lookup"><span data-stu-id="5edbe-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="5edbe-168">Note que estas categorias podem ser partilhadas entre a Gestão de projeto, e Despesas ou Projeto e Produção, mas não entre Despesas e Produção.</span><span class="sxs-lookup"><span data-stu-id="5edbe-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="5edbe-169">Deve tomar as seguintes decisões para cada categoria de despesas.</span><span class="sxs-lookup"><span data-stu-id="5edbe-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="5edbe-170">**Decisões:**</span><span class="sxs-lookup"><span data-stu-id="5edbe-170">**Decisions:**</span></span>

- <span data-ttu-id="5edbe-171">O que é uma categoria de despesa?</span><span class="sxs-lookup"><span data-stu-id="5edbe-171">What is the expense category?</span></span> <span data-ttu-id="5edbe-172">Os exemplos incluem categorias para voos, hotel ou quilometragem.</span><span class="sxs-lookup"><span data-stu-id="5edbe-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="5edbe-173">A categoria de despesa também pode ser utilizada na Gestão de projetos e contabilística?</span><span class="sxs-lookup"><span data-stu-id="5edbe-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="5edbe-174">O que é um tipo de despesa?</span><span class="sxs-lookup"><span data-stu-id="5edbe-174">What is the expense type?</span></span>
- <span data-ttu-id="5edbe-175">Qual o método de pagamento predefinido para a categoria de despesa?</span><span class="sxs-lookup"><span data-stu-id="5edbe-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="5edbe-176">As despesas na categoria de despesa têm de ser discriminadas?</span><span class="sxs-lookup"><span data-stu-id="5edbe-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="5edbe-177">Qual a conta predefinida principal para a categoria de despesa?</span><span class="sxs-lookup"><span data-stu-id="5edbe-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="5edbe-178">Qual o grupo de impostos sobre as vendas de artigos predefinido para a categoria de despesa?</span><span class="sxs-lookup"><span data-stu-id="5edbe-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="5edbe-179">São permitidos métodos de pagamento adicionais para a categoria de despesa?</span><span class="sxs-lookup"><span data-stu-id="5edbe-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="5edbe-180">Se forem permitidos métodos de pagamento adicionais, quais são?</span><span class="sxs-lookup"><span data-stu-id="5edbe-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="5edbe-181">Existem subcategorias nesta categoria de despesa?</span><span class="sxs-lookup"><span data-stu-id="5edbe-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="5edbe-182">Se existirem subcategorias, também tem de tomar as seguintes decisões:</span><span class="sxs-lookup"><span data-stu-id="5edbe-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="5edbe-183">Alguma das subcategorias está excluída da recuperação de impostos?</span><span class="sxs-lookup"><span data-stu-id="5edbe-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="5edbe-184">Qual o grupo impostos sobre vendas de artigos das subcategorias?</span><span class="sxs-lookup"><span data-stu-id="5edbe-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="5edbe-185">Se a categoria de despesas também for utilizada na gestão e contabilidade do Projeto, responda às restantes questões.</span><span class="sxs-lookup"><span data-stu-id="5edbe-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="5edbe-186">Caso contrário, passe para a próxima secção.</span><span class="sxs-lookup"><span data-stu-id="5edbe-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="5edbe-187">Que contas de custos serão utilizadas para as seguintes despesas?</span><span class="sxs-lookup"><span data-stu-id="5edbe-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="5edbe-188">Custo</span><span class="sxs-lookup"><span data-stu-id="5edbe-188">Cost</span></span>
    - <span data-ttu-id="5edbe-189">Alocação de vencimentos</span><span class="sxs-lookup"><span data-stu-id="5edbe-189">Payroll allocation</span></span>
    - <span data-ttu-id="5edbe-190">Valor do custo WIP</span><span class="sxs-lookup"><span data-stu-id="5edbe-190">WIP-cost value</span></span>
    - <span data-ttu-id="5edbe-191">Item de custo</span><span class="sxs-lookup"><span data-stu-id="5edbe-191">Cost-item</span></span>
    - <span data-ttu-id="5edbe-192">Item de valor de custo WIP</span><span class="sxs-lookup"><span data-stu-id="5edbe-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="5edbe-193">Perdas acumuladas</span><span class="sxs-lookup"><span data-stu-id="5edbe-193">Accrued loss</span></span>
    - <span data-ttu-id="5edbe-194">Perdas acumuladas WIP</span><span class="sxs-lookup"><span data-stu-id="5edbe-194">WIP-accrued loss</span></span>

- <span data-ttu-id="5edbe-195">Que contas de receitas serão utilizadas para o seguinte?</span><span class="sxs-lookup"><span data-stu-id="5edbe-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="5edbe-196">Receitas faturadas</span><span class="sxs-lookup"><span data-stu-id="5edbe-196">Invoiced revenue</span></span>
    - <span data-ttu-id="5edbe-197">Valor das vendas de receitas acumuladas</span><span class="sxs-lookup"><span data-stu-id="5edbe-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="5edbe-198">Valor de vendas WIP</span><span class="sxs-lookup"><span data-stu-id="5edbe-198">WIP-sales value</span></span>
    - <span data-ttu-id="5edbe-199">Produção de receitas acumuladas</span><span class="sxs-lookup"><span data-stu-id="5edbe-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="5edbe-200">Produção WIP</span><span class="sxs-lookup"><span data-stu-id="5edbe-200">WIP-production</span></span>
    - <span data-ttu-id="5edbe-201">Lucros de receitas acumuladas</span><span class="sxs-lookup"><span data-stu-id="5edbe-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="5edbe-202">Lucros WIP</span><span class="sxs-lookup"><span data-stu-id="5edbe-202">WIP-profit</span></span>
    - <span data-ttu-id="5edbe-203">Subscrição de receitas acumuladas</span><span class="sxs-lookup"><span data-stu-id="5edbe-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="5edbe-204">Subscrição WIP</span><span class="sxs-lookup"><span data-stu-id="5edbe-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="5edbe-205">Impostos</span><span class="sxs-lookup"><span data-stu-id="5edbe-205">Taxes</span></span>

<span data-ttu-id="5edbe-206">Para tarifas relacionadas com despesas, deve determinar o que está incluído ou ativado nos relatórios de despesas.</span><span class="sxs-lookup"><span data-stu-id="5edbe-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="5edbe-207">**Decisões:**</span><span class="sxs-lookup"><span data-stu-id="5edbe-207">**Decisions:**</span></span>

- <span data-ttu-id="5edbe-208">O imposto sobre as vendas está incluído nos montantes das despesas?</span><span class="sxs-lookup"><span data-stu-id="5edbe-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="5edbe-209">A recuperação de impostos deve ser ativada para as despesas?</span><span class="sxs-lookup"><span data-stu-id="5edbe-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="5edbe-210">Quando estava a planear o livro razão geral, se decidisse aplicar o imposto de vendas dos EUA e usar as regras fiscais, não pode ativar a recuperação de impostos nas despesas.</span><span class="sxs-lookup"><span data-stu-id="5edbe-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="5edbe-211">(Para aplicar o imposto sobre vendas dos EUA e usar as regras fiscais, defina a opção **Aplicar impostos sobre vendas** como **Sim**.)</span><span class="sxs-lookup"><span data-stu-id="5edbe-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="5edbe-212">Políticas</span><span class="sxs-lookup"><span data-stu-id="5edbe-212">Policies</span></span>

<span data-ttu-id="5edbe-213">Ao criar políticas de relatório de despesas, pode ajudar a sua organização a economizar tempo e dinheiro quando os colaboradores incorrerem em despesas em seu nome.</span><span class="sxs-lookup"><span data-stu-id="5edbe-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="5edbe-214">As políticas ajudam a garantir que os colaboradores permaneçam no orçamento, forneçam todas as informações necessárias e gastem dinheiro apenas quando assim o exigirem.</span><span class="sxs-lookup"><span data-stu-id="5edbe-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="5edbe-215">Deve tomar as seguintes decisões para cada política de relatório de despesas e cada política de aprovação de relatório de despesas que criar.</span><span class="sxs-lookup"><span data-stu-id="5edbe-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="5edbe-216">**Decisões:**</span><span class="sxs-lookup"><span data-stu-id="5edbe-216">**Decisions:**</span></span>

- <span data-ttu-id="5edbe-217">O que é o nome da política?</span><span class="sxs-lookup"><span data-stu-id="5edbe-217">What is the name of the policy?</span></span>
- <span data-ttu-id="5edbe-218">Para que serve a política de despesas?</span><span class="sxs-lookup"><span data-stu-id="5edbe-218">What is the expense policy for?</span></span>
- <span data-ttu-id="5edbe-219">Se já decidiu ativar Despesas entre empresas, a que empresas da sua organização se aplicará esta política?</span><span class="sxs-lookup"><span data-stu-id="5edbe-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="5edbe-220">Quando é que a política entra em vigor?</span><span class="sxs-lookup"><span data-stu-id="5edbe-220">When does the policy become effective?</span></span>
- <span data-ttu-id="5edbe-221">Quando expira a política?</span><span class="sxs-lookup"><span data-stu-id="5edbe-221">When does the policy expire?</span></span>
- <span data-ttu-id="5edbe-222">Qual é a regra da política?</span><span class="sxs-lookup"><span data-stu-id="5edbe-222">What is the policy rule?</span></span>
- <span data-ttu-id="5edbe-223">O que é o resultado da regra da política?</span><span class="sxs-lookup"><span data-stu-id="5edbe-223">What is the outcome of the policy rule?</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]