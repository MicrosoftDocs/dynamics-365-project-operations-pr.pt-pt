---
title: Como posso fazer uma "reserva flexível" de recursos na aplicação, versão 2.x?
description: Este artigo descreve como efetuar uma reserva flexível de membros da equipa com o Project Service.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a35799b422fa338c2666e1b2aa11bc2a54f5cce3
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122267"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a>Como posso fazer uma "reserva flexível" de recursos na aplicação Web (aplicação Project Service v2.x)?

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

É possível agendar temporariamente ou efetuar uma "reservar flexível" de um recurso para uma equipa de projeto para mostrar que pretende atribuir o recurso a um projeto. Reservas flexíveis não consomem a capacidade disponível de um recurso. Membros da equipa reservados sem compromisso não podem ser atribuídos a tarefas do projeto. Apenas os recursos com o Estado Reserva Fixa e Tipo de Submissão Submetido podem ser atribuídos a tarefas (assumindo que têm horas de reserva fixa para abranger o esforço de atribuição).

Membros da equipa do projeto reservados de forma flexível aparecem na grelha Membro da Equipa com as respetivas horas reservadas flexíveis apresentadas na coluna Reserva Flexível. Estes também aparecem no quadro da agenda. Novamente, eles não indicam qualquer consumo de capacidade, uma vez que a reserva flexível não consome a capacidade de um recurso.

Existem três formas de efetuar uma reserva flexível de um membro da equipa para um projeto com o Project Service, versão 2.x. É possível reservar de forma flexível com o quadro da agenda, através da funcionalidade Manter Reservas ou criando um recurso genérico. Estes métodos são descritos abaixo.

## <a name="soft-book-with-the-schedule-board"></a>Efetue uma reserva flexível com o quadro da agenda

Para efetuar uma reserva flexível com o quadro da agenda, siga este procedimento: 
1. Abra o quadro da agenda.
2. Selecione o separador Projeto no painel inferior dos Requisitos de Reserva do quadro da agenda.
3. Localize o projeto em que pretende efetuar uma reserva flexível de recurso. Se tiver vários projetos, clique no cabeçalho da coluna Projeto e, em seguida, utilize o filtro para localizar o projeto.
4. Clique no projeto, em seguida arraste e largue-o na grelha de tempo do recurso.
5. Esta ação abre o painel Criar Reserva de Recursos à direita. Ajuste a data de início e de fim, selecione o Estado de Reserva como Flexível e defina as horas. 
6. Clique em Reservar.
7. Novamente no projeto, o recurso agora irá mostrar como um membro da equipa com as horas flexíveis na coluna Reserva Suave.

Tenha em atenção que não pode atribuí-lo a tarefas na estrutura hierárquica do trabalho (WBS), uma vez que os recursos têm de ser reservados de forma fixa na equipa a ser atribuída.

## <a name="soft-book-using-the-maintain-bookings-feature"></a>Efetue uma reserva flexível através da funcionalidade Manter Reservas

Para efetuar uma reserva flexível com Manter Reservas, siga este procedimento:
1. Na grelha de membro de equipa, clique em Novo.
2. Selecione o recurso reservável, função, de/para.
3. Selecione um método de alocação diferente de Nenhum:
- Capacidade Total
- Capacidade Percentual
- Por Horas, Distribuir Uniformemente
- Por Horas, Carregamento no Início
4. Clique em Guardar. Verá o recurso na grelha de equipa e as respetivas horas indicadas como Fixas.
5. Mantenha as reservas do recurso clicando em Manter Reservas.
6. Quando se abre o quadro da agenda, expanda o recurso para apresentar as reservas. A reserva será apresentada como Fixa.
7. Com o botão direito do rato, clique na reserva, em Alterar Estado, selecione Reserva Flexível e, em seguida, Flexível. O estado da reserva é agora Flexível.
8. Depois de fechar o quadro da agenda, verá que as horas para o recurso foram alteradas de Fixas para Flexíveis na grelha de membro da equipa.
Note que, se efetuar uma reserva fixa para a equipa e, em seguida, atribuir-lhe tarefas no WBS, quando utiliza o manter reservas para alterar o estado Fixa para Flexível, irá remover as atribuições das tarefas para esse recurso, uma vez que apenas recursos reservados de forma fixa podem ser atribuídos a tarefas.

## <a name="soft-book-by-creating-a-generic-resource"></a>Efetue uma reserva flexível através da criação de um recurso genérico

Pode criar uma reserva flexível gerando um membro da equipa de recurso genérico, preenchendo com o quadro da agenda ou um Pedido de Recursos e alterando o tipo durante a reserva.
Para isso, utilize o seguinte procedimento:

1. No WBS do projeto, atribua funções às tarefas para as quais pretende gerar membros da equipa genéricos.
2. Clique em Gerar Equipa do Projeto.
3. Na grelha de membro da equipa de projeto, selecione o recurso genérico e clique em Reservar.
4. No quadro da agenda, selecione o recurso que pretende reservar.
5. No painel Criar Reserva de Recursos do quadro da agenda, altere o Estado de Reserva para Flexível.
6. Clique em Reservar ou Reservar e Sair.

Depois de fechar o quadro da agenda, verá o recurso selecionado adicionado à equipa com horas flexíveis, bem como as horas atribuídas. Também irá ver que o recurso genérico permanece na equipa como um indicador de que as tarefas estão atribuídas a um membro da equipa reservado de forma flexível.

Quando estiver pronto para alterar um recurso de membro de equipa reservado de forma flexível para reserva fixa para que seja possível atribuir-lhes a tarefas, faça o seguinte:

1. Selecione o recurso e clique em Manter Reservas.
2. Quando se abre o quadro da agenda, expanda o recurso para apresentar as reservas. Verá a reserva marcada como Flexível.
3. Com o botão direito na reserva, em Alterar Estado, selecione Reserva Fixa e, em seguida, Fixa. O estado da reserva é agora Fixa
4. Depois de fechar quadro da agenda, verá que as horas para o recurso foram alteradas de Flexíveis para Fixas na grelha de membro da equipa. Agora, pode atribuir o recurso a tarefas (desde que exista alinhamento entre as horas de trabalho reservadas fixas e as horas de esforço da tarefa para atribuição). Tenha em atenção que, se seguiu os passos de preenchimento do recurso genérico no item 3 acima, quando altera o estado do recurso reservável de forma flexível para fixa, o membro de equipa genérico é removido da equipa.
