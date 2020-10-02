---
title: Definir políticas de despesas
description: Pode definir as políticas de despesas que os seus trabalhadores devem seguir ao introduzir e submeter relatórios de despesas e requisições de viagem.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fbab7fd94fa429876216ee82b716da8d847fb01a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896655"
---
# <a name="define-expense-policies"></a>Definir políticas de despesas

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Pode definir as políticas que os seus trabalhadores devem seguir ao introduzir e submeter relatórios de despesas e requisições de viagem.         
Implementar políticas de despesas pode ajudá-lo a gerir as despesas de forma eficaz.         

Por exemplo, pode definir uma política para as despesas com hotéis em Nova Iorque, que diz que a despesa por noite não pode exceder USD 250.       
Se um trabalhador apresentar um relatório de despesas ou requisição de viagem quando a taxa de quarto exceder esse valor, o sistema notificará         
trabalhador que o montante da política para a despesa foi excedido. Pode configurar a mensagem que o trabalhador irá receber quando        
definir a política.      
        
Pode definir três tipos de políticas:         
        
- **Aviso**: Permite ao trabalhador apresentar um relatório de despesas ou requisição de viagem, mas a despesa será marcada para todos os aprovadores e         
  para relatórios posteriores.        

- **Erro**: Exige que o trabalhador reveja as despesas para cumprir a política antes de apresentar o relatório de despesas ou a requisição de viagem.        
 
 - **Justificação**: Exige que o trabalhador ou um gestor insira uma justificação por exceder o valor da apólice antes de apresentar o relatório de despesas ou a requisição de viagem.        

## <a name="policy-tips"></a>Sugestões de Política
Aqui ficam algumas sugestões que podem ajudar na criação de novas políticas para a gestão de despesas: 

- As políticas são válidas a partir da data, o que significa que uma apólice não produzirá efeito se for criada com uma data após a data em que a despesa ocorreu. Por exemplo, cria hoje uma nova política para impor uma despesa máxima de refeição de 50 euros. As despesas existentes registadas a partir de ontem não serão verificadas em relação a esta política.
- Ao criar uma política para uma categoria de despesas que possa ser discriminada, considere adicionar uma condição para o tipo de linha de despesas. Algumas políticas, como a necessidade de um recibo, podem não fazer sentido para linhas discriminadas. Nesta situação, a política só é aplicada à linha de cabeçalho ou a uma linha não discriminada. 
- As políticas de gestão de despesas são avaliadas em relação à entidade de origem por defeito. Para cenários entre empresas, pode definir a política a avaliar em relaçãoà entidade de destino (entidade tomadora de empréstimos) em vez disso. Para executar as políticas contra a entidade de destino, ligue a funcionalidade **Avaliar política de despesas em relação à entidade legal tomadora de empréstimos** na área de trabalho **Recurso de Gestão**.

## <a name="when-to-evaluate-policies"></a>Quando avaliar políticas

Nos parâmetros de gestão de despesas, pode selecionar para avaliar as políticas de gestão de despesas quando uma linha é guardada ou quando um relatório de despesas é submetido. Se optar por avaliar quando uma linha é guardada, os utilizadores terão visibilidade mais cedo sobre o que precisam de fazer para completar o seu relatório de despesas de uma só vez. Caso contrário, pode atrasar a avaliação da política e economizar tempo, validando no final, durante a submissão ao fluxo de trabalho.
