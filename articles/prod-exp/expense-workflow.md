---
title: Fluxo de trabalho de gestão de despesas
description: Este artigo explica como pode usar o sistema de fluxos de trabalho no Microsoft Dynamics 365 Finance, para configurar um processo de revisão para relatórios de despesas na gestão de Despesas.
author: ShylaThompson
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 71efc89d9167ef1ee546c67c123efeb37125cc02
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929734"
---
# <a name="expense-management-workflow"></a>Fluxo de trabalho de gestão de despesas

Pode utilizar o sistema de fluxo de trabalho para configurar um processo de revisão para relatórios de despesas na gestão de Despesas. Pode configurar um fluxo de trabalho que utilize os seguintes critérios para determinar quem aprova relatórios de despesas:

- A hierarquia de relatórios de funcionários e os limites de aprovação predefinidos
- Aprovação a vários níveis que suporta aprovadores provisórios e um aprovador final
- Dimensões financeiras e responsabilidade do projeto
- Atribuição a utilizadores ou grupos de utilizadores específicos

Podem ser criadas aprovações de fluxos de trabalho para relatórios de despesas, requisições de viagens, adiantamentos de dinheiro e recuperação do imposto sobre o valor acrescentado (IVA).

**Exemplo**

O processo que se segue é um exemplo do fluxo de trabalho de gestão de despesas para um relatório de despesas.

1. Um empregado cria e guarda um relatório de despesas.
2. O funcionário submete o relatório de despesas para aprovação. O aprovador é identificado com base nas regras definidas aquando da configuração do fluxo de trabalho.
3. O aprovador recebe uma notificação de que um relatório de despesas está pronto para aprovação. O aprovador revê o relatório de despesas e verifica que estão reunidas as seguintes condições:

    - As despesas não violam nenhuma política de despesas. Se uma despesa violar uma política, o aprovador verifica que o relatório de despesas inclui uma justificação comercial válida.
    - Os recibos eletrónicos são anexados ao relatório de despesas.

4. O aprovador aprova o relatório de despesas.
5. O relatório de despesas é atribuído ao coordenador de Contas a pagar para publicação.
6. Ocorre um dos seguintes passos, dependendo se a publicação automática é configurada:

    - Se o registo automático for configurado, o relatório de despesas é processado para pagamento, e o estado do relatório de despesas é atualizado.
    - Se a publicação automática não estiver configurada, o coordenador das Contas a pagar verifica que todos os recibos originais foram apresentados e que os recibos estão alinhados com as despesas do relatório de despesas. Todos os códigos fiscais inscritos no relatório de despesas devem também ser verificados como corretos.

Após a verificação destes requisitos, o relatório de despesas é publicado.

Após o relatório de despesas ser publicado, o pagamento é autorizado para o relatório de despesas, e o empregado é reembolsado.


[!INCLUDE[footer-include](../includes/footer-banner.md)]