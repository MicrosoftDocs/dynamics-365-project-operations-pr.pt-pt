---
title: Configuração do Project Operations e integração de dados de configuração
description: Este tópico fornece informações sobre a configuração e definição de mapas de escrita dupla do Project Operations.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6d263f7c5ef0d562edde6a603340a3b8746195df190fdb527bfa40297f68eed2
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986550"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Configuração do Project Operations e integração de dados de configuração

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Este tópico fornece informações sobre a integração de escrita dupla do Project Operations para entidades de definição e configuração.

## <a name="project-contracts-contract-lines-and-projects"></a>Contratos do projeto, linhas do contrato e projetos

Os contratos de projeto, as linhas de contrato e os projetos são criados e sincronizados em aplicações Dataverse para aplicações Finance and Operations para gestão contabilística adicional. Os registos nestas entidades só podem ser criados e apagados em Dataverse. No entanto, atributos contabilísticos como os incumprimentos do grupo de impostos sobre vendas e as dimensões financeiras podem ser adicionados a estes registos nas aplicações Finance and Operations.

  ![Conceitos de integração de contrato do projeto.](./media/1ProjectContract.jpg)

A atividade de vendas, oportunidades e as cotações são rastreadas em Dataverse e não sincronizam para as aplicações Finance and Operations porque não há nenhuma contabilidade a jusante associada a esta atividade.

A funcionalidade do contrato do projeto em Dataverse cria um registo de contrato de projeto em aplicações Finance and Operations usando o mapa de tabelas do **Cabeçalho do contrato do projeto (salesorders)**. Guardar um contrato de projeto no Dataverse também inicia a criação de um registo de entidade de contrato de clientes. Este registo é sincronizado com aplicações Finance and Operations que utilizam o mapa de tabelas **Fonte de financiamento do projeto (msdyn\_projectcontractssplitbillingrules)**. Este mapa também sincroniza adições, atualizações e supressões de clientes do contrato de projeto. As percentagens de faturação divididas entre os clientes do contrato de projeto são dominadas apenas em Dataverse e não não sincronizadas com aplicações Finance and Operations.

Após a criação de um contrato de projeto em Dataverse, o contabilista do projeto pode atualizar os atributos contabilísticos deste contrato de projeto em aplicações Finance and Operations indo para **Gestão de projetos e gestão contabilística** > **Contratos de projeto** > **Configurar** > **Apresentar gestão contabilística predefinida**. O contabilista pode rever os atributos do contrato de projeto operacional, tais como data de entrega solicitada e valor do contrato, selecionando o ID do contrato do projeto em aplicações Finance and Operations que abrem o registo do contrato de projeto em Dataverse.

A entidade do projeto está sincronizada com aplicações Finance and Operations que utilizam o mapa de tabelas de **Projetos V2 (msdyn\_projects)**. O contabilista do projeto pode:

  - Rever projetos em aplicações Finance and Operations indo a **Gestão de projetos e gestão contabilística** > **Todos os projetos**. 
  - Atualizar os atributos contabilísticos para o projeto em aplicações Finance and Operations indo para **Gestão de projetos e gestão contabilística** > **Todos os projetos** > **Configurar** > **Mostrar contabilidade predefinida**.  
  - Reveja os atributos do projeto operacional, tais como datas estimadas de início e fim, selecionando o ID do projeto em aplicações Finance and Operations que abrem o registo do projeto em Dataverse.

Um projeto está associado a um contrato de projeto através da entidade **Linha de contrato do Projeto**.

As linhas de contrato do projeto em Dataverse criam uma regra de faturação de contrato do projeto em aplicações Finance and Operations usando o mapa de tabelas do **Linhas do contrato do projeto (salesorderdetails)**. O método de faturação define o tipo de regra de faturação do contrato do projeto em aplicações Finance and Operations:

  - As linhas de contrato de projeto com um método de faturação de tempo e material criam uma regra de faturação do tempo e do tipo de material.
  - As linhas de contrato de um método de faturação fixa criam uma regra de faturação de marco.

As linhas de contrato de projeto podem ser revistas pelo contabilista do projeto em aplicações Finance and Operations, indo para **Gestão de projetos e gestão contabilística** > **Contratos de projeto** > **Configurar** > **Mostrar gestão contabilística predefinida** e rever os detalhes no separador **Linhas de contrato**. O contabilista também pode definir dimensões financeiras padrão para as linhas de contrato de preço fixo neste separador.

## <a name="billing-milestones"></a>Marcos de faturação

As linhas de contrato de projeto utilizando o método de faturação de preço fixo são faturadas através de marcos de faturação. Os marcos da faturação são sincronizados para projetar transações em conta em aplicações Finance and Operations, utilizando o mapa de tabelas de **Marços da linha de contrato de integração de Project Operations (msdyn\_contractlinescheduleofvalues)**.

  ![Integração de marcos de faturação.](./media/2Milestones.jpg)

O contabilista pode rever as transações contabilísticas e ajustar os atributos contabilísticos dessas transações indo para **Gestão de projetos e gestão contabilística** > **Contratos de projeto** > **Manter** > **Transações de conta** ou **Gestão de projetos e gestão contabilística** > **Todos os projetos** > **Manter** > **Transações de conta**.

Quando cria pela primeira vez um marco de faturação para uma determinada linha de contrato de projeto, o sistema cria automaticamente um projeto de estimativa de receitas de preço fixo para o projeto associado a esta linha de contrato. Os projetos de estimativa de receitas a preço fixo podem ser revistos indo para **Gestão de projetos e gestão contabilística** > **Projetos de estimativa de receitas de preço fixo**.

### <a name="project-tasks"></a>Tarefas do projeto

As tarefas do projeto são sincronizadas com aplicações Finance and Operations através do mapa de tabelas de **Tarefas do Projeto (msdyn\_projecttasks)** apenas para fins de referência. Criar, atualizar e eliminar operações não é suportado através das aplicações Finance and Operations.

  ![Integração de tarefas de projeto.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Recursos do projeto

A entidade de **Funções de recursos do Projeto** é sincronizada com aplicações Finance and Operations que utilizam **Funções de recursos do projeto para todas as empresas (bookableresourcecategories)** apenas para fins de referência. Como as funções de recursos em Dataverse não são específicas da empresa, o sistema cria automaticamente os respetivos registos de funções de recursos específicos da empresa em aplicações Finance and Operations automaticamente para todas as entidades jurídicas incluídas no âmbito de integração de escrita dupla.

![Integração de funções de recurso.](./media/5Resources.jpg)

Os recursos do projeto no Project Operations são mantidos em Dataverse e não são sincronizados com aplicações Finance and Operations.

### <a name="transaction-categories"></a>Categorias de transações

As categorias de transações são mantidas em Dataverse e sincronizadas para aplicações Finance and Operations que utilizam o mapa de tabelas **Categorias de transações do Projeto (msdyn\_transactioncategories)**. Após a sincronização do registo da categoria de transação, o sistema cria automaticamente quatro registos de categoria partilhada. Cada registo corresponde a um tipo de transação em aplicações Finance and Operations e liga-os ao registo da categoria de transação.

![Integração de categorias de transação.](./media/4TransactionCategories.jpg)

A utilização de categorias de transações para estimativas e valores reais requer que o contabilista ou administrador do sistema crie categorias de projetos correspondentes em todas as entidades legais. Para obter mais informações, consulte [Configurar categorias de projetos](../project-accounting/configure-project-categories.md).
