---
title: Considerações de atualização - versão 2.x ou 1.x para a versão 3 do Microsoft Dynamics 365 Project Service Automation
description: Este tópico descreve informações sobre as considerações que deve fazer ao atualizar da versão 2.x ou 1.x para a versão 3 do Project Service Automation.
manager: kfend
ms.prod: ''
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/13/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: ff0777705c6d0e2c0d8aa4ed191f4ae6b1786100
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281672"
---
# <a name="upgrade-considerations---psa-version-2x-or-1x-to-version-3"></a>Considerações sobre atualização - PSA versão 2.x ou 1.x para a versão 3

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="project-service-automation-and-field-service"></a>Project Service Automation e Field Service
Ambos o Dynamics 365 Project Service Automation e o Dynamics 365 Field Service utilizam a solução Universal Resourcing Scheduling (URS) para agendamento de recursos. Se tiver o Project Service Automation e o Field Service na sua instância, atualize ambas as soluções para a versão mais recente. Para o Project Service Automation, essa é a versão 3.x. Para o Field Service, é a versão 8.x. A atualização do Project Service Automation ou do Field Service instalará a versão mais recente do URS. Se tanto as soluções do Project Service Automation e do Field Service, na mesma instância, não forem atualizadas para a versão mais recente, pode haver algum comportamento inconsistente.

## <a name="resource-assignments"></a>Atribuições de recursos
No Project Service Automation versão 2 e versão 1, as atribuições de tarefas eram armazenadas como tarefas subordinadas (também chamadas de tarefas de linha) na **entidade Tarefa** e eram indiretamente relacionadas com a entidade **Atribuição de Recurso**. A tarefa de linha ficava visível na janela pop-up de atribuição da WBS (Estrutura Hierárquica do Trabalho).

![Tarefas de linha no WBS no Project Service Automation versão 2 e a versão 1](media/upgrade-line-task-01.png)

Na versão 3 do Project Service Automation, o esquema subjacente de atribuição de recursos reserváveis às tarefas foi alterado. A tarefa de linha foi preterida e há uma relação 1:1 direta entre a tarefa na **entidade Tarefa** e o membro da equipa na entidade **Atribuição de Recurso**. As tarefas atribuídas a um membro da equipa do projeto agora são armazenadas diretamente na entidade Atribuição de Recurso.  

Estas alterações causam impacto na atualização dos projetos existentes que possuem atribuições de recursos para recursos reserváveis nomeados e recursos genéricos numa equipa do projeto. Este tópico descreve as considerações que deve fazer em relação aos projetos ao atualizar para a versão 3. 

### <a name="tasks-assigned-to-named-resources"></a>Tarefas atribuídas a recursos nomeados
Ao utilizar a entidade de tarefa subjacente, as tarefas na versão 2 e na versão 1 permitem que os membros da equipa desempenhem uma função diferente das suas funções predefinidas. Por exemplo, Catalina Araújo, que recebeu, por predefinição, a função de Gestor do Programa, pode receber a atribuição de uma tarefa com a função de Programador. Na versão 3, a função do membro da equipa nomeado é sempre a predefinição, de modo que qualquer tarefa que seja atribuída a Catalina utilize a sua função predefinida de Gestor do Programa.

Se tiver atribuído a um recurso uma tarefa fora da sua função predefinida nas versões 2 e 1, ao atualizar, a função predefinida será atribuída ao recurso nomeado para todas as atribuições de tarefas, independentemente da atribuição de função na versão 2. Esta atribuição resulta em diferenças nas estimativas calculadas da versão 2 ou versão 1 em relação à versão 3, pois as estimativas são calculadas com base na função do recurso, e não na atribuição da tarefa de linha. Por exemplo, na versão 2, duas tarefas foram atribuídas a Bárbara Araújo. A função na tarefa de linha da tarefa 1 era Programador e, na tarefa 2, Gestor do Programa. A função predefinida de Bárbara Araújo é Gestor do Programa.

![Várias funções atribuídas a um recurso](media/upgrade-multiple-roles-02.png)

Como as funções de Programador e Gestor do Programa são diferentes, as estimativas de custo e vendas são as seguintes:

![Estimativas de custo para as funções do recurso](media/upggrade-cost-estimates-03.png)

![Estimativas de vendas para as funções do recurso](media/upgrade-sales-estimates-04.png)

Ao atualizar para a versão 3, as tarefas de linha são substituídas por atribuições de recursos na tarefa do membro da equipa de recurso reservável. A atribuição utilizará a função predefinida do recurso reservável. Na imagem a seguir, Bárbara Araújo, que possui a função de Gestor do Programa, é o recurso.

![Atribuições de recursos](media/resource-assignment-v2-05.png)

Como as estimativas baseiam-se na função predefinida do recurso, as estimativas de custo e vendas podem ser alteradas. No gráfico seguinte, a função **Programador** já não é visualizada, pois agora a função é obtida da função predefinida do recurso reservável.

![Estimativas de custo para funções predefinidas](media/resource-assignment-cost-estimate-06.png)
![Estimativas de vendas para funções predefinidas](media/resource-assignment-sales-estimate-07.png)

Depois de a atualização ser concluída, poderá editar a função de um membro da equipa como algo diferente do padrão atribuído. No entanto, se modificar a função de membros da equipa, ela será alterada em todas as suas tarefas atribuídas, pois já não é permitido atribuir várias funções aos membros da equipa na versão 3.

![Atualizar uma função de recurso](media/resource-role-assignment-08.png)

Isto também é válido para as tarefas de linha atribuídas a recursos nomeados quando altera a unidade organizacional do recurso de predefinido para outra unidade organizacional. Após a conclusão da atualização da versão 3, a atribuição utilizará a unidade organizacional predefinida do recurso, em vez da unidade definida na tarefa de linha.

### <a name="tasks-assigned-to-generic-resources"></a>Tarefas atribuídas a recursos genéricos
Na versão 2 e na versão 1, pode definir a função e a unidade organizacional numa tarefa e, depois, utilizar o recurso **Gerar equipa** para gerar recursos genéricos com base nos atributos definidos na tarefa. Na versão 3, cria os membros da equipa genéricos com função e unidade organizacional e, em seguida, atribua os membros da equipa às tarefas.

Na versão 2 e na versão 1, os projetos com recursos genéricos podem estar em dois estados ou numa combinação de ambos no nível da tarefa. Por exemplo, é possível ter os seguintes cenários:

- Tarefas com funções e unidades organizacionais definidas, mas nenhuma atribuição de recurso afiliado foi gerada.
- Tarefas com recursos de membros da equipa genéricos atribuídos por meio da criação de um recurso genérico utilizando o recurso **Gerar equipa**.

Antes de iniciar a atualização, é recomendável gerar de novo a equipa para cada projeto que possui tarefas atribuídas a recursos genéricos ou que ainda tem de executar o processo nelas.

Para as tarefas atribuídas a membros da equipa genéricos que foram gerados utilizando **Gerar equipa**, a atualização irá manter o recurso genérico na equipa e, também, a atribuição a esse membro da equipa genérico. Recomendamos que gere o requisito de recurso para o membro da equipa genérico após a atualização, mas antes de reservar ou submeter um pedido de recurso. Isto irá preservar todas as atribuições de unidade organizacional dos membros da equipa genéricos que forem diferentes da unidade organizacional de contratação do projeto.

Por exemplo, no projeto Projeto Z, a unidade organizacional de contratação é a Contoso US. No plano do projeto, a função Consultor Técnico foi atribuída às tarefas de teste da fase de implementação, e a unidade organizacional atribuída é a Contoso India.

![Atribuição de organização na fase de implementação](media/org-unit-assignment-09.png)

Após a fase de implementação, a tarefa de teste de integração é atribuída à função Consultor Técnico, mas a organização é definida como Contoso US.  

![Atribuição de organização da tarefa de teste de integração](media/org-unit-generate-team-10.png)

Ao gerar uma equipa para o projeto, dois membros da equipa genéricos são criados devido às unidades organizacionais diferentes nas tarefas. As tarefas da Contoso India serão atribuídas ao Consultor técnico 1 e o Consultor técnico 2 receberá as tarefas da Contoso US.  

![Membros da equipa genéricos gerados](media/org-unit-assignments-multiple-resources-11.png)

> [!NOTE]
> No Project Service Automation versões 2 e 1, o membro da equipa não mantém a unidade organizacional, esta é mantida na tarefa de linha.

![Tarefas de linha versão 1 e versão 2 no Project Service Automation](media/line-tasks-12.png)

Pode ver a unidade organizacional na vista de estimativas. 

![Estimativas da unidade organizacional](media/org-unit-estimates-view-13.png)
 
Quando a atualização é concluída, a unidade organizacional na tarefa de linha que corresponde ao membro da equipa genérico é adicionada a esse membro e a tarefa de linha é removida. Por isso, recomendamos que, antes de atualizar, gere a equipa em cada projeto que contém recursos genéricos, ou a gere novamente.

Para as tarefas atribuídas a uma função com uma unidade organizacional diferente daquela do projeto de contratação e sem uma equipa gerada, a atualização criará um membro da equipa genérico para a função, mas utilizará a unidade de contratação do projeto para a unidade organizacional do membro da equipa. Voltando ao exemplo do Projeto Z, a função Consultor Técnico foi atribuída à unidade organizacional de contratação Contoso US e às tarefas de teste de plano do projeto na fase de implementação com a unidade organizacional atribuída à Contoso India. A tarefa de teste de integração concluída após a fase de implementação foi atribuída à função Consultor Técnico. A unidade organizacional é a Contoso US e uma equipa não foi gerada. A atualização criará um membro da equipa genérico, um Consultor técnico que possui as horas atribuídas das três tarefas e uma unidade organizacional da Contoso US, a unidade organizacional de contratação do projeto.   
 
Alteração na predefinição de unidades organizacionais de atribuição de recursos diferentes em membros da equipa não-gerados é o motivo pelo qual recomendamos que gere ou gere novamente a equipa em cada projeto que contém recursos genéricos antes da atualização, de modo a que as atribuições da unidade organizacional não sejam perdidas.



[!INCLUDE[footer-include](../includes/footer-banner.md)]