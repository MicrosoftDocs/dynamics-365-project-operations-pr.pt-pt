---
title: Configurar e utilizar pagamentos de fornecedor paga quando pago
description: Este tópico explica como criar termos paga quando pago (PWP) para que possa libertar pagamentos parciais de fornecedores, com base nos pagamentos dos clientes.
author: RadhikaRS
manager: AnnBe
ms.date: 03/30/2020
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
ms.openlocfilehash: e872c4a2d35cef4cddc6851615c6c4d73b4e9d9a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082383"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a>Configurar e utilizar pagamentos de fornecedor paga quando pago

[!include [banner](../includes/banner.md)]

Quando aprova um fornecedor para trabalhar como subcontratado, poderá pretender reter o pagamento ao fornecedor até que o seu cliente lhe pague pelo projeto. Para suportar este cenário, pode configurar os termos de paga quando pago (PWP) quando configurar a nota de encomenda (PO) com o fornecedor.

Por exemplo, quando um cliente paga um valor numa fatura do projeto, pode libertar parte ou o total do montante da fatura do fornecedor. Basta configurar os termos PWP que especificam se o fornecedor será pago depois de receber uma percentagem do pagamento relacionado do cliente. Se receber o pagamento parcial de um cliente, pode libertar manualmente algumas das faturas relacionadas do fornecedor para pagamento.

O exemplo a seguir descreve o processo quando são utilizados os termos PWP.

## <a name="example"></a>Exemplo

A sua organização concorda em fornecer a um cliente 100 computadores que tenham software instalado, por um preço de 150,00 dólares americanos (USD) por computador. Em seguida, contrata um fornecedor para lhe fornecer os computadores que têm software instalado. De acordo com o contrato, o cliente deve aprovar a qualidade dos computadores antes de pagar à sua organização. A política da sua organização é reter o pagamento aos fornecedores até que o cliente lhe pague. Por isso, configura o projeto para que tenha uma percentagem PWP de 100 por cento.

O fornecedor envia-lhe os 100 computadores que têm software instalado, juntamente com uma fatura para 10.000,00 USD. Como os termos PWP estão configurados para o seu projeto, não paga ao fornecedor após a receção dos computadores. Em vez disso, envia os computadores para o cliente, juntamente com uma fatura para 15.000,00. O cliente inspeciona os computadores e aprova a totalidade da fatura do projeto.

Depois de receber o pagamento total do cliente, paga ao vendedor 10.000,00, o valor total da fatura do fornecedor.

## <a name="set-up-pwp-terms-for-a-project"></a>Configurar termos PWP para um projeto

Ao configurar os termos PWP para um projeto, deve especificar, em percentagem, o montante mínimo que um cliente deve pagar-lhe pelo projeto antes de pagar ao fornecedor. O limiar é calculado automaticamente nas faturas do cliente para o projeto. Siga estes passos para configurar a percentagem de limiar para os termos PWP.

1. Vá para **Gestão de projetos e contabilística** \> **Projetos** \> **Todos os projetos**.
2. Encontre e abra o projeto para o qual pretende configurar os termos PWP.
3. No Separador Rápido **Contratos de fornecedor**, selecione **Adicionar linha**.
3. No campo **Código da conta**, selecione uma das seguintes opções:

    - **Tabela** – Os termos PWP aplicam-se a um único fornecedor.
    - **Grupo** – Os termos PWP aplicam-se a todos os fornecedores de um grupo de fornecedores.
    - **Todos** – Os termos PWP aplicam-se a todos os fornecedores.

4. Se selecionou **Tabela** ou **Grupo** no passo anterior, no campo **Fornecedor/Grupo de Fornecedores**, selecione o fornecedor ou grupo de fornecedores a que os termos PWP se aplicam. Se selecionou **Todos** no passo anterior, o campo **Fornecedor/Grupo de Fornecedores** não pode ser editado.
5. Se forem configurados termos de sinal do fornecedor para o fornecedor no projeto, no campo **Termos de sinal do fornecedor**, selecione o ID da regra para os termos de sinal.
6. No campo **Percentagens de limiar PWP**, introduza a percentagem de limiar para o projeto. A percentagem que inseriu para o projeto define o valor mínimo que o cliente deve pagar antes de pagar ao vendedor.

## <a name="create-a-po-that-has-pwp-terms"></a>Criar um NE que tenha termos PWP

Quando publica uma fatura de um fornecedor, se o fornecedor estiver sujeito a termos PWP, esses termos são mostrados nas linhas da NE. Para criar uma NE que tenha termos PWP, siga estes passos.

1. Vá à **Aprovisionamento e Fornecimento** \> **Notas de encomenda** \> **Todas as notas de encomenda**.
2. No Painel de Ação, selecione **Novo**. Em seguida, na caixa de diálogo **Criar nota de encomenda**, introduza as informações necessárias e selecione **OK**.

    Em alternativa, abra uma NE existente na página de lista **Todas as notas de encomenda**.

4. Na página **Notas de encomendas**, no Separador Rápido **Linhas de notas de encomenda**, reveja os detalhes da linha de NE para o fornecedor. A opção **Paga quando pago** é selecionada automaticamente e o valor no campo **Percentagem de limiar PWP** é automaticamente copiado do campo **Percentagens de limiar PWP** na página **Projetos**.
6. Se não quiser aplicar os termos PWP ao fornecedor para uma linha de NE, limpe a opção **Paga quando pago**. Neste caso, o campo **Percentagens de limiar PWP** para a linha de NE será reposto para 0 (zero).

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Atualize um pagamento do cliente e pague ao fornecedor

Quando um fornecedor conclui o seu trabalho num projeto e lhe envia uma fatura, deve rever o estado do projeto e as faturas dos clientes para determinar se os termos PWP foram cumpridos para o projeto. Se os termos PWP para o fornecedor forem cumpridos, pode determinar quais as linhas na fatura do fornecedor a pagar, com base nos pagamentos do cliente para o projeto. Se decidir pagar ao fornecedor mesmo que os termos PWP não tenham sido cumpridos, pode anular os termos PWP na página **Fatura do fornecedor com paga quando pago**.

1. Vá à **Gestão de projetos e contabilística** \> **Inquéritos e relatórios** \> **Inquéritos de sinal** \> **Fatura de fornecedor com paga quando pago**.
2. Na página **Faturas do fornecedor com paga quando pago**, no campo de pesquisa, introduza valores para encontrar a fatura do fornecedor que pretende rever e, em seguida, selecione **Pesquisar**.
3. No Separador Rápido **Linhas de fatura do fornecedor**, selecione as linhas que pretende alterar.
4. Se as condições **Paga quando pago** forem cumpridas para a linha de fatura, selecione **Libertar pagamento ao fornecedor**. A opção **Paga quando pago** é desselecionada e o valor do campo **Pronto para pagamento** é alterado para **Sim**.
