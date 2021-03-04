---
title: Adiantamento de tesouraria
description: Este tópico fornece informações sobre os adiantamentos de tesouraria.
author: suvaidya
manager: AnnBe
ms.date: 02/01/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 58864790720824cecad8ce1ff7ff0a335a42cc03
ms.sourcegitcommit: 7aa0b7fb22213d8baa2d69efece9a636d9f62493
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/01/2021
ms.locfileid: "5098898"
---
# <a name="cash-advance"></a>Adiantamento de tesouraria

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Um adiantamento de tesouraria permite que os colaboradores peçam dinheiro emprestado à respetiva empresa antes de incorrerem em quaisquer despesas. Quando um adiantamento de tesouraria pedido é aprovado e pago, o colaborador pode utilizar o dinheiro para as despesas empresariais que podem estar prestes a acontecer. 

## <a name="create-and-submit-a-cash-advance-request"></a>Criar e submeter um pedido de adiantamento de tesouraria
Para criar um novo adiantamento em dinheiro e apresentar um pedido de adiantamento em numerário, faça o seguinte: 

1. Em **As minhas despesas**, selecione **Adiantamentos de dinheiro** > **Novo**. 
2. Na página **Novo pedido de adiantamento de tesouraria**, introduza a finalidade da despesa e selecione a localização onde a despesa será feita.
3. Introduza o montante e a moeda do pedido e, em seguida, selecione **Guardar**. 
4. Quando estiver pronto para submeter o pedido de adiantamento de tesouraria, na página **de adiantamento de tesouraria**, selecione **Fluxo de trabalho** > **Submeter**.

## <a name="modify-a-cash-advance-request"></a>Modificar um pedido de adiantamento de tesouraria

Pode modificar um pedido de adiantamento de tesouraria se não tiver sido submetido para aprovação.

1. Em **As minhas despesas: Adiantamentos de dinheiro** localize e selecione o adiantamento em dinheiro que pretende editar.
2. Selecione **Editar** e faça as alterações necessárias ao pedido de adiantamento de tesouraria. 
3. Selecione **Guardar e fechar**.


## <a name="view-cash-advance-requests"></a>Ver pedidos de adiantamento de tesouraria
Pode rever a lista de todos os adiantamentos de tesouraria que estão em rascunho, submetidos, em revisão ou pagos em **As Minhas Despesas: Adiantamentos de Tesouraria**. 

## <a name="approve-cash-advance-requests"></a>Aprovar pedidos de adiantamento de tesouraria

Os gestores ou utilizadores configurados como aprovadores no fluxo de trabalho poderão aprovar os adiantamentos de tesouraria que lhes são submetidos para revisão. 

1. Para aprovar um adiantamento de tesouraria, em **Processar adiantamentos de tesouraria**, selecione **Adiantamentos de tesouraria para minha revisão**.
2. Selecione o adiantamento de tesouraria que precisa para rever e selecione **Aprovar**.  

## <a name="pay-cash-advances"></a>Pagar adiantamentos de tesouraria 
Normalmente, o seguinte procedimento é feito por um contabilista ou um utilizador com permissões contabilísticas.

1. Para publicar adiantamentos de tesouraria aprovados, selecione **Adiantamentos de tesouraria aprovados** e, em seguida, selecione **Pagar e transferir**.  
2. Forneça os detalhes do diário para os adiantamentos de tesouraria e, em seguida, selecione **OK**. 

## <a name="submit-an-expense-report-against-a-paid-cash-advance"></a>Submeter um relatório de despesas para um adiantamento de tesouraria pago 

Quando criar e apresentar um relatório de despesas para o adiantamento de dinheiro que já recebeu, as despesas serão automaticamente ajustadas face a esse adiantamento. Se o seu adiantamento de tesouraria for superior ao montante gasto, tem de devolver o saldo à empresa através da categoria de despesa **Devolver dinheiro**. Se o adiantamento em dinheiro pago pela empresa for inferior ao valor que gastou, a empresa deve reembolsar-lhe o saldo. 

### <a name="example"></a>Exemplo
Planeia viajar de Seattle para Nova Iorque para uma conferência. Cria um pedido de adiantamento de dinheiro para 3000,00 USD com base no custo estimado do bilhete da conferência, voos, hotel, refeições e táxi. Não será pago a menos que o seu gestor aprove este pedido. Após a aprovação do seu gestor, o adiantamento de tesouraria pedido é pago sob a forma de 3000 USD na sua conta bancária. Participa na conferência. Depois de concluída a viagem, descobre que a despesa total foi de apenas 2790 USD. Selecione **Dinheiro** no campo **Método de pagamento** e submeta as suas despesas de 2790,00 USD. O montante de despesas submetido é ajustado automaticamente em relação ao adiantamento de tesouraria de 3000 USD que lhe foi emprestado. Deve agora um saldo de 210,00 USD (3000,00 - 2790,00), que pode devolver à empresa utilizando a categoria de despesas **Devolução de dinheiro**.

