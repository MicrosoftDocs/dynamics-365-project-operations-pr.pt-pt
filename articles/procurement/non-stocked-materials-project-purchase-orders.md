---
title: Encomendar materiais não existentes em stock para um projeto através de notas de encomenda do projeto
description: Este artigo explica como encomendar materiais não existentes em stock para um projeto através de notas de encomenda do projeto.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fe24faa143869af2396f3b0f28aae31417cadda7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929826"
---
# <a name="order-procurement-categories-or-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Encomende categorias de aquisição ou materiais sem stock para um projeto utilizando as encomendas de compra de projeto

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

O Departamento de aprovisionamento da sua organização pode utilizar [notas de encomenda](/dynamics365/supply-chain/procurement/purchase-order-overview) para monitorizar bens e ordens de serviços. Encomendas de compra para categorias de aquisição ou materiais sem stock podem ser atribuídas a um projeto. A faturação destas notas de encomenda regista o custo em relação ao projeto.

## <a name="prerequisites"></a>Pré-requisitos
Conclua os passos a seguir para ativar a funcionalidade de notas de encomenda do projeto.

1. No Dynamics 365 Finance, aceda à área de trabalho **Gestão de funcionalidades**.
2. Na lista de funcionalidades, encontre e selecione a funcionalidade **Ativar notas de encomenda no Project Operations para cenários baseados em recursos/itens não existentes em stock**.
3. Selecione **Ativar**.
4. Configure os materiais não existentes em stock e as faturas de fornecedores pendentes como descrito em [Configurar materiais não existentes em stock e faturas de fornecedores pendentes](configure-materials-nonstocked.md).
5. Configure categorias de aquisição como descrito em [Utilizar categorias de aquisição com encomendas de compra de projeto e faturas de fornecedor pendentes](configure-procurement-categories.md).

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Criar a nota de encomenda de um projeto a partir da lista de notas de encomenda do projeto

1. No Finance, aceda a **Gestão e contabilidade de projetos** > **Projetos** > **Todos os Projetos** e selecione um projeto.
2. No Painel de Ações, no separador **Gerir**, no grupo **Novo**, selecione **Tarefa de item** > **Nota de encomenda**.
3. Na página **Criar nota de encomenda**, selecione o fornecedor ao qual pretende atribuir a nota de encomenda, introduza outras informações pertinentes e, em seguida, selecione **OK**.
4. Na página **Nota de encomenda**, na grelha **Linha da nota de encomenda**, selecione **Adicionar linha**.
5. Introduza um número de item ou categoria de aquisição, quantidade, unidade, preço unitário e outras informações pertinentes.

    > [!NOTE]
    > Só é possível utilizar categorias de aquisição, itens sem stock e serviços com encomendas de compra do projeto. Os itens em stock não são suportados.

6. Continue a adicionar itens ou categorias de aquisição conforme necessário e confirme a encomenda de compra.

    Os recibos de bens e serviços podem ser registados através da criação e do registo de um recibo do produto.

    > [!NOTE]
    > Os recibos de produtos não são registados nos valores reais do projeto no Microsoft Dataverse e não afetam o sub-razão do projeto.

    Depois de um fornecedor enviar a fatura dos itens e serviços na nota de encomenda, o departamento de aprovisionamento pode gerar uma fatura para a nota de encomenda ao aceder a **Fatura** > **Gerar** > **Fatura** no Painel de Ações. Para obter mais informações sobre as faturas de fornecedores pendentes, consulte [Comprar materiais não existentes em stock através de uma fatura de fornecedor pendente](pending-vendor-invoices.md).
