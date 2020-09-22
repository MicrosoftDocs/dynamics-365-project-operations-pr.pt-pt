---
title: Alterações de entidade, controlo e interface de utilizador (Project Service Automation 3.x)
description: Este tópico descreve alterações de soluções para o Microsoft Dynamics Project Service Automation 3.x.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/15/2019
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 9f8828c6-541c-4945-8c99-5785118e191d
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
ms.openlocfilehash: 56aa0bb8272b886bcd15dadd0f74fff3bc43e26b
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754565"
---
# <a name="entity-control-and-user-interface-changes-project-service-automation-3x"></a>Alterações de entidade, controlo e interface de utilizador (Project Service Automation 3.x)
Com o lançamento do Microsoft Dynamics Project Service Automation (PSA) 3.x, muitas alterações foram efetuadas nas entidades, controlos, vistas e interfaces de utilizador. Este tópico fornece informações sobre estas alterações importantes.

## <a name="parent-child-relationships-for-sales-document-sales-document-line-sales-document-line-detail-entities"></a>Relações principal-subordinado para documento de vendas, linha de documento de vendas, entidades de detalhe de linha de documento de vendas
Nas versões do Dynamics 365 Project Service Automation (PSA) lançadas antes da versão 3.0, algumas das relações entre documentos de vendas, linhas de documentos de vendas e entidades de detalhe de linha de documento de vendas foram implementadas por meio de campos de cadeia que continham uma representação em cadeia do GUID da entidade relacionada. Isso ocorreu devido às limitações da plataforma que exigiam um código personalizado significativo nos lados do servidor e do cliente da solução para fazer com que essas relações funcionassem de maneira semelhante às relações de entidade típicas do Dynamics CRM e para fazer com que os campos de cadeia agissem como campos de pesquisa.

O PSA 3.0 foi atualizado para alavancar as novas relações de entidade entre o documento de vendas e as entidades da linha de documento de vendas.

Como os campos de pesquisa agora podem ser utilizados para indicar referências a entidades, os campos que mantinham o valor da cadeia do GUID da entidade relacionada nas versões anteriores já não são necessários e, portanto, foram preteridos. O código personalizado do lado do cliente e do servidor que lida com as relações definidas pelos campos de cadeia legados também foi preterido.

### <a name="entity-schema-changes"></a>Alterações no esquema da entidade
A tabela a seguir fornece uma lista individual dos campos de cadeia preteridos e dos novos campos de pesquisa para as entidades. 

 Entidade |   Campo preterido (cadeia) | Novo campo (pesquisa)
--- | --- | ---
invoicedetail (Linha de Fatura) |  msdyn_contractline |    msdyn_contractlineid
msdyn_actual (valor real) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_contractlineinvoiceschedule (Agenda de Faturação de Item de Contrato do Projeto) |    msdyn_contractline |    msdyn_contractlineid
msdyn_contractlinescheduleofvalue (Marco do Item de Contrato do Projeto) |   msdyn_contractline |    msdyn_contractlineid
msdyn_fact (facto) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_invoicelinetransaction (Detalhe de Linha de Fatura) | msdyn_invoiceline <br> msdyn_salescontractline | msdyn_invoicelineid <br> msdyn_salescontractlineid
msdyn_journalline (Linha do Diário) |  msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlineresourcecategory (Categoria de Recurso de Item de Contrato do Projeto) | msdyn_salescontractline |   msdyn_contractlineid
msdyn_orderlinetransaction (Detalhe de Item de Contrato do Projeto) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlinetransactioncategory (Categoria de Transação de Item de Contrato do Projeto) |   msdyn_contractline |    msdyn_contractlineid
msdyn_orderlinetransactionclassification (Classificação de Transação de Item de Contrato do Projeto) |   msdyn_contractline |    msdyn_contractlineid
msdyn_quotelineinvoiceschedule (Agenda de Faturação de Linha de Proposta) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelineresourcecategory (Categoria de Recurso de Linha de Proposta) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinescheduleofvalue (Marco da Linha de Proposta) | msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransaction (Detalhe de Linha de Proposta) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactioncategory (Categoria de Transação de Linha de Proposta) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactionclassification (Classificação de Transação de Linha de Proposta) |  msdyn_quoteline |   msdyn_quotelineid
SalesOrderDetail (Linha de Encomenda) | msdyn_quotelineid | msdyn_quoteline 

### <a name="deprecated-custom-views-and-controls"></a>Vistas e controlos personalizados preteridos
As seguintes vistas e controlos personalizados e os respetivos artefactos relacionados foram preteridos.

- Vista de exigibilidade.
- Controlos de grelha personalizados para mostrar os detalhes de linha de proposta na página **Informações do Projeto** referente à linha de proposta.
- Controlos de grelha personalizados para mostrar os detalhes de item de contrato do projeto na página **Informações do Projeto** referente à linha da ordem de venda.

> [!NOTE]
> Para obter a lista completa de recursos preteridos, consulte [Recursos Web preteridos no Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md)

## <a name="unified-client-interface-app-module"></a>Módulo da Aplicação da Interface Unificada do Cliente
Com a introdução dos Módulos de Aplicação da Interface Unificada do Cliente (UCI), as entradas do mapa do site do PSA foram removidas do sistema.  
A funcionalidade relacionada com a mudança de formulários para Oportunidade, Proposta, Encomenda e Fatura foi preterida, pois já não é necessária porque o Módulo da Aplicação UCI inclui apenas as versões do PSA dos formulários.  

Os seguintes recursos Web foram preteridos:

- msdyn_\SalesDocument\SalesDocumentFormLoader.js
- msdyn_\SalesDocument\PSSalesDocumentCustomFormIds.js

> [!NOTE]
> Para obter a lista completa de recursos preteridos, consulte [Recursos Web preteridos no Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md).


