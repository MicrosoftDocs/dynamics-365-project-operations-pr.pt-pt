---
title: Aplicação móvel Project Timesheet
description: Este tópico fornece informações sobre a aplicação móvel Microsoft Dynamics 365 Project Timesheet. A aplicação móvel Project Timesheet permite aos utilizadores submeter e aprovar as folhas de horas para os projetos nos respetivos dispositivos móveis.
author: abruer
ms.date: 04/08/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 517c6f2b749fa3ed44b198b799489e7e29e34d7f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009900"
---
# <a name="project-timesheet-mobile-application"></a>Aplicação móvel Project Timesheet

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Descrição Geral

A aplicação móvel Microsoft Dynamics 365 Project Timesheet permite aos utilizadores submeter e aprovar as folhas de horas para os projetos nos respetivos dispositivos móveis (iPhone ou Android). Esta aplicação móvel surge na funcionalidade da folha de horas que reside na área Gestão de projetos e contabilística do Dynamics 365 Finance, melhorando a produtividade e a eficiência dos utilizadores, bem como permitir a entrada e a aprovação atempadas das folhas de horas do projeto.

## <a name="download-and-install-the-mobile-app"></a>Transferir e instalar a aplicação móvel

Transfira e instale a aplicação móvel Microsoft Dynamics 365 Project Timesheet para Android ou iPhone a partir da loja de aplicações do seu dispositivo.

## <a name="enable-the-app"></a>Ativar a aplicação 

No Finance, a aplicação móvel Project Timesheet tem de ser ativada. Para ativar a funcionalidade, aceda a **Parâmetros da gestão de projetos e contabilística \> Folha de Horas** e selecione o parâmetro **Ativar Microsoft Dynamics 365 Project Timesheet**.

## <a name="sign-in-to-the-app"></a>Iniciar sessão na aplicação

1.  Inicie a aplicação no seu dispositivo móvel.

2.  Introduza o seu URL do Finance.

3.  Quando iniciar sessão pela primeira vez, ser-lhe-á solicitado o nome de utilizador e a palavra-passe. Introduza as suas credenciais.

4.  Iniciará sessão na sua empresa predefinida.

## <a name="submit-a-project-timesheet"></a>Enviar uma folha de horas do projeto

Pode criar e enviar uma folha de horas do projeto na aplicação. Pode basear uma nova folha de horas em informações de uma folha de horas anterior, linhas guardadas ou atribuições de projetos. Se for designado como delegado, também pode introduzir uma folha de horas para outro trabalhador. Para criar uma folha de horas como delegado, selecione o botão **Menu** e, em seguida, selecione um nome de recurso.

A página da folha de horas criará uma nova folha de horas para o período da folha de horas, baseado na data atual. Será apresentada a semana de trabalho. Se o período da folha de horas abranger várias semanas, poderá selecionar mais uma semana de trabalho a partir dos separadores da semana de trabalho.
Se existir uma folha de horas para a data atual, será apresentada. Se precisar de criar uma nova folha de horas num período de folhas de horas diferente, selecione o botão **Menu** e, em seguida, selecione **Nova folha de horas**.

Pode introduzir informações do projeto ao clicar na ação **Adicionar tempo** ou a ação **Copiar tempo de**. A ação **Copiar tempo de** copiará a informação da linha do projeto, mas não as horas. O menu **Copiar tempo de** inclui as seguintes opções:

- **Copiar a partir da folha de horas existente** - Copiar linhas de uma folha de horas existente.

- **Cópia a partir do favorito** - Crie novas linhas de folha de horas ao utilizar as definições da folha de horas que selecionou como favoritos.

- **Copiar a partir da atribuição** - Criar novas linhas da folha de horas a partir dos projetos atribuídos.

A informação do projeto que é apresentada depende dos parâmetros móveis que definiu na página **Parâmetros da gestão de projetos e contabilística**.

No campo **Entidade jurídica**, selecione a entidade jurídica para a qual executou o trabalho do projeto. O campo **Entidade jurídica** está disponível apenas se foi ativado o suporte de folhas de horas entre empresas para a sua entidade jurídica.

Selecione o cliente que está associado ao projeto para a folha de horas. Para o lançamento inicial em Android, a entrada pelo cliente não é suportada, porque primeiro tem de selecionar o projeto. Se selecionou o projeto primeiro, o campo **Cliente** é preenchido automaticamente.

No campo **Projeto**, selecione o projeto para o qual está a introduzir tempo. O campo **Cliente** é preenchido automaticamente.

As pesquisas de clientes e projetos permitem pesquisar tanto em clientes como em projetos.

Selecione a informação nos campos **Categoria**, **Atividade**, **Propriedade da linha**, **Grupo de impostos sobre vendas** e **Grupo de impostos sobre vendas de itens**, conforme necessário. Estes campos podem ser substituídos.

O campo **Propriedade da linha** será definido com um valor predefinido, baseado nos Parâmetros da Gestão de projetos e contabilística. Quando os parâmetros de projeto/categoria e categoria/recurso estão ativados, o valor **Propriedade da linha** será definido para o valor predefinido que definiu para esta validação. Quando os parâmetros de projeto/categoria e categoria/recurso não estão ativados, o valor **Propriedade da linha** assumirá como predefinição de acordo com o campo **Ativar propriedade da linha predefinida** na página **Parâmetros da gestão de projetos e contabilística**. O valor **Propriedade da linha** pode ser substituído.

Selecione um dia para adicionar tempo. Introduza o número de horas que trabalhou em cada dia.

Para adicionar comentários sobre as horas que está a introduzir, clique em **Adicionar comentários** e, em seguida, introduza comentários para uma audiência interna, audiência de clientes ou ambos.
Os comentários internos podem ser vistos pelos gestores de projetos. Os comentários dos clientes são incluídos nas faturas.

Para guardar a linha como favorito, selecione a caixa de verificação e, em seguida, clique em **Guardar como favorito**.

A dimensão financeira e o suporte de anexos não são fornecidos na aplicação móvel.

Continue a adicionar linhas do projeto conforme necessário para preencher a sua folha de horas.

Clique em **Enviar** para enviar a folha de horas para o fluxo de trabalho de aprovação.

## <a name="review-timesheets"></a>Rever folhas de horas

Está disponível no menu uma lista das folhas de horas que é necessário rever. Esta opção só está disponível se tiver sido designado como um aprovador do fluxo de trabalho. É suportada a aprovação do cabeçalho e da linha. A aprovação a nível da linha oferece a capacidade de marcar uma ou mais linhas para aprovação. Depois de rever as informações da folha de horas, clique em **Aprovar**, **Delegar** ou **Voltar** para prosseguir com o fluxo de trabalho.


[!INCLUDE[footer-include](../includes/footer-banner.md)]