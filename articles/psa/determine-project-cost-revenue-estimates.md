---
title: Determinar estimativas de receitas e custo do projeto
description: Como determinar estimativas de receitas e custo do projeto no Project Service
author: ruhercul
manager: kfend
ms.prod: ''
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a91e988632d2b2cdebfe7fd17516c5d6886728fc
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148837"
---
# <a name="determine-project-cost-and-revenue-estimates"></a>Determinar estimativas de receitas e custo do projeto 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

As estimativas do projeto fornecem a vista financeira do trabalho estimado e agendado na estrutura hierárquica do trabalho. A vista de estimativas informa-o sobre o impacto das receitas e do custo do trabalho planeado. A vista de estimativas fornece uma ferramenta para ver as informações sobre várias dimensões predefinidas para melhor o informar sobre o impacto financeiro do projeto.  
  
## <a name="cost-and-sales-value-of-the-project"></a>Valor das vendas e do custo do projeto  
As listas de preços do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] definem o custo e as taxas de faturação para as funções dos projetos utilizarem. Com base nas funções associadas às tarefas na estrutura hierárquica do trabalho do projeto, poderá determinar o impacto do custo e das receitas do trabalho envolvido.  
  
## <a name="cost-price-defaulting"></a>Assumir o valor predefinido do preço de custo  
Cada projeto pertence a uma organização (indicada em **Unidade Proprietária** no projeto.) A lista de preços associada à unidade organizacional proprietária determina o preço de custo unitário. As capacidades do [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] determinam os preços de custo das funções ao procurarem a combinação de função, a unidade e a unidade organizacional na lista de preços de custo para obter o preço de custo correto para a data efetiva nas linhas de estimativa.  
  
Se a combinação de função, unidade e unidade organizacional não resultarem num preço de custo da lista de preços da unidade proprietária, a unidade é ignorada a favor da combinação de função e unidade organizacional. Se existir um preço de custo, este preço é convertido para a unidade escolhida na linha de estimativa.  
  
Se a combinação de função e unidade organizacional não resultar num preço de custo, a unidade organizacional é ignorada a favor da combinação de função e unidade, e o preço é assumido por predefinição após aplicação de qualquer conversão, se for necessário.  
  
 Se não existir um preços para a função, o preço de custo assume por predefinição 0,00 na linha de estimativa.  
  
 Todas os montantes de custo nas linhas de estimativa de custos estão na moeda da unidade organizacional proprietária.  
  
## <a name="sales-price-defaulting"></a>Assumir o valor predefinido do preço venda  
A lista de preços de venda baseia-se na entidade de vendas a que o projeto está anexado. A lista de preços de venda associada à proposta ou ao contrato determina o preço de venda unitário. Se a proposta ou o contrato tiver uma lista de preços personalizada, será a lista de preços de venda predefinida para as estimativas do projeto. Se não existir uma associação às entidades de venda, a lista de preços de venda predefinida nas definições dos parâmetros será a lista de preços de venda predefinida do projeto. Cada linha de estimativa tem uma unidade organizacional do recurso associada para indicar a unidade organizacional a partir da qual os recursos serão reservados para concluir a tarefa. O preço de venda para as funções associadas é determinado ao procurar a combinação de função, unidade e unidade organizacional do recurso na lista de preços de venda para obter o preço de venda correto para a data efetiva nas linhas de estimativa.  
  
Se a combinação de função, unidade e unidade organizacional do recurso não resultar num preço de venda a partir da lista de preços de venda, o sistema irá ignorar a unidade e procurar a combinação de função e unidade organizacional do recurso. Se o preço de venda for encontrado, irá ser convertido para a unidade escolhida na linha de estimativa de venda.  
  
Se o sistema não encontrar o preço para a função, o preço de venda tem de assumir por predefinição 0,00 na linha de estimativa.  
  
A vista de estimativas tem uma vista de grelha que apresenta uma grelha simples de linhas de estimativa com a unidade e o custo total, e o preço de venda.  
  
## <a name="time-phased-view-of-project-estimates"></a>Vista faseada no tempo das estimativas do projeto  
Na vista faseada no tempo para as estimativas do projeto, os dados das estimativas da vista de grelha são articulados por predefinição por função e mostra a propagação dos dados de estimativa ao longo da linha cronológica na escala temporal.  
  
## <a name="effort-estimate-allocation-based-on-task-mode"></a>Alocação de estimativas de esforço baseada no modo de tarefa  
Na vista faseada no tempo, a estimativa de esforço total para a tarefa é distribuída através da alocação de determinado número de horas de esforço por período de tempo unitário da escala temporal escolhida. No Project Service, o modo de tarefa determina a forma como o esforço é alocado ao longo da duração da tarefa. Os dois tipos de alocação são alocação uniforme e alocação baseada nas horas de trabalho. 
  
## <a name="work-hours-based-allocation"></a>Alocação baseada nas horas de trabalho  
O modo de tarefa de agendamento automático para uma tarefa regula o facto de, para o número de recursos estimado na tarefa, serem estimados para serem utilizados durante as horas de trabalho completas por dia. Isto aplica-se ao alocar o esforço dividindo-o ao longo da duração das tarefas, também na vista faseada no tempo. Por exemplo, numa escala temporal ‘Dia’, como uma tarefa estimada para ser concluída por um recurso, o esforço alocado por dia não excederá as horas de trabalho por dia definidas no calendário do projeto. Consequentemente, a alocação do esforço assegura sempre que os recursos têm uma estimativa de utilização durante todo o dia.  
  
## <a name="even-distribution"></a>Distribuição uniforme  
O modo de tarefa agendada manualmente não cumpre as horas de trabalho, o calendário do projeto ou o número de recursos definido na tarefa. A agenda da tarefa baseia-se na intervenção do utilizador. Para estas tarefas, a alocação do esforço por período de tempo unitário da escala temporal escolhida não tem quaisquer fatores de limitação. O esforço total na tarefa é dividido e alocado equitativamente para cada período de tempo unitário na escala temporal escolhida.  
  
Desta forma, o modo de tarefa definido na tarefa determina a distribuição do esforço ou a alocação do esforço por período de tempo unitário nas estimativas faseadas no tempo.  
  
## <a name="grouping-and-time-phasing-options"></a>Opções de agrupamento e faseamento no tempo  
Esta vista ajuda a compreender a distribuição do esforço, do custo e das estimativas de venda baseadas no dia, semana, mês ou ano. A opção Agrupar Por permite articular os dados das estimativas em duas outras dimensões: categoria e recurso. Na vista de grelha e na vista faseada no tempo, poderá escolher os campos a apresentar. Os totais para cada um bloco de tempo são apresentados na parte inferior a indicar o total estimado do esforço, custo e vendas do dia, semana, mês ou ano.  
  
O preço de custo e o preço de venda predefinidos são efetivos para a data. Quando as taxas para as funções são alteradas, será mais transparente na vista faseada no tempo, durante a visualização dos dados de estimativa articulados no ‘Recurso’ e faseados no tempo por semana.  
  
## <a name="expense-estimates"></a>Estimativas de despesas  
Qualquer despesa que for incorrida no projeto que não esteja relacionada diretamente com o trabalho a efetuar pode ser registada nas estimativas do projeto na vista de grelha. Poderá fazê-lo através da opção **Adicionar estimativa de venda** na vista de grelha. As estimativas de despesas podem ser registadas para uma tarefa específica ou para todo o projeto. Pode escolher categorias de despesas nestas linhas e escolher uma data provisória quando se espera que se incorra na despesa. Se o custo e a lista de preços de venda associados tiverem preços predefinidos, ou percentagens de margem de lucro definidas para as categorias de despesa, será assumido o valor por omissão na linha de estimativa ao efetuar a associação.  
  
### <a name="see-also"></a>Consulte Também  
 [Guia do Gestor de Projeto](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]