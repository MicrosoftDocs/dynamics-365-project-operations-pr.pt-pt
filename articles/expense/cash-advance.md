---
title: Adiantamento de tesouraria
description: Este tópico fornece informações sobre os adiantamentos de tesouraria.
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: c5839fbdab58903555936324139b76f4c94b6c35
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122763"
---
# <a name="cash-advance"></a>Adiantamento de tesouraria

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Um adiantamento de tesouraria permite que os colaboradores peçam dinheiro emprestado à respetiva empresa antes de incorrerem em quaisquer despesas. Quando um adiantamento de tesouraria pedido é aprovado e pago, o colaborador pode utilizar o dinheiro para as despesas empresariais que podem estar prestes a acontecer. 

## <a name="create-and-submit-a-cash-advance-request"></a>Criar e submeter um pedido de adiantamento de tesouraria

1. Em **As Minhas Despesas**, selecione **Adiantamentos de tesouraria** > **Novo** para criar um novo adiantamento de tesouraria. 
2. Na página **Novo pedido de adiantamento de tesouraria**, introduza a finalidade da despesa e selecione a localização onde a despesa será feita.
3. Introduza o montante e a moeda do pedido e, em seguida, selecione **Guardar**. 
4. Quando estiver pronto para submeter o pedido de adiantamento de tesouraria, na página **de adiantamento de tesouraria**, selecione **Fluxo de trabalho** > **Submeter**.

## <a name="modify-a-cash-advance-request"></a>Modificar um pedido de adiantamento de tesouraria

Pode modificar um pedido de adiantamento de tesouraria se não tiver sido submetido para aprovação.

1. Em **As Minhas Despesas: Adiantamentos de Tesouraria**, localize e selecione o adiantamento de tesouraria que pretende editar.
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

Quando cria e submete um relatório de despesas para o adiantamento de tesouraria que já recebeu, as despesas serão ajustadas automaticamente face a esse adiantamento. Se o seu adiantamento de tesouraria for superior ao montante gasto, tem de devolver o saldo à empresa através da categoria de despesa **Devolver dinheiro**. Se o adiantamento de tesouraria pago pela empresa for inferior ao montante gasto, a empresa terá de reembolsar-lhe o saldo. 

### <a name="example"></a>Exemplo
Planeia viajar para uma conferência de Seattle para a Cidade de Nova Iorque. Crie um pedido de adiantamento de tesouraria de 3000 USD, uma vez que a estimativa de custo do bilhete, voos, hotel, refeições e táxi para ir à conferência tem este valor aproximado. Não lhe será pago a menos que o seu gestor tenha aprovado este pedido. Após a aprovação do seu gestor, o adiantamento de tesouraria pedido é pago sob a forma de 3000 USD na sua conta bancária. Participa na conferência. Depois de concluída a viagem, descobre que a despesa total foi de apenas 2790 USD. Selecione **Numerário** no campo **Método de pagamento** e submeta as suas despesas para 2790 USD. O montante de despesas submetido é ajustado automaticamente em relação ao adiantamento de tesouraria de 3000 USD que lhe foi emprestado. Deve agora um saldo de 210 USD (3000-2790) à empresa, que pode devolver à empresa através da categoria de despesas **Devolver dinheiro**. 
