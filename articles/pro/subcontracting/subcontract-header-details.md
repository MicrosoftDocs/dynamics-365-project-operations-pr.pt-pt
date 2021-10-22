---
title: Detalhes do cabeçalho para subcontratos
description: Este tópico explica a funcionalidade fornecida no cabeçalho do subcontrato no Project Operations.
author: rumant
ms.date: 09/14/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ee863d31b45e7de962488fe804202ddfe580eb04
ms.sourcegitcommit: 083e3d219cd5126eecb74debb1b70b361680b1f6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/18/2021
ms.locfileid: "7501340"
---
# <a name="header-details-for-subcontracts"></a>Detalhes do cabeçalho para subcontratos

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

Este tópico explica a funcionalidade fornecida no cabeçalho do subcontrato no Dynamics 365 Project Operations.

Como um Gestor de Projeto planeia e executa projetos, pode empregar subcontratantes e comprar produtos e serviços de fornecedores. Quando um Gestor de Projeto necessita de comprar produtos ou serviços, pode criar um subcontrato no Project Operations.

Para criar um subcontrato, execute os seguintes passos.

1. No painel de navegação, selecione **Subcontratos** e na página **Subcontrato**, selecione **Novo**.
2. Introduza as informações necessárias e selecione **Guardar**.

    A tabela seguinte fornece informações sobre os campos na página **Cabeçalho do subcontrato**.

    | Campo | Descrição |Impacto Funcional |
    |---|------|---| 
    | Nome | O nome do subcontrato. | Em todas as listas pendentes de subcontratos, o nome do subcontrato é listado na primeira coluna para ajudar a identificar o subcontrato. | 
    | Descrição | Uma breve descrição dos serviços e produtos que estão a ser comprados no subcontrato. | Nenhuma |
    | Fornecedor | O nome da empresa à qual os produtos e serviços estão a ser comprados. Este registo de conta tem um tipo de relação de **Fornecedor** ou **Prestador**. | Com base no fornecedor selecionado, os valores predefinidos são introduzidos automaticamente para os seguintes campos:<br/> **• Moeda** </br> **• Listas de preços** </br> **• Termos de Pagamento**</br> **• Endereço de Pagamento**</br> **• Morada para Faturação**</br> **• Nome para Faturação** </br>**• Gestor de Contas do Fornecedor**|
    | Data do Subcontrato | A data de criação do subcontrato. | A data do subcontrato é utilizada para selecionar a lista de preços de compra correta, quer a partir das listas de preços anexadas ao fornecedor relacionado, quer a partir dos parâmetros do projeto. |
    | Razão do Estado | O estado do subcontrato. | O estado determina a fase do subcontrato no processo de negócio e se pode ser editado. <br/>Os valores incluem:<br>• **Rascunho**: o subcontrato pode ser editado. Só pode editar subcontratos com um estado de **Rascunho**.<br/>• **Confirmado**: a negociação com o fornecedor foi concluída e o subcontrato foi aprovado para entrega. <br/>• **Fechado**: a entrega do subcontrato foi concluída.<br/>• **Cancelado**: o subcontrato foi cancelado e não existe uma entrega planeada.  | 
    | Moeda | A moeda de compra dos produtos e serviços. O valor predefinido é introduzido automaticamente a partir da conta do fornecedor, mas pode ser alterado. | A moeda do subcontrato é utilizada para selecionar a lista de preços de compra, quer a partir das listas de preços anexadas ao fornecedor relacionado, quer a partir dos parâmetros do projeto. As listas de preços noutra moeda não podem ser associadas ao subcontrato. O custo de horas, despesas e materiais que os recursos do fornecedor entregam a partir deste subcontrato é registado nesta moeda no projeto. A moeda do contrato não pode ser alterada depois de guardar o registo do subcontrato.|
    | Unidade de Contratação | A divisão da empresa que está a celebrar um contrato ou um subcontrato de compra com o fornecedor. | Nenhuma |
    | Prazos de pagamento | Os termos de pagamento nas faturas do fornecedor que são emitidas neste subcontrato. O valor predefinido é introduzido automaticamente a partir do registo da conta do fornecedor. | Os termos de pagamento do subcontrato são copiados para todas as faturas do fornecedor relacionadas com este subcontrato. Os termos de pagamento podem ser atualizados se o subcontrato tiver um estado de **Rascunho**. | 
    | Endereço de Pagamento | O endereço do fornecedor para o qual os pagamentos devem ser enviados. O valor predefinido é introduzido automaticamente a partir do registo da conta do fornecedor. | O endereço de pagamento do subcontrato é copiado como o endereço de pagamento para todas as faturas do fornecedor criadas para este subcontrato. O endereço de pagamento pode ser atualizado se o subcontrato tiver um estado de **Rascunho**.|
    | Nome para Faturação | O nome da pessoa ou divisão na empresa do fornecedor que enviará a fatura. O valor predefinido é introduzido automaticamente a partir do registo da conta do fornecedor. | O valor **Nome para Faturação** do subcontrato é copiado para todas as faturas do fornecedor relacionadas com este subcontrato. Este campo pode ser atualizado se o subcontrato tiver um estado de **Rascunho**.|
    | Morada para Faturação | O endereço que é utilizado nas faturas do fornecedor. O valor predefinido é introduzido automaticamente a partir do registo da conta do fornecedor. | Este endereço é o endereço "fatura de" nas faturas do fornecedor criadas para este subcontrato. |
    | Subtotal | Se um subcontrato não tiver itens, introduza o subtotal da encomenda antes de impostos. Se o subcontrato tiver linhas, este campo é só de leitura. O montante mostrado é o montante do subtotal de todos os itens do subcontrato. | Nenhuma |
    | Imposto Total | Se um subcontrato não tiver itens, introduza o total de impostos neste subcontrato. Se o subcontrato tiver linhas, este campo é só de leitura. O montante mostrado é a soma do montante de impostos de todos os itens do subcontrato. | Nenhuma |
    | Montante Total | Este campo calculado mostra o montante total do subcontrato com os impostos. | Nenhuma |
    | Data Confirmada | A data de confirmação do subcontrato. | Nenhuma |
    | Pretendido Por | Por predefinição, este campo é definido para o nome do utilizador que cria o subcontrato. No entanto, o criador do subcontrato pode alterar o valor para indicar a pessoa em nome da qual está a criar o subcontrato. | Nenhuma |
    | Gestor de Contas do Fornecedor | O nome do contacto principal da conta do fornecedor. O valor predefinido é introduzido automaticamente a partir do registo da conta do fornecedor. Pode selecionar um contacto diferente como gestor de conta do fornecedor do subcontrato. | Pode configurar alertas de e-mail para notificar o contacto quando forem feitas alterações ao subcontrato devido a negociações de preços. |
