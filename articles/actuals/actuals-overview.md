---
title: Valores Reais
description: Este tópico fornece informações sobre como trabalhar com valores reais no Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 13c429763fa805fae5324e4dcf1bf7669e842281
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126328"
---
# <a name="actuals"></a>Valores Reais 

_**Aplica-se a:** Project Operations para cenários baseados em recursos/não armazenados_

Os valores reais são a quantidade de trabalho que foi concluída num projeto. São criados como resultado de entradas de hora e despesa, e entradas de diário e faturas.

## <a name="journal-lines-and-time-submission"></a>Envio de linhas do diário e tempo

Para mais informações sobre a entrada de hora, consulte [Descrição geral da entrada de hora](../time/time-entry-overview.md).

### <a name="time-and-materials"></a>Hora e materiais

Quando uma entrada de hora que é submetida está associada a um projeto que é mapeado para um item de contrato de tempo e materiais, o sistema cria duas linhas do diário, uma para o custo e uma para as vendas não faturadas.

### <a name="fixed-price"></a>Preço fixo

Quando uma entrada de hora que é submetida está associada a um projeto que está mapeado para um item de contrato de preço fixo, o sistema cria uma linha do diário para o custo.

### <a name="default-pricing"></a>Preço predefinido

A lógica para criar preços predefinidos reside na linha do diário. Os valores do campo da entrada de hora são copiados para a linha do diário. Estes valores incluem a data da transação, o item de contrato para o qual o projeto está mapeado e a moeda resulta na lista de preços apropriada.

Os campos que afetam os preços predefinidos, como **Função** e **Unidade Organizacional** são utilizados para determinar o preço adequado na linha do diário. Pode adicionar um campo personalizado na entrada de hora. Se pretende que o valor do campo seja propagado aos valores reais, crie o campo na entidade Valores Reais e utilize mapeamentos de campos para copiar o campo a partir da entrada de hora para o valor real.

## <a name="journal-lines-and-basic-expense-submission"></a>Submissão de linhas do diário e despesas básicas

Para mais informações sobre a entrada de despesa, consulte [Descrição geral da despesa](../expense/expense-overview.md).

### <a name="time-and-materials"></a>Hora e materiais

Quando uma entrada de despesa básica que é submetida está associada a um projeto que é mapeado para um item de contrato de tempo e materiais, o sistema cria duas linhas do diário, uma para o custo e uma para as vendas não faturadas.

### <a name="fixed-price"></a>Preço fixo

Quando uma entrada de despesa básica que é submetida está associada a um projeto que está mapeado para um item de contrato de preço fixo, o sistema cria uma linha do diário para o custo.

### <a name="default-pricing"></a>Preço predefinido

A lógica para introduzir os preços predefinidos para as despesas baseia-se na categoria de despesa. A data da transação, o item de contrato para o qual o projeto está mapeado e a moeda são utilizados para determinar a lista de preços apropriada. No entanto, por predefinição, o montante que é introduzido para o preço é definido diretamente nas linhas do diário de despesas relacionadas para o custo e as vendas.

A entrada baseada em categorias de preços predefinidos por unidade em entradas de despesa não está disponível.

## <a name="use-entry-journals-to-record-costs"></a>Utilizar diários de entrada para registar custos

Poderá utilizar os diários de entrada para registar o custo ou a receita nas classes de material, taxa, hora, despesa ou imposto. Os diários podem ser utilizadas para as finalidades seguintes:

- Registe o custo real dos materiais e vendas num projeto.
- Mova os valores reais da transação a partir de outro sistema para o Microsoft Dynamics 365 Project Operations.
- Registe os custos que ocorreram noutro sistema. Estes custos podem incluir os custos de aprovisionamento ou subcontratação.

> [!IMPORTANT]
> A aplicação não valida o tipo de linha de diário ou o preço relacionado que é introduzido na linha do diário. Assim, só um utilizador plenamente consciente do impacto contabilístico que os valores reais têm no projeto deve utilizar diários de entrada para criar valores reais. Dado o impacto deste tipo de diário, deve escolher cuidadosamente quem tem acesso para criar diários de entrada.
## <a name="record-actuals-based-on-project-events"></a>Registar os valores reais baseado nos eventos do projeto

O Project Operations regista as transações financeiras que ocorrem durante um projeto. Estas transações são registadas como reais. As tabelas seguintes mostram os diferentes tipos de valores reais criados, dependendo do facto de o projeto ser um projeto de tempo e material ou de preço fixo, que se encontra na fase pré-venda, ou é um projeto interno.

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a>O recurso pertence à mesma unidade organizacional que a unidade organizacional do projeto

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

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a>O recurso pertence a uma unidade organizacional que difere da unidade organizacional do projeto

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