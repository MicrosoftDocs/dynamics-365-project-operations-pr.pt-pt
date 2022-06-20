---
title: Integração de fatura de fornecedor
description: Este artigo fornece informações sobre a integração de faturas de fornecedores no Project Operations.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d1e41638b6fe827e9e577860a78a84a9948053e4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912070"
---
# <a name="vendor-invoice-integration"></a>Integração de fatura de fornecedor

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Os contratos relacionados com o projeto em Dynamics 365 Project Operations podem ser registados indo para **Contas a pagar** > **Faturas** > **Faturas pendentes de fornecedor** e utilizando um documento de fatura do fornecedor pendente. Para obter mais informações, consulte [Comprar materiais não armazenados utilizando uma fatura pendente do fornecedor](../procurement/pending-vendor-invoices.md).

> [!IMPORTANT]
> Antes de utilizar a funcionalidade descrita neste artigo, reveja e aplique as configurações necessárias. Para obter mais informações, consulte [Ativar materiais não armazenados e faturas pendentes do fornecedor](../procurement/configure-materials-nonstocked.md).

No Project Operations, as faturas de fornecedor relacionadas com o projeto são publicadas utilizando regras especiais de publicação:

- O custo relacionado com o projeto (incluindo o imposto não recuperável) não é imediatamente registado na conta de custos do projeto no livro razão. Em vez disso, o custo é colocado na **Conta de integração de aquisições**. Esta conta é configurada no separador **Gestão de projetos e gestão contabilística** > **Configuração** > **gestão de projetos e parâmetros de gestão contabilística** no **Project Operations no Dynamics 365 Customer engagement**.
- A dupla escrita sincroniza os dados da fatura do fornecedor para Microsoft Dataverse utilizando os seguintes mapas de tabela:

     - **Entidade de exportação de faturas de projeto de integração do Project Operations (msdyn_projectvendorinvoices)**: Este mapa de tabela sincroniza as informações do cabeçalho da fatura do fornecedor. Apenas as faturas do fornecedor com pelo menos uma linha que contenha uma identificação do projeto são sincronizadas para Dataverse.
     - **Entidade de exportação de linha de fatura de projeto de integração do Project Operations (msdyn_projectvendorinvoicelines)**: Este mapa de tabela sincroniza as informações da linha da fatura do fornecedor. Apenas as linhas que contêm uma identificação do projeto são sincronizadas para Dataverse.

     > [!NOTE]
     > Os detalhes da fatura do fornecedor em Dataverse não são editáveis.

Auxiliar de impostos, auxiliar de fornecedor e outras publicações financeiras são registados conforme aplicável no Dynamics 365 Finance quando a fatura do fornecedor é publicada.

![Integração de fatura de fornecedor.](media/DW7VendorInvoice.png)

Quando os registos são escritos a uma entidade de **Fatura do Fornecedor** em Dataverse, inicia-se um processo de aprovação automatizada dos registos. Se necessário, o estado do processo de aprovação automatizado pode ser revisto em Dataverse indo para **Definições avançadas** > **Sistema** > **Trabalhos do sistema**. Após a aprovação estar concluída, o sistema cria registos de classe de transações de material na entidade **Valores reais**.

Os valores reais relacionados com material são então processados utilizando o mapa de tabela de dupla escrita **Valores reais de integração do Project Operations (msdyn_actuals)**. Para mais informações, consulte [Estimativas e valores reais](resource-dual-write-estimates-actuals.md).

O processo periódico, **Importar de teste** cria linhas de diários de integração do Project Operations relacionados com fatura de fornecedor. A conta offset é predefinida para a conta de integração de procuração. Quando o diário de integração é publicado, o saldo da conta para a transação de fatura de fornecedor é limpo e o valor da linha para a conta de custos do projeto é movido. As transações de sub-livros razão de projetos também são criadas para efeitos de faturação a jusante e reconhecimento de receitas.
