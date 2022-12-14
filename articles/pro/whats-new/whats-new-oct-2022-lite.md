---
title: Novidades de outubro de 2022 - Implementação do Project Operations Lite
description: Este artigo fornece informações sobre as atualizações de qualidade que estão disponíveis na versão de outubro de 2022 da implementação lite do Microsoft Dynamics 365 Project Operations.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: b6975e1f8645721fc03239b355b117eb664785f0
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806645"
---
# <a name="whats-new-october-2022---project-operations-lite-deployment"></a>Novidades de outubro de 2022 - Implementação do Project Operations Lite

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

Este artigo aplica-se aos seguintes componentes e versões do Microsoft Dynamics 365 Project Operations:

- Project Operations num ambiente Dataverse, versão 4.57.0.176

## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versão

| Área de funcionalidades | Nome da funcionalidade | Mais informações |
| --- | --- | --- |
| Planeamento e Monitorização de Projetos | **Agendamento Externo do Project Operations**<br>O modo de agendamento externo permite aos clientes criar, atualizar e eliminar entidades de forma nativa relacionadas com as estruturas hierárquicas de trabalho (WBS) utilizando APIs do Dataverse nativas, sem os limites atuais impostos pelo Project for the Web. | [Agendamento Externo](/dynamics365/project-operations/project-management/external-scheduling) |
| Implementação e Configuração | <p>**Permitir que os clientes escolham o tipo de implementação**<br>As atualizações condicionados por produto (PDUs) do Project Operations são utilizadas para instalar automaticamente uma solução de Escrita dupla do Project Operations quando as soluções de Escrita dupla central e de orquestração estão instaladas no ambiente.</p><p>Esta caraterística introduz um novo parâmetro **Comportamento da atualização de versão da solução** nos parâmetros do Projeto. Quando este parâmetro estiver definido como **Só Lite**, as PDUs deixarão de instalar automaticamente uma solução de Escrita dupla do Project Operations, mesmo que as soluções de Escrita dupla central e de orquestração estejam instaladas no ambiente. Este comportamento irá beneficiar clientes que pretendam utilizar soluções de Escrita dupla para integrar ordens de venda em aplicações de finanças e operações, mas que pretendem utilizar o Project Operations num modo Lite (ou seja, sem integração com aplicações de finanças e operações).</p> | |

## <a name="quality-updates"></a>Atualizações de qualidade

| Área de funcionalidades | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Faturação e Preços | 2316317 | O sistema permite a criação de faturas sem transações faturáveis. |
| Faturação e Preços | 2737300 | Valide a disponibilidade do campo Cliente antes de o formulário ser acedido. |
| Faturação e Preços | 2744948 | Adicione um verificação nula para o método Faturação. |
| Faturação e Preços | 2763515 | Identificador do erro de referência nula quando o contrato de vendas da fatura está em falta. |
| Faturação e Preços | 2844301 | A criação de faturas em lote falha devido a um erro. |
| Faturação e Preços | 2845869 | Armazenamento incorreto do Serviço da Organização. |
| Faturação e Preços | 2853729 | Os detalhes da Função e do Preço são atualizados quando o tipo Faturação é modificado. |
| Faturação e Preços | 2940350 | Quando o preço dos valores reais é definido, apenas as listas de preços devem ser introduzidas automaticamente. |
| Implementação e Configuração | 3001206 | A entidade msdyn\_replaylogheader está a impedir atualizações de versão de Organizações de Clientes. |
| Gestão de oportunidades | 2755582 | Identificador de exceções de referência nula no Assistente da Regra de Divisão de Faturação. |
| Gestão de oportunidades | 2761477 | Quando a faturação dividida, a eliminação de um marco (cabeçalho) deixa marcos órfãos. |
| Gestão de oportunidades | 2767595 | Quando um registo de utilização de materiais é aberto no formulário principal, o recurso Reservável para o registo é alterado para o utilizador atualmente com sessão iniciada. |
| Planeamento e Monitorização de Projetos | 2790384 | O tempo limite do OperationSet Pendente é demasiado curto. |
| Gestão de Recursos | 2751560 | Unidades de Organização Preferenciais Inconsistentes em Requisito de Recursos. |
| Subcontratos | 2907231 | A fase do processo de faturas do fornecedor não pode avançar. |
| Tempo e Despesa | 2867363 | Os registos não saem da vista Ausências/Férias para Aprovação quando são colocadas em fila para aprovação. |
| Tempo e Despesa | 2894405 | TESA: o diretório POC não utilizado está a causar problemas de conformidade. |
