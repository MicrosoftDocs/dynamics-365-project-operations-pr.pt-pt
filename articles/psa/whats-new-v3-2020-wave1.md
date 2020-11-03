---
title: Novidades ou alterações no Project Service Automation versão 3.x, vaga 1 de 2020
description: Este tópico inclui informações sobre o que há de novo e o que foi alterado no Project Service Automation versão 3, vaga 1 de 2020.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 16b51995f863d9ee54172625dacbf081c51c8556
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082350"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="10dc2-103">Novidades ou alterações no Project Service Automation versão 3, vaga 1 de 2020</span><span class="sxs-lookup"><span data-stu-id="10dc2-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>
<span data-ttu-id="10dc2-104">O tópico realça as principais considerações de atualização quando migrar para a versão mais recente do Project Service Automation (PSA) versão 3.x, vaga 1 de 2020.</span><span class="sxs-lookup"><span data-stu-id="10dc2-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="10dc2-105">Entrada de tempo</span><span class="sxs-lookup"><span data-stu-id="10dc2-105">Time entry</span></span>
<span data-ttu-id="10dc2-106">A experiência de entrada de tempo foi prorrogada para fornecer capacidades para expandir a introdução de tempo a mais cenários de clientes.</span><span class="sxs-lookup"><span data-stu-id="10dc2-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="10dc2-107">Isto inclui a capacidade de adicionar tipos de entrada, que agora direcionam o comportamento específico com base no nome do esquema do campo **Definições de entrada de tempo** , apresentado como **Origem da Hora**.</span><span class="sxs-lookup"><span data-stu-id="10dc2-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings** , displayed as **Time Source**.</span></span> <span data-ttu-id="10dc2-108">Foi adicionada uma nova solução, chamada Tempo, Despesa, Estados e Aprovações (TESA) para suportar esta funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="10dc2-108">A new solution, called Time, Expense, Statusing, and Approvals (TESA) has been added to support this functionality.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="10dc2-109">Considerações sobre a atualização</span><span class="sxs-lookup"><span data-stu-id="10dc2-109">Upgrade consideration</span></span>
<span data-ttu-id="10dc2-110">Para suportar esta funcionalidade, as funções existentes no PSA foram atualizadas para incluir novos privilégios.</span><span class="sxs-lookup"><span data-stu-id="10dc2-110">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="10dc2-111">Estes privilégios concedem acesso de leitura à nova entidade **Definições de Entrada de Hora**.</span><span class="sxs-lookup"><span data-stu-id="10dc2-111">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="10dc2-112">Os utilizadores que necessitam da capacidade de registar a hora devem receber a função de utilizador **Utilizador de Entrada de Tempo** , para além das funções existentes.</span><span class="sxs-lookup"><span data-stu-id="10dc2-112">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="10dc2-113">Esta função inclui a nova funcionalidade e assegura que a entrada de tempo continuará a funcionar.</span><span class="sxs-lookup"><span data-stu-id="10dc2-113">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

<span data-ttu-id="10dc2-114">Além disso, se tiver algum módulo de aplicação personalizado que inclua todos os formulários para a entidade de entrada de tempo, será necessário remover o **Formulário de Criação Rápida de Entrada de Tempo TESA** do módulo.</span><span class="sxs-lookup"><span data-stu-id="10dc2-114">Additionally, if you have any custom app modules that include all forms for the time entry entity, you will be required to remove the **TESA time Entry Quick Create Form** from the module.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="10dc2-115">Alterações a entradas de tempo expandidas atualmente</span><span class="sxs-lookup"><span data-stu-id="10dc2-115">Currently extended time entry changes</span></span>
<span data-ttu-id="10dc2-116">Para minimizar o impacto sobre os utilizadores atuais da entrada de tempo, esta alteração de função é a única exigência básica necessária para continuar a utilizar a entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="10dc2-116">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="10dc2-117">Se tiver criado vistas personalizadas ou experiências de entrada de tempo separadas, tem de definir os campos **Definição de Entrada de Tempo** para o valor correto do PSA.</span><span class="sxs-lookup"><span data-stu-id="10dc2-117">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>
