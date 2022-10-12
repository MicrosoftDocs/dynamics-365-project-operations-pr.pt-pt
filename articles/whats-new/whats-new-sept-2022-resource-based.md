---
title: Novidades de setembro de 2022 - Project Operations para cenários baseados em recursos/itens não existentes em stock
description: Este artigo fornece informação sobre as atualizações de qualidade que estão disponíveis na versão de setembro de 2022 do Microsoft Dynamics 365 Project Operations para cenários baseados em recursos/sem stock.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: ef8b4dd98d64dac1e2420f8e6a104258f126f112
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621279"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades de setembro de 2022 - Project Operations para cenários baseados em recursos/itens não existentes em stock

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Este artigo aplica-se aos seguintes componentes e versões do Microsoft Dynamics 365 Project Operations:

- Project Operations num ambiente Dataverse, versão 4.46.0.60
- Gestão de projetos e contabilidade num ambiente do Dynamics 365 Finance versão 10.0.29

## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versão

| Área de funcionalidades | Nome da funcionalidade | Mais informações |
| --- | --- | --- |
| Gestão de oportunidades | **Revisão e Ativação de Propostas**<br>O Project Operations suporta integralmente o processo de vendas. As propostas do projeto podem ser ativadas para representar um estado onde a proposta é só de leitura e está a ser revista. As propostas ativadas podem ser revistas para criar novas propostas que tenham um número de revisão incrementado. Propostas de projeto ativada ou revisões de propostas pode ser fechada como ganha ou perdida. | [Ativar e rever uma proposta de projeto](/dynamics365/project-operations/sales/activation-and-revision) |
| Faturação e Preços | **Predefinição do preço agnóstico de fuso horário**<br>O Project Operations introduziu o conceito de uma data agnóstica de fuso horário em todos os valores reais do projeto. Um novo campo, **Data da transação**, está agora disponível em linhas do diário e valores reais, e será utilizado para armazenar a data em que a transação ocorreu, mas sem converter essa data para a Hora Universal Coordenada. Esta data será utilizada para processos a jusante, como a predefinição de preços e a criação de faturas. | <p>[Determinar taxas de custo para estimativas e valores reais com base no projeto](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Determinar preços de venda para estimativas e valores reais baseados no projeto](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Faturação e Preços | **O preço com data em vigor é substituído no Project Operations**<br>As Definições manuais de preço com data efetiva oferecem uma forma de definir manualemnte ou alterar preços específicos na lista de preços. | [Definições manuais de preço com data efetiva](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Subcontratos | **Reconciliação de faturas de subcontratação e de fornecedor**<br>Esta caraterística permite que os clientes criem subcontratos para comprarem tempo de recurso, categorias de despesas e materiais utilizados para trabalho no projeto. Também permite que os clientes gravem, nas aplicações de finanças e operações, faturas de fornecedor que estarão disponíveis para os gestores de projeto no Dataverse para verificação. | <p>[Gestão de subcontratos](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Criar faturas de fornecedor](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Tempo e Despesa | **Aprovador Global**<br>Esta caraterística permite o fornecedor independente de software (ISV) e a aprovação centralizada, independentemente do estado do projeto ou do membro da sua organização no projeto. | [Segurança e aprovações](/dynamics365/project-operations/approvals/approvals-security) |
| Gestão de despesas | **Capacidade de publicar o passivo de despesas na moeda de fornecedor**<br>Esta caraterística permite que os relatórios sejam publicados numa moeda do fornecedor para o método de pagamento em numerário. | [Capacidade de publicar o passivo de despesas na moeda de fornecedor](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Aprovisionamento do Projeto | **Pagamentos de fornecedor paga quando pago**<br>Esta caraterística permite que a caraterística Pagar quando pago (PWP) seja utilizada em ambientes sem stock do Project Operations. Permite que os pagamentos ao fornecedor sejam bloqueados/retidos, com base em termos de retenção, até que o pagamento seja recebido pelo cliente. | [Pagamentos de fornecedor paga quando pago](/dynamics365/project-operations/procurement/pay-when-paid) |
| Aprovisionamento do Projeto | **Requisições de compra do projeto**<br>Esta caraterísticas permite que os utilizadores criem notas de encomenda relacionadas com o projeto em entidades legais em que o Project Operations na integração do Dynamics 365 Customer Engagement está ativado. As notas de encomendas do projeto podem ser utilizadas para gravar aprovisionamento de material sem stock para o projeto pela persona do departamento de Aprovisionamento. As notas de encomenda não serão sincronizadas com o Dataverse. No entanto, pode utilizar uma entidade virtual para emergir as linhas da nota de encomenda do Projeto no Dataverse para obter informações do gestor do projeto. O custo da fatura do fornecedor relacionado com o projeto está integrado com a entidade de Valores Reais do Projeto no Dataverse. O custo do projeto é registado no subrazão do Projeto utilizando o diário de Integração do Project Operations. | |

## <a name="project-operations-dual-write-maps-updates"></a>Atualizações de mapas de escrita dupla do Project Operations

A tabela seguinte mostra os mapas de escrita dupla que foram modificados ou adicionados na versão de setembro de 2022 do Project Operations.

| Mapa da entidade | Versão atualizada | Comentários |
| -------------- | ------------------- | ------------|
| Valores reais de integração com o Project Operations (msdyn_actuals) | 1.0.0.15 | Este mapa suporta o processamento de valores reais de subcontrato com o Project Operations para cenários baseados em recursos. |
| Entidade de exportação de faturas de projeto de integração de projetos do Project Operations (msdyn_projectvendorinvoices) | 1.0.0.2 | Este mapa suporta o processamento de valores reais de subcontrato com o Project Operations para cenários baseados em recursos. |
| Entidade de exportação de linhas de faturas de projeto de integração de projetos do Project Operations (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Este mapa suporta o processamento de valores reais de subcontrato com o Project Operations para cenários baseados em recursos. |

Execute sempre a versão mais recente do mapa no seu ambiente e ative todos os mapas de tabelas relacionados à medida que atualiza a sua solução do Project Operations Dataverse e a versão da solução Finance. Algumas funcionalidades e capacidades podem não funcionar corretamente se a versão mais recente do mapa não estiver ativada. Pode ver a versão ativa do mapa na coluna **Versão** na página **Escrita Dupla**. Para ativar uma nova versão do mapa, selecione **Versões do mapa de tabela** , selecione a versão mais recente e, em seguida, guarde a versão selecionada. Se tiver personalizado um mapa de tabela de origem, volte a aplicar as alterações. Para mais informações, consulte [Gestão do ciclo de vida da aplicação](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se ocorrer um problema quando iniciar o mapa, siga as instruções na secção [Problema de colunas de tabela em falta em mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) do guia de resolução de problemas do serviço Escrita dupla.

## <a name="quality-updates"></a>Atualizações de qualidade

### <a name="project-operations-on-dataverse"></a>Project Operations no Dataverse

| Área de funcionalidades | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Faturação e Preços | 2754422 | As estimativas de Materiais e Despesas não são fornecidas para Finanças quando os projetos são copiados no Dataverse. |
| Tempo e Despesa | 2787409 | Um aprovador não válido pode aprovar uma entrada de tempo que não pertença ao projeto. |
| Gestão de oportunidades | 2788907 | Mensagem de erro atualizada sobre a validação de exclusividade para linhas de encomenda que incluem sinalizadores. |
| Tempo e Despesa | 2842253 | Processamento de exceção nula para aprovação de tempo. |
| Faturação e Preços | 2844181 | A falha ao obter o ID de correlação bloqueia a criação de faturas. |
| Faturação e Preços | 2876628 | QLD, CLD – Estimar a resolução da lista de preços deverá utilizar campos de intervalo de datas legados da lista de preços. |
| Subcontratos | 2893222 | Se não for especificada nenhuma função para um item de subcontrato, deverá ser possível selecioná-lo num membro da equipa para qualquer função. |

### <a name="project-management-and-accounting-in-finance"></a>Gestão de projetos e contabilística em Finanças

Para obter informações sobre as correções de erros incluídas nesta atualização, inicie sessão no Microsoft Dynamics Lifecycle Services e consulte o [Artigo BDC](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Funcionalidades ligadas por predefinição na próxima versão

A tabela que se segue lista as funcionalidades que estão ativadas por predefinição na versão 10.0.30. A maioria das funcionalidades que foram ativadas automaticamente podem ser desativadas na [Gestão de funcionalidades](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). No futuro, algumas funcionalidades que foram automaticamente ativadas podem ser removidas da Gestão de funcionalidades e tornar-se obrigatórias. Esta alteração assegura que os clientes estão a utilizar a funcionalidade atual, para que os melhoramentos possam basear-se na funcionalidade atual à medida que são adicionados. As funcionalidades nunca serão ativadas automaticamente em menos de um ano, a menos que sejam determinadas como essenciais.

| Nome da funcionalidade | Data de ativação | Funcionalidade adicionada | Estado de funcionalidade | Módulo |
| --- | --- | --- |--- |--- |
| Ativar a operação assíncrona quando o utilizador necessitar de alternar entre operações de sincronização e assíncronas | 21 de outubro de 2022 | 9 de abril de 2021 | Ativada por predefinição | Gestão de despesas |
| Avaliação da política de despesas para os recibos requeridos | 21 de outubro de 2022 | 20 de dezembro de 2021 | Ativada por predefinição | Gestão de despesas |
| Vista de lista de relatórios de despesas criados por colaboradores delegados | 21 de outubro de 2022 | 19 de fevereiro de 2020 | Ativada por predefinição | Gestão de despesas |
| Cálculo dos totais de quilometragens por ano fiscal | 21 de outubro de 2022 | 10 de maio de 2022 | Ativada por predefinição | Gestão de despesas |
