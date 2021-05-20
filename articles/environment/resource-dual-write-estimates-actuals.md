---
title: Estimativas do projeto e integração de valores reais
description: Este tópico fornece informações sobre a integração de escritas dupla do Project Operations para estimativas de projetos e valores reais.
author: sigitac
manager: Annbe
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 88df3385fac0a78a827d65a77d3b04c9d6499536
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955812"
---
# <a name="project-estimates-and-actuals-integration"></a>Estimativas do projeto e integração de valores reais

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Este tópico fornece informações sobre a integração de escritas dupla do Project Operations para estimativas de projetos e valores reais.

## <a name="project-estimates"></a>Estimativas do projeto

O trabalho de projeto, as estimativas de despesas e materiais são criados e mantidos no Microsoft Dataverse e sincronizados nas aplicações Finance and Operations com fins de gestão contabilística. Criar, atualizar e eliminar operações não são suportados através das aplicações Finance and Operations.

A criação de estimativas requer uma configuração de gestão contabilística válida para o projeto. Os projetos associados a linhas de contrato devem ter um perfil de custo e receita válido definido nas regras de custos e perfis de receitas do Projeto. Para mais informações, consulte [Configurar Gestão contabilística para projetos faturáveis](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Estimativas de trabalho

As estimativas de trabalho são criadas pelo Gestor de Projeto ou Gestor de Recursos que também atribui um recurso genérico ou nomeado à tarefa do projeto. Os registos de atribuição de recursos podem ser revistos no separador **Atribuições de Recursos** na página **Detalhes do Projeto** no Dataverse. Os registos de atribuição de recursos em Dataverse criam registos de previsão de hora em aplicações Finance and Operations que utilizam a **entidade de integração do Project Operations para estimativas de horas (msdyn\_resourceassignments)**.

   ![Integração de estimativas de trabalho](./Media/DW4LaborEstimates.png)

A dupla escrita sincroniza os registos de atribuição de recursos à tabela de teste (**ProjCDSEstimateHoursImport**), e utiliza a lógica de negócio para criar e atualizar registos de previsão de horas (**ProjForecastEmpl**).

O contabilista do Projeto analisa os registos de horas de previsão criados em aplicações Finance and Operations, indo para a **Gestão do projeto e contabilidade** > **Todos os projetos** > **Plano** > **Previsões horárias**.

## <a name="expense-estimates"></a>Estimativas de despesas

As estimativas de despesas são criadas pelo gestor do Projeto no separador **Estimativas de Despesas** na página **Detalhes do Projeto** em Dataverse. Os registos de estimativa de despesas são armazenados na entidade da **Linha de Estimativa** em Dataverse. Estes registos de estimativa têm classe de transações, **Despesa** e são sincronizados com registos de previsão de despesas em aplicações Finance and Operations que utilizam a **entidade de integração do Project Operations para estimativas de despesas (msdyn\_estimatelines)**.

   ![Integração de estimativas de despesa](./Media/DW4ExpenseEstimates.png)

A dupla escrita sincroniza os registos de estimativa de despesa à tabela de teste, (**ProjCDSEstimateExpenseImport)** e utiliza a lógica de negócio para criar e atualizar registos de previsão de despesa (**ProjForecastCost**). Estimativa de linhas de loja estimativa de vendas e estimativa de custos recordes separadamente. A lógica de negócio em aplicações Finance and Operations povoa um único registo de previsão de despesas usando este detalhe na tabela de teste.

O contabilista do Projeto pode rever os registos de previsão de despesa criados em aplicações Finance and Operations, indo para a **Gestão do projeto e contabilidade** > **Todos os projetos** > **Plano** > **Previsões de despesa**.

## <a name="material-estimates"></a>Estimativas de material

As estimativas de material são criadas pelo gestor do Projeto no separador **Estimativas de material** na página **Detalhes do Projeto** em Dataverse. Os registos de estimativa de material são armazenados na entidade da **Linha de Estimativa** em Dataverse. Estes registos de estimativa têm a classe de transações, **Material** e são sincronizados com registos de previsão de artigos em aplicações Finance and Operations que utilizam a **tabela do Project Operations para estimativas de material (msdyn\_estimatelines)**.

   ![Integração de estimativas de material](./Media/DW4MaterialEstimates.png)

A dupla escrita sincroniza os registos de estimativa de material à tabela de teste **ProjForecastSalesImpor**, e utiliza a lógica de negócio para criar e atualizar registos de previsão de artigo (**ForecastSales**). Estimativa de linhas de loja estimativa de vendas e estimativa de custos recordes separadamente. A lógica de negócio em aplicações Finance and Operations povoa um único registo de previsão de artigo usando este detalhe na tabela de teste.

O contabilista do Projeto pode rever os registos de previsão de artigo criados em aplicações Finance and Operations, indo para a **Gestão do projeto e contabilidade** > **Todos os projetos** > **Plano** > **Previsões de artigo**.

## <a name="project-actuals"></a>Valores reais do projeto

Os valores reais do projeto são criados em Dataverse, com base no tempo, despesas, material e atividade de faturação. Todos os atributos operacionais destas transações, incluindo quantidade, preço de custo, preço de venda e projeto são capturados nesta entidade Dataverse. Para mais informações, ver [Valores reais](../actuals/actuals-overview.md). Os registos de valores reais são sincronizados com aplicações Finance and Operations que utilizam o mapa de tabela de escrita dupla **Valores reais da integração do Project Operations (msdyn\_actuals)** para contabilidade a jusante.

   ![Integração de valores reais](./Media/DW4Actuals.png)

O mapa de tabela de **Valores reais de integração do Project Operations** sincroniza todos os registos da entidade **Valores reais** em Dataverse, com o atributo **Skip Sync (apenas uso interno)** definido como **Falso**. Este valor de atributo é definido em Dataverse automaticamente quando o registo é criado. Exemplos em que este atributo é definido para **Verdadeiro** são:

  - Os valores reais de custo do projeto para transações interempresa. Para obter mais informações, consulte [Criar transações interempresa](../project-accounting/create-intercompany-transactions.md). Estes registos são ignorados porque o sistema recria o custo real do projeto em aplicações Finance and Operations quando a fatura do fornecedor interempresa é publicada.
  - Registos de vendas negativos não faturados criados quando a fatura proforma é confirmada. Estes registos são ignorados porque o sub-livro razão do projeto em aplicações Finance and Operations não inverte o registo de vendas não faturados na faturação, mas altera o estado para faturar totalmente.

O mapa de tabela de dupla escrita sincroniza os valores reais da tabela de teste, **ProjCDSActualsImport**. Estes registos são processados pelo processo periódico **Importar da tabela de teste** ao criar linhas de diário do Project Operations e linhas de proposta de fatura de projeto. Para mais informações, consulte [diário de Integração no Project Operations](../project-accounting/project-operations-integration-journal.md).

Dataverse captura também as ligações entre as transações de valores reais do projeto na entidade de **ligação de transações**. Para obter mais informações, consulte [ligar valores reais para registos originais](../actuals/linkingactuals.md). As ligações entre transações de valores reais também são sincronizadas com aplicações Finance and Operations que utilizam o mapa de tabelas de dupla escrita, **entidade de integração para relações de transação de projetos (msdyn\_transactionconnections)**. Estes registos são usados pelo processo periódico, **Importar da tabela de teste** ao criar linhas de diário do Project Operations e linhas de proposta de fatura de projeto.

A publicação de um diário de integração do Project Operations e de uma proposta de fatura do projeto despoleta uma atualização nos respetivos registos na tabela de teste, **ProjCDSActualsImport**. O sistema captura e regista os seguintes atributos contabilísticos para transações de valores reais:

- Montante de moeda contabilística
- Câmbio
- Número de voucher
- Valor de imposto sobre vendas

O mapa da tabela **Valores reais de integração do Project Operations** atualiza os registos dos respetivos registos de valores reais no Dataverse com esta informação.
