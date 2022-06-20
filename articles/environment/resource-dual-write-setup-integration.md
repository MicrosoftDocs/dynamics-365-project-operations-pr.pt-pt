---
title: Configuração do Project Operations e integração de dados de configuração
description: Este artigo fornece informações sobre a preparação e configuração de mapas de escrita dupla do Project Operations.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 173ff01e938af48d2d6488d5e59cf4e74b3af8e4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914554"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Configuração do Project Operations e integração de dados de configuração

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Este artigo fornece informações sobre a integração de escrita dupla do Project Operations para entidades de preparação e configuração.

## <a name="project-contracts-contract-lines-and-projects"></a>Contratos do projeto, linhas do contrato e projetos

Os contratos de projeto, linhas de contrato e projetos são criados no Dataverse e sincronizados com as aplicações de Finanças e Operações para contabilidade adicional. Os registos nestas entidades só podem ser criados e apagados em Dataverse. No entanto, os atributos de contabilidade, tais como as predefinições do grupo de impostos de vendas e as dimensões financeiras, podem ser adicionadas a estes registos nas aplicações de finanças e operações.

  ![Conceitos de integração de contrato do projeto.](./media/1ProjectContract.jpg)

As atividades de vendas, oportunidades e cotações são monitorizadas no Dataverse e não são sincronizadas com as aplicações de finanças e operações porque não existe nenhuma contabilidade a jusante associada a esta atividade.

A funcionalidade de contrato do projeto no Dataverse cria um registo de contrato de projeto nas aplicações de finanças e operações através do mapa de tabela **Cabeçalho de contratos do projeto (salesorders)**. Guardar um contrato de projeto no Dataverse também inicia a criação de um registo de entidade de contrato de clientes. Este registo é sincronizado com as aplicações de finanças e operações utilizando o mapa de tabela **Origem de fundos do projeto (msdyn\_projectcontractssplitbillingrules)**. Este mapa também sincroniza adições, atualizações e supressões de clientes do contrato de projeto. A divisão de percentagem de faturação entre clientes do contrato do projeto só é dominada no Dataverse e não é sincronizada com as aplicações de finanças e operações.

Depois de um contrato do projeto ser criado no Dataverse, o contabilista do projeto pode atualizar os atributos de contabilidade para este contrato de projeto nas aplicações de finanças e operações, acedendo a **Gestão de projeto e contabilidade** > **Contratos de projeto** > **Configurar** > **Mostrar contabilidade predefinida**. O contabilista pode rever atributos do contrato do projeto operacional, tais como a data de entrega e o montante do contrato solicitados, selecionando o ID do contrato do projeto nas aplicações de finanças e operações, que abrem o histórico de contrato do projeto relacionado no Dataverse.

A entidade do projeto é sincronizada com as aplicações de finanças e operações utilizando o mapa de tabela **Projects V2 (msdyn\_projects)**. O contabilista do projeto pode:

  - Reveja projetos nas aplicações de finanças e operações acedendo a **Gestão de projetos e contabilidade** > **Todos os projetos**. 
  - Atualizar atributos de contabilidade para o projeto nas aplicações de finanças e operações acedendo a **Gestão de projetos e contabilidade** > **Todos os projetos** > **Configuar** > **Mostrar contabilidade predefinida**.  
  - Reveja os atributos de projeto operacionais, como datas de início e de fim estimadas, selecionando o ID do projeto nas aplicações de finanças e operações, que abre o registo de projeto relacionado no Dataverse.

Um projeto está associado a um contrato de projeto através da entidade **Linha de contrato do Projeto**.

As linhas de contrato do projeto no Dataverse criam uma regra de faturação de contrato de projeto nas aplicações de finanças e operações através do mapa de tabela **Linhas de contratos do projeto (salesorderdetails)**. O método de faturação define o tipo de regra de faturação de contrato do projeto nas aplicações de Finanças e Operações:

  - As linhas de contrato de projeto com um método de faturação de tempo e material criam uma regra de faturação do tempo e do tipo de material.
  - As linhas de contrato de um método de faturação fixa criam uma regra de faturação de marco.

As linhas de contrato do projeto podem ser revistas pelo contabilista do projeto nas aplicações de finanças e operações, acedendo a **Gestão de projeto e contabilidade** > **Contratos do projeto** > **Configurar** > **Mostrar contabilidade predefinida** e revendo os detalhes no separador **Linhas do contrato**. O contabilista pode também definir as dimensões financeiras predefinidas para as linhas de contrato do método de faturação de preço fixo neste separador.

## <a name="billing-milestones"></a>Marcos de faturação

As linhas de contrato de projeto utilizando o método de faturação de preço fixo são faturadas através de marcos de faturação. Os marcos de faturação são sincronizados para projetar transações em conta nas aplicações de finanças e operações utilizando o mapa de tabela **Marcos de linha de contrato de integração no Project Operations (msdyn\_contractlinescheduleofvalues)**.

  ![Integração de marcos de faturação.](./media/2Milestones.jpg)

O contabilista pode rever as transações contabilísticas e ajustar os atributos contabilísticos dessas transações indo para **Gestão de projetos e gestão contabilística** > **Contratos de projeto** > **Manter** > **Transações de conta** ou **Gestão de projetos e gestão contabilística** > **Todos os projetos** > **Manter** > **Transações de conta**.

Quando cria pela primeira vez um marco de faturação para uma determinada linha de contrato de projeto, o sistema cria automaticamente um projeto de estimativa de receitas de preço fixo para o projeto associado a esta linha de contrato. Os projetos de estimativa de receitas a preço fixo podem ser revistos indo para **Gestão de projetos e gestão contabilística** > **Projetos de estimativa de receitas de preço fixo**.

### <a name="project-tasks"></a>Tarefas do projeto

As tarefas de projeto são sincronizadas com as aplicações De finanças e operações através do mapa de tabela **Tarefas do projeto (msdyn\_projecttasks)** apenas para fins de referência. A criação, atualização e eliminação de operações não é suportada através das aplicações de finanças e operações.

  ![Integração de tarefas de projeto.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Recursos do projeto

A entidade **Funções de recurso do projeto** é sincronizada com as aplicações de finanças e operações, através do mapa de tabela **Funções de recursos do projeto para todas as companhias (bookableresourcecategories)** apenas para efeitos de referência. Uma vez que as funções de recurso no Dataverse não são específicas da empresa, o sistema cria automaticamente os respetivos registos de funções de recursos específicos da empresa nas aplicações de finanças e operações para todas as entidades legais incluídas no âmbito de integração de escrita dupla.

![Integração de funções de recurso.](./media/5Resources.jpg)

Os recursos do projeto no Project Operations são mantidos no Dataverse e não são sincronizados com as aplicações de Finanças e Operações.

### <a name="transaction-categories"></a>Categorias de transações

As categorias de transação são mantidas no Dataverse e sincronizadas com as aplicações de Finanças e Operações utilizando o mapa de tabela **Categorias de transação do Projeto (msdyn\_transactioncategories)**. Após a sincronização do registo da categoria de transação, o sistema cria automaticamente quatro registos de categoria partilhada. Cada registo corresponde a um tipo de transação nas aplicações de Finanças e Operações e liga-os ao registo de categoria de transações.

![Integração de categorias de transação.](./media/4TransactionCategories.jpg)

A utilização de categorias de transações para estimativas e valores reais requer que o contabilista ou administrador do sistema crie categorias de projetos correspondentes em todas as entidades legais. Para obter mais informações, consulte [Configurar categorias de projetos](../project-accounting/configure-project-categories.md).
