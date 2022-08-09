---
title: Estimativas do projeto e integração de valores reais
description: Este artigo fornece informações sobre a integração de escrita dupla do Project Operations para estimativas de projeto e valores reais.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: dc8f65aec6f2328ccef5f9591a0f4d9c792b0d8f
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029094"
---
# <a name="project-estimates-and-actuals-integration"></a>Estimativas do projeto e integração de valores reais

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Este artigo fornece informações sobre a integração de escrita dupla do Project Operations para estimativas de projeto e valores reais.

## <a name="project-estimates"></a>Estimativas do projeto

As estimativas do trabalho de projeto, de despesas e materiais são criadas e mantidas no Microsoft Dataverse e sincronizadas com as aplicações de finanças e operações para fins de gestão contabilística. As operações de criação, atualização e eliminação não são suportadas nas aplicações de finanças e operações.

A criação de estimativas requer uma configuração de gestão contabilística válida para o projeto. Os projetos associados a linhas de contrato devem ter um perfil de custo e receita válido definido nas regras de custos e perfis de receitas do Projeto. Para mais informações, consulte [Configurar Gestão contabilística para projetos faturáveis](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Estimativas de trabalho

As estimativas de trabalho são criadas pelo Gestor de Projeto ou Gestor de Recursos que também atribui um recurso genérico ou nomeado à tarefa do projeto. Os registos de atribuição de recursos podem ser revistos no separador **Atribuições de Recursos** na página **Detalhes do Projeto** no Dataverse. Os registos de atribuição de recursos no Dataverse criam registos de previsão de horas nas aplicações de finanças e operações utilizando a **Entidade de integração do Project Operations para estimativas de horas (msdyn\_resourceassignments)**.

   ![Integração de estimativas de trabalho.](./Media/DW4LaborEstimates.png)

A dupla escrita sincroniza os registos de atribuição de recursos à tabela de teste (**ProjCDSEstimateHoursImport**), e utiliza a lógica de negócio para criar e atualizar registos de previsão de horas (**ProjForecastEmpl**).

O contabilista do projeto revê os registos de previsão de horas criados nas aplicações de finanças e operações, acedendo a **Gestão de projeto e contabilidade** > **Todos os projetos** > **Plano** > **Previsões de horas**.

## <a name="expense-estimates"></a>Estimativas de despesas

As estimativas de despesas são criadas pelo gestor do Projeto no separador **Estimativas de Despesas** na página **Detalhes do Projeto** em Dataverse. Os registos de estimativa de despesas são armazenados na entidade da **Linha de Estimativa** em Dataverse. Estes registos de estimativa têm a classe de transações **Despesas** e são sincronizados com os registos de previsão de despesas nas aplicações de finanças e operações utilizando a **Entidade de integração do Project Operations para estimativas de despesas (msdyn\_estimatelines)**.

   ![Integração de estimativas de despesa.](./Media/DW4ExpenseEstimates.png)

A dupla escrita sincroniza os registos de estimativa de despesa à tabela de teste, (**ProjCDSEstimateExpenseImport)** e utiliza a lógica de negócio para criar e atualizar registos de previsão de despesa (**ProjForecastCost**). Estimativa de linhas de loja estimativa de vendas e estimativa de custos recordes separadamente. A lógica de negócio nas aplicações de finanças e operações povoa um único registo de previsão de Despesas utilizando este detalhe na tabela de teste.

O contabilista do projeto pode rever os registos de previsão de despesas nas aplicações de finanças e operações, acedendo a **Gestão de projeto e contabilidade** > **Todos os projetos** > **Plano** > **Previsões de despesas**.

## <a name="material-estimates"></a>Estimativas de material

As estimativas de material são criadas pelo gestor do Projeto no separador **Estimativas de material** na página **Detalhes do Projeto** em Dataverse. Os registos de estimativa de material são armazenados na entidade da **Linha de Estimativa** em Dataverse. Estes registos de estimativa têm a classe de transações **Material** e são sincronizados com os registos de previsão de item nas aplicações de finanças e operações utilizando a **Tabela de integração do Project Operations para estimativas de material (msdyn\_estimatelines)**.

   ![Integração de estimativas de material.](./Media/DW4MaterialEstimates.png)

A dupla escrita sincroniza os registos de estimativa de material à tabela de teste **ProjForecastSalesImpor**, e utiliza a lógica de negócio para criar e atualizar registos de previsão de artigo (**ForecastSales**). Estimativa de linhas de loja estimativa de vendas e estimativa de custos recordes separadamente. A lógica de negócio nas aplicações de finanças e operações povoa um único registo de previsão de Item utilizando este detalhe na tabela de teste.

O contabilista do projeto pode rever os registos de previsão do item nas aplicações de finanças e operações, acedendo a **Gestão de projeto e contabilidade** > **Todos os projetos** > **Plano** > **Previsões de itens**.

## <a name="project-actuals"></a>Valores reais do projeto

Os valores reais do projeto são criados em Dataverse, com base no tempo, despesas, material e atividade de faturação. Todos os atributos operacionais destas transações, incluindo quantidade, preço de custo, preço de venda e projeto são capturados nesta entidade Dataverse. Para mais informações, ver [Valores reais](../actuals/actuals-overview.md). Os dados reais são sincronizados com as aplicações de finanças e operações utilizando o mapa de tabela de escrita dupla **Valores reais de integração do Project Operations (msdyn\_actuals)** para a gestão contabilística a jusante.

   ![Integração de valores reais.](./Media/DW4Actuals.png)

O mapa de tabela de **Valores reais de integração do Project Operations** sincroniza todos os registos da entidade **Valores reais** em Dataverse, com o atributo **Skip Sync (apenas uso interno)** definido como **Falso**. Este valor de atributo é definido em Dataverse automaticamente quando o registo é criado. Exemplos em que este atributo é definido para **Verdadeiro** são:

  - Os valores reais de custo do projeto para transações interempresa. Para obter mais informações, consulte [Criar transações interempresa](../project-accounting/create-intercompany-transactions.md). Estes registos são ignorados porque o sistema recria o custo do projeto real nas aplicações de finanças e operações quando a fatura do fornecedor entre empresas é publicada.
  - Registos de vendas negativos não faturados criados quando a fatura proforma é confirmada. Estes dados são ignorados porque o auxiliar do projeto nas aplicações de finanças e operações não reverte o registo de vendas não faturadas na faturação, mas altera o estado para totalmente faturado.

O mapa de tabela de dupla escrita sincroniza os valores reais da tabela de teste, **ProjCDSActualsImport**. Estes registos são processados pelo processo periódico **Importar da tabela de teste** ao criar linhas de diário do Project Operations e linhas de proposta de fatura de projeto. Para mais informações, consulte [diário de Integração no Project Operations](../project-accounting/project-operations-integration-journal.md).

Dataverse captura também as ligações entre as transações de valores reais do projeto na entidade de **ligação de transações**. Para obter mais informações, consulte [ligar valores reais para registos originais](../actuals/linkingactuals.md). As hiperligações entre transações reais também são sincronizadas com as aplicações de finanças e operações utilizando o mapa de tabela de escrita dupla, **Entidade de integração para relações de transação do projeto (msdyn\_transactionconnections)**. Estes registos são usados pelo processo periódico, **Importar da tabela de teste** ao criar linhas de diário do Project Operations e linhas de proposta de fatura de projeto.

A publicação de um diário de integração do Project Operations e de uma proposta de fatura do projeto despoleta uma atualização nos respetivos registos na tabela de teste, **ProjCDSActualsImport**. O sistema captura e regista os seguintes atributos contabilísticos para transações de valores reais:

- Montante de moeda contabilística
- Câmbio
- Número de voucher
- Valor de imposto sobre vendas

O mapa da tabela **Valores reais de integração do Project Operations** atualiza os registos dos respetivos registos de valores reais no Dataverse com esta informação.
