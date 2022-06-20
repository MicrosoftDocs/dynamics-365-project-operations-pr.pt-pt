---
title: Faturação do fornecedor - Conceito e criação
description: Este artigo descreve o conceito de faturas de fornecedor, cenários de utilização e como criar faturas de fornecedor no Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 38f0760697522b7a5e561cec7d38dfd5c3eaf9fc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911472"
---
# <a name="vendor-invoicing---concept-and-creation"></a>Faturação do fornecedor - Conceito e criação

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

A faturação de fornecedor no Microsoft Dynamics 365 Project Operations pode ser utilizada para registar custos das entregas de serviços e/ou materiais num projeto por parte de fornecedores.

Quando os serviços e/ou materiais são subcontratados a um fornecedor, um subcontrato representa o contrato com esse fornecedor. À medida que o fornecedor entrega os serviços, ou se os materiais são recebidos e utilizados em tarefas do projeto, os custos são registados no projeto. Periodicamente, o fornecedor envia faturas que são verificadas e corresponderam aos custos registados no projeto. Após o processo de verificação estar concluído, a fatura do fornecedor é confirmada e lançada para pagamento.

## <a name="scenarios-for-use"></a>Cenários de utilização

As faturas dos fornecedores no Project Operations podem ser utilizadas para suportar dois cenários diferentes.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Os clientes utilizam as experiências completas de subcontratação

As experiências de fatura do fornecedor oferecem uma forma de verificar e corresponder a entradas de tempo, utilização de material e entradas de despesas que se referem a componentes subcontratados com linhas de fatura do fornecedor. Este processo pode ser utilizado para verificar a precisão das linhas de fatura do fornecedor. Depois de concluído o processo de verificação e da fatura do fornecedor ser confirmada, a aplicação irá inverter os valores reais registados pelo tempo, despesas e materiais aprovados, bem como criar novos valores reais de custos utilizando as linhas de fatura do fornecedor.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Os clientes não utilizam as experiências completas de subcontratação mas pretendem ter uma vista unificada dos custos dos projetos no Project Operations

Se estiver a monitorizar o processo de subcontrato num sistema de terceiros, pode registar custos desse sistema de terceiros para o Project Operations criando faturas de fornecedores que não se referem a subcontratos. Deste modo, os gestores de projetos podem ter uma vista única e unificada de todos os custos num determinado projeto.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Criação de faturas de fornecedor no Project Operations

Podem ser criadas faturas de fornecedor de duas formas:

- Na página da lista de faturas do fornecedor ou na página de detalhes de uma fatura de um único fornecedor
- Na página de lista de subcontrato ou na página de detalhes de um único subcontrato

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Criação a partir da página de lista de faturas do fornecedor ou página de detalhes

1. Aceda a **Comprar** \> **Faturas de fornecedor**.
2. Na página lista de faturas do fornecedor ou na página de detalhes para uma fatura de um único fornecedor, selecione **Novo** para criar uma nova fatura de fornecedor.

As faturas dos fornecedores que são criadas desta forma também se podem referir a um subcontrato.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Criação a partir da página de lista de subcontrato ou página de detalhes

1. Aceda a **Comprar** \> **Subcontratos**.
2. Selecione um ou mais subcontratos.
3. Na página lista de subcontrato ou na página de detalhes para uma único subcontrato, selecione **Criar fatura de fornecer** para criar uma nova fatura de fornecedor.

É criada uma nova fatura de fornecedor no estado **Rascunho** para cada subcontrato que selecionou.

As faturas de fornecedor que criar desta forma referem-se sempre ao subcontrato no cabeçalho da fatura do fornecedor. Cada linha no subcontrato que tenha um método de faturação de tempo e material fará com que seja criada uma linha na fatura do fornecedor. Cada linha no subcontrato que tenha um método de faturação de preço fixo fará com que seja criada uma linha na fatura do fornecedor para cada marcos de item de subcontrato que tenha o estado **Pronto para faturar**.

Os seguintes campos e registos relacionados serão copiados do subcontrato para o cabeçalho da fatura do fornecedor:

- Fornecedor.
- As listas de preços relacionadas serão copiadas para a fatura do fornecedor como listas de preços.
- Moeda.
- Unidade de contratação.
- Termos de pagamento.

Para itens de subcontrato de tempo e material, os seguintes campos e registos relacionados serão copiados do item de subcontrato para a linha de fatura do fornecedor:

- Referências de subcontrato e item de subcontrato
- Classe de transação
- Função
- Categoria de transação
- Campos de produto
- Project
- Tarefa
- Recurso reservável

Para itens de subcontrato de preço fixo, os seguintes campos serão copiados do item de subcontrato e marco de item de subcontrato para a linha de fatura do fornecedor:

- Referências de subcontrato e item de subcontrato.
- Classe de transação. Por predefinição, o valor será **Marcos**.
- O nome e o montante dos marcos serão copiados a partir do marco de item de subcontrato relacionado.
- O utilizador poderá selecionar um projeto e uma tarefa na linha de fatura do fornecedor.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
