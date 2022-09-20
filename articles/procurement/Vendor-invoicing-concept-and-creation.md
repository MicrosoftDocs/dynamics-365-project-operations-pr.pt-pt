---
title: Criar faturas de fornecedor
description: Este artigo descreve o conceito de faturas de fornecedor e explica como as criar de fornecedor no Microsoft Dynamics 365 Project Operations.
author: suvaidya
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 7f6c1ec46f23b6823734b28755b80ced4e3f9325
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475435"
---
# <a name="create-vendor-invoices"></a>Criar faturas de fornecedor

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Para utilizar a funcionalidade descrita neste artigo, tem de ativar a funcionalidade **Ativar o processamento de valores reais de subcontratos com o Project Operations para recursos baseados em cenários** na área de trabalho **Gestão de funcionalidades**.

A faturação a fornecedor no Microsoft Dynamics 365 Project Operations pode ser utilizada para registar custos das entregas de serviços e/ou materiais num projeto que é concluído por fornecedores.

Quando os serviços e/ou materiais são subcontratados a um fornecedor, um subcontrato representa o contrato com esse fornecedor. À medida que o fornecedor entrega os serviços, ou que os materiais são recebidos e utilizados em tarefas do projeto, os custos são registados no projeto. Em seguida, o fornecedor envia as faturas periodicamente. Estas faturas que são verificadas e correspondidas aos custos registados no projeto. Após o processo de verificação estar concluído, a fatura do fornecedor é confirmada e lançada para pagamento.

## <a name="scenarios-for-use"></a>Cenários de utilização

As faturas dos fornecedores no Project Operations podem ser utilizadas para suportar dois cenários diferentes:

- Os clientes utilizam as experiências completas de subcontratação.
- Os clientes não utilizam as experiências completas de subcontratação mas pretendem ter uma vista unificada dos custos dos projetos no Project Operations.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Os clientes utilizam as experiências completas de subcontratação

As experiências de fatura do fornecedor oferecem uma forma de verificar entradas de tempo, utilização de material e entradas de despesas que se referem a componentes subcontratados e correspondê-las com linhas de fatura do fornecedor. Este processo pode ser utilizado para verificar a precisão das linhas de fatura do fornecedor. Depois de concluído o processo de verificação e da fatura do fornecedor ser confirmada, o sistema reverte os valores reais registados ao longo dos registos de utilização de tempo, despesas e materiais aprovados e, em seguida, cria novos valores reais de custos utilizando as linhas de fatura do fornecedor.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Os clientes não utilizam as experiências completas de subcontratação mas pretendem ter uma vista unificada dos custos dos projetos no Project Operations

Se estiver a monitorizar o processo de subcontrato num sistema de terceiros, pode registar custos desse sistema de terceiros para o Project Operations criando faturas de fornecedores que não se referem a subcontratos. Deste modo, os gestores de projetos podem ter uma vista única e unificada de todos os custos num determinado projeto.

## <a name="create-vendor-invoices-in-project-operations"></a>Criar faturas de fornecedor no Project Operations

As faturas de fornecedores são criadas no Dynamics 365 Finance, utilizando o módulo **Contas a pagar**. Não pode criar faturas de fornecedor diretamente no Dataverse.

### <a name="set-up-vendor-invoice-verification"></a>Configurar a verificação de faturas de fornecedor

Se a fatura do fornecedor se destina a um subcontrato no Dataverse, tem de ativar o parâmetro **É necessária verificação manual pelo PM**. A definição da opção determina se a fatura do fornecedor deve ser confirmada automaticamente no Dataverse ou se necessita de confirmação manual. O cabeçalho de cada fatura de fornecedor do projeto inclui uma opção com o mesmo nome. Por predefinição, a opção no cabeçalho de todas as faturas de fornecedor do projeto está definida com o valor definido aqui. No entanto, pode atualizar o valor conforme necessário no cabeçalho de faturas de fornecedor individual.

Se a opção estiver definida como **Sim**, a fatura de fornecedor que é criada no Finance e sincronizada com o Dataverse tem o estado **Rascunho**. Em seguida, a fatura tem de ser validada e verificada pelo gestor do projeto e verificada, antes de ser processada e publicada nas contas de projeto e de razão específicas no Finance.

Se a opção estiver definida como **Não**, a fatura do fornecedor é confirmada automaticamente. Não é necessária qualquer ação adicional.

Para configurar a verificação de faturas de fornecedor, siga estes passos.

1. No Finance, aceda a **Gestão de projetos e gestão contabilística** \> **Configurar** \> **Parâmetros da Gestão de projetos e gestão contabilística**.
1. No separador **Financeira**, defina a a opção **É necessária verificação manual pelo PM** como **Sim**, se a política da empresa requerer a verificação de faturas do fornecedor de subcontratação. Se não for necessária verificação pelo gestor de projeto no Dataverse, deixe o conjunto de opções como **Não**. Por predefinição, a definição será utilizada na página **Fatura do fornecedor pendente**.

> [!NOTE]
> As faturas de fornecedores criadas para subcontratos no Dataverse só podem ser processadas corretamente se a opção **É necessária verificação manual pelo PM** estiver definida como **Sim**. Os valores reais de custo de tempo, material e despesas que os subcontratantes criam só podem ser correspondidos manualmente às linhas de fatura do fornecedor pelo gestor do projeto, apenas se esta opção estiver definida como **Sim**.

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>Definir uma conta de integração de aquisições para faturas de fornecedor

Quando uma fatura de fornecedor é publicada no Finance para o Project Operations – Ambiente integrado (sem stock), as finanças são publicadas na conta de integração de aquisições. O sistema gera os valores reais no Dataverse para a fatura publicada. Estes valores reais são publicados no Finance utilizando o diário de integração do Projeto. A publicação deste diário de integração de Projeto publica o custo real e reverte a conta de integração de aquisições.

Para configurar uma conta de integração de aquisições para faturas de fornecedor, siga estes passos.

1. No Finance, aceda a **Gestão de projetos e gestão contabilística** \> **Configurar** \> **Parâmetros da Gestão de projetos e gestão contabilística**.
1. No separador **Project operations no Dynamics 365 Customer Engagement**, seleccione **Materiais** \> **Conta de integração de aquisições**.

### <a name="create-and-post-subcontract-vendor-invoices"></a>Criar e publicar faturas de fornecedores de subcontratos

Quando um escrituário de Contas a pagar recebe uma fatura do subcontratante, é criada uma nova fatura no Finance.

1. No Finance, aceda a **Contas a pagar** \> **Faturas** \> **Faturas de fornecedores pendentes**.
1. No **Painel de Ações**, selecione **Novo** para criar uma fatura de fornecedor.
1. No cabeçalho da fatura, no campo **Conta de faturação**, selecione **Subcontratante**.
1. Selecione a data da fatura.
1. No separador **Cabeçalho**, deverão definir a opção **É necessária verificação manual pelo PM** como **Sim**. A predefinição desta opção vem a partir da página **Parâmetros de gestão de projeto e gestão contabilística**. No entanto, pode ser alterado ao nível da fatura do fornecedor.
1. No Separador rápido **Linha da fatura**, selecione **Adicionar linha** para criar uma linha de fatura de fornecedor.
1. Selecione a categoria de aquisição que foi criada para itens de subcontrato e introduza o preço unitário, a unidade de medida e a quantidade.
1. Na secção de linhas da fatura do fornecedor, no separador **Projeto**, selecione o projeto em relação ao qual o subcontratante partilha a fatura de subcontrato.
1. Selecione a categoria do projeto. Pode ser de qualquer tipo de **Item**, **Despesa**, **Materiais** ou **Horas**.despesa
1. Selecione a função apenas se a categoria de projeto selecionada for do tipo **Hora**.
1. Selecione **Publicar** para publicar a fatura de fornecedor.

Em alternativa, pode criar uma fatura de fornecedor acedendo a **Contas a pagar** \> **Faturas** \> **Abrir faturas de fornecedor** e selecionando **Nova**.

Quando a fatura do fornecedor é publicada, a mesma fica disponível no Dataverse para verificação e processamento pelo gestor de projeto.

## <a name="vendor-invoice-processing-in-dataverse"></a>Processamento de faturas de fornecedor no Dataverse

Na fatura do fornecedor que é criada no Dataverse, alguns valores de campo são gerados pela fatura do fornecedor que é registada no Finance. Os outros valores são valores predefinidos e vêm do subcontrato.

Os seguintes campos e registos relacionados serão copiados do subcontrato para o cabeçalho da fatura do fornecedor:

- Moeda
- Unidade de contratação
- Prazos de pagamento

Nas linhas de fatura do fornecedor, o Project Operations utiliza os seguintes valores de campo para inserir a referência de subcontrato e item de subcontrato predefinidos:

- Classe de transação
- Função
- Categoria de transação
- Campos de produto
- Project
- Tarefa

> [!NOTE]
> Os itens de subcontrato de preço fixo não são suportados no Project Operations.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
