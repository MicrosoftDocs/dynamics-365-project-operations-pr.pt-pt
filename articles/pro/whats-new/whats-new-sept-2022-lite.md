---
title: Novidades de setembro de 2022 - Implementação do Project Operations Lite
description: Este artigo fornece informações sobre as atualizações de qualidade que estão disponíveis na versão de setembro de 2022 da implementação lite do Microsoft Dynamics 365 Project Operations.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 2cce7ae25f05258e8bf0bab9430324bc9b30e329
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621294"
---
# <a name="whats-new-september-2022---project-operations-lite-deployment"></a>Novidades de setembro de 2022 - Implementação do Project Operations Lite

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

Este artigo aplica-se aos seguintes componentes e versões do Microsoft Dynamics 365 Project Operations:

- Project Operations num ambiente Dataverse, versão 4.46.0.60

## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versão

| Área de funcionalidades | Nome da funcionalidade | Mais informações |
| --- | --- | --- |
| Gestão de oportunidades | **Revisão e Ativação de Propostas**<br>O Project Operations suporta integralmente o processo de vendas. As propostas do projeto podem ser ativadas para representar um estado onde a proposta é só de leitura e está a ser revista. As propostas ativadas podem ser revistas para criar novas propostas que tenham um número de revisão incrementado. Propostas de projeto ativada ou revisões de propostas pode ser fechada como ganha ou perdida. | [Ativar e rever uma proposta de projeto](/dynamics365/project-operations/sales/activation-and-revision) |
| Faturação e Preços | **Predefinição do preço agnóstico de fuso horário**<br>O Project Operations introduziu o conceito de uma data agnóstica de fuso horário em todos os valores reais do projeto. Um novo campo, **Data da transação**, está agora disponível em linhas do diário e valores reais, e será utilizado para armazenar a data em que a transação ocorreu, mas sem converter essa data para a Hora Universal Coordenada. Esta data será utilizada para processos a jusante, como a predefinição de preços e a criação de faturas. | <p>[Determinar taxas de custo para estimativas e valores reais com base no projeto](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Determinar preços de venda para estimativas e valores reais baseados no projeto](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Faturação e Preços | **O preço com data em vigor é substituído no Project Operations**<br>As Definições manuais de preço com data efetiva oferecem uma forma de definir manualemnte ou alterar preços específicos na lista de preços. | [Definições manuais de preço com data efetiva](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Tempo e Despesa | **Aprovador Global**<br>Esta caraterística permite o fornecedor independente de software (ISV) e a aprovação centralizada, independentemente do estado do projeto ou do membro da sua organização no projeto. | [Segurança e aprovações](/dynamics365/project-operations/approvals/approvals-security) |

## <a name="quality-updates"></a>Atualizações de qualidade

| Área de funcionalidades | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Faturação e Preços | 2754422 | As estimativas de Materiais e Despesas não são fornecidas para o Dynamics 365 Finance quando os projetos são copiados no Dataverse. |
| Tempo e Despesa | 2787409 | Um aprovador não válido pode aprovar uma entrada de tempo que não pertença ao projeto. |
| Gestão de oportunidades | 2788907 | Mensagem de erro atualizada sobre a validação de exclusividade para linhas de encomenda que incluem sinalizadores. |
| Tempo e Despesa | 2842253 | Processamento de exceção nula para aprovação de tempo. |
| Faturação e Preços | 2844181 | A falha ao obter o ID de correlação bloqueia a criação de faturas. |
| Faturação e Preços | 2876628 | QLD, CLD – Estimar a resolução da lista de preços deverá utilizar campos de intervalo de datas legados da lista de preços. |
| Subcontratos | 2893222 | Se não for especificada nenhuma função para um item de subcontrato, deverá ser possível selecioná-lo num membro da equipa para qualquer função. |
