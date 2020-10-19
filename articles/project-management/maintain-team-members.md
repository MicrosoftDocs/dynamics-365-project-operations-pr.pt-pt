---
title: Manter membros da equipa
description: Este tópico fornece informações sobre a reserva de recursos nomeados para as equipas do projeto e atribuir às mesmas tarefas
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f5b36628e90896c9fe6570de71c95eab83a44ebd
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961925"
---
# <a name="maintain-team-members"></a>Manter membros da equipa

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Pode adicionar um recurso nomeado à sua equipa do projeto, reservando-o diretamente para a equipa.

1. No Dynamics 365 Project Operations, vá para **Projetos** e selecione para abrir o projeto que está a reservar.
2. Na página **Projeto**, no separador **Equipa**, selecione **Novo**. 
3. Na caixa de diálogo **Criação Rápida de Membro de Equipa do Projeto**, selecione o recurso reservável. O campo **Função** será preenchido com a função predefinida do recurso se tiver atribuído um. Pode alterar a função. 
4. Selecione as datas de início e fim, em que o recurso será necessário e selecione o método de alocação da capacidade do recurso. 
5. No campo **Aprovador do Projeto**, selecione **Sim** se pretender que o membro da equipa seja um aprovador do projeto. O membro da equipa pode aprovar as entradas de hora e despesas submetidas para este projeto. 
6. Selecione **Guardar**.

Agora, pode atribuir o recurso reservado a tarefas no projeto. Na página **Projeto**, selecione o separador **Agenda** para atribuir tarefas ao novo recurso. O seletor de recursos que é iniciado a partir do campo **Recursos** na grelha de tarefas irá mostrar os membros da equipa que pode selecionar.


No Project Operations, as reservas de recursos e as atribuições de tarefas não estão intimamente associadas. Quando utiliza o seletor de recursos na agenda, pode atribuir tarefas a membros da equipa durante mais horas do que as reservas deles cobrem no projeto.

As diferenças entre as reservas dos membros da equipa e as atribuições são mostradas nos separadores **Equipa** e **Reconciliação de Recursos**. Também pode conciliar as diferenças entre as reservas e as atribuições para os recursos a um nível mais detalhado.

Utilize o seletor de recursos no separador **Agenda** para procurar e selecionar recursos reserváveis que ainda não fazem parte da equipa do projeto. Estes recursos são mostrados no seletor de recursos como **Outros Recursos**.

Quando efetua uma seleção, o recurso é adicionado à equipa do projeto e atribuído à tarefa, mas não são geradas reservas.

Pode utilizar a capacidade de expansão da reserva do separador **Reconciliação** ou o **Quadro da Agenda** para reservar a capacidade do recurso para o projeto.

Depois de um membro da equipa ficar reservado no seu projeto, pode utilizar **Manter reservas** ou o **Quadro da Agenda** diretamente para gerir as respetivas reservas.
