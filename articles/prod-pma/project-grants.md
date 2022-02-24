---
title: Concessões de projeto
description: Este tópico explica como criar ou modificar um concessão.
author: RadhikaRS
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 89801696d6a2924d78c85f6e9b4281409222dbb0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082585"
---
# <a name="project-grants"></a>Concessões de projeto

[!include [banner](../includes/banner.md)]

Uma concessão é uma dádiva de dinheiro para um propósito ou projeto específico. Normalmente, existem restrições sobre como uma concessão pode ser gasta. Na Gestão de projetos e contabilística, pode introduzir e monitorizar concessões, e definir as respetivas relações a projetos e contratos de projetos. Por exemplo, pode efetuar as seguintes tarefas:

- Associar concessões com projetos e fontes de financiamento através de ligações para as páginas **Projeto** e **Detalhes do contrato do projeto**.
- Introduza e monitorize as alterações a uma concessão à medida que passa de um estado para outro.
- Introduza e monitorize custos, montantes solicitados e montantes atribuídos.
- Crie concessões principais e associe-lhes subconcessões.

Pode criar uma concessão introduzindo todos os detalhes num novo registo, ou pode copiar os detalhes de uma concessão existente e, em seguida, atualizá-los.

## <a name="create-a-new-grant"></a>Criar uma nova concessão

1. Vá a **Gestão de projetos e contabilística** \> **Concessões** \> **Concessões**.
2. Selecione **Nova** \> **Concessão**.
3. Na página de detalhes da concessão, no Separador Rápido **Geral**, no campo **ID da Concessão**, introduza um identificador alfanumérico para a concessão.
4. No campo **Nome da concessão**, introduza um nome exclusivo para a concessão.
5. No campo **Descrição**, adicione detalhes sobre a nova concessão.

    A maioria dos outros campos na página são opcionais, e pode inserir a quantidade de informação que quiser.

    A lista que se segue descreve as informações especificadas em cada Separador Rápido da página de detalhes da concessão:

    - **Geral** – Introduza o nome, estado, descrição, finalidade e montante da concessão.
    - **Informações de contacto** – Introduza detalhes sobre os colaboradores, o departamento que gere a concessão, e o cliente ou origem de organização da concessão. Também pode indicar se a sua organização é uma entidade pass-through que recebe a concessão e, em seguida, passa-a para outro destinatário. Selecione **Adicionar** para adicionar informações de contacto, tais como números de telefone e endereços de e-mail para a organização que fornece a concessão.
    - **Datas e prazos** – Introduza datas relacionadas com a concessão e o pedido de concessão. Exemplos incluem a data de vencimento da aplicação, a data de apresentação e a data em que a concessão é aprovada ou rejeitada.
    - **Projetos associados e contratos de projeto** – Só pode introduzir informações sobre este Separador Rápido se o campo **Estado da concessão** no Separador Rápido **Geral** estiver definido para **Ativa** ou **Atribuída**. Selecione entre as seguintes opções para completar a tarefa relacionada:

        - **Adicionar fonte de financiamento** – Adicione uma nova fonte de financiamento para a concessão. Pode introduzir todos os detalhes agora, ou pode usar informações predefinidas e, em seguida, atualizá-la mais tarde.
        - **Adicionar contrato de projeto** – Adicione ou atualize informações sobre contratos de projeto.
        - **Adicionar projeto** – Adicionar ou atualizar detalhes do projeto.

    - **Configuração** – Introduza detalhes sobre fundos de correspondência, se estas informações forem necessárias. Muitas organizações que concedem concessões exigem que os beneficiários gastem uma quantidade específica do seu próprio dinheiro ou recursos, para corresponder ao montante que é atribuído na concessão. No campo **Projeto local ou ID de monitorização**, pode introduzir um identificador que difere do identificador do projeto.

        > [!NOTE]
        > Se uma parte da concessão for atribuída a uma organização diferente, defina a opção **Sub-outorgante** para **Sim**. Para as concessões atribuídas nos Estados Unidos, pode especificar se uma concessão será atribuída ao abrigo de um mandato estatal ou de um mandato federal.

    - **Detalhes da redução** – Adicionar ou atualizar informações sobre a frequência com que os fundos de concessão podem ser retirados, faturados ou gastos.

## <a name="create-a-new-grant-from-a-copy"></a>Criar uma nova concessão a partir de uma cópia

1. Vá a **Gestão de projetos e contabilística** \> **Concessões** \> **Concessões**.
2. Selecione **Nova** \> **Cópia a partir da concessão**.
3. Introduza um identificador alfanumérico e um nome para a nova concessão e, em seguida, selecione **OK**.
4. Na página de detalhes da concessão, reveja os detalhes da concessão copiada e faça quaisquer alterações que sejam necessárias. A maioria dos campos na página são opcionais.

## <a name="view-or-modify-grant-details"></a>Ver ou modificar detalhes da concessão

1. Vá a **Gestão de projetos e contabilística** \> **Concessões** \> **Concessões**.
2. Selecione a concessão a modificar.
3. No Painel de Ação, no separador **Concessão**, no grupo **Manter**, selecione **Editar**.
4. Reveja os detalhes da concessão e faça quaisquer alterações que sejam necessárias.
