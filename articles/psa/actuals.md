---
title: Descrição geral dos valores reais
description: Este tópico fornece informações sobre os valores reais do projeto.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 63ad6544f0ec0a893aebd8d81f3ee895e51c294e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146137"
---
# <a name="actuals-overview"></a>Descrição geral dos valores reais

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Os valores reais são a quantidade de trabalho que foi concluída num projeto. Os valores reais do projeto podem ser novamente rastreados para os documentos de origem. Estes documentos de origem incluem horas, despesas e entradas de diário, além de faturas.

![Como os valores reais do projeto são rastreados para os documentos de origem](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a>Submeter uma entrada de tempo

No PSA, quando é submetida uma entrada de tempo para um projeto que está mapeado para um item de contrato de hora e material, são criadas duas linhas do diário. Uma linha é para o custo e a outra linha é para as vendas não faturadas. Quando é submetida uma entrada de tempo para um projeto que está mapeado para um item de contrato de preço fixo, é criada uma linha do diário apenas para o custo. 

A lógica para a introdução de preços predefinidos reside na linha do diário. Todos os valores de campo de uma entrada de tempo são copiados para a linha do diário. Estes campos incluem a data da transação, o item de contrato para o qual o projeto está mapeado e a moeda resulta na lista de preços apropriada. 

Os campos que afetam os preços predefinidos, como **Função** e **Unidade Organizacional** fazem com que seja introduzido um preço apropriado por predefinição na linha do diário. Se adicionar um campo personalizado à entrada de tempo e pretender que o valor do campo seja propagado aos valores reais, crie o campo na entidade Valores Reais e utilize mapeamentos de campos para copiar o campo a partir da entrada de tempo para o valor real.

## <a name="submitting-an-expense-entry"></a>Submeter uma entrada de despesa

No PSA, quando é submetida uma entrada de despesa para um projeto que está mapeado para um item de contrato de hora e material, são criadas duas linhas do diário. Uma linha é para o custo e a outra linha é para as vendas não faturadas. Quando é submetida uma entrada de despesa para um projeto que está mapeado para um item de contrato de preço fixo, é criada uma linha do diário apenas para o custo.

A lógica para a entrada de preços predefinidos para despesas é baseada na categoria de despesa que é selecionada na página **Entrada de despesa**, A data da transação, o item de contrato para o qual o projeto está mapeado e a moeda são utilizados para determinar a lista de preços apropriada. No entanto, para o preço propriamente dito, o montante introduzido pelo utilizador é definido diretamente nas linhas do diário de despesas relacionadas para o custo e as vendas, por predefinição.

Na versão atual do PSA, a entrada baseada em categorias de preços predefinidos por unidade em entradas de despesa não está disponível.

## <a name="using-entry-journals-to-record-costs"></a>Utilizar diários de Entrada para registar custos

Em PSA, os diários de Entrada permitem-lhe registar o custo ou a receita nas classes de material, taxa, hora, despesa ou imposto. Um diário tem um cabeçalho, linhas e uma ação de **Confirmação**. Seguem-se alguns cenários em que poderá utilizar um diário:

- Tem de registar os custos reais de materiais e as vendas num projeto.
- Tem de mover os valores reais da transação a partir de outro sistema para o PSA.
- Tem de registar os custos que ocorreram noutro sistema, tal como os custos de aprovisionamento ou subcontratação.

> [!IMPORTANT]
> A utilização de diários de Entrada para criar valores reais deve ser feita apenas por um utilizador que esteja plenamente consciente do impacto contabilístico que os Valores Reais têm no projeto. Isto porque a aplicação não valida o tipo de linha do diário, ou o preço relacionado que é introduzido na linha do diário. Devido ao impacto deste tipo de diário, tenha o cuidado adequado a quem é dado acesso para criar diários de Entrada.     


## <a name="recording-actuals-based-on-project-events"></a>Registar valores reais com base em eventos de projeto

O PSA regista as transações financeiras que ocorrem durante um projeto. Estas transações são registadas como **reais**. As tabelas seguintes mostram os diferentes tipos de valores reais criados, dependendo do facto de o projeto ser um projeto de tempo e material ou de preço fixo, que se encontra na fase pré-venda, ou é um projeto interno.

**O recurso pertence à mesma unidade organizacional que a unidade organizacional do projeto**

<table>
<thead>
<tr>
<th rowspan="3">Evento</th>
<th colspan="4">Projeto faturável ou vendido</th>
<th rowspan="3">Projeto na fase pré-venda</th>
<th rowspan="3">Projeto interno</th>
</tr>
<tr>
<th colspan="2">Hora e materiais</th>
<th colspan="2">Preço fixo</th>
</tr>
<tr>
<th>Valores Reais</th>
<th>Moeda da transação</th>
<th>Preço fixo</th>
<th>Moeda da transação</th>
</tr>
</thead>
<tbody>
<tr>
<td>É criada uma entrada de hora.</td>
<td colspan="6">Sem atividade na entidade Valores Reais</td>
</tr>
<tr>
<td>É submetida uma entrada de hora.</td>
<td colspan="6">Sem atividade na entidade Valores Reais</td>
</tr>
<tr>
<td rowspan="2">A hora é aprovada e não ocorre nenhuma alteração ou aumento nas horas faturáveis durante a aprovação.</td>
<td>Custo real</td>
<td>Moeda da unidade de contratação</td>
<td rowspan="2">Custo real</td>
<td rowspan="2">Moeda da unidade de contratação
<td rowspan="2">Custo real</td>
<td rowspan="2">Custo real</td>
</tr>
<tr>
<td>Valor real de vendas não faturadas – Faturável</td>
<td>Moeda do contrato do projeto</td>
</tr>
<tr>
<td rowspan="3">A hora é aprovada e ocorre uma diminuição nas horas faturáveis durante a aprovação.</td>
<td>Custo real</td>
<td>Moeda da unidade de contratação</td>
<td rowspan="3">Custo real</td>
<td rowspan="3">Moeda da unidade de contratação</td>
<td rowspan="3">Custo real</td>
<td rowspan="3">Custo real</td>
</tr>
<tr>
<td>Valor real de vendas não faturadas – Faturável para a nova quantidade</td>
<td>Moeda do contrato do projeto</td>
</tr>
<tr>
<td>Valor real de vendas não faturadas – Não faturável para a diferença</td>
<td>Moeda do contrato do projeto</td>
</tr>
<tr>
<td rowspan="2">É confirmada uma fatura e não ocorre nenhuma alteração ou aumento nas horas faturáveis.</td>
<td>Estorno de vendas não faturadas</td>
<td>Moeda do contrato do projeto</td>
<td rowspan="2">Vendas faturadas para marco</td>
<td rowspan="2">Moeda do contrato do projeto</td>
<td rowspan="2">Não aplicável</td>
<td rowspan="2">Não aplicável</td>
</tr>
<tr>
<td>Vendas faturadas</td>
<td>Moeda do contrato do projeto</td>
</tr>
<tr>
<td rowspan="3">É confirmada uma fatura e ocorre uma diminuição nas horas faturáveis.</td>
<td>Estorno de vendas não faturadas</td>
<td>Moeda do contrato do projeto</td>
<td rowspan="3">Não aplicável</td>
<td rowspan="3">Não aplicável</td>
<td rowspan="3">Não aplicável</td>
<td rowspan="3">Não aplicável</td>
</tr>
<tr>
<td>Vendas faturadas – Faturável para a nova quantidade</td>
<td>Moeda do contrato do projeto</td>
</tr>
<tr>
<td>Vendas não faturadas – Não faturável para a diferença</td>
<td>Moeda do contrato do projeto</td>
</tr>
<tr>
<td rowspan="2">Uma fatura é corrigida para aumentar a quantidade faturável.</td>
<td>Vendas faturadas – Estorno</td>
<td>Moeda do contrato do projeto</td>
<td rowspan="5">
<ul>
<li>Estorno de vendas faturadas para marco</li>
<li>Alterar o estado do marco de <strong>Faturado</strong> para <strong>Pronto para faturação</strong></li>
</ul>
</td>
<td rowspan="5">Moeda do contrato do projeto</td>
<td rowspan="5">Não aplicável</td>
<td rowspan="5">Não aplicável</td>
</tr>
<tr>
<td>Vendas faturadas</td>
<td>Moeda do contrato do projeto</td>
</tr>
<tr>
<td rowspan="3">Uma fatura é corrigida para diminuir a quantidade faturável.</td>
<td>Vendas faturadas – Estorno</td>
<td>Moeda do contrato do projeto</td>
</tr>
<tr>
<td>Vendas faturadas para a nova quantidade</td>
<td>Moeda do contrato do projeto</td>
</tr>
<tr>
<td>Vendas não faturadas – Faturável para a diferença</td>
<td>Moeda do contrato do projeto</td>
</tr>
</tbody>
</table>

**O recurso pertence a uma unidade organizacional que difere da unidade organizacional do projeto**

<table>
<thead>
<tr>
<th rowspan="3">Evento</th>
<th colspan="4">Projeto faturável ou vendido</th>
<th rowspan="3">Projeto na fase pré-venda</th>
<th rowspan="3">Projeto interno</th>
</tr>
<tr>
<th colspan="2">Hora e materiais</th>
<th colspan="2">Preço fixo</th>
</tr>
<tr>
<th>Valores Reais</th>
<th>Moeda da transação</th>
<th>Preço fixo</th>
<th>Moeda da transação</th>
</tr>
</thead>
<tbody>
<tr>
<td>É criada uma entrada de hora.</td>
<td colspan="6">Sem atividade na entidade Valores Reais</td>
</tr>
<tr>
<td>É submetida uma entrada de hora.</td>
<td colspan="6">Sem atividade na entidade Valores Reais</td>
</tr>
<tr>
<td rowspan="4">A hora é aprovada e não ocorre nenhuma alteração ou aumento nas horas faturáveis durante a aprovação.</td>
<td>Custo real</td>
<td>Moeda da unidade de contratação</td>
<td rowspan="4">Custo real</td>
<td rowspan="4">Moeda da unidade de contratação</td>
<td rowspan="4">Custo real</td>
<td rowspan="4">Custo real</td>
</tr>
<tr>
<td>Valor real de vendas não faturadas – Faturável</td>
<td>Moeda do contrato do projeto</td>
</tr>
<tr>
<td>Custo de unidade de atribuição de recursos</td>
<td>Moeda da unidade de atribuição de recursos</td>
</tr>
<tr>
<td>Vendas interorganizacionais</td>
<td>Moeda da unidade de contratação</td>
</tr>
<tr>
<td rowspan="5">A hora é aprovada e ocorre uma diminuição nas horas faturáveis durante a aprovação.</td>
<td>Custo real</td>
<td>Moeda da unidade de contratação</td>
<td rowspan="5">Custo real</td>
<td rowspan="5">Moeda da unidade de contratação</td>
<td rowspan="5">Custo real</td>
<td rowspan="5">Custo real</td>
</tr>
<tr>
<td>Custo de unidade de atribuição de recursos</td>
<td>Moeda da unidade de atribuição de recursos</td>
</tr>
<tr>
<td>Vendas interorganizacionais</td>
<td>Moeda da unidade de contratação</td>
</tr>
<tr>
<td>Valor real de vendas não faturadas – Faturável para a nova quantidade</td>
<td>Moeda do contrato do projeto</td>
</tr>
<tr>
<td>Valor real de vendas não faturadas – Não faturável para a diferença</td>
<td>Moeda do contrato do projeto</td>
</tr>
<tr>
<td rowspan="2">É confirmada uma fatura e não ocorre nenhuma alteração ou aumento nas horas faturáveis.</td>
<td>Estorno de vendas não faturadas</td>
<td>Moeda do contrato do projeto</td>
<td rowspan="2">Vendas faturadas para marco</td>
<td rowspan="2">Moeda do contrato do projeto</td>
<td rowspan="2">Não aplicável</td>
<td rowspan="2">Não aplicável</td>
</tr>
<tr>
<td>Vendas faturadas</td>
<td>Moeda do contrato do projeto</td>
</tr>
<tr>
<td rowspan="3">É confirmada uma fatura e ocorre uma diminuição nas horas faturáveis.</td>
<td>Estorno de vendas não faturadas</td>
<td>Moeda do contrato do projeto</td>
<td rowspan="3">Não aplicável</td>
<td rowspan="3">Não aplicável</td>
<td rowspan="3">Não aplicável</td>
<td rowspan="3">Não aplicável</td>
</tr>
<tr>
<td>Vendas faturadas – Faturável para a nova quantidade</td>
<td>Moeda do contrato do projeto</td>
</tr>
<tr>
<td>Vendas não faturadas – Não faturável para a diferença</td>
<td>Moeda do contrato do projeto</td>
</tr>
<tr>
<td rowspan="2">Uma fatura é corrigida para aumentar a quantidade faturável.</td>
<td>Vendas faturadas – Estorno</td>
<td>Moeda do contrato do projeto</td>
<td rowspan="5">
<ul>
<li>Estorno de vendas faturadas para marco</li>
<li>Alterar o estado do marco de <strong>Faturado</strong> para <strong>Pronto para faturação</strong></li>
</ul>
</td>
<td rowspan="5">Moeda do contrato do projeto</td>
<td rowspan="5">Não aplicável</td>
<td rowspan="5">Não aplicável</td>
</tr>
<tr>
<td>Vendas faturadas</td>
<td>Moeda do contrato do projeto</td>
</tr>
<tr>
<td rowspan="3">Uma fatura é corrigida para diminuir a quantidade faturável.</td>
<td>Vendas faturadas – Estorno</td>
<td>Moeda do contrato do projeto</td>
</tr>
<tr>
<td>Vendas faturadas para a nova quantidade</td>
<td>Moeda do contrato do projeto</td>
</tr>
<tr>
<td>Vendas não faturadas – Faturável para a diferença</td>
<td>Moeda do contrato do projeto</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]