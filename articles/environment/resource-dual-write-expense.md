---
title: Integração de gestão de despesas
description: Este artigo fornece informações sobre a integração de relatório de despesas no Project Operations utilizando a escrita dupla.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: c64c318dc1915a9a87b6ae3c6b8a2aa6d3c9cd36
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924628"
---
# <a name="expense-management-integration"></a>Integração de gestão de despesas

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Este artigo fornece informações sobre a integração de relatórios de despesas de [implementação de despesas total](../expense/expense-overview.md) do Project Operations utilizando a escrita dupla.

## <a name="expense-categories"></a>Categorias de despesas

Numa implementação de despesas completa, as categorias de despesas são criadas e mantidas nas aplicações de Finanças e Operações. Para criar uma nova categoria de despesas, complete os seguintes passos:

1. Em Microsoft Dataverse, crie uma categoria de **Transação**. A integração de escrita dupla sincroniza esta categoria de transações com as aplicações Finanças e Operações. Para obter mais informações, consulte [Configurar categorias de projetos](/dynamics365/project-operations/project-accounting/configure-project-categories) e [Configuração do Project Operations e integração de dados de configuração](resource-dual-write-setup-integration.md). Como resultado desta integração, o sistema cria quatro registos de categoria partilhados nas aplicações Finanças e Operações.
2. Em Finanças, vá à **Gestão de despesas** > **Configuração** > **Categorias partilhadas** e selecione uma categoria partilhada com uma classe de transação de **Despesas**. Defina o parâmetro **Pode ser usado em Despesa** para **Verdadeiro** e defina o tipo de despesa a utilizar.
3. Utilizando este registo de categoria partilhada, crie uma nova categoria de despesas indo para **Gestão de despesa** > **Configuração** > **Categorias de despesa** e selecionando **Novo**. Quando o registo é guardado, a dupla escrita utiliza o mapa de tabela, **Entidade de exportação de despesas de integração do Project Operations (msdyn\_expensecategories)** para sincronizar este registo para Dataverse.

  ![Integração de categorias de despesas.](./media/DW6ExpenseCategories.png)

As categorias de despesas nas aplicações de finanças e operações são específicas de empresas ou de entidades legais. Existem registos separados e correspondentes de entidades jurídicas específicas em Dataverse. Quando um gestor de projetos estima as despesas, não podem selecionar categorias de despesas que foram criadas para um projeto que é propriedade de uma empresa diferente da empresa proprietária do projeto em que estão a trabalhar. 

## <a name="expense-reports"></a>Relatórios de despesas

Os relatórios de despesas são criados e aprovados nas aplicações de Finanças e Operações. Para obter mais informações, consulte [Criar e processar relatórios de despesas em Dynamics 365 Project Operations](/learn/modules/create-process-expense-reports/). Depois do relatório de despesas ser aprovado pelo diretor do projeto, é publicado no livro razão. No Project Operations, as linhas de relatório de despesas relacionadas com o projeto são publicadas utilizando regras especiais de publicação:

  - O custo relacionado com o projeto (incluindo o imposto não recuperável) não é imediatamente registado na conta de custos do projeto em geral, mas é registado na conta de integração de despesas. Esta conta é configurada no separador **Gestão de projetos e gestão contabilística** > **Configuração** > **gestão de projetos e parâmetros de gestão contabilística**, **Project Operations no Dynamics 365 Customer engagement**.
  - A dupla escrita sincroniza para Dataverse utilizando o mapa da tabela **Entidade de exportação de despesas de projeto de integração do Project Operations (msdyn\_expenses)**.
  - O sub-livro razão de impostos, o sub-livro razão de fornecedores e outros destacamentos financeiros são registados conforme aplicável no momento da publicação do relatório de despesas.

  ![Integração de relatórios de despesas.](./media/DW6ExpenseReports.png)

Quando um registo é escrito na entidade **Despesa** em Dataverse, o sistema aciona o processo de aprovação automatizado do registo. Se necessário, o estado do processo de aprovação automatizado pode ser revisto em Dataverse indo para **Definições avançadas** > **Sistema** > **Trabalhos do sistema**. Após a aprovação estar concluída, os registos de classe de transações de despesas são criados na entidade **Valores reais**.

Os valores reais relacionados com as despesas são então processados utilizando o mapa de tabela de dupla escrita **Valores reais de integração do Project Operations (msdyn\_actuals)**. Para mais informações, consulte [Estimativas e valores reais](resource-dual-write-estimates-actuals.md).

O processo periódico, **Importar de teste** cria linhas de diários relacionados com o relatório de despesas no diário de integração do Project Operations. A conta offset é predefinida para a conta de integração de despesas. O Diário de Integração de destacamento limpa o saldo da conta para a transação de despesas e transfere o valor da despesa para a conta de custos do projeto. O sistema também cria transações de sub-livros razão de projetos para efeitos de faturação a jusante e reconhecimento de receitas.
