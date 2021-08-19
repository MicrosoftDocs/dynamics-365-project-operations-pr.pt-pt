---
title: Atribuir recursos reserváveis genéricos a uma equipa de tarefas e projetos
description: Este tópico fornece informações sobre a reserva de recursos genéricos para equipas de tarefas e projetos.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: d9a81d7242e78dafad871bb07c03459f1de21884d196c6ee7dd9619b2c410404
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007115"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a>Atribuir recursos reserváveis genéricos a uma tarefa e gerar requisitos de recursos 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Além da reserva e da atribuição de recursos nomeados ou reais ao seu projeto, pode atribuir recursos genéricos a tarefas do projeto. Estes recursos podem servir como marcadores de posição para os recursos nomeados até estar pronto para definir a equipa para o seu projeto com os recursos nomeados. 

1. No Project Service Automation (PSA), abra a página **Projeto** e no separador **Agenda**, introduza o nome da posição do recurso genérico na célula **Recurso** da agenda. Alternativamente, clique no ícone **Recurso** na célula para abrir o seletor de recursos e, em seguida, introduza o nome do recurso genérico que pretende criar.

![Criar e atribuir um membro da equipa genérico.](media/RM-how-to-9.png)

Isto irá abrir o painel **Criação Rápida: Membro da Equipa do Projeto**. 

2. Introduza a função e a unidade organizacional do membro da equipa de recurso genérico e, em seguida, clique em **Guardar**.

![Criação rápida de membros da equipa genéricos.](media/RM-how-to-10.png)

3. Depois de ter criado o novo membro da equipa de recurso genérico, o mesmo é atribuído à tarefa. Pode continuar a atribuir esse recurso genérico a outras tarefas na agenda de tarefas.

![Atribuir um membro da equipa genérico existente a tarefas.](media/RM-how-to-11.png)

4. Depois de ter atribuído o recurso genérico, pode gerar um requisito de recurso e cumpri-lo, reservando diretamente ou submetendo um pedido de recurso a um gestor de recursos.

![Gerar um requisito para um membro da equipa genérico.](media/RM-how-to-12.png)

Na grelha de membros da equipa, além de poder utilizar o seletor de recursos conforme mencionado acima, pode adicionar recursos genéricos diretamente. Os recursos são adicionados com um requisito de recurso baseado no método de datas de início/fim e alocação especificado no painel **Criação Rápida: Membro da Equipa do Projeto**.

Pode ver uma diferença se adicionar o membro da equipa genérico diretamente e, em seguida, atribuir mais tarefas ao recurso genérico do que o necessário para cobrir as horas. Clique em **Gerar Requisito** para regenerar o requisito para equilibrar as horas necessárias com as atribuições.

Também pode clicar na ligação **Requisito de recurso** na grelha de equipa para abrir o requisito e adicionar competências, recursos preferenciais, etc.

![Requisito de recurso.](media/RM-how-to-13.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]