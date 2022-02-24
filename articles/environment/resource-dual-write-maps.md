---
title: Versões de mapa de escrita dupla do Project Operations
description: Este tópico fornece a lista de mapas de escrita dupla necessários para Dynamics 365 Project Operations.
author: sigitac
manager: Annbe
ms.date: 04/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fa0342985f2c860cd3cb3f686f0dcaa59d8cfd41
ms.sourcegitcommit: bc51629df94c164325cf2afee387d0e7cda66da7
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/23/2021
ms.locfileid: "5939028"
---
# <a name="project-operations-dual-write-map-versions"></a>Versões de mapa de escrita dupla do Project Operations

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

A utilização de Dynamics 365 Project Operations para cenários de recursos/não armazenados requer um conjunto de mapas de dupla escrita para estar em execução no ambiente. 

## <a name="prerequisite-maps-dual-write-orchestration-solution"></a>Mapas de pré-requisito: Solução de orquestração de escrita dupla

São necessários os seguintes mapas pré-requisitos para a solução de Project Operations. Certifique-se de que executa os mapas listados na tabela seguinte e quaisquer mapas de tabelas relacionados no seu ambiente.

| Mapa de tabelas | Sincronização inicial |
| --- | --- |
| Livro razão (msdyn_ledgers) | Requer sincronização inicial para o mapa de tabela e todos os pré-requisitos. Mestre para sincronização inicial em aplicações Finance and Operations. |
| Entidades legais (cdm_companies) | Não necessário. O sistema povoa esta entidade automaticamente quando os ambientes estão ligados usando a dupla escrita. |
| Clientes V3 (contas) | Não é necessário para o aprovisionamento. |
| Fornecedores V2 (msdyn_vendors) | Não é necessário para o aprovisionamento. |

1. Na lista de mapas, selecione o mapa Livro-razão **(msdyn\_ledgers)** com todos os pré-requisitos e selecione a caixa de verificação de **sincronização inicial**. No Campo **Master para sincronização inicial** selecione aplicações **Finance and Operations** para mapa de livros razão e todos os mapas pré-requisitos. Selecione **Executar**.

![Sincronização do mapa de livros](media/DW6.png)

1. Siga os mesmos passos para todos os mapas de tabela restantes listados na tabela acima. Não selecione a caixa de verificação de **sincronização inicial** quando executar esses mapas.

## <a name="project-operations-dual-write-maps"></a>Mapas de escrita dupla do Project Operations

São necessários os seguintes mapas para uma solução de Project Operations.

| **Mapa da entidade** | **Versão mais recente** | **Sincronização inicial** |
| --- | --- | --- |
| Entidade de integração para as relações de transações do projeto (msdyn\_transactionconnections) | 1.0.0.0 | Não é necessário para o aprovisionamento. |
| Cabeçalhos de contrato de projeto (encomendas de vendas) | 1.0.0.1 | Não é necessário para o aprovisionamento. |
| Itens de contrato do projeto (salesorderdetails) | 1.0.0.0 | Não é necessário para o aprovisionamento. |
| Fonte de financiamento do projeto (msdyn_projectcontractsplitbillingrules) | 1.0.0.1 | Não é necessário para o aprovisionamento. |
| Tabela de integração do Project Operations para estimativas de materiais (msdyn\_estimatelines) | 1.0.0.0 | Não é necessário para o aprovisionamento. |
| Propostas de fatura do projeto V2 (faturas) | 1.0.0.2 | Não é necessário para o aprovisionamento. |
| Valores reais de integração com o Project Operations (msdyn_actuals) | 1.0.0.14 | Não é necessário para o aprovisionamento. |
| Marcos do item de contrato de integração com o Project Operations (msdyn_contractlinesscheduleofvalues) | 1.0.0.4 | Não é necessário para o aprovisionamento. |
| Entidade de integração com o Project Operations para estimativas de despesa (msdyn_estimateslines) | 1.0.0.2 | Não é necessário para o aprovisionamento. |
| Entidade de integração com o Project Operations para estimativas de horas (msdyn_resourceassignments) | 1.0.0.5 | Não é necessário para o aprovisionamento. |
| Entidade de exportação de categorias de despesas do projeto de integração com o Project Operations (msdyn_expensecategories) | 1.0.0.2 | Não é necessário para o aprovisionamento. |
| Entidade de exportação de despesas do projeto de integração com o Project Operations (msdyn_expenses) | 1.0.0.2 | Não é necessário para o aprovisionamento. |
| Entidade de exportação de faturas de projeto de integração de projetos do Project Operations (msdyn_projectvendorinvoices) | 1.0.0.0 | Não é necessário para o aprovisionamento. |
| Entidade de exportação de linhas de faturas de projeto de integração de projetos do Project Operations (msdyn_projectvendorinvoicelines) | 1.0.0.0 | Não é necessário para o aprovisionamento. |
| Funções de recursos de projeto para todas as Empresas (bookableresourcecategories) | 1.0.0.1 | Requer uma sincronização inicial para o mapa de tabela sincronizar as funções de gestor de projeto e de recursos dos membros da Equipa que são povoadas no ambiente Dynamics 365 Dataverse durante o aprovisionamento. Dataverse é a principal fonte para a sincronização inicial. |
| Tarefas do projeto (msdyn_projecttasks) | 1.0.0.4 | Não é necessário para o aprovisionamento. |
| Categorias de transações de projetos (msdyn_transactioncategories) | 1.0.0.0 | Não é necessário para o aprovisionamento. |
| Projetos V2 (msdyn_projects) | 1.0.0.1 | Não é necessário para o aprovisionamento. |

Complete os seguintes passos para executar os mapas listados.

1. Ative as funções de recursos do Projeto para mapa de tabela **todas as empresas (bookableresourcecategories)**, uma vez que este mapa requer a sincronização inicial. No campo **Master para sincronização inicial**, selecione **Common data service**. 

 ![Sincronização do mapa da tabela de funções de recursos](media/6ResourceInitialSync.jpg)

 Espere até que o estado do mapa esteja **a funcionar** antes de passar para o próximo passo.

2. Selecione todos os mapas restantes necessários. Pode filtrar na lista de mapas de escrita dupla usando a palavra-chave, na pesquisa **Projeto** no canto superior direito. Pode selecionar vários mapas e depois executar. Para obter mais informações, consulte [Gerir vários mapas de tabelas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/multiple-entity-maps). Certifique-se de ativar e executar mapas de entidades relacionadas.

### <a name="project-operations-dual-write-map-versions"></a>Versões de mapa de escrita dupla do Project Operations

Execute sempre a versão mais recente do mapa no seu ambiente. Certas funcionalidades e capacidades podem não funcionar corretamente se existirem alguma das seguintes condições:

- Um mapa não está ativado.
- A versão mais recente do mapa não está ativada. 
- Os mapas de mesa relacionados não estão ativados.

Pode ver a versão ativa do mapa na coluna **Versão** na página **Escrita Dupla**. Pode ativar uma nova versão do mapa selecionando **Versões do mapa de tabela** , selecionando a versão mais recente e, em seguida, guardar a versão selecionada. Se tiver personalizado um mapa de tabela fora da caixa, terá de reaplicar as alterações. Para mais informações, consulte [Gestão do ciclo de vida da aplicação](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).
