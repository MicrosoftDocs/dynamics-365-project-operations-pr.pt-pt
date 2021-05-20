---
title: Comprar materiais não armazenados utilizando uma fatura pendente do fornecedor
description: Este tópico explica como registar faturas pendentes do fornecedor.
author: sigitac
manager: tfehr
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7a706f419443dcdf92ce3b247d719943272907d0
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880674"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a>Comprar materiais não armazenados utilizando uma fatura pendente do fornecedor

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

À medida que uma empresa adquire materiais não armazenados para um projeto, os custos podem ser imediatamente registados contra o projeto. 

Por exemplo, a Contoso Robotics US está a realizar um projeto de renovação de equipamentos e precisa de licenças de software. Estas licenças são obtidas a partir de um fornecedor terceiro.  Utilizando Dynamics 365 Finance, o escriturário das Contas a pagar regista um documento de fatura do fornecedor pendente e atribui os custos da licença diretamente contra o projeto de renovação do equipamento. 

> [!IMPORTANT]
> Antes de utilizar a funcionalidade descrita neste tópico, reveja e aplique as configurações necessárias. Para obter mais informações, consulte [Ativar materiais não armazenados e faturas pendentes do fornecedor](configure-materials-nonstocked.md). 

## <a name="post-a-project-related-pending-vendor-invoice"></a>Publicar uma fatura pendente do fornecedor relacionada com o projeto 

As faturas pendentes do fornecedor podem ser registadas na página de **faturas pendentes do fornecedor** (**Contas a pagar** > **Faturas** > **Pendentes do fornecedor**). Complete os seguintes passos para publicar uma fatura pendente do fornecedor relacionada com o projeto:

1. Vá a **Contas a pagar** > **Faturas** e selecione **Nova**. 
2. No campo **Conta da fatura**, selecione um fornecedor e no campo **Número**, introduza a identificação da fatura do fornecedor.
3. Adicione uma linha à fatura do fornecedor e no campo **número do artigo**, selecione o artigo não armazenado comprado ao fornecedor. 

    > [!NOTE]
    > As linhas de fatura do fornecedor que se baseiam numa categoria de compras não podem ser registadas contra o projeto. 
    
5. Adicionar a quantidade comprada. O sistema preencherá o preço unitário com base na configuração do preço do artigo não armazenado. 
6. Verifique o valor total e outros detalhes obrigatórios na linha.
7. Nos detalhes da linha, no separador **Projeto**, selecione o ID do projeto para o quais este artigo será gravado.
8. Opcionalmente, selecione o número de atividade e atualize a categoria de projeto e propriedade de linha.
9. Publique a fatura pendente do fornecedor. Quando a fatura é publicada, o sistema regista:
    
    - O valor do saldo do fornecedor.
    - O valor do imposto sobre vendas.
    - O custo contra o projeto é registado na conta de integração de contratos públicos.
    - A transação real do projeto em Dataverse. Esta transação é ainda processada através do [diário de Integração do Project Operations](../project-accounting/project-operations-integration-journal.md). A publicação deste diário transfere o montante da conta de integração de aquisições para a conta de custos do projeto.
