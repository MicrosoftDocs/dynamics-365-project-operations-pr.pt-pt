---
title: O que há de novo março de 2022 - Implementação de Project Operations lite
description: Este artigo fornece informações sobre as atualizações de qualidade que estão disponíveis na versão de março de 2022 da implementação do Project Operations Lite.
author: sigitac
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 321d59568bfd33bb00a1500afe514fbecf9a0250
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934242"
---
# <a name="whats-new-march-2022---project-operations-lite-deployment"></a>O que há de novo março de 2022 - Implementação de Project Operations lite

_Aplica-se a: Implementação lite – negócio para faturação pró-forma_

Este artigo aplica-se aos seguintes componentes e versões do Microsoft Dynamics 365 Project Operations:

- Project Operations num ambiente Dataverse, versão 4.30.0.99

## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versão

- Subcontratação: criação de faturas de fornecedor e experiências correspondentes

## <a name="quality-updates"></a>Atualizações de qualidade

| Área de funcionalidades | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Tempo e despesa | 2388011 | Mostrar comentários de rejeição a apresentadores de entrada de tempo durante a aprovação em massa. |
| Planeamento e monitorização de projetos | 2495294 | Os detalhes do projeto não podem ser editáveis na página **Detalhes da tarefa**. |
| Faturação e preços | 2499605 | Os marcos do contrato criados a partir dos marcos das cotações estão incorretamente marcados como só de leitura. |
| Planeamento e monitorização de projetos | 2506050 | O conjunto de operações permanece pendente durante uma hora, caso não haja alterações para guardar. Em seguida, o conjunto será erradamente marcado como **Com falhas**, pelo que deverá ser concluído imediatamente. |
| Faturação e preços | 2507401 | As unidades de contratação predefinida estão incorretamente inseridas em projetos devido à colocação incorreta em cache. |
| Faturação e preços | 2541660 | **Validação de criação de encomendas de venda** em dupla escrita deve ser apenas para encomendas baseadas em projetos. |
| Faturação e preços | 2552745 | O imposto não está dividido entre clientes que tenham configurado regras de faturação divididas. |
| Faturação e preços | 2558859 | Mensagens de erro melhoradas quando as dimensões de preços estão configuradas. |
| Faturação e preços | 2558933 | **Importar de estimativas do projeto** falha quando **msdyn\_project** é adicionado como uma dimensão de preços. |
| Faturação e preços | 2559101 | A eliminação de parâmetros do projeto não está bloqueada e causa problemas. |
| Gestão de oportunidades | 2570390 | O plug-in de escrita dupla força o tipo de conta a ser **Cliente** em cotações, encomendas e oportunidades, mesmo quando esse tipo de conta não está correto. |
| Faturação e preços | 2586097 | Os valores reais de custo dividido faturado não são revertidos quando um projeto é removido de um item de contrato do projeto. |
| Faturação e preços | 2589619 | O imposto sobre material de escrita é propagado para valores reais de vendas não faturadas e para a fatura. |
| Gestão de oportunidades | 2594015 | Não é possível fechar uma cotação se tiver sido ganha para clientes que tenham termos de pagamento **Net60**. |
| Planeamento e monitorização de projetos | 2595841 | No Project for the Web, os utilizadores recebem uma mensagem de erro sobre um **msdyn\_actual** em falta quando criam um novo pedido de recurso. |
| Tempo e Despesa | 2602511 | O campo **Rejeitado por** para entradas de tempo mostra o **Sistema** vez de um utilizador nomeado como o tendo rejeitado. |
| Tempo e Despesa | 2602528 | Um aprovador de projetos pode aprovar tempo em projetos nos quais não se encontra listado como aprovador. |
| Faturação e preços | 2608550 | É possível confirmar uma fatura de correção mesmo que não haja alterações à original. |

## <a name="removed-and-deprecated-features"></a>Funcionalidades removidas e preteridas

O artigo [Funcionalidades removidas ou preteridas no Project Operations](../../whats-new/removed-depreciated-features-project.md) descreve as funcionalidades que foram removidas ou preteridas para o Dynamics 365 Project Operations.

- Uma funcionalidade removida já não está disponível no produto.
- Uma funcionalidade preterida não está no desenvolvimento ativo e poderá ser removida numa atualização futura.

Um anúncio de preterido irá aparecer no artigo [Funcionalidades removidas ou preteridas no Project Operations](../../whats-new/removed-depreciated-features-project.md) 12 meses antes de qualquer funcionalidade ser removida do produto.
