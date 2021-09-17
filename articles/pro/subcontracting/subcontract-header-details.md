---
title: Detalhes do cabeçalho para subcontratos
description: Este tópico explica a funcionalidade fornecida no cabeçalho do subcontrato no Project Operations.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 49158af1a430033db3a5db57a840512c45bc17e2
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323655"
---
# <a name="header-details-for-subcontracts"></a>Detalhes do cabeçalho para subcontratos

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

Este tópico explica a funcionalidade fornecida no cabeçalho do subcontrato no Dynamics 365 Project Operations.

Como um Gestor de Projeto planeia e executa projetos, pode empregar subcontratantes e comprar produtos e serviços de fornecedores. Quando um Gestor de Projeto necessita de comprar produtos ou serviços, pode criar um subcontrato no Project Operations.

Para criar um subcontrato, execute os seguintes passos.

1. No painel de navegação, selecione **Subcontratos** e na página **Subcontrato**, selecione **Novo**.
2. Introduza as informações necessárias e selecione **Guardar**.

    A tabela seguinte fornece informações sobre os campos na página Cabeçalho do subcontrato.

    | **Campo** | **Descrição** |
    | --- | --- | 
    | Nome | O nome do subcontrato. |
    | Descrição | Uma breve descrição dos serviços e produtos que estão a ser comprados no subcontrato. |
    | Fornecedor | O nome da empresa à qual os produtos e serviços estão a ser comprados. Este registo de conta tem um tipo de relação de **Fornecedor** ou **Prestador**. |
    | Data do Subcontrato | A data em que o subcontrato é criado. |
    | Razão do Estado | O estado do subcontrato. |
    | Moeda | A moeda na qual os produtos e serviços são comprados. O valor neste campo é o valor predefinido da conta do fornecedor, mas pode ser alterado. As listas de preços do projeto, que são utilizadas na definição do preço de produtos e serviços nos subcontratos, devem utilizar esta moeda. As listas de preços em qualquer outra moeda não podem ser associadas ao subcontrato. O custo dos produtos e serviços incorrido neste subcontrato será registado no projeto nesta moeda. |
    | Unidade de Contratação | A divisão da empresa que está a celebrar um contrato ou um subcontrato de compra com o fornecedor. |
    | Prazos de pagamento | Os termos de pagamento nas faturas do fornecedor emitidas neste subcontrato. O valor neste campo é o valor predefinido do registo de conta do fornecedor. |
    | Endereço de Pagamento | O endereço para onde é enviado o pagamento das faturas do fornecedor. O valor neste campo é o valor predefinido do registo de conta do fornecedor. |
    | Nome para Faturação | O nome da pessoa ou divisão na empresa do fornecedor que enviará a fatura. O valor neste campo é o valor predefinido do registo de conta do fornecedor e será utilizado como o nome do contacto principal nas faturas do fornecedor criadas para este subcontrato. |
    | Morada para Faturação | O endereço utilizado nas faturas deste fornecedor. O valor neste campo é o valor predefinido do registo de conta do fornecedor. Este endereço também é utilizado como o endereço da fatura nas faturas do fornecedor criadas para este subcontrato. |
    | Subtotal | Se um subcontrato não tiver linhas, introduza um valor neste campo que indique o subtotal da encomenda antes de incluir os impostos. Se o subcontrato tiver linhas, este campo é só de leitura. O montante apresentado é o subtotal de todas as linhas no subcontrato. |
    | Imposto Total | Se um subcontrato não tiver linhas, introduza um valor neste campo que indique os impostos neste subcontrato. Se o subcontrato tiver linhas, este campo é só de leitura. O montante apresentado é a soma do montante do imposto de todas as linhas no subcontrato. |
    | Montante Total |  Este campo calculado mostra o montante total do subcontrato com os impostos.  |
    | Data Confirmada | A data em que o subcontrato foi confirmado.  |
    | Pretendido Por | O valor predefinido neste campo é o nome do utilizador que cria o subcontrato. Este valor pode ser alterado pelo criador do subcontrato para indicar a pessoa que está a criar o subcontrato em nome de outra pessoa.  |
    | Gestor de Contas do Fornecedor | O nome do contacto principal da conta do fornecedor. O valor neste campo é o valor predefinido do registo de conta do fornecedor. O valor deste campo pode ser alterado pelo utilizador para selecionar um contacto diferente, como o gestor de conta do fornecedor do subcontrato. Este contacto pode configurar e enviar alertas de e-mail e negociações de preços. |


