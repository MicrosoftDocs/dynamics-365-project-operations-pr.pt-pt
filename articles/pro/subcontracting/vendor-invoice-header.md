---
title: Detalhes do cabeçalho para faturas do fornecedor
description: Este tópico explica a funcionalidade que é fornecida no cabeçalho da fatura do fornecedor no Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 17be106d5486358ff0bbf011af3da26a4c85a274
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575594"
---
# <a name="header-details-for-vendor-invoices"></a>Detalhes do cabeçalho para faturas do fornecedor

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

Este tópico explica a funcionalidade que é fornecida no cabeçalho da fatura do fornecedor no Microsoft Dynamics 365 Project Operations.

À medida que os gestores do projeto planeiam e executam projetos, poderão utilizar subcontratantes e adquirir produtos e serviços a fornecedores. Durante a execução de um projeto, os custos são incorridos com serviços, materiais e categorias de despesas obtidos em subcontratações com fornecedores. Os fornecedores faturam estes custos aos projetos criando faturas de fornecedores.

A tabela seguinte fornece informações sobre os campos nos cabeçalhos da fatura do fornecedor no Project Operations.

| Campo | Description | Impacto funcional |
| --- | --- | --- |
| Name | O nome da fatura do fornecedor. | Em todas as listas pendentes da fatura de fornecedores, o nome da fatura do fornecedor é listado na primeira coluna para ajudar a identificar a fatura do fornecedor. Por predefinição, quando uma fatura de fornecedor é criada a partir de um subcontrato, o campo **Nome** da fatura do fornecedor é definido para um valor composto pelo nome do subcontrato para além da data atual. |
| Description | Uma breve descrição dos serviços e produtos que estão a ser faturados na fatura do fornecedor. | None |
| Fornecedor | O nome da empresa que está a faturar os produtos e serviços. Esta empresa deve ser um registo de conta que tem um tipo de relação de **Fornecedor** ou **Prestador**. | <p>Com base no fornecedor selecionado, os valores predefinidos são introduzidos automaticamente nos seguintes campos:</p><ul><li>Moeda</li><li>Listas de preços</li><li>Prazos de pagamento</li><li>Endereço de pagamento</li></ul> |
| Subcontrato | Uma referência do subcontrato da fatura do fornecedor. | <p>Com base no subcontrato selecionado, os valores predefinidos são introduzidos automaticamente nos seguintes campos:</p><ul><li>Moeda</li><li>Listas de preços</li><li>Prazos de pagamento</li><li>Endereço de pagamento</li></ul><p>O subcontrato que está selecionado no cabeçalho da fatura do fornecedor está inserido por predefinição nas linhas de fatura do fornecedor e não pode ser alterado aí.</p> |
| Data da fatura | A data para os valores reais de custo que serão criados quando a fatura do fornecedor for confirmada. | A data da fatura também é utilizada para selecionar a lista de preços de compra correta, quer a partir das listas de preços anexadas ao fornecedor relacionado, quer a partir dos parâmetros do projeto. |
| Razão do estado | O estado da fatura do fornecedor. | <p>O estado determina a fase da fatura do fornecedor no processo de negócio e se pode ser editada. Eis alguns dos valores disponíveis:</p><ul><li>**Rascunho** – a fatura do fornecedor pode ser editada.</li><li>**Confirmada** – A fatura do fornecedor foi verificada e confirmado. As faturas do fornecedor neste estado não podem ser editadas ou eliminadas.</li><li>**Em processo** – A fatura do fornecedor está a ser revista. As faturas do fornecedor neste estado podem ser editadas, mas não podem ser eliminadas.</li><li>**Cancelada** – A fatura do fornecedor foi cancelada. As faturas do fornecedor neste estado não podem ser editadas ou eliminadas.</li></ul> |
| Moeda | A moeda em que o fornecedor está a faturar para os produtos e serviços na fatura do fornecedor. | Numa fatura de fornecedor que se refere a um subcontrato, a moeda do subcontrato é inserida por predefinição como moeda da fatura do fornecedor. Numa fatura de fornecedor que não se refere a um subcontrato, o valor predefino é inserido a partir do registo de conta de fornecedor e pode ser alterado. Depois de uma fatura de fornecedor ser guardada, a moeda deixa de poder ser editada. |
| Unidade de contratação | A divisão da empresa responsável por receber os serviços e/ou produtos do fornecedor. | None |
| Prazos de pagamento | Os termos de pagamento nas faturas do fornecedor que são emitidos. O valor predefinido é introduzido automaticamente a partir do registo da conta do fornecedor. | Os termos de pagamento de um subcontrato são copiados para todas as faturas do fornecedor relacionadas com o subcontrato. Os termos de pagamento podem ser atualizados se a fatura do fornecedor estiver no estado **Rascunho**. |
| Endereço de pagamento | O endereço do fornecedor para o qual os pagamentos devem ser enviados. O valor predefinido é introduzido automaticamente a partir do registo da conta do fornecedor. | O endereço de pagamento de um subcontrato é copiado como o endereço de pagamento para todas as faturas do fornecedor criadas para esse subcontrato. O endereço de pagamento pode ser atualizado se a fatura do fornecedor estiver no estado **Rascunho**. |
| Subtotal | Se a fatura do fornecedor não tiver linhas, introduza o subtotal da fatura antes de impostos. Se a fatura do fornecedor tiver linhas, este campo é só de leitura. Neste caso, o montante apresentado é o montante do subtotal de todas as linhas na fatura do fornecedor. | None |
| Imposto total | Se a fatura do fornecedor não tiver linhas, introduza o valor total de impostos no subcontrato. Se a fatura do fornecedor tiver linhas, este campo é só de leitura. Neste caso, o montante apresentado é o montante da soma do valor de impostos de todas as linhas na fatura do fornecedor. | None |
| Montante total | Este campo calculado mostra o montante total da fatura do fornecedor após os impostos serem incluídos. | None |

> [!NOTE]
> Não é possível alterar os seguintes campos na fatura de um fornecedor depois de a fatura do fornecedor ser guardada: **Fornecedor**, **Subcontrato**, **Moeda**, **Unidade de contratação** e **Termos de pagamento**. Se for necessária alguma alteração a estes campos numa fatura de fornecedor, terá de eliminar a fatura do fornecedor e criar uma nova fatura de fornecedor.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
