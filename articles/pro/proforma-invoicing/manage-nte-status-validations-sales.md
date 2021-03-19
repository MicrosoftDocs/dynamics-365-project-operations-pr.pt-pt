---
title: Gerir estado a não exceder e validações
description: Este tópico fornece informações sobre as verificações de limite a não exceder realizadas no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c5c491d4014ffc2568d7df72b542761ec9b1a90b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274044"
---
# <a name="manage-not-to-exceed-status-and-validations"></a>Gerir estado a não exceder e validações 

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

## <a name="not-to-exceed-on-approvals"></a>A não exceder em aprovações

Quando uma entrada de tempo ou de despesa é submetida, é criado um registo de aprovação. Se a aprovação for faturável e mapear para um item de contrato de tempo e material, o sistema completa uma verificação de validação a não exceder aos seguintes níveis:

  - Verificação contra o limite configurado para o cliente no item de contrato do projeto
  - Verificação contra o limite configurado no item de contrato
  - Verificação contra o limite configurado para o cliente
  - Verificação contra o limite configurado no contrato

As verificações a cada nível implicam assegurar que o montante das vendas nesta aprovação não violará o limite a não exceder a esse nível após a contabilização do montante do registo de tarefas pendentes de faturação já registadas, bem como do montante faturado até à data a esse nível.

Se a verificação passar, a aprovação recebe um estado de validação de **Sucesso**.

Se a verificação falhar, a aprovação recebe um estado de validação de **Falhada**. O detalhe de validação a não exceder informará o utilizador a que nível a validação falhou.

Quando o tempo ou entrada de despesas apresentados for considerado não faturável, o estado de validação a não exceder é definido como **Não Aplicável** com o detalhe de validação igual ao **Não aplicável**.

## <a name="not-to-exceed-on-unbilled-sales-actuals"></a>Valores reais a não exceder em vendas não faturadas

Quando uma entrada de tempo ou de despesa é aprovada, os registos de custos e de valores reais de vendas não faturados são criados. Se o valor real de vendas não faturado for faturável e mapear para um item de contrato de tempo e material, a aplicação realiza uma verificação de validação a não exceder aos seguintes níveis:

  - Verificação contra o limite configurado para o cliente do item de contrato do projeto
  - Verificação contra o limite configurado no item de contrato
  - Verificação contra o limite configurado para o cliente
  - Verificação contra o limite configurado no contrato

As verificações a cada nível asseguram que o montante das vendas neste valor real não violará o limite a não exceder a esse nível após a contabilização do montante do registo de tarefas pendentes de faturação já registadas, bem como do montante faturado até à data a esse nível.

Se a verificação passar, o valor real de vendas não faturados recebem um estado a não exceder de **Comprometido**.

Se a verificação falhar, o valor real de vendas não faturados recebem um estado a não exceder de **Falhado**. O detalhe de validação informa o utilizador a que nível a validação falhou.

Quando o valor real de vendas não faturadas for considerado não faturável ou grátis, se não houver uma configuração de limite a não exceder a nenhum dos quatro níveis, ou se o valor real a ser criado for o Custo, Sinal, Unidade de Atribuição de Recursos ou Vendas entre organizações, os campos **Estado A Não Exceder** e **Validação a Não Exceder** têm de ser definidos como **Não Aplicável**.

## <a name="reset-the-not-to-exceed-status"></a>Redefinir o estado a não exceder

Pode efetuar uma reposição em massa do estado a não exceder. Isto permite que os gestores de projetos ajustem a validação a não exceder para priorizar a faturação de um determinado corpo de trabalho, tempo ou despesas sobre outros que já estão comprometidos a partir do valor disponível a não exceder.

Após o estado a não exceder ser reposto em valores reais de vendas não faturados, o montante comprometido é reduzido. O gestor do Projeto pode selecionar outro corpo de trabalho, tempo ou despesas que anteriormente falharam na validação a não exceder e reavaliá-los. Com a redução do montante comprometido, estes valores reais passarão agora a validação. Isto ajuda o gestor do Projeto a exercer maior influência e controlo sobre as transações faturáveis para esse período.

Para redefinir o estado a não exceder, selecione um ou mais valores reais a partir da vista **Registo de Tarefas Pendentes de Faturação de Tempo e Material** ou **Valores Reais** e, em seguida, selecione **Repor Estado a Não Exceder**.

O estado a não exceder é reposto para **Não Avaliado** em todos os dados relevantes selecionados. Os valores reais que têm a sua reposição do estado a não exceder são valores reais de vendas não faturados que ainda não estão faturados, não numa fatura de rascunho, e são marcados como faturáveis. Quaisquer outros valores reais selecionados são ignorados.

## <a name="reevaluate-not-to-exceed-status"></a>Reavaliar estado a não exceder

Pode efetuar uma reavaliação em massa do estado a não exceder. A reavaliação do estado a não exceder é útil quando:

  - Houve uma renegociação de limites a não exceder com o cliente e os valores reais terão de ser reavaliados.
  - O gestor do Projeto quer afinar a faturação de registo de tarefas pendentes de vendas não faturadas, priorizando um corpo de trabalho em relação a outro.

Para reavaliar o estado a não exceder, selecione um ou mais valores reais a partir da vista **Registo de Tarefas Pendentes de Faturação de Tempo e Material** ou **Valores Reais** e selecione **Reavaliar Estado a Não Exceder**.

Todos os valores reais selecionados relevantes com um limite a não exceder será avaliado em comparação com a configuração do limite a não exceder. Os valores reais são relevantes para reavaliação do estado a não exceder são valores reais de vendas que não foram faturados, não numa fatura de rascunho, e são marcados como faturáveis. Quaisquer outros valores reais selecionados.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]