---
title: Subsídios diários
description: Este tópico fornece informações sobre as regras de subsídio diário por dia que são utilizadas na gestão de Despesas.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 7d1c4ac7781cb711e2cc0d09606d422b4dd554f3
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082278"
---
# <a name="per-diems"></a><span data-ttu-id="e30f1-103">Subsídios diários</span><span class="sxs-lookup"><span data-stu-id="e30f1-103">Per diems</span></span>

<span data-ttu-id="e30f1-104">_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_</span><span class="sxs-lookup"><span data-stu-id="e30f1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="e30f1-105">Um subsídio diário é um subsídio que é pago a um trabalhador que viaja em trabalho.</span><span class="sxs-lookup"><span data-stu-id="e30f1-105">A per diem is an allowance that is paid to a worker who is traveling for work.</span></span> <span data-ttu-id="e30f1-106">Na Gestão de despesas, pode criar regras de subsídio diário para várias situações de viagem.</span><span class="sxs-lookup"><span data-stu-id="e30f1-106">In Expense management, you can create per diem rules for  various travel situations.</span></span> <span data-ttu-id="e30f1-107">As tarifas de subsídio diário podem basear-se na época do ano, na localização da viagem ou em ambas.</span><span class="sxs-lookup"><span data-stu-id="e30f1-107">Per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="e30f1-108">Ao criar uma regra de subsídio diário, pode especificar que uma percentagem da tarifa do subsídio diário será retida se um trabalhador receber refeições ou serviços gratuitos.</span><span class="sxs-lookup"><span data-stu-id="e30f1-108">When you create a per diem  rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="e30f1-109">Também pode definir um número mínimo e máximo de horas para as quais a tarifa do subsídio por dia pode aplicar-se à viagem de um trabalhador.</span><span class="sxs-lookup"><span data-stu-id="e30f1-109">You can also set a minimum and maximum number of hours that the per diem rate can apply to a worker's travel.</span></span>

## <a name="configuration"></a><span data-ttu-id="e30f1-110">Configuração</span><span class="sxs-lookup"><span data-stu-id="e30f1-110">Configuration</span></span> 

1. <span data-ttu-id="e30f1-111">Para adicionar localizações do subsídio por dia, vá para **Configurar** > **Cálculos e códigos** > **Localizações do subsídio diário**.</span><span class="sxs-lookup"><span data-stu-id="e30f1-111">To add per diem locations, go to **Set up** > **Calculations and codes** > **Per diem locations**.</span></span>
2. <span data-ttu-id="e30f1-112">Para cada uma das localizações acima adicionadas, selecione uma tarifa e moeda do subsídio por dia que sejam válidas entre uma data de início e fim específicas para despesas de hotel e refeições, entre outras.</span><span class="sxs-lookup"><span data-stu-id="e30f1-112">For each of the locations added above, select a per diem rate and currency that is valid between a specific start and end date for hotel, meals, and other expenses.</span></span> <span data-ttu-id="e30f1-113">As tarifas e a moeda do subsídio por dia são configuradas em **Configurar** > **Cálculos e códigos** > **Subsídios por dia**.</span><span class="sxs-lookup"><span data-stu-id="e30f1-113">Per diem rates and currencies are configured under **Set up** > **Calculations and codes** > **Per diems**.</span></span>
3. <span data-ttu-id="e30f1-114">Na página **Localizações do subsídio por dia** , configure os níveis de tarifas de subsídio diário.</span><span class="sxs-lookup"><span data-stu-id="e30f1-114">On the **Per diem locations** page, configure per diem rate tiers.</span></span> <span data-ttu-id="e30f1-115">Os níveis de tarifas do subsídio diário permitem definir a divisão percentual de um subsídio diário para despesas de hotel e refeições, entre outras.</span><span class="sxs-lookup"><span data-stu-id="e30f1-115">Per diem rate tiers allow you to define the percentage split of a daily allowance for hotel, meal, and other expenses.</span></span> 
4. <span data-ttu-id="e30f1-116">Para especificar a redução percentual de refeição para pequeno-almoço, almoço ou jantar, atualize os campos na página **Parâmetros de gestão de despesas** no separador **Subsídio diário**.</span><span class="sxs-lookup"><span data-stu-id="e30f1-116">To specify the meal percentage reduction for breakfast, lunch, or dinner, update the fields on the **Expense management parameters** page on the **Per diem** tab.</span></span> 
    
## <a name="submit-expenses-using-per-diem"></a><span data-ttu-id="e30f1-117">Submeter despesas através do subsídio diário</span><span class="sxs-lookup"><span data-stu-id="e30f1-117">Submit expenses using per diem</span></span>
<span data-ttu-id="e30f1-118">Para submeter despesas através do subsídio diário, utilize a categoria de despesa **Subsídio diário** quando criar um relatório de despesas.</span><span class="sxs-lookup"><span data-stu-id="e30f1-118">To submit expenses utilizing per diems, use the **Per diem** expense category when you create an expense report.</span></span> <span data-ttu-id="e30f1-119">Introduza a **Data de início do subsídio diário** , **Data de fim do subsídio diário** e a **Localização do subsídio diário**.</span><span class="sxs-lookup"><span data-stu-id="e30f1-119">Enter the **Per diem from date** , **Per diem to date** ,  and the **Per diem location**.</span></span> <span data-ttu-id="e30f1-120">O montante será calculado com base nas tarifas do subsídio diário para a localização selecionada. A redução de refeições será calculada com base nos níveis de tarifas do subsídio diário.</span><span class="sxs-lookup"><span data-stu-id="e30f1-120">The amount will be calculated based on the per diem rates for the selected location and meal reduction will be calculated based on the per diem rate tiers.</span></span>
