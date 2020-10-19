---
title: Criar atribuições de recursos
description: Este tópico fornece informações sobre como criar atribuições de recursos genéricos e nomeados.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 20eb3880b17fb1f765ad79bd720520b0c8004c0a
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906285"
---
# <a name="create-resource-assignments"></a>Criar atribuições de recursos

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_


Uma atribuição de recursos é a associação direta de um membro da equipa do projeto a uma tarefa do nó de folha. Este tópico fornece informações sobre as diferentes formas de atribuir recursos.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Criar um membro da equipa genérico através de atribuição da tarefa


Quando cria um membro da equipa genérico através de uma atribuição da tarefa, crie um marcador de posição ou um recurso genérico. Este recurso genérico descreve as características do recurso nomeado que, em última análise, pretende que trabalhe nas tarefas. Em seguida, gere um requisito, ou submete um pedido utilizando o requisito, que é utilizado para procurar e reservar o recurso nomeado.

1. Na grelha Agenda para uma tarefa, selecione o ícone Recurso na célula **Recurso**.
2. Escreva um nome para servir como o nome do recurso de marcador de posição. Por exemplo, Gestor do Programa.
3. Selecione **Criar** e no campo **Criação Rápida de Membro da Equipa do Projeto**, defina a função do recurso genérico.
4. Atribua tarefas conforme seja necessário a este recurso de marcador de posição ao selecionar o recurso no **Seletor de Recursos** para a tarefa. Os recursos listados em **Membros da Equipa**.
5. Quando concluir a atribuição de recurso genérico, selecione-o no separador **Equipa**, selecione o recurso genérico e, em seguida, selecione **Gerar Requisito** para criar um requisito de recurso para o recurso genérico.
6. Selecione **Reservar** para o recurso genérico e, em seguida, utilize o Quadro da agenda para localizar e reservar um recurso real. Também é possível enviar o requisito para preenchimento por um gestor de recursos.
7. Quando o recurso genérico está totalmente concluído (a conclusão parcial dos requisitos do recurso não resultará numa atribuição de recursos) com um recurso nomeado, o recurso genérico é removido da equipa. As atribuições de tarefas para o recurso genérico são atribuídas ao recurso nomeado que concluiu o requisito de recurso do recurso genérico.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Atribuir um recurso nomeado da lista de todos os recursos reserváveis

Pode utilizar a caixa de pesquisa no **Seletor de Recursos** para procurar todos os recursos reserváveis ativos e atribui-los a qualquer tarefa do nó de folha. Os recursos atribuídos desta forma são adicionados à equipa sem quaisquer reservas. Isto é semelhante à adição de um membro da equipa e à seleção de **Nenhum** como o método de alocação. O recurso é apresentado nos separadores **Equipa**, **Atribuição de Recurso** e **Reconciliação** como recursos apenas com atribuições e um défice de reserva. Reserve-os se quiser utilizar a sua disponibilidade.

1. A partir da grelha de tarefas, quadro ou linha cronológica, navegue para a célula **Atribuído a**.
2. Na caixa de pesquisa, comece a escrever um nome. Os resultados da pesquisa para o nome são apresentados no **Seletor de Recursos** em **Outros Recursos**.
3. Selecione o recurso que pretende atribuir à tarefa ou selecione o nome do recurso em **Outros Recursos da Equipa**.
