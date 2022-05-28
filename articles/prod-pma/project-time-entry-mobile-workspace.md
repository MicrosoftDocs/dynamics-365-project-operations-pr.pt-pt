---
title: Área de trabalho móvel da entrada de hora do projeto
description: Este tópico fornece informações sobre a área de trabalho móvel da entrada de hora do Projeto. Esta área de trabalho permite aos utilizadores introduzir e guardar as horas num projeto através do seu dispositivo móvel.
author: Yowelle
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 64a80d931332a4d6edfcd175d7168a7815ddca38
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683966"
---
# <a name="project-time-entry-mobile-workspace"></a>Área de trabalho móvel da entrada de hora do projeto

[!include [banner](../includes/banner.md)]

Este tópico fornece informações sobre a área de trabalho móvel **Entrada de hora do projeto**. Esta área de trabalho permite aos utilizadores introduzir e guardar as horas num projeto através do seu dispositivo móvel.

Esta área de trabalho móvel destina-se a ser utilizada com a aplicação móvel Dynamics 365 Unified Ops. 

## <a name="overview"></a>Descrição Geral
Como parte do seu trabalho diário, os recursos do projeto estão muitas vezes no local ou a viajar. A área de trabalho móvel **Entrada de hora do projeto** permite que os utilizadores introduzam as horas faturáveis ou não faturáveis para um projeto no dispositivo móvel à sua escolha. Por isso, os recursos do projeto podem registar entradas de hora a qualquer altura e em qualquer lugar. Também podem ver as entradas de hora que já foram registadas. 

Especificamente, na área de trabalho móvel **Entrada de hora do projeto**, os utilizadores podem executar estas tarefas:

-   Para qualquer data selecionada, introduza o número de horas que gastou numa tarefa específica.
-   Procure por nome de projeto ou cliente para localizar o projeto para o qual pretende introduzir horas.
-   Especifique a categoria e a atividade pelo tempo que dedicou.
-   Registe o tempo como faturável ou não faturável para o projeto.
-   Opcionalmente,: introduza quaisquer comentários externos ou internos.

## <a name="prerequisites"></a>Pré-requisitos
Os pré-requisitos diferem consoante a versão do Microsoft Dynamics 365 que foi implementada para a sua organização.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Pré-requisitos se utilizar o Dynamics 365 Finance
Se o Finance foi implementado para a sua organização, o administrador de sistema tem de publicar a área de trabalho móvel **Entrada de hora do projeto**. Para obter instruções, consulte [Publicar uma área de trabalho móvel](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Pré-requisitos se utilizar a versão 1611 com a Platform update 3 ou posterior
Se a versão 1611 com a Platform update 3 ou posterior tiver sido implementada para a sua organização, o administrador de sistema tem de satisfazer os seguintes pré-requisitos. 

<table>
<thead>
<tr class="header">
<th>Pré-requisito</th>
<th>Função</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td>Implementar KB 4018050.</td>
<td>Administrador de sistema</td>
<td>O KB 4018050 é uma atualização de is X++ ou correção de metadados que contém a área de trabalho móvel <strong>Entrada de hora do projeto</strong>. Para implementar o KB 4018050, o seu administrador de sistema tem de seguir estes passos.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Transfira a correção de metadados do Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Instale a correção de metadados</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Crie um pacote implementável</a> que contenha os modelos <strong>ApplicationSuite</strong> e <strong>ProjectMobile</strong> e, em seguida, carregue o pacote implementável para o LCS.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Aplique o pacote implementável</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Publique a área de trabalho móvel <strong>Entrada de hora do projeto</strong>.</td>
<td>Administrador de sistema</td>
<td>Consulte <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publicar uma área de trabalho móvel</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Transferir e instalar a aplicação móvel

Transferir e instalar a aplicação móvel Finanças e Operações:

-   [Para telemóveis Android](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Para iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Iniciar sessão na aplicação móvel
1.  Inicie a aplicação no seu dispositivo móvel.
2.  Introduza o seu URL do Dynamics 365.
3.  Quando iniciar sessão pela primeira vez, ser-lhe-á solicitado o nome de utilizador e a palavra-passe. Introduza as suas credenciais.
4.  Depois de iniciar sessão, são mostradas as áreas de trabalho disponíveis para a sua empresa. Note que, se o seu administrador de sistema publicar uma nova área de trabalho mais tarde, terá de atualizar a lista de áreas de trabalho móveis.

[![Pull to refresh.](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Introduza o tempo através da área de trabalho móvel Entrada de hora do projeto
1.  No seu dispositivo móvel, selecione a área de trabalho **Entrada de hora do projeto**.
2.  Selecione **Entrada de hora**. São mostradas as datas do calendário da semana atual.
3.  Para uma data selecionada, selecione **Ações** &gt; **Nova entrada**.
4.  Introduza o número de horas a registar.
5.  Selecione o projeto para a entrada de hora. Uma lista mostra os projetos que são carregados na sua aplicação para utilização offline. Por predefinição, são carregados 50 itens, mas um programador pode alterar este número. Para mais informações, consulte [Plataforma móvel](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
6.  Se o seu projeto não estiver na lista, selecione **Procurar**. Procure por nome ou mude para a pesquisa por nome de projeto ou cliente.
7.  Selecione uma categoria. Uma lista mostra as categorias que são carregadas na sua aplicação para utilização offline. Por predefinição, são carregados 50 itens, mas um programador pode alterar este número. Para mais informações, consulte [Plataforma móvel](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
8.  Se a sua categoria não estiver na lista, selecione **Procurar**. Procure por categoria ou mude para a pesquisa por nome de categoria.
9.  Selecione uma atividade. Uma lista mostra as atividades que são carregadas na sua aplicação para utilização offline. Por predefinição, são carregados 50 itens, mas um programador pode alterar este número. Para mais informações, consulte [Plataforma móvel](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
10. Se a sua atividade não estiver na lista, selecione **Procurar**. Procure por número de atividade ou mude para a pesquisa finalidade.

11. Selecione a propriedade da linha.
12. Opcional: introduza quaisquer comentários externos e internos.
13. Selecione **Concluído**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]