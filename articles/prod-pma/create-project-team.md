---
title: Criar uma equipa de projeto
description: Este artigo fornece informações sobre como criar e gerir equipas do projeto.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df9df8b3ee9b42a33c6031c78ff3673cad47bfe6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927342"
---
# <a name="create-a-project-team"></a>Criar uma equipa de projeto

[!include [banner](../includes/banner.md)]

Para utilizar as funções previamente configuradas num projeto, um gestor de projetos tem de associar as funções ao projeto. Podem ser atribuídas várias funções para um projeto. Para evitar confusões, estas funções são etiquetadas automaticamente durante a reserva. Por exemplo, se o gestor de projetos necessitar de três engenheiros de software, são geradas automaticamente três funções de Engenheiro de software com **Engenheiro de software 1**, **Engenheiro de software 2** e **Engenheiro de software 3** como etiquetas. Se a função tinha características de função definidas anteriormente, são aplicadas como um filtro durante as pesquisas de um recurso. Podem ser adicionadas características adicionais conforme seja necessário para refinar ainda mais a pesquisa.

As definições de visualização também podem ser personalizadas para oferecem uma melhor visão da disponibilidade dos recursos. Existem opções para mostrar a disponibilidade horária, diária, semanal, mensal, trimestral e anual. Também existe uma opção para mostrar a capacidade disponível e restante nos recursos. Esta opção é útil para a gestão do tempo, quando está a estimar o tempo disponível para as atividades ou disponibilidade de recursos.

O gestor do projetos pode selecionar uma função na página e, em seguida, se estiver disponível um recurso que se ajusta ao requisito, selecione para reservar um recurso para preencher a função. Note que os recursos não têm de ser reservados neste momento na fase de planeamento. Quando cria uma WBS, pode substituir as funções por recursos com pessoal para o projeto. Se as funções forem substituídas por recursos com pessoal na WBS, a configuração do recurso atualiza automaticamente a listagem e o agendamento da equipa do projeto.

[![Lista da equipa do projeto que inclui as funções e os recursos reais.](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

O gestor de projetos tem várias opções para reservar um recurso para um projeto, tais como **Capacidade restante**, **Capacidade total**, **Capacidade Percentual** e **Especificar horas**. Estas opções de reserva podem ser canceladas em qualquer altura se as atribuições de recursos forem alteradas. São suportados dois tipos de reserva:

- **Reserva Fixa** – A reserva de recursos foi aprovada e confirmada para trabalhar no compromisso durante o período especificado.
- **Reserva flexível** – As reservas de recursos forem definidas provisoriamente para trabalharem no compromisso durante o período especificado.

O procedimento seguinte explica como criar uma equipa do projeto.

## <a name="create-a-project-team"></a>Criar uma equipa de projeto

1. Na página da lista **Todos os projetos**, selecione um projeto e, em seguida, selecione **Editar**.
2. No separador **Equipa do projeto e agendamento**, no campo **Data de fim da agenda**, introduza a data de início da agenda acrescida de um mês. Por exemplo, se a data de início da agenda for 24 de junho de 2017 (24/06/2017), introduza **24/07/2017**.
3. Selecione **Adicionar**.
4. No painel **Adicionar funções ao projeto**, no campo **Função**, selecione **Gestor de Projetos Sénior**.
5. Selecione **Competências necessárias**.
6. Na página **Escolha características**, as características que definiu anteriormente para a função Gestor de projetos sénior são selecionadas por predefinição. Selecione **OK**.
7. Na página **Adicionar funções ao projeto**, no campo **Número de recursos**, introduza **1**.
8. No campo **Recursos**, a pesquisa mostra todos os recursos que têm as competências necessárias. Selecione **Daniel Goldschmidt** e, em seguida, selecione **Criar**.
9. Na página **Projeto**, selecione **Adicionar**.
10. No painel **Adicionar funções ao projeto**, no campo **Função**, selecione **Membro da equipa**. No campo **Número de recursos**, introduza **5**.
11. Selecione **Criar**.
12. Na página **Projetos**, selecione **Concluir recurso**.

## <a name="monitor-project-teams"></a>Monitorizar equipas do projeto
1. Na página **Todos os projetos**, selecione a ligação **ID do Projeto** para o projeto **Fase de Atualização 2 XYZ**.
2. No Separador Rápido **Equipa do projeto e agendamento**, verifique se os recursos do projeto que são listados estão corretos.


[!INCLUDE[footer-include](../includes/footer-banner.md)]