---
title: Configurar políticas de despesas
description: Pode configurar as políticas de despesas que os seus trabalhadores devem seguir ao introduzir e submeter relatórios de despesas e requisições de viagem no Microsoft Dynamics 365 Finance.
author: suvaidya
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa4f628a918e6e099a723ed05994f63d6ad847f5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005760"
---
# <a name="set-up-expense-policies"></a>Configurar políticas de despesas

Pode definir as políticas que os seus trabalhadores devem seguir ao introduzir e submeter relatórios de despesas e requisições de viagem.         
Implementar políticas de despesas pode ajudá-lo a gerir as despesas de forma eficaz.         

Por exemplo, pode definir uma política para as despesas com hotéis em Nova Iorque, que diz que a despesa por noite não pode exceder USD 250.       
Se um trabalhador apresentar um relatório de despesas ou uma requisição de viagem em que a taxa de quarto exceder esse valor, o sistema notificará        
trabalhador que o montante da política para a despesa foi excedido. Pode configurar a mensagem que o trabalhador irá receber quando        
definir a política.      
        
Pode definir três tipos de políticas:         
        
- Aviso – Permite ao trabalhador apresentar um relatório de despesas ou requisição de viagem, mas a despesa será marcada para todos os aprovadores e        
  para relatórios posteriores.        

- Erro – Exige que o trabalhador reveja as despesas para cumprir a política antes de apresentar o relatório de despesas ou a requisição de viagem.       
 
 - Justificação – Exige que o trabalhador ou um gestor insira uma justificação por exceder o valor da apólice antes de apresentar o relatório de despesas ou a requisição de viagem.        

## <a name="policy-tips"></a>Sugestões de Política
Aqui ficam algumas sugestões que podem ajudar na criação de novas políticas para a gestão de despesas. 
* As políticas são válidas a partir da data e não produzirá efeito se a política for criada com uma data após a data em que a despesa ocorreu. Por exemplo, se estiver a criar uma nova política hoje para impor uma despesa de refeição máxima de 50 $, então quaisquer despesas existentes inscritas a partir de ontem não serão verificadas contra esta política.
* Ao criar uma política para uma categoria de despesas que possa ser discriminada, considere adicionar uma condição para o tipo de linha de despesas. Algumas políticas, tais como a necessidade de um recibo, podem não fazer sentido para linhas discriminadas e só devem ser aplicadas à linha de cabeçalho ou a uma linha não discriminada. 
* As políticas de gestão de despesas são avaliadas em relação à entidade de origem por defeito. Para cenários entre empresas, pode definir a política a avaliar em relaçãoà entidade de destino (entidade tomadora de empréstimos) em vez disso. Para executar as políticas contra a entidade de destino, ligue a funcionalidade "Avaliar política de despesas em relação à entidade legal" tomadora de empréstimos na área de trabalho **Gestão de Funcionalidades**.

## <a name="when-to-evaluate-policies"></a>Quando avaliar políticas

Nos parâmetros de gestão de despesas, existe uma opção para avaliar as políticas de gestão de despesas quando uma linha é guardada ou quando um relatório de despesas é submetido. Se optar por avaliar quando uma linha é guardada, isto garante que os utilizadores terão visibilidade mais cedo sobre o que precisam de fazer para completar o seu relatório de despesas de uma só vez. Caso contrário, pode atrasar a avaliação da política e economizar tempo se fizer com que a validação ocorra no final, durante a submissão ao fluxo de trabalho.


[!INCLUDE[footer-include](../includes/footer-banner.md)]