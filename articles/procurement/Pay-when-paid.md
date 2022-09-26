---
title: Pagamentos de fornecedor paga quando pago
description: Este tópico explica como utilizar o cenário de pagamento paga quando pago (PWP).
author: mukumarm
ms.date: 08/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: mukumarm
ms.openlocfilehash: d1fe8d92663b31b22dc405fc1f3e06d976e6c5dc
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/16/2022
ms.locfileid: "9525344"
---
# <a name="pay-when-paid-vendor-payments"></a>Pagamentos de fornecedor paga quando pago

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Este tópico explica como utilizar o cenário de pagamento paga quando pago (PWP).

## <a name="create-a-purchase-order-that-has-pwp-terms"></a>Criar uma nota de encomenda que tenha termos PWP

Quando publica uma fatura de um fornecedor, se o fornecedor estiver sujeito a termos PWP, esses termos são mostrados nas linhas da nota de encomenda (NE). Para criar uma NE que tenha termos PWP, siga estes passos.

1. No Microsoft Dynamics 365 Finance, siga um destes passos:

    - Vá à **Aprovisionamento e Fornecimento** \> **Notas de encomenda** \> **Todas as notas de encomenda**. No Painel de Ação, selecione **Novo**. Na caixa de diálogo **Criar nota de encomenda**, selecione o fornecedor para o qual estão configurados os termos PWP no projeto, introduza outras informações necessárias e, em seguida, selecione **OK**.
    - Vá para **Gestão de projetos e contabilística** \> **Projetos** \> **Todos os projetos**. No Painel de Ação, no separador **Gerir**, selecione **Tarefa do item**. Selecione a nota de encomenda. Selecione o fornecedor para o qual estão configurados os termos PWP no projeto e, em seguida, selecione **OK**.

2. Na página **Nota de encomenda**, no separador **Linhas da ordem encomenda**, selecione **Adicionar linha** para criar uma linha de nota de encomenda.
3. Selecione o número do item ou a categoria de aprovisionamento e, em seguida, introduza os outros detalhes necessários. Reveja os detalhes da linha da NE para o fornecedor.

    A opção **Paga quando pago** é selecionada automaticamente e o valor no campo **Percentagem de limiar PWP** é automaticamente copiado do campo **Percentagens de limiar PWP** na página **Projetos**.

4. Se não quiser aplicar os termos PWP ao fornecedor para uma linha de NE, limpe a opção **Paga quando pago**. Neste caso, o campo **Percentagem de limiar PWP** para a linha de NE será reposto para **0** (zero).
5. Na página **Nota de encomenda**, no Painel de Ações, no separador **Compra** , selecione **Confirmar** para confirmar a nota de encomenda.
6. No Painel de Ações, no separador **Fatura**, selecione **Fatura** para gerar a fatura para a nota de encomenda.

## <a name="create-a-project-invoice-proposal"></a>Crie uma proposta de fatura do projeto

As propostas de fatura do projeto são utilizadas para criar faturas do projeto para o cliente. No cenário PWP, os pagamentos aos fornecedores dependem dos pagamentos dos clientes, de acordo com as definições de PWP. No entanto, existem opções que lhe permitem libertar os pagamentos sem pagamento dos clientes, conforme necessário. Para criar uma fatura de projeto para o cliente, siga estes passos.

1. Em aplicações de cativação de clientes, aceda a **Projeto** \> **Projetos** e selecione o projeto.
2. No separador **Valores Reais**, selecione a linha real que é gerada pela NE que tem o tipo de transação **Vendas não Faturadas**. Em seguida, selecione **Pronto para faturar**.
3. Aceda a **Sales** \> **Vendas** \> **Contrato do projeto** e selecione o contrato do projeto.
4. No Painel de Ação, selecione **Fatura** para gerar a fatura do cliente.
5. No Finance. vá à **Gestão de projetos e contabilidade** \> **Periódico** \> **Importar da tabela de teste** e selecione **OK** para gerar o diário de integração do Project Operations.
6. Aceda a **Gestão de projetos e contabilidade** \> **Faturas do projeto** \> **Proposta de fatura do projeto** e selecione **Publicar** para publicar a proposta de fatura que foi gerada para o projeto.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Atualize um pagamento do cliente e pague ao fornecedor

Quando um fornecedor conclui o seu trabalho num projeto e lhe envia uma fatura, deve rever o estado do projeto e as faturas dos clientes para determinar se os termos PWP foram cumpridos para o projeto. Se os termos PWP para o fornecedor forem cumpridos, pode determinar quais as linhas na fatura do fornecedor a pagar, com base nos pagamentos do cliente para o projeto. Se decidir pagar ao fornecedor mesmo que os termos PWP não tenham sido cumpridos, pode anular os termos PWP na página **Fatura do fornecedor com paga quando pago**.

1. No Finance, aceda a **Gestão de projetos e contabilidade** \> **Projetos** \> **Todos os projetos** e selecione o projeto.
2. No Painel de Ação, selecione **Controlo** e, em seguida, selecione **Faturas de fornecedor** para mostrar todas as faturas de fornecedor que foram geradas para o projeto.
3. Na página **Faturas do fornecedor com paga quando pago**, no campo de pesquisa, introduza valores para encontrar a fatura do fornecedor que pretende rever e, em seguida, selecione **Pesquisar**.
4. Selecione a opção **Pagar quando pago** para ver apenas faturas PWP.
5. No Separador Rápido **Linhas de fatura do fornecedor**, selecione as linhas que pretende lançar para pagamento.
6. Selecione **Lançar pagamento de fornecedor**. A opção **Paga quando pago** é desselecionada e o valor do campo **Pronto para pagamento** é alterado para **Sim**.
