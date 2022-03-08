---
title: Ver a utilização faturável para recursos
description: Este tópico fornece informações sobre a vista de utilização de recursos.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 32dba5acd95c1d192556153240ebd51343112be53aa3db93e5e6f127c2d960e9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007160"
---
# <a name="view-chargeable-utilization-for-resources"></a>Ver a utilização faturável para recursos

[!include [banner](../includes/psa-now-project-operations.md)]
 
A **Vista de Utilização** na página **Utilização de Recursos do Project Service** mostra a utilização faturável de cada recurso reservável. Como a vista é baseada no quadro da agenda, irá encontrar muitas das mesmas funções.

> ![Captura de ecrã da Vista de Utilização.](media/FAQ-utilization-1.png)
 

O cálculo de utilização faturável funciona da seguinte maneira:

   Utilização faturável = (Horas reais faturáveis) / (capacidade do recurso)

As células representam a utilização faturável calculada durante o período selecionado (dias, semanas ou meses).

As cores em cada uma das células mostram a utilização faturável para um recurso em comparação com a sua utilização faturável de destino. 

A utilização de destino pode ser definida na função predefinida do recurso ou no recurso individual propriamente dito. O cálculo examina a pessoa pelo destino em primeiro lugar e, em seguida, para a função predefinida do recurso.

## <a name="set-target-on-a-resource"></a>Definir destino num recurso

1. Aceda a **Recursos** \> **Recursos**. 
2. Selecione um recurso para abrir o registo. 
3. No separador **Project Service**, pode definir a utilização de destino do recurso.

> ![Captura de ecrã da utilização do separador Project Service para definir a utilização de destino.](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a>Definir utilização de destino numa função

1. Aceda a **Recursos** \> **Funções do Recurso**. 
2. Selecione uma função e abra o registo. 
3. Defina a utilização de destino para a função.

> ![Captura de ecrã da utilização de Funções de Recursos para definir a utilização de destino.](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a>Calcular a utilização faturável para um recurso

Para calcular a utilização faturável de um recurso terá de concluir alguns pré-requisitos. 

### <a name="set-default-role-for-individual-resource"></a>Definir função predefinida para recurso individual

Em primeiro lugar, a utilização de destino tem ser definida no recurso individual ou nas funções do recurso. Se estiver a utilizar funções de recursos para destinos, cada recurso individual tem de ter uma função predefinida. 

1. Para definir isto, aceda a **Recursos** \> **Recursos**. 
2. Selecione um recurso, abra o registo e, em seguida, selecione o separador **Project Service**. 
3. Na grelha **Função do Recurso**, certifique-se de que existe uma função para o recurso e que **É Predefinição** está definido como **Sim**.
 
### <a name="change-billing-type-for-resource-role"></a>Alterar o tipo de faturação para a função do recurso

As funções de recursos têm de ser definidas para ter um tipo de faturação de **Faturável**. 

1. Aceda a **Recursos** \> **Funções do Recurso**. 
2. Abra o registo que pretende atualizar e defina o tipo de faturação predefinido como **Faturável**.

### <a name="set-working-hours-for-resource-role"></a>Definir horas de trabalho para a função do recurso
 
O recurso tem de ter horas de expediente para o cálculo de capacidade. 

1. Aceda a **Recursos** \> **Recursos**. 
2. Selecione um recurso para abrir o registo e, em seguida, selecione **Mostrar Horas de Trabalho**. 
3. Pode atualizar em massa a lista de recursos ao aplicar um **Modelo de Horas de Trabalho** a partir da vista de **Lista de Recursos**.

## <a name="troubleshooting-chargeable-actual-hours"></a>Resolução de problemas de horas reais faturáveis

As horas reais faturáveis são obtidas a partir da entidade **Valores Reais**. Os valores reais com uma faturação de tipo **Faturável** estão incluídos no cálculo e, por este motivo, deve ter projetos nos quais os valores reais são faturáveis.

Se não está a ver utilização faturável, eis alguns aspetos que pode verificar:

- A capacidade é definida nas horas de trabalho dos recursos.
- O recurso tem uma utilização de destino definida individualmente ou tem uma função padrão atribuída. A função tem uma utilização de destino definida.
- Os valores reais têm um tipo de faturação **Faturável** para o período para o qual está à espera de um cálculo de utilização. Verifique o seguinte se estiver a ver valores reais com tipos de faturação diferentes de faturável:

  - A função utilizada nos valores reais tem um tipo de faturação padrão diferente de faturável.
  - A função do item de contrato do projeto que apoia o projeto foi definida como não faturável.
  - O projeto não tem um item de contrato associado.



[!INCLUDE[footer-include](../includes/footer-banner.md)]