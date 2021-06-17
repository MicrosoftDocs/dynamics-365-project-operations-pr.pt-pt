---
title: Definições do contrato de projeto
description: Este tópico fornece informações sobre os campos que impactam os itens de contratos e a informação sobre o contrato que são resumidas em todos os itens de linha.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1e6971553bb436ee5bcad2c335d32c929ddc4800
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996175"
---
# <a name="header-details-for-project-based-contracts"></a>Detalhes do cabeçalho para contratos baseados em projetos

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Este tópico fornece informações sobre campos que se aplicam a todo o contrato do projeto, incluindo definições que impactam todas os itens de contrato. Informações sobre o contrato que são resumidas em todos os itens de contrato para impulsionar KPIs do contrato do projeto também estão incluídas.

A tabela que se segue lista os campos de um contrato de projeto que são exclusivos do Dynamics 365 Project Operations ou têm algumas mudanças importantes no comportamento das encomendas de vendas no Dynamics 365 Sales.

| Campo | Localização | Descrição | Impacto a jusante |
| --- | --- | --- | --- |
| Tipo | Separador **Resumo** (oculto) | Este é um campo do conjunto de opções com as seguintes opções:</br>- **Baseado em trabalho** (Disponível apenas quando o Project Operations está instalado)</br>- **Baseado em item** (Disponível apenas quando o Project Operations e o Sales estão instalados)</br>- **Baseado em Manutenção do serviço** (Disponível quando o Dynamics 365 Field Service está instalado) | No Project Operations, o valor deste campo reverte à predefinição **Baseado em trabalho** e classifica o contrato como um contrato baseado em projetos. Um contrato deve ser baseado em projetos para ativar todas as extensões e funcionalidades específicas do projeto. |
| Empresa Proprietária | Separador **Resumo** | A entidade legal que contabiliza os custos e receitas decorrentes dos projetos associados a este contrato de projeto. Quando um contrato é criado a partir de uma proposta, este campo é copiado a partir do campo correspondente no registo da proposta. | A empresa proprietária equipara-se ao conceito de entidade legal no módulo **Gestão de projetos e contabilística** do Project Operations. Todos os custos e receitas decorrentes deste projeto são contabilizados no Livro Razão Geral da empresa proprietária. |
| Cliente | Separador **Resumo** | Uma referência ao registo da conta ou empresa do cliente. Quando um contrato é criado a partir de uma proposta, este campo é copiado a partir do campo correspondente no registo da proposta. | A moeda no contrato de projeto reverte para a predefinição com base na moeda do cliente. A moeda pode ser alterada antes do contrato ser guardado. |
| Gestor de Contas | Separador **Resumo** | O nome do Gestor de Conta para este negócio. Quando um contrato é criado a partir de uma proposta, este campo é copiado a partir do campo correspondente no registo da proposta. | O Gestor de Conta é responsável pela gestão da relação com o cliente até à conclusão do projeto. Baseado no registo de recurso reservável associado ao Gestor de Conta, a unidade de contratação assume por predefinição o contrato de projeto. |
| Unidade de Contratação | Separador **Resumo** | A unidade organizacional responsável pela entrega dos projetos associados a este contrato. Quando um contrato é criado a partir de uma proposta, este campo é copiado a partir do campo correspondente no registo da proposta. | A unidade de contratação é a divisão da empresa que executa os projetos. Todas as unidades de contratação têm uma moeda, e esta moeda é utilizada para reportar os custos estimados e reais incorridos durante o projeto. |
| Lista de Preços de Produtos | Separador **Resumo** | Esta é a lista de preços que é utilizada para os preços predefinidos nos itens de contrato baseados em produtos. A lista de opções pendentes para este campo mostra uma lista de listas de preços onde a moeda da lista de preços corresponde à moeda no contrato. Quando um contrato é criado a partir de uma proposta, este campo é copiado a partir do campo correspondente no registo da proposta. No contrato de projeto, este campo assume por predefinição o registo da conta, mas pode ser alterado. | Não existe nenhuma relevância a jusante para este campo. |
| Moeda | Separador **Resumo** | A moeda utilizada para reportar o valor deste negócio e a moeda em que o cliente será faturado. Quando um contrato é criado a partir de uma proposta, este campo é copiado a partir do campo correspondente no registo da proposta. No contrato de projeto, este campo assume por predefinição o registo da conta, mas pode ser alterado. | Depois de um contrato ser guardado, este campo deixa de ser editável. Este campo é utilizado para assumir por predefinição as listas de preços de produtos e projetos no contrato. A moeda no contrato é utilizada para corresponder à moeda na lista de preços. |
| Limite a Não Exceder | Separador **Resumo** | Este campo indica o máximo negociado sobre o valor final que o cliente acordou para este negócio. | O máximo é avaliado durante a execução e é aplicável em todos os itens e projetos associados a este negócio. |
| Data de Entrega Pretendida | Separador **Resumo** | Quando um contrato é criado a partir de uma proposta de projeto, este campo é copiado a partir do campo correspondente na proposta do projeto. | Esta data é utilizada como data de fim para gerar agendas de faturação. |

Os seguintes KPIs estão disponíveis no separador **Desempenho do Contrato** de um contrato de projeto.

| Campo | Localização | Descrição |
| --- | --- | --- |
| Valor de Contrato | Contrato geral | O valor total do contrato do Projeto. |
| Montante Cobrado | Contrato geral | A soma dos montantes em todas as faturas contra este contrato. |
| Custo Incorrido | Contrato geral | A soma de todos os custos reais registados em todos os projetos que estão mapeados para o contrato. |
| Margem Bruta | Contrato geral | Valor faturado – Custo incorrido até à data / Valor faturado |
| Margem Esperada | Contrato geral | (Valor do contrato – Custos estimados) / Custos estimados do valor do contrato = A soma de todos os custos estimados em todos os projetos mapeados no contrato.|
| Valor de Contrato | Itens baseados em projetos | O valor do item de contrato. |
| Montante faturado | Itens baseados em projetos | Para o item de contrato de preço fixo: A soma dos montantes em todos os valores reais de marcos de vendas faturados contra este item de contrato em várias faturas criadas para este contrato. Para o item de contrato de hora e material: A soma dos montantes em todos os valores reais de vendas faturados faturáveis contra este item de contrato em várias faturas criadas para este contrato. |
| Custo Incorrido | Itens baseados em projetos | A soma de todos os custos reais registados em todos os projetos mapeados para o item de contrato. |
| Margem Bruta | Itens baseados em projetos | (Valor faturado – Custo incorrido até à data) / Valor faturado |
| Margem Esperada | Itens baseados em projetos | (Valor do item de contrato na moeda base – Custos estimados para o item de contrato na moeda base) / Valor do item de contrato na moeda base |
| Custo Incorrido | Detalhe de um item baseado em projeto | Tempo: A soma do valor em tempo de custo real registada para esta função no projeto mapeado para o item de contrato. Despesas: A soma do valor dos custos reais registados de todas as despesas para esta categoria no projeto mapeado para o item de contrato. |
| Quantidade registada | Detalhe de um item baseado em projeto | Tempo: A quantidade do tempo total no custo real registado para uma função no projeto que é mapeada para este item de contrato. Despesas: Todas as quantidades para esta categoria de despesas nos custos reais de despesas no projeto são mapeadas para este item de contrato. |
| Montante Cobrado | Detalhe de um item baseado em projeto | Para um item de contrato de preço fixo, este campo é deixado em branco no nível do detalhe e só é mostrado ao nível do item de contrato. Por um item de contrato de tempo e material, os cálculos são concluídos ao nível dos detalhes. Os detalhes mostram a soma do montante em todas as linhas de receita faturadas contra este item de contrato que são faturáveis. |
| Quantidade Cobrada | Detalhe de um item baseado em projeto | Para um item de contrato de preço fixo, este campo é deixado em branco no nível do detalhe e só é mostrado ao nível do item de contrato. Por um item de contrato de tempo e material, os cálculos são concluídos ao nível dos detalhes para o tempo e despesas. Tempo: A soma de horas em todas as linhas de receita faturadas para esta função contra este item de contrato que são faturáveis. Despesas: Todas as quantidades para esta categoria de despesas nos custos reais de despesas no projeto são mapeadas para este item de contrato. |
| Valor de Contrato | Itens baseados em produtos | O valor do item de contrato deste item de contrato baseado em produtos. |
| Montante Cobrado | Itens baseados em produtos | A soma dos montantes em todos as linhas de fatura contra este item de contrato baseado no produto em várias faturas que são criadas para este contrato. |
| Custo Incorrido | Itens baseados em produtos | A soma de todos os custos reais registados em todos os projetos mapeados para o item de contrato. |
| Margem Bruta | Itens baseados em projetos | Valor faturado – Custo incorrido até à data / Valor faturado |
| Margem Esperada | Itens baseados em produtos | (Valor da linha do contrato - Custos estimados para a linha de contrato) / Valor da linha contratual |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
