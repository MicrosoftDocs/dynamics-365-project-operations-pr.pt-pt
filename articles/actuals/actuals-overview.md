---
title: Valores Reais
description: Esta tópico fornece informações sobre como trabalhar com valores reais no Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 04/01/2021
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
ms.openlocfilehash: 304c51a4e502ad6ecec1fd821e98d6604ddd59ba
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852558"
---
# <a name="actuals"></a>Valores Reais 

_**Aplica-se a:** Project Operations para cenários baseados em recursos/não armazenados, implementação leve - negócio para faturação pró-forma_

Os valores reais representam os progressos financeiros e de programação revistos e aprovados num projeto. São criados como resultado da aprovação do tempo, despesas, entradas de utilização de materiais e entradas de diário e faturas.

## <a name="journal-lines-and-time-submission"></a>Envio de linhas do diário e tempo

Para mais informações sobre a entrada de hora, consulte [Descrição geral da entrada de hora](../time/time-entry-overview.md).

### <a name="time-and-materials"></a>Hora e materiais

Quando uma entrada de hora que é submetida está associada a um projeto que é mapeado para um item de contrato de tempo e materiais, o sistema cria duas linhas do diário, uma para o custo e uma para as vendas não faturadas.

### <a name="fixed-price"></a>Preço fixo

Quando uma entrada de hora que é submetida está associada a um projeto que está mapeado para um item de contrato de preço fixo, o sistema cria uma linha do diário para o custo.

### <a name="default-pricing"></a>Preço predefinido

A lógica para criar preços predefinidos reside na linha do diário. Os valores do campo da entrada de hora são copiados para a linha do diário. Estes valores incluem a data da transação, o item de contrato para o qual o projeto está mapeado e a moeda resulta na lista de preços apropriada.

Os campos que afetam os preços predefinidos, como **Função** e **Unidade de recursos** são usados para determinar o preço apropriado na linha do diário. Pode adicionar um campo personalizado na entrada de hora. Se pretender que o valor do campo seja propagado aos valores reais, crie o campo nas tabelas **Valores reais** e **Linha do diário**. Utilize código personalizado para propagar o valor de campo selecionado da Entrada de Tempo para Valores reais através da linha do diário utilizando as origens de transação. Para obter mais informações sobre as origens e ligações de transações, consulte [Ligar valores reais a registos originais](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-basic-expense-submission"></a>Submissão de linhas do diário e despesas básicas

Para mais informações sobre a entrada de despesa, consulte [Descrição geral da despesa](../expense/expense-overview.md).

### <a name="time-and-materials"></a>Hora e materiais

Quando uma entrada de despesa básica que é submetida está associada a um projeto que é mapeado para um item de contrato de tempo e materiais, o sistema cria duas linhas do diário, uma para o custo e uma para as vendas não faturadas.

### <a name="fixed-price"></a>Preço fixo

Quando uma entrada de despesa submetida é ligada a um projeto que está mapeado para um item de contrato de preço fixo, o sistema cria uma linha do diário para o custo.

### <a name="default-pricing"></a>Preço predefinido

A lógica para introduzir os preços predefinidos para as despesas baseia-se na categoria de despesa. A data da transação, o item de contrato para o qual o projeto está mapeado e a moeda são utilizados para determinar a lista de preços apropriada. Os campos que afetam os preços predefinidos, como **Categoria de transação** e **Unidade** são usados para determinar o preço apropriado na linha do diário. No entanto, isto só funciona quando o método de preços na tabela de preços é **Preço por unidade**. Se o método de preços for **A custo** ou **Margem de lucro sobre o custo**, o preço introduzido quando a entrada de despesas é criada é utilizado para o custo e o preço na linha de diário de vendas é calculado com base no método de preços. 

Pode adicionar um campo personalizado na entrada de despesas. Se pretender que o valor do campo seja propagado aos valores reais, crie o campo nas tabelas **Valores reais** e **Linha do diário**. Utilize código personalizado para propagar o valor de campo selecionado da Entrada de Tempo para Valores reais através da linha do diário utilizando as origens de transação. Para obter mais informações sobre as origens e ligações de transações, consulte [Ligar valores reais a registos originais](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-material-usage-log-submission"></a>Submissão de linhas de diário e de registo de utilização de materiais

Para obter mais informações sobre a entrada de despesas, consulte o [Registo de utilização de materiais.](../material/material-usage-log.md)

### <a name="time-and-materials"></a>Hora e materiais

Quando uma entrada de registo de utilização de material submetida está ligada a um projeto que está mapeado para uma linha de contrato de tempo e materiais, o sistema cria duas linhas do diário, uma para custo e outra para vendas não faturadas.

### <a name="fixed-price"></a>Preço fixo

Quando uma entrada de registo de utilização de material é ligada a um projeto que está mapeado para um item de contrato de preço fixo, o sistema cria uma linha do diário para o custo.

### <a name="default-pricing"></a>Preço predefinido

A lógica para introduzir preços predefinidos para o material baseia-se na combinação do produto e da unidade. A data da transação, o item de contrato para o qual o projeto está mapeado e a moeda são utilizados para determinar a lista de preços apropriada. Os campos que afetam os preços predefinidos, como **ID do produto** e **Unidade** são usados para determinar o preço apropriado na linha do diário. No entanto, isto só funciona para produtos de catálogo. Para os produtos de write-in, o preço introduzido quando a entrada de registo de utilização do material é criado é utilizado para o custo e preço de venda nas linhas de diário. 

Pode adicionar um campo personalizado na entrada **Registo de utilização de material**. Se pretender que o valor do campo seja propagado aos valores reais, crie o campo nas tabelas **Valores reais** e **Linha do diário**. Utilize código personalizado para propagar o valor de campo selecionado da Entrada de Tempo para Valores reais através da linha do diário utilizando as origens de transação. Para obter mais informações sobre as origens e ligações de transações, consulte [Ligar valores reais a registos originais](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="use-entry-journals-to-record-costs"></a>Utilizar diários de entrada para registar custos

Poderá utilizar os diários de entrada para registar o custo ou a receita nas classes de material, taxa, hora, despesa ou imposto. Os diários podem ser utilizadas para as finalidades seguintes:

- Mover os valores reais da transação a partir de outro sistema para o Microsoft Dynamics 365 Project Operations.
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
