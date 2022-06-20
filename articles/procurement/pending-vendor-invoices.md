---
title: Compra de materiais sem stock ou categorias de aquisição com uma fatura de fornecedor pendente
description: Este artigo explica como gravar faturas pendentes de fornecedores.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b1c05755f6759e90e031a11261f15a2c4b6b716e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922006"
---
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>Compra de materiais sem stock ou categorias de aquisição com uma fatura de fornecedor pendente

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

À medida que uma empresa adquire materiais sem stock ou categorias de aquisição para um projeto, os custos podem ser registados imediatamente em relação ao projeto. 

Por exemplo, a Contoso Robotics US está a realizar um projeto de renovação de equipamentos e precisa de licenças de software. Estas licenças são obtidas a partir de um fornecedor terceiro.  Utilizando o Dynamics 365 Finance, o escriturário das Contas a pagar regista um documento de fatura do fornecedor pendente e atribui os custos da licença diretamente ao projeto de renovação de equipamento. 

> [!IMPORTANT]
> Antes de utilizar a funcionalidade descrita neste artigo, reveja e aplique as configurações necessárias. Para mais informações, consulte [Ativar materiais sem stock e faturas pendentes do fornecedor](configure-materials-nonstocked.md) e [Usar categorias de aquisição com encomendas de compra de projeto e faturas de fornecedor pendentes](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>Publicar uma fatura pendente do fornecedor relacionada com o projeto 

As faturas pendentes do fornecedor podem ser registadas na página de **faturas pendentes do fornecedor** (**Contas a pagar** > **Faturas** > **Pendentes do fornecedor**). Complete os seguintes passos para publicar uma fatura pendente do fornecedor relacionada com o projeto:

1. Aceda a **Contas a pagar** > **Faturas** e selecione **Nova**. 
1. No campo **Conta da fatura**, selecione um fornecedor e, em seguida, no campo **Número**, insira a identificação da fatura do fornecedor.
1. Adicione uma linha à fatura do fornecedor e, em seguida, no campo **Número de item**, selecione o item sem stock que foi comprado ao fornecedor. Em alternativa, no campo **Categoria de aquisição**, selecione a categoria de aquisição que foi comprada ao fornecedor.   
1. Adicione a quantidade que foi comprada. O sistema preenche o preço unitário, com base na configuração de preço de item sem stock. 
1. Verifique o valor total e outros detalhes obrigatórios na linha.
1. Nos detalhes da linha, no separador **Projeto**, selecione o ID do projeto em que este item será registado.
1. Opcional: selecione o número da atividade e atualize a categoria do projeto e a propriedade de linha.
1. Publique a fatura do fornecedor pendente. Quando a fatura é publicada, o sistema regista as seguintes informações:
    
    - O valor do saldo do fornecedor.
    - O valor do imposto sobre vendas.
    - O custo contra o projeto é registado na conta de integração de contratos públicos.
    - A transação de custo real do projeto em Dataverse.  Esta transação é ainda processada através do [diário de Integração do Project Operations](../project-accounting/project-operations-integration-journal.md). A publicação deste diário transfere o montante da conta de integração de aquisições para a conta de custos do projeto. 
    - Compras faturadas ao cliente do projeto através do método de faturação de horas e materiais. Adicionalmente, são criadas transações de vendas não faturadas para as compras em Dataverse. A lista de preços do produto em Dataverse é utilizada para os preços de venda e os montantes da transação de venda não faturada.
