---
title: Atribuir recursos reserváveis genéricos a uma equipa de tarefas e projetos
description: Este tópico fornece informações sobre a reserva de recursos genéricos para equipas de tarefas e projetos.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: ca0999ae5413d824dd1384fe2262e5226695a5f8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082419"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a>Atribuir recursos reserváveis genéricos a uma tarefa e gerar requisitos de recursos 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Além da reserva e da atribuição de recursos nomeados ou reais ao seu projeto, pode atribuir recursos genéricos a tarefas do projeto. Estes recursos podem servir como marcadores de posição para os recursos nomeados até estar pronto para definir a equipa para o seu projeto com os recursos nomeados. 

1. No Project Service Automation (PSA), abra a página **Projeto** e no separador **Agenda** , introduza o nome da posição do recurso genérico na célula **Recurso** da agenda. Alternativamente, clique no ícone **Recurso** na célula para abrir o seletor de recursos e, em seguida, introduza o nome do recurso genérico que pretende criar.

![Criar e atribuir um membro da equipa genérico](media/RM-how-to-9.png)

Isto irá abrir o painel **Criação Rápida: Membro da Equipa do Projeto**. 

2. Introduza a função e a unidade organizacional do membro da equipa de recurso genérico e, em seguida, clique em **Guardar**.

![Criação rápida de membros da equipa genéricos](media/RM-how-to-10.png)

3. Depois de ter criado o novo membro da equipa de recurso genérico, o mesmo é atribuído à tarefa. Pode continuar a atribuir esse recurso genérico a outras tarefas na agenda de tarefas.

![Atribuir um membro da equipa genérico existente a tarefas](media/RM-how-to-11.png)

4. Depois de ter atribuído o recurso genérico, pode gerar um requisito de recurso e cumpri-lo, reservando diretamente ou submetendo um pedido de recurso a um gestor de recursos.

![Gerar um requisito para um membro da equipa genérico](media/RM-how-to-12.png)

Na grelha de membros da equipa, além de poder utilizar o seletor de recursos conforme mencionado acima, pode adicionar recursos genéricos diretamente. Os recursos são adicionados com um requisito de recurso baseado no método de datas de início/fim e alocação especificado no painel **Criação Rápida: Membro da Equipa do Projeto**.

Pode ver uma diferença se adicionar o membro da equipa genérico diretamente e, em seguida, atribuir mais tarefas ao recurso genérico do que o necessário para cobrir as horas. Clique em **Gerar Requisito** para regenerar o requisito para equilibrar as horas necessárias com as atribuições.

Também pode clicar na ligação **Requisito de recurso** na grelha de equipa para abrir o requisito e adicionar competências, recursos preferenciais, etc.

![Requisito de recurso](media/RM-how-to-13.png)

