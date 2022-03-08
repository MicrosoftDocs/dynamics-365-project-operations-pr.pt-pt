---
title: Definições de proposta do projeto
description: Este tópico fornece informações sobre as informações e definições aplicáveis às propostas do projeto e que as afetam.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3f11188a47c6f0c7de9fb591fd3be3e22f8f7d842fb6d075c1f43d9baea4d225
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993480"
---
# <a name="header-details-for-project-based-quotes"></a>Detalhes do cabeçalho para propostas baseadas em projetos

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_


Este artigo explica as informações aplicáveis a uma proposta de projeto. Isto inclui as definições que afetam todas as linhas de proposta e as informações sobre a proposta que são resumidas em todos os itens para impulsionar os KPI da proposta de projeto.

A tabela que se segue lista os campos de um resumo de informação numa proposta de projeto que são exclusivos do Dynamics 365 Project Operations ou têm algumas mudanças importantes no comportamento das propostas no Dynamics 365 Sales.

| **Campo** | **Localização** | **Descrição** | **Impacto a jusante** |
| --- | --- | --- | --- |
| Tipo | Separador Resumo (oculto) | Este campo do conjunto de opções tem as seguintes opções:</br>- Baseado em trabalho (disponível apenas quando o Project Operations está instalado)</br>- Baseado em item (disponível apenas quando o Project Operations e o Sales estão instalados)</br>- Baseado em manutenção do serviço (disponível quando o Dynamics 365 Field Service está instalado) | Quando utiliza as aplicações do Project Operations, o valor deste campo é definido automaticamente como **Baseado em trabalho**. Isto classifica a proposta como uma proposta baseada em projetos. Uma proposta deve ser baseada em projetos para ativar todas as extensões e funcionalidades específicas do projeto. |
| Empresa Proprietária | Resumo | A entidade legal que irá contabilizar os custos e receitas decorrentes deste projeto ou projetos associados a esta proposta. Quando uma proposta é criada a partir de uma Oportunidade, este campo é copiado a partir do campo correspondente na Oportunidade. | A empresa proprietária equipara-se ao conceito de entidade legal no módulo **Gestão de projetos e contabilística** do Project Operations. Todos os custos e receitas decorrentes deste projeto serão contabilizados no Razão geral da empresa proprietária. |
| Cliente Potencial | Separador Resumo | Referência ao registo da conta ou empresa do cliente. Um cliente válido a referenciar na proposta de projeto tem de ser configurado como cliente na empresa proprietária da proposta. A empresa proprietária mostra a lista de entidades legais, que são configuradas no módulo **Gestão de projetos e contabilística** do Project Operations. Quando uma proposta é criada a partir de uma oportunidade, este campo é copiado a partir do campo correspondente na oportunidade. | A moeda na proposta de projeto assume por predefinição a moeda do cliente. Isto pode, no entanto, ser alterado antes de a proposta ser guardada. |
| Gestor de Contas | Separador Resumo | O nome do Gestor de conta para este negócio. Quando uma proposta é criada a partir de uma oportunidade, este campo é copiado a partir do campo correspondente na oportunidade. | O Gestor de conta é responsável pela gestão da relação com o cliente até à conclusão deste projeto. Baseado no registo de recurso reservável associado ao Gestor de conta, a unidade de contratação assume por predefinição a proposta de projeto.|
| Unidade de Contratação | Separador Resumo | A unidade organizacional que é responsável pela entrega do projeto ou projetos associados a esta proposta. Quando uma proposta é criada a partir de uma oportunidade, este campo é copiado a partir do campo correspondente na oportunidade. | A unidade de contratação é a divisão da empresa que executará os projetos após o fecho do negócio. Todas as unidades de contratação têm uma moeda, e esta moeda é utilizada para reportar os custos estimados e reais incorridos durante a execução do projeto. |
| Lista de preços de produtos | Separador Resumo | Esta é a lista de preços que é utilizada para os preços predefinidos nas linhas da proposta baseadas em produtos. A lista de opções para este campo mostra uma lista de listas de preços onde a moeda da lista de preços corresponde à moeda na proposta. Quando uma proposta é criada a partir de uma oportunidade, este campo é copiado a partir do campo correspondente na oportunidade. Este campo na oportunidade assume por predefinição o registo da conta, mas pode ser alterado. | Quando uma proposta é ganha, o valor do campo é copiado para o contrato do projeto que é criado. |
| Moeda | Separador Resumo | Isto indica a moeda que será utilizada para reportar o valor deste negócio. Esta também é a moeda em que o cliente será faturado se o negócio for ganho. Quando uma proposta é criada a partir de uma oportunidade, este campo é copiado a partir do campo correspondente na oportunidade. Este campo na oportunidade assume por predefinição o registo da conta, mas pode ser alterado pelo utilizador.  | Depois de uma proposta ser guardada, este campo deixa de ser editável. Isto é utilizado para assumir por predefinição as listas de preços de produtos e projetos na proposta. A moeda na proposta é utilizada para corresponder à moeda na lista de preços. |
| Limite a não exceder | Separador Resumo | Isto indica o máximo negociado sobre o valor final que o cliente está a acordar para este negócio. | Este máximo é avaliado durante a execução e é aplicável em todos os itens e projetos associados a este negócio. |
| Data de entrega pretendida | Separador Resumo | Quando uma proposta é criada a partir de uma oportunidade, este campo é copiado a partir do campo correspondente na oportunidade. | Esta data é utilizada como data de fim para gerar agendas de faturação. |

Abaixo estão os separadores e os KPIs disponíveis numa proposta de projeto que são exclusivos do Project Operations ou têm algumas alterações importantes no comportamento das propostas de Vendas:

| **Campo** | **Localização** | **Descrição** |
| --- | --- | --- |
| Análise de rentabilidade | Separador na Proposta | O separador mostra as métricas seguintes:</br>- Custo faturável total</br></br>- Custo não faturável total</br>- Receitas totais</br>- Receitas totais (base)</br>- Margem bruta</br>- Margem bruta ajustada|
| Comparação com as Expectativas do Cliente | Separador na Proposta | Este separador mostra as métricas seguintes:</br>- Conclusão estimada</br>- Conclusão pretendida</br>- Orçamento do cliente</br>- Valor da proposta |
| Análise de proposta | Separador na Proposta | Este separador resume os seguintes KPsIs principais para uma proposta de projeto</br>- Comparação com as expectativas do cliente em relação ao orçamento e à agenda</br>- Margem bruta</br>- Margem bruta ajustada |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
