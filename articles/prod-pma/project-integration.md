---
title: Integração com o Microsoft Project Client
description: Planear e manter uma agenda de projetos pode ser complexo, pelo que os gestores de projetos precisam de utilizar ferramentas que os ajudem a gerir esta tarefa. A integração com o Microsoft Project Client fornece suporte para abrir e gerir uma estrutura hierárquica do trabalho do projeto.
author: Yowelle
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 732b72d9819fc149c4b2c783b3dc7f7eec3f0393
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082465"
---
# <a name="microsoft-project-client-integration"></a>Integração com o Microsoft Project Client

[!include [banner](../includes/banner.md)]

Planear e manter uma agenda de projetos pode ser complexo, pelo que os gestores de projetos precisam de utilizar ferramentas que os ajudem a gerir esta tarefa. A integração com o Microsoft Project Client fornece suporte para abrir e gerir uma estrutura hierárquica do trabalho do projeto. O gestor de projetos pode lançar quaisquer alterações de volta à estrutura hierárquica do trabalho do projeto do Dynamics 365 Finance.

> [!NOTE]
> Se estiver a utilizar a atualização de julho (versão 10.0.4), tem de instalar o KB 4054797 e KB 4055884.

## <a name="configure-the-microsoft-project-client-add-in"></a>Configurar o suplemento do Microsoft Project Client
Para ativar a integração com o Microsoft Project Client, é necessário instalar um suplemento do Microsoft Dynamics 365 na aplicação Microsoft Project Client do utilizador. Isto é feito ao abrir a **Área de trabalho de gestão de projetos**.

•   Clique em **Configurar o suplemento de cliente do projeto** a partir da secção **Ligações** > **Configurar** da área de trabalho.

•   Clique em **Abrir** e, em seguida, clique em **Executar** quando for solicitado.

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>Abrir e editar uma estrutura hierárquica do trabalho existente de rascunho no Microsoft Project Client
Se um projeto no Dynamics 365 Finance já tiver uma estrutura hierárquica do trabalho criada, esta poderá ser aberta na aplicação Microsoft Project Client se a estrutura hierárquica do trabalho estiver no estado de rascunho. Para abrir a partir da página **Projeto**, clique na ligação **Abrir no Microsoft Project** a partir do separador **Plano**. Esta página também pode ser aberta a partir da aplicação Microsoft Project Client ao clicar em **Abrir** no separador **Microsoft Dynamics 365**. Selecione a **Entidade jurídica** e **Projeto** a partir da lista.

> [!NOTE]
> Se estiver a utilizar o Internet Explorer como browser, terá de clicar em **Guardar** para abrir manualmente a partir da localização para a qual o ficheiro foi transferido. Ou clique em **Guardar e abrir** para abrir o ficheiro no Microsoft Project Client. Não mude o nome do ficheiro ao guardar.

Antes de fazer quaisquer edições ao ficheiro através do Microsoft Project Client, terá de verificá-lo. Clique em **Dar saída** no separador **Microsoft Dynamics 365**. Isto evitará que outros utilizadores editem simultaneamente a estrutura hierárquica do trabalho a partir do Finance. Para publicar a estrutura hierárquica do trabalho depois de concluir quaisquer edições, clique em **Dar entrada** no separador **Microsoft Dynamics 365**.

Se já foi adicionada uma equipa de projeto ao projeto no Finance, a lista de recursos será preenchida com os membros da equipa. Se uma equipa de projeto ainda não tiver sido adicionada ao projeto, poderá selecionar os recursos e criar a equipa no Microsoft Project Client ao clicar no botão **Recursos** no separador **Microsoft Dynamics 365**. 

Os seguintes dados serão sincronizados de volta com o Finance como parte do processo de registo de entrada:

•   Nome da tarefa

•   Data de início

•   Data de conclusão

•   Antecessores

•   Nomes de recursos

•   Categoria

•   Categoria de recurso

•   Horas de trabalho

•   Notas

•   Prioridade

> [!NOTE]
> Se adicionar quaisquer outras colunas ao seu ficheiro do Microsoft Project Client, elas não serão guardadas no ficheiro e não serão apresentadas quando o ficheiro for reaberto.

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Crie a estrutura hierárquica do trabalho para um projeto existente ao utilizar o Microsoft Project Client
Para criar uma nova estrutura hierárquica do trabalho ao utilizar o Microsoft Project Client, siga estes passos:


1.  Abra o Microsoft Project Client.

2.  No separador **Microsoft Dynamics 365**, clique em **Abrir**.

3.  Selecione a **Entidade jurídica** para o projeto.

4.  Selecione o **Projeto**.

5.  Clique em **Registo de saída** no separador **Microsoft Dynamics 365**.

6.  Quando estiver pronto para publicar no Finance, clique em **Registo de entrada** no separador **Microsoft Dynamics 365**.

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Substitua a estrutura hierárquica do trabalho existente para um projeto existente ao utilizar o Microsoft Project Client
Para criar uma nova estrutura hierárquica do trabalho ao utilizar o Microsoft Project Client e substituir uma estrutura hierárquica do trabalho existente para um projeto existente, siga estes passos:

1.  Abra o Microsoft Project Client.

2.  Crie a agenda no Microsoft Project Client.

3.  No separador **Microsoft Dynamics 365**, clique em **Guardar alterações** > **Substituir o projeto existente**.

4.  Selecione a **Entidade jurídica** para o projeto.

5.  Selecione o **Projeto**.

6.  Clique em **OK**.

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>Criar um novo projeto a partir do Microsoft Project Client


1.  Abra o Microsoft Project Client.

2.  Crie a agenda no Microsoft Project Client.

3.  No separador **Microsoft Dynamics 365**, clique em **Guardar alterações** > **Guardar no novo Projeto**.

4.  Selecione a **Entidade jurídica** para o projeto.

5.  Introduza o **ID de projeto**, se for necessário.

6.  Introduza o **Nome do projeto**.

7.  Selecione o **Tipo de projeto**, **Grupo do projeto** e o **ID do contrato de projeto**. Em alternativa, pode criar um novo contrato de projeto ao clicar em **Novo**.

8.  Selecione o **Calendário** a utilizar para a atribuição de recursos.

11. Clique em **OK**.
