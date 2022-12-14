---
title: Criar atribuições de recursos
description: Este artigo fornece informações sobre a criação de atribuições de recursos genéricas e nomeadas.
author: ruhercul
ms.date: 11/22/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 42dd2906ce8db8844bf4dea232f24aca58a5d951
ms.sourcegitcommit: 9b1136d95f19cc039d675a4a1b0962ca3ec61646
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 11/30/2022
ms.locfileid: "9812008"
---
# <a name="create-resource-assignments"></a>Criar atribuições de recursos

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_


Uma atribuição de recursos é a associação direta de um membro da equipa do projeto a uma tarefa do nó de folha. Este artigo fornece informações sobre as diferentes formas de atribuir recursos.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Criar um membro da equipa genérico através de atribuição da tarefa


Quando cria um membro da equipa genérico através de uma atribuição da tarefa, crie um marcador de posição ou um recurso genérico. Este recurso genérico descreve as características do recurso nomeado que, em última análise, pretende que trabalhe nas tarefas. Em seguida, gere um requisito, ou submete um pedido utilizando o requisito, que é utilizado para procurar e reservar o recurso nomeado.

1. Na grelha Agenda para uma tarefa, selecione o ícone Recurso na célula **Recurso**.
2. Escreva um nome para servir como o nome do recurso de marcador de posição. Por exemplo, Gestor do Programa.
3. Selecione **Criar** e no campo **Criação Rápida de Membro da Equipa do Projeto**, defina a função do recurso genérico.
4. Atribua tarefas conforme seja necessário a este recurso de marcador de posição ao selecionar o recurso no **Seletor de Recursos** para a tarefa. Os recursos listados em **Membros da Equipa**.
5. Quando concluir a atribuição de recurso genérico, selecione-o no separador **Equipa**, selecione o recurso genérico e, em seguida, selecione **Gerar Requisito** para criar um requisito de recurso para o recurso genérico.
6. Selecione **Reservar** para o recurso genérico e, em seguida, utilize o Quadro da agenda para localizar e reservar um recurso real. Também é possível enviar o requisito para preenchimento por um gestor de recursos.
7. Quando o recurso genérico é totalmente cumprido com um recurso nomeado, o recurso genérico é removido da equipa. (O cumprimento de requisito de recursos parcial não resultará numa atribuição de recursos.) As atribuições para o recurso genérico são atribuídas ao recurso nomeado que cumpriu o requisito de recursos do recurso genérico.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Atribuir um recurso nomeado da lista de todos os recursos reserváveis

Pode utilizar a caixa de pesquisa no **Seletor de Recursos** para procurar todos os recursos reserváveis ativos e atribui-los a qualquer tarefa do nó de folha. Os recursos atribuídos desta forma são adicionados à equipa sem quaisquer reservas. Isto é semelhante à adição de um membro da equipa e à seleção de **Nenhum** como o método de alocação. O recurso é apresentado nos separadores **Equipa**, **Atribuição de Recurso** e **Reconciliação** como recursos apenas com atribuições e um défice de reserva. Reserve-os se quiser utilizar a sua disponibilidade.

1. A partir da grelha de tarefas, quadro ou linha cronológica, navegue para a célula **Atribuído a**.
2. Na caixa de pesquisa, comece a escrever um nome. Os resultados da pesquisa para o nome são apresentados no **Seletor de Recursos** em **Outros Recursos**.
3. Selecione o recurso que pretende atribuir à tarefa ou selecione o nome do recurso em **Outros Recursos da Equipa**.

## <a name="editing-resource-assignment-contours"></a>Editar desvios de atribuição de recursos

Por predefinição, quando os recursos são atribuídos a uma tarefa na agenda, o respetivo esforço é distribuído linearmente a cada recurso, com base no horário de trabalho desse recurso e no modo de agenda do projeto. Um gestor de projetos pode utilizar a grelha de atribuição de recursos para refinar as estimativas de esforço de cada recurso atribuído a uma ou muitas tarefas em escalas de tempo diferentes. Esta caraterística ajuda os gestores de projetos a produzirem estimativas de custo e de vendas mais precisas, impulsionadas pelos contornos da atribuição de recursos que são gerados quando um recurso é atribuído a uma tarefa. Além disso, os gestores de projetos podem refletir mais facilmente a procura de recursos necessária para criar a procura num requisito de recurso.

### <a name="navigation"></a>Navegação

Para aceder à grelha de edição de contornos, o gestor de projetos primeiro seleciona o separador **Tarefas** na página principal do projeto e, em seguida, seleciona o separador **Atribuições**.

![Separador Atribuições no separador Tarefas da página principal do projeto.](media/AssignmentGrid.png)

A grelha suporta dois métodos de agrupamento: **agrupar por recurso** e **agrupar por tarefa**. Ao contrário da vista de grelha, as colunas não são configuráveis. As únicas colunas visíveis são **Atribuído A**, **Nome da Tarefa**, **Início da Atribuição**, **Conclusão da Atribuição** e **Esforço da Atribuição**.

Quando a grelha é composta inicialmente, começa no contorno de atribuição mais antigo. Se a agenda não contiver quaisquer atribuições que tenham esforço, a grelha estará em branco e não irá compor nada.

![Grelha de atribuição em branco.](media/emptyassignmentgrid.png)

Se pretender ver os seus contornos e escalas de tempo diferentes, a grelha de atribuição de recursos só de leitura e a grelha de reconciliação de recursos também estão disponíveis.

### <a name="resource-calendars"></a>Calendários de recursos

A capacidade de editar um contorno para um dia específico é regida pelos dias de trabalho do recurso, como refletido no respetivo calendário. Se uma célula estiver desativada para um determinado recurso, esse recurso não terá dias de trabalho durante esse período.

Os contornos de um recurso podem expandir-se para além das datas de início e de fim atuais da tarefa atribuída. Se um contorno for atualizado para ser posterior à data de fim mais recente de uma tarefa ou à data de início mais recente de uma tarefa, a data de fim ou a data de início da tarefa serão alteradas em conformidade. No entanto, se um contorno é atualizado para ser anterior à data de início de uma tarefa associada a uma antecessora, a atualização falhará porque a atribuição acionará a tarefa a iniciar para ser iniciada antes da antecessora ser concluída, e esse comportamento não é atualmente suportado.

### <a name="co-authoring"></a>Cocriação

As alterações à grelha de atribuição de recursos são automaticamente refletidas em quaisquer vistas associadas, incluindo vistas de gráfico, de linha cronológica, de quadro e de grelha. Se vários utilizadores estão a rever o projeto ao mesmo tempo, quaisquer alterações que um utilizador faça serão refletidas na grelha. Pelo contrário, todas as alterações efetuadas na grelha de atribuição de recursos serão mostradas a todos os outros utilizadores que estão a ver o projeto na mesma sessão.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
