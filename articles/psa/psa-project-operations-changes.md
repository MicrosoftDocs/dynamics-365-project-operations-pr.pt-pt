---
title: Alterações de características do Project Service Automation para o Project Operations
description: Este artigo fornece uma descrição geral das alterações de caraterísticas do Project Service Automation para o Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: a9c69fc4296d30763f3994a4955e64ab258ceb4f
ms.sourcegitcommit: 675e9f3615e701c5f998de3a5ea3e25df11ae107
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/09/2022
ms.locfileid: "9459941"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>Alterações de características do Project Service Automation para o Project Operations

A atualização do Dynamics 365 Project Service Automation para o Dynamics 365 Project Operations Lite será realizada em três fases. Este artigo fornece informações sobre as principais alterações que pode esperar quando a atualização estiver concluída.

| Entrega da atualização de versão | Fase 1 <br>(janeiro de 2022) | Fase 2 <br>(novembro de 2022) | Fase 3  |
|------------------|------------------------|---------------------------|---------------------------|
| Não há dependência na estrutura hierárquica do trabalho (WBS) para projetos. | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| A WBS está incluída nos limites atualmente suportados do Project Operations. | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| A WBS fora dos limites atualmente suportados do Project Operations, incluindo o suporte para o Project Desktop Client. | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>Gestão de projetos

As alterações mais significativas na experiência do utilizador encontram-se na área de planeamento do projeto. O Project Operations adotou uma nova experiência moderna para gerir uma estrutura hierárquica do trabalho (WBS), impulsionando as capacidades de agendamento fornecidas pelo [Project for the Web](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5).

## <a name="differences-in-the-scheduling-experience"></a>Diferenças na experiência de agendamento

A tabela seguinte resume as diferenças de agendamento entre o Project Service Automation e o Project Operations.

|  A agendar     |   Project Operations   |   Assistente de Serviço a Pacientes   |
|-----------------|------------------------|---------|
| Modelos de projeto - Capacidade de definir e aplicar modelos de projeto quando um projeto é criado  |  &nbsp;    | :heavy_check_mark: |
| Integração da estrutura hierárquica do trabalho (WBS) com desktop client   |    &nbsp;  | :heavy_check_mark: |
| Restrições - Não iniciar antes de, terminar mais cedo que  | :heavy_check_mark: |   &nbsp;  |
| Marcos - Tarefas com duração zero   | :heavy_check_mark:  |  &nbsp;  |
| As tarefas orientadas por recursos irão respeitar a disponibilidade dos recursos atribuídos   | :heavy_check_mark: |  &nbsp;    |
| Edição faseada por tempo - Editar planos e trabalhar numa base diária   |   &nbsp;  | :heavy_check_mark: |
| Agendamento automático/manual - Utilizar o motor de agendamento do Projeto para agendar tarefas de forma automática ou manual |  &nbsp; | :heavy_check_mark:  |
| Editar grandes projetos diretamente na interface de utilizador: não existe limite para o tamanho de planos que são editáveis  | Limite de tarefas de 500  | :heavy_check_mark:       |
| Percentagem concluída - Progresso da tarefa de marcação   | :heavy_check_mark:  |  &nbsp;  |
| [Modos da Agenda do Projeto](../project-management/scheduling-modes.md) - Definir o projeto como unidades fixas, esforço fixo ou duração fixa | :heavy_check_mark: | &nbsp; |
| Linha Cronológica - Crie e personalize a vista cronológica para visualizar os detalhes da agenda e comunicar com os intervenientes. | :heavy_check_mark:  | &nbsp; |
| Tarefas orientadas pelo esforço - Agendamento do suporte do motor para agendamento de uma tarefa orientada pelo esforço  | :heavy_check_mark:  | &nbsp; |
| Caixa de diálogo **Informações de tarefas** - Guardar detalhes da tarefa utilizando uma caixa de diálogo | :heavy_check_mark:  |  &nbsp;  |
| Arrastar e largar - Tarefas com várias seleções e modificação da sua posição na WBS | :heavy_check_mark: | &nbsp;  |
| Vistas persistentes flexíveis - Definir mais vistas granulares de atributos de tarefa   | :heavy_check_mark:  | &nbsp; |
| Ordenar e filtrar a WBS  | :heavy_check_mark:  | &nbsp; |
| Vista de quadros para entrega de projeto não cascata  | :heavy_check_mark:   | &nbsp; |
| Vista Cronológica - Gráfico de Gantt interativo utilizado para visualizar e editar a WBS   | :heavy_check_mark:  | &nbsp; |
| Atalhos de Teclado - Utilizar atalhos de teclado para operações comuns como, por exemplo, indentar ou inserir  | :heavy_check_mark:  |  &nbsp; |
| Anular em múltiplos níveis - Realizar a análise teste de hipóteses para compreender completamente o impacto das alterações ao reverter e voltar a aplicar um conjunto de operações completo | :heavy_check_mark: | &nbsp; |
| Cortar/Copiar/Colar - Colaborar no desenvolvimento da agenda copiando e colando detalhes da agenda entre aplicações  | :heavy_check_mark: | &nbsp; |
| Listas de verificação de tarefas - Adicionar até 20 itens da lista de verificação a uma tarefa   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>Planeamento de projeto

A página **Projeto** no Project Operations tem um número significativo de diferenças comparativamente com a página **Projeto** no Project Service Automation.

As seguintes ações foram removidas da página **Projetos** como parte da atualização da Fase 1:

  - **Abrir no MS Project**
  - **Criar Modelo**
  - **Desassociar do MS Project**

A página **Projeto** no Project Operations inclui os seguintes separadores novos.

- **Estimativas de Material**
- **Configuração de Faturação de Tarefas**

O separador **Estado** foi removido e o campo **Estado** está agora no separador **Resumo** com o modo de agendamento do projeto.

   ![Atualizações à página Projeto.](media/projectform.png)

O separador **Agenda** mudou de nome para o separador **Tarefa** e apresenta uma nova experiência de planeamento de projeto com o Project for the Web.

   ![Novo separador tarefas de Projeto.](media/tasktab.png)

## <a name="scheduling-modes"></a>Modos de agendamento

O Project Operations introduziu uma nova funcionalidade [Modos de agendamento](../project-management/scheduling-modes.md). Todos os projetos de Project Service Automation existentes assumem por predefinição uma **Duração fixa** no Project Operations. No entanto, a predefinição para novos projetos pode ser gerida acedendo a **Definições** > **Pârametros** > **Pârametro** > **Modo agenda**.

   ![Definições do parâmetro do projeto para o modo Agenda.](media/projectparameter.png)

## <a name="project-planning-limits"></a>Limites de planeamento de projeto

O Project Operations baseia-se no Project for the Web para todas as operações de agendamento de projetos. O Project for the Web gere a estrutura hierárquica do trabalho utilizando os limites na tabela seguinte.

| **Campo**                                          | **Limite**             |
|----------------------------------------------------|-----------------------|
| Total de tarefas máximo para um projeto                  | 500                   |
| Duração total máxima para um projeto               | 3650 dias (10 anos)  |
| Total de recursos máximo para um projeto              | 300                   |
| Total de ligações máximo (apenas a sucessora) para um projeto | 600                   |
| Total de campos personalizados máximo para um projeto          | 10                    |
| Nível máximo da hierarquia                            | 10 níveis             |
| Máximo de ligações (sucessora + antecessora)            | 20                    |
| Duração máxima da tarefa da folha                      | 1250 dias             |
| Duração máxima de uma tarefa de resumo                 | 3650 dias (10 anos)  |
| Máximo de recursos atribuídos a uma tarefa               | 20 recursos          |
| Intervalo de datas suportado para uma tarefa                    | 1/1/2000 - 31/12/2149 |
| Itens da lista de verificação                                    | 20                    |

## <a name="project-planning-extensibility-and-development"></a>Extensibilidade e desenvolvimento do planeamento de projetos

Depois de atualizar para o Project Operations, tem de utilizar as API de Agendamento de Projetos para executar operações de criação, atualização e eliminação nas seguintes entidades:

|   Nome da entidade           |   Nome lógico da entidade       |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Tarefa de Projeto            | msdyn_projecttask           |
| Dependência de Tarefa de Projeto | msdyn_projecttaskdependency |
| Atribuição de Recurso     | msdyn_resourceassignment    |
| Registo do Projeto          | msdyn_projectbucket         |
| Membro da Equipa do Projeto     | msdyn_projectteam           |

Se tiver atualmente personalizações que envolvam estas entidades, consulte [Utilizar API da agenda de projetos para realizar operações com as entidades de agendamento](../project-management/schedule-api-preview.md) para orientações de implementação.

## <a name="data-model-changes"></a>Alterações ao modelo de dados

Como parte da Fase 1 da atualização, existem alterações ao modelo de dados. Estas alterações são sobretudo alterações de campo a entidades existentes. Na Fase 1, as entidades, **msydn_project** e **msdyn_projectteam** são uma refatoração das personalizações. 

> [!IMPORTANT]
> Esta secção será atualizada com entidades adicionais à medida que as fases de atualização futuras são concluídas.

Os seguintes campos foram substituídos por campos novos.

|   Entity          |   Antigo nome lógico   |   Novo nome lógico    |
|-------------------|----------------------|-----------------------|
| msdyn_project     | msdyn_actualhours    | msdyn_effortcompleted |
| msdyn_project     | msdyn_plannedhours   | msdyn_effort          |
| msdyn_project     | msdyn_remaininghours | msdyn_effortremaining |
| msdyn_project     | msdyn_scheduledend   | msdyn_finish          |
| msdyn_project     | msdyn_wbsduration    | msdyn_duration        |
| msdyn_projectteam | msdyn_assignedhours  | msdyn_effort          |
| msdyn_projectteam | msdyn_from           | msdyn_start           |
| msdyn_projectteam | msdyn_to             | msdyn_finish          |

Foram adicionados os seguintes campos.

|   Entity          |   Nome lógico                               |   Description |
|-------------------|----------------------------------------------|---------------|
| msdyn_project     | msdyn_actualfeesales                         | Mostra o valor agregado da taxa de vendas no projeto. Para utilização apenas no Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialcost                     | Mostra o valor agregado do custo material real no projeto. Para utilização apenas no Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialsales                    | Mostra o valor agregado da venda material real no projeto. Para utilização apenas no Project Service Automation. |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | O item de contrato associado a este projeto. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | Este é um campo do sistema interno, utilizado para **Copiar o projeto** associado ao Identificador de correlação. Para utilização apenas no Project Service Automation. |
| msdyn_project     | msdyn_copyprojectsessionid                   | Este é um campo do sistema interno, utilizado para **Copiar o projeto** associado ao Identificador de sessão. Para utilização apenas no Project Service Automation. |
| msdyn_project     | msdyn_globalrevisiontoken                    | Token de revisão global xRM da ultima sincronização do serviço de agendamento do projeto. |
| msdyn_project     | msdyn_msprojectdocument                      | O documento do Microsoft Project que pertence ao projeto. |
| msdyn_project     | msdyn_plannedmaterialcost                    | O valor agregado do custo material planeado no projeto. Para utilização apenas no Project Service Automation. |
| msdyn_project     | msdyn_plannedmaterialsales                   | O valor agregado da venda material planeada no projeto. Para utilização apenas no Project Service Automation. |
| msdyn_project     | msdyn_program                                | O programa com que este projeto está relacionado. |
| msdyn_project     | msdyn_quotelineproject                       | A linha de Proposta associada a este projeto. |
| msdyn_project     | msdyn_replaylogheader                        | O cabeçalho dos registos de reprodução. |
| msdyn_project     | msdyn_schedulemode                           | O modo de agendamento predefinido utilizado para todas as tarefas do projeto.  |
| msdyn_project     | msdyn_taskearlieststart                      | A data de início mais antiga de qualquer tarefa no projeto.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | O membro da equipa do projeto do qual este membro da equipa do projeto foi copiado. |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | Indica se deve criar o requisito de recursos para um membro da equipa genérico recentemente criado.  |
| msdyn_projectteam | msdyn_deletestatus                           | O estado de eliminação do membro da equipa a monitorizar se existir um pedido de eliminação enviado ao serviço de agendamento do projeto e se envia uma resposta de volta com êxito dentro do intervalo de tempo esperado. |
| msdyn_projectteam | msdyn_effortcompleted                        | Monitoriza o esforço realizado pelo membro da equipa nas respetivas atribuições. |
| msdyn_projectteam | msdyn_effortremaining                        | Monitoriza o esforço a concluir pelo membro da equipa nas respetivas atribuições. |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | O tempo de espera a partir do momento em que o membro da equipa envia um pedido de eliminação ao serviço de agendamento do projeto até ao membro da equipa é efetivamente eliminado no Microsoft Dataverse.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | O carimbo de data/hora a gravar quando o pedido de eliminação do membro da equipa é enviado para o serviço de agendamento do projeto. |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Mostra o membro da equipa do projeto do qual este membro da equipa do projeto foi copiado.  |

## <a name="project-templates"></a>Modelos de projeto

O Project Operations não fornece suporte a modelos de projeto. No entanto, é possível replicar grande parte da funcionalidade principal com a utilização da [API da cópia do projeto](../project-management/dev-copy-project.md).

## <a name="desktop-add-in-support"></a>Suporte de add-ins de ambiente de trabalho

O suporte para o add-in do Microsoft Project Desktop não estará disponível nas duas primeiras fases da atualização. Na Fase 3, os clientes que tenham projetos maiores que os limites atualmente suportados do Project for the Web poderão utilizar o add-in de ambiente de trabalho.

## <a name="editing-resource-assignment-contours"></a>Editar desvios de atribuição de recursos

A capacidade de editar desvios de atribuição de recursos estará disponível quando a Fase 2 da atualização estiver disponível.

## <a name="billing-and-pricing"></a>Faturação e preços

As seguintes novas funcionalidades foram adicionadas ao Project Operations. Estas funcionalidades são aditivas por natureza e não têm impacto no modelo de dados do Project Service Automation.

- [Registar a utilização do material em projetos e tarefas de projeto](../material/material-usage-log.md)
- [Gestão de subcontratos](../pro/subcontracting/managing-subcontracts-overview.md)
- [Adiantamentos e contratos baseados em sinais](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Estado a não exceder e validações do contrato](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [Faturação baseada nas tarefas](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>Componentes preteridos

As tabelas seguintes documentam todos os campos preteridos que são movidos para a solução de componentes preterida após a atualização. Para mais informações e uma ligação à solução, consulte [Dynamics 365 Project Service Automation 3x para o Project Operations 4x componentes preteridos](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution).

### <a name="invoicedetail"></a>invoicedetail

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
|invoicedetail.msdyn_contractline    |

### <a name="msdyn_actual"></a>msdyn_actual

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_actual.msdyn_salescontractline                                                          |

### <a name="msdyn_characteristicreqforteammember"></a>msdyn_characteristicreqforteammember

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_characteristicreqforteammember.msdyn_characteristic                                     |
| msdyn_characteristicreqforteammember.msdyn_characteristicreqforteammemberid                   |
| msdyn_characteristicreqforteammember.msdyn_characteristictype                                 |
| msdyn_characteristicreqforteammember.msdyn_name                                               |
| msdyn_characteristicreqforteammember.msdyn_ratingvalue                                        |
| msdyn_characteristicreqforteammember.msdyn_resourcerequirementid                              |

### <a name="msdyn_contractlineinvoiceschedule"></a>msdyn_contractlineinvoiceschedule

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_contractlineinvoiceschedule.msdyn_contractline                                          |
| msdyn_contractlinescheduleofvalue.msdyn_contractline                                          |
 
### <a name="msdyn_dataexport"></a>msdyn_dataexport

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_dataexport.msdyn_dataexportid                                                           |
| msdyn_dataexport.msdyn_datatoken                                                              |
| msdyn_dataexport.msdyn_entityname                                                             |
| msdyn_dataexport.msdyn_exportedrecordcount                                                    |
| msdyn_dataexport.msdyn_exportstatus                                                           |
| msdyn_dataexport.msdyn_linkedentitydata                                                       |
| msdyn_dataexport.msdyn_name                                                                   |
| msdyn_dataexport.msdyn_pagingdata                                                             |

### <a name="msdyn_fact"></a>msdyn_fact

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_fact.msdyn_salescontractline                                                            |

### <a name="msdyn_findworkevent"></a>msdyn_findworkevent

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_findworkevent.msdyn_bookableresource                                                    |
| msdyn_findworkevent.msdyn_findworkeventid                                                     |
| msdyn_findworkevent.msdyn_name                                                                |
| msdyn_findworkevent.msdyn_timestamp                                                           |
| msdyn_findworkevent.msdyn_type                                                                |
| msdyn_findworkevent.msdyn_value                                                               |
| msdyn_findworkevent.msdyn_work                                                                |

### <a name="msdyn_invoicelinetransaction"></a>msdyn_invoicelinetransaction

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_invoicelinetransaction.msdyn_invoiceline                                                |
| msdyn_invoicelinetransaction.msdyn_salescontractline                                          |

### <a name="msdyn_journalline"></a>msdyn_journalline

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_journalline.msdyn_salescontractline                                                     |

### <a name="msdyn_opportunitylineresourcecategory"></a>msdyn_opportunitylineresourcecategory

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylineresourcecategory.msdyn_billingtype                                       |
| msdyn_opportunitylineresourcecategory.msdyn_description                                       |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylineresourcecategoryid                 |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylinetransactionclassification          |
| msdyn_opportunitylineresourcecategory.msdyn_resourcecategory                                  |

### <a name="msdyn_opportunitylinetransaction"></a>msdyn_opportunitylinetransaction

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransaction.msdyn_accountcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_accountingdate                                         |
| msdyn_opportunitylinetransaction.msdyn_accountvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_amount                                                 |
| msdyn_opportunitylinetransaction.msdyn_amount_base                                            |
| msdyn_opportunitylinetransaction.msdyn_amountmethod                                           |
| msdyn_opportunitylinetransaction.msdyn_basisamount                                            |
| msdyn_opportunitylinetransaction.msdyn_basisamount_base                                       |
| msdyn_opportunitylinetransaction.msdyn_basisprice                                             |
| msdyn_opportunitylinetransaction.msdyn_basisprice_base                                        |
| msdyn_opportunitylinetransaction.msdyn_basisquantity                                          |
| msdyn_opportunitylinetransaction.msdyn_billingtype                                            |
| msdyn_opportunitylinetransaction.msdyn_bookableresource                                       |
| msdyn_opportunitylinetransaction.msdyn_contactcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_contactvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_customertype                                           |
| msdyn_opportunitylinetransaction.msdyn_description                                            |
| msdyn_opportunitylinetransaction.msdyn_documentdate                                           |
| msdyn_opportunitylinetransaction.msdyn_enddatetime                                            |
| msdyn_opportunitylinetransaction.msdyn_exchangeratedate                                       |
| msdyn_opportunitylinetransaction.msdyn_opportunityline                                        |
| msdyn_opportunitylinetransaction.msdyn_opportunitylinetransactionid                           |
| msdyn_opportunitylinetransaction.msdyn_percent                                                |
| msdyn_opportunitylinetransaction.msdyn_price                                                  |
| msdyn_opportunitylinetransaction.msdyn_price_base                                             |
| msdyn_opportunitylinetransaction.msdyn_pricelist                                              |
| msdyn_opportunitylinetransaction.msdyn_product                                                |
| msdyn_opportunitylinetransaction.msdyn_project                                                |
| msdyn_opportunitylinetransaction.msdyn_quantity                                               |
| msdyn_opportunitylinetransaction.msdyn_resourcecategory                                       |
| msdyn_opportunitylinetransaction.msdyn_resourceorganizationalunitid                           |
| msdyn_opportunitylinetransaction.msdyn_startdatetime                                          |
| msdyn_opportunitylinetransaction.msdyn_task                                                   |
| msdyn_opportunitylinetransaction.msdyn_transactioncategory                                    |
| msdyn_opportunitylinetransaction.msdyn_transactionclassification                              |
| msdyn_opportunitylinetransaction.msdyn_transactiontypecode                                    |
| msdyn_opportunitylinetransaction.msdyn_unit                                                   |
| msdyn_opportunitylinetransaction.msdyn_unitschedule                                           |
| msdyn_opportunitylinetransaction.msdyn_vendortype                                             |

### <a name="msdyn_opportunitylinetransactioncategory"></a>msdyn_opportunitylinetransactioncategory

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactioncategory.msdyn_billingtype                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_description                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactioncategoryid           |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactionclassification       |
| msdyn_opportunitylinetransactioncategory.msdyn_transactioncategory                            |

### <a name="msdyn_opportunitylinetransactionclassificatio"></a>msdyn_opportunitylinetransactionclassificatio

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactionclassificatio.msdyn_billingtype                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_description                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_include                                   |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunityline                           |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunitylinetransactionclassificatioid |
| msdyn_opportunitylinetransactionclassificatio.msdyn_transactionclassification                 |

### <a name="msdyn_orderlineresourcecategory"></a>msdyn_orderlineresourcecategory

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlineresourcecategory.msdyn_contractline                                            |

### <a name="msdyn_orderlinetransaction"></a>msdyn_orderlinetransaction

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransaction.msdyn_salescontractline                                            |
| msdyn_orderlinetransactioncategory.msdyn_contractline                                         |

### <a name="msdyn_orderlinetransactionclassification"></a>msdyn_orderlinetransactionclassification

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransactionclassification.msdyn_contractline                                   |

### <a name="msdyn_project"></a>msdyn_project

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_project.msdyn_actualdurationminutes                                                     |
| msdyn_project.msdyn_actualhours                                                               |
| msdyn_project.msdyn_istemplate                                                                |
| msdyn_project.msdyn_plannedhours                                                              |
| msdyn_project.msdyn_projecttemplate                                                           |
| msdyn_project.msdyn_remaininghours                                                            |
| msdyn_project.msdyn_scheduleddurationminutes                                                  |
| msdyn_project.msdyn_scheduledend                                                              |
| msdyn_project.msdyn_stagename                                                                 |
| msdyn_project.msdyn_wbsduration                                                               |


### <a name="msdyn_projecttask"></a>msdyn_projecttask

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttask.msdyn_actualdurationminutes                                                 |
| msdyn_projecttask.msdyn_actualeffort                                                          |
| msdyn_projecttask.msdyn_aggregationdirection                                                  |
| msdyn_projecttask.msdyn_assignedresources                                                     |
| msdyn_projecttask.msdyn_assignedteammembers                                                   |
| msdyn_projecttask.msdyn_autoscheduling                                                        |
| msdyn_projecttask.msdyn_costestimatecontour                                                   |
| msdyn_projecttask.msdyn_effortcontour                                                         |
| msdyn_projecttask.msdyn_islinetask                                                            |
| msdyn_projecttask.msdyn_numberofresources                                                     |
| msdyn_projecttask.msdyn_remaininghours                                                        |
| msdyn_projecttask.msdyn_resourceutilization                                                   |
| msdyn_projecttask.msdyn_salesestimatecontour                                                  |
| msdyn_projecttask.msdyn_scheduledhours                                                        |
| msdyn_projecttask.msdyn_wbsid                                                                 |

### <a name="msdyn_projecttaskstatususer"></a>msdyn_projecttaskstatususer

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttaskstatususer.msdyn_bookableresource                                            |
| msdyn_projecttaskstatususer.msdyn_description                                                 |
| msdyn_projecttaskstatususer.msdyn_expectedcompletiondate                                      |
| msdyn_projecttaskstatususer.msdyn_expectedhourstocomplete                                     |
| msdyn_projecttaskstatususer.msdyn_iscompleted                                                 |
| msdyn_projecttaskstatususer.msdyn_name                                                        |
| msdyn_projecttaskstatususer.msdyn_percentcomplete                                             |
| msdyn_projecttaskstatususer.msdyn_projecttaskid                                               |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatusindicator                                  |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatususerid                                     |

### <a name="msdyn_projectteam"></a>msdyn_projectteam

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteam.msdyn_applicantcount                                                        |
| msdyn_projectteam.msdyn_applicantsavailable                                                   |
| msdyn_projectteam.msdyn_assignedhours                                                         |
| msdyn_projectteam.msdyn_description                                                           |
| msdyn_projectteam.msdyn_from                                                                  |
| msdyn_projectteam.msdyn_hoursrequested                                                        |
| msdyn_projectteam.msdyn_membershipstatus                                                      |
| msdyn_projectteam.msdyn_number                                                                |
| msdyn_projectteam.msdyn_to                                                                    |

### <a name="msdyn_projectteammembersignup"></a>msdyn_projectteammembersignup

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteammembersignup.msdyn_bookableresource                                          |
| msdyn_projectteammembersignup.msdyn_membershipstatus                                          |
| msdyn_projectteammembersignup.msdyn_name                                                      |
| msdyn_projectteammembersignup.msdyn_projectteammembersignupid                                 |
| msdyn_projectteammembersignup.msdyn_teammembership                                            |

### <a name="msdyn_projecttransactioncategory"></a>msdyn_projecttransactioncategory

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttransactioncategory.msdyn_billingtype                                            |
| msdyn_projecttransactioncategory.msdyn_name                                                   |
| msdyn_projecttransactioncategory.msdyn_project                                                |
| msdyn_projecttransactioncategory.msdyn_projecttransactioncategoryid                           |
| msdyn_projecttransactioncategory.msdyn_transactioncategory                                    |

### <a name="msdyn_quotelineinvoiceschedule"></a>msdyn_quotelineinvoiceschedule

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_quotelineinvoiceschedule.msdyn_quoteline                                                |
| msdyn_quotelineresourcecategory.msdyn_quoteline                                               |
| msdyn_quotelinescheduleofvalue.msdyn_quoteline                                                |
| msdyn_quotelinetransaction.msdyn_quoteline                                                    |
| msdyn_quotelinetransactioncategory.msdyn_quoteline                                            |
| msdyn_quotelinetransactionclassification.msdyn_quoteline                                      |

### <a name="msdyn_resourceassignment"></a>msdyn_resourceassignment

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_resourceassignment.msdyn_hours                                                          |
| msdyn_resourceassignment.msdyn_fromdate                                                       |
| msdyn_resourceassignment.msdyn_msprojectclientid                                              |
| msdyn_resourceassignment.msdyn_todate                                                         |
| msdyn_resourceassignmentdetail.msdyn_duration                                                 |
| msdyn_resourceassignmentdetail.msdyn_from                                                     |
| msdyn_resourceassignmentdetail.msdyn_name                                                     |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentdetailid                               |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentid                                     |

### <a name="salesorderdetail"></a>salesorderdetail

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| salesorderdetail.msdyn_quoteline                                                              |

