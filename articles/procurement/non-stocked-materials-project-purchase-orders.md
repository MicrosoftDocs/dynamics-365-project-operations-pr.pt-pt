---
title: Encomendar materiais não existentes em stock para um projeto através de notas de encomenda do projeto
description: Este tópico explica como encomendar materiais não existentes em stock para um projeto através de notas de encomenda do projeto.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6e0307ad6474feef96fc8080877eccbbbc7259db
ms.sourcegitcommit: 2d96345fb3afc3b174530285f95271b5ccbdea03
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7563036"
---
# <a name="order-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Encomendar materiais não existentes em stock para um projeto através de notas de encomenda do projeto

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

O Departamento de aprovisionamento da sua organização pode utilizar [notas de encomenda](/dynamics365/supply-chain/procurement/purchase-order-overview) para monitorizar bens e ordens de serviços. As notas de encomenda de materiais não existentes em stock podem ser atribuídas a um projeto. A faturação destas notas de encomenda regista o custo em relação ao projeto.

## <a name="prerequisites"></a>Pré-requisitos
Conclua os passos a seguir para ativar a funcionalidade de notas de encomenda do projeto.

1. No Dynamics 365 Finance, vá para a área de trabalho **Gestão de Funcionalidades**.
2. Na lista de funcionalidades, encontre e selecione a funcionalidade **Ativar notas de encomenda no Project Operations para cenários baseados em recursos/itens não existentes em stock**.
3. Selecione **Ativar**.
4. Configure os materiais não existentes em stock e as faturas de fornecedores pendentes como descrito em [Configurar materiais não existentes em stock e faturas de fornecedores pendentes](configure-materials-nonstocked.md).

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Criar a nota de encomenda de um projeto a partir da lista de notas de encomenda do projeto

1. No Finance, aceda a **Gestão e contabilidade de projetos** > **Projetos** > **Todos os Projetos** e selecione um projeto.
2. No Painel de Ações, no separador **Gerir**, no grupo **Novo**, selecione **Tarefa de item** > **Nota de encomenda**.
3. Na página **Criar nota de encomenda**, selecione o fornecedor ao qual pretende atribuir a nota de encomenda, introduza outras informações pertinentes e, em seguida, selecione **OK**.
4. Na página **Nota de encomenda**, na grelha **Linha da nota de encomenda**, selecione **Adicionar linha**.
5. Introduza um número de item, a quantidade, a unidade, o preço unitário e outras informações pertinentes.

    > [!NOTE]
    > Só é possível utilizar serviços e itens não existentes em stock com notas de encomenda do projeto. Os itens em stock e as categorias de aprovisionamento não são suportados.

6. Continue a adicionar itens conforme necessário e confirme a nota de encomenda.

    Os recibos de bens e serviços podem ser registados através da criação e do registo de um recibo do produto.

    > [!NOTE]
    > Os recibos de produtos não são registados nos valores reais do projeto no Microsoft Dataverse e não afetam o sub-razão do projeto.

    Depois de um fornecedor enviar a fatura dos itens e serviços na nota de encomenda, o departamento de aprovisionamento pode gerar uma fatura para a nota de encomenda ao aceder a **Fatura** > **Gerar** > **Fatura** no Painel de Ações. Para obter mais informações sobre as faturas de fornecedores pendentes, consulte [Comprar materiais não existentes em stock através de uma fatura de fornecedor pendente](pending-vendor-invoices.md).
