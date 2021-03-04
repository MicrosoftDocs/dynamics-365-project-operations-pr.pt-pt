---
title: Configurar funções em modelos de Estrutura hierárquica do trabalho
description: Este tópico fornece informações sobre a configuração de informações sobre a função dos modelos da Estrutura hierárquica do trabalho.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 143f1094c653fb7ac0e026b7875aa162a3eb83f7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082384"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a>Configurar funções em modelos de Estrutura hierárquica do trabalho

[!include [banner](../includes/banner.md)]

Os gestores de projetos podem configurar modelos de Estrutura hierárquica do trabalho (WBS) que podem aplicar quando criam uma WBS para novos projetos. Os gestores de projetos podem adicionar funções quando criam um modelo. Utilize o seguinte procedimento para atribuir uma função a um modelo de WBS.

1. Selecione **Gestão de projetos e contabilística** > **Configurar** > **Projetos** > **Modelos de estrutura hierárquica do trabalho**.
2. Selecione **Detalhes** para um modelo de WBS selecionado.
3. Selecione uma tarefa na lista e, em seguida, no campo **Função** , selecione uma função a atribuir à tarefa.

## <a name="work-with-a-wbs"></a>Trabalhar com uma WBS

Pode criar uma nova WBS ou copiar uma WBS a partir de um modelo de WBS existente. Um gestor de projetos pode gerir facilmente os recursos ao atribuir funções a novas tarefas na WBS. As funções podem ser substituídas após a aquisição de um recurso ou depois de recurso confirmado para trabalhar na tarefa ser identificado. Esta flexibilidade permite que os gestores de projetos executem as seguintes tarefas:

- Identificar o número de recursos necessários para os pacotes de trabalho da WBS.
- Estimar os custos do projeto.
- Determinar um orçamento preliminar.
- Estimar a duração da atividade, baseado nas funções e nos recursos.
- Desenvolver alguns planos de gestão de projetos, baseado na informação do projeto disponível.

Foram adicionadas opções adicionais na WBS para melhorar a utilização da funcionalidade de atribuição de recursos.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Opção</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Atribuições de recursos</td>
<td>Veja os recursos atribuídos, as datas, o número de horas e o tipo de reserva para as tarefas na WBS.</td>
</tr>
<tr class="even">
<td>Gerar automaticamente a equipa</td>
<td>Adicione automaticamente os recursos planeados ao utilizar funções associadas a uma tarefa. O Finance sugere automaticamente recursos planeados através da análise de decisão de vários critérios baseada em funções. Depois de definidas as funções e o esforço (horas) para as tarefas numa WBS, e depois de a estrutura ter sido libertada, selecione <strong>Gerar automaticamente a equipa</strong>. O número necessário de recursos planeados é adicionado à WBS e ao separador <strong>Agendamento do projeto e da equipa</strong>.</td>
</tr>
<tr class="odd">
<td>Recurso (lista pendente)</td>
<td>Na página <strong>Iniciar atribuição de recursos</strong>, pode selecionar recursos para reserva fixa ou reserva flexível, baseado na duração especificada. Pode ajustar as definições de vista para ver e definir a duração das atividades dos recursos. Pode selecionar e atribuir recursos a nível do pacote de trabalho ao utilizar as seguintes opções:
<ul>
<li><strong>Aceitar</strong> – Confirmar alterações ao recurso atribuído a uma tarefa.</li>
<li><strong>Cancelar</strong> – Cancelar as alterações ao recurso atribuído a uma tarefa.</li>
<li><strong>Atribuir automaticamente</strong> – É selecionado automaticamente um recurso com pessoal disponível que tenha uma função de correspondência, e atribuído à tarefa selecionada.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Na página **Todos os projetos** , selecione o projeto **Fase de Atualização 2 XYZ**.
2. Selecione **Plano** > **Atividades** > **Estrutura hierárquica do trabalho**.
3. Selecione **Novo** para adicionar as seguintes atividades de nível um à WBS:

    - A iniciar
    - Planeamento
    - A executar
    - Monitorização e Controlo
    - Fechar

4. Defina as datas e o esforço (horas), como mostra a seguinte ilustração.

    [![Definir as datas e o esforço](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Selecione a linha da tarefa **A iniciar** e, em seguida, no campo **Função** , selecione **Gestor de Projetos Sénior**.
6. Selecione **Publicar**.
7. Na mesma linha, no campo **Recursos** , selecione **Daniel Goldschmidt** e, em seguida, selecione **Aceitar**.
8. Selecione a linha de tarefa **Planeamento** e, em seguida, no campo **Função** , selecione **Analista de negócios**.
9. Selecione **Publicar** e, em seguida, selecione **Gerar automaticamente a equipa**.
10. Na caixa de mensagem apresentada, selecione **Sim**.
11. No campo **Recursos** , verifique se o valor é **Analista de negócios 1**.
12. Para o recurso **Analista de negócios 1** abra a pesquisa e selecione **Iniciar atribuições de recursos**. Em seguida, selecione um trabalhador para a tarefa.
13. Selecione **Atribuição flexível** &gt; **Capacidade Total**.

    > [!NOTE] 
    > Não receberá um aviso de que o recurso especificado é agora 2, porque o número de recursos permanece 1.

14. Na página **Estrutura hierárquica do trabalho** , valide a atribuição de recursos na WBS e selecione **Guardar**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]