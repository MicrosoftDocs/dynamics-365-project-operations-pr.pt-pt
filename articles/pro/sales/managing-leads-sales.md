---
title: Gerir oportunidades potenciais – lite
description: Este tópico fornece informações sobre como gerir as oportunidades potenciais baseadas em projetos (pro).
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e789295d4b1f5a53fcf179a2998f60d35f48f99
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 11/12/2020
ms.locfileid: "4513803"
---
# <a name="manage-leads---lite"></a>Gerir oportunidades potenciais – lite

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

As oportunidades potenciais baseadas em projetos podem ser geridas e qualificadas no Project Operations. O processo de gestão de oportunidades potenciais inclui a criação de oportunidades potenciais baseadas no trabalho e a qualificação dessas oportunidades potenciais. 

## <a name="list-of-project-sales-leads"></a>LIsta de oportunidades potenciais baseadas em projetos

Na secção **Vendas**, no painel de navegação esquerdo, abra a página da lista **Oportunidades Potenciais** para ver uma lista de todos os registos de oportunidades potenciais no sistema. As oportunidades potenciais da lista são baseadas no trabalho e outros tipos de oportunidades potenciais que podem ser criadas se também tiver as aplicações do Dynamics 365 Sales ou Dynamics 365 Field Service.

Pode criar um vista filtrada para ver apenas as oportunidades potenciais pistas baseadas em projetos ao criar um filtro no valor **Tipo**. Por exemplo, pode selecionar para mostrar apenas as oportunidades potenciais baseadas no trabalho.

## <a name="creating-a-new-lead-for-a-project-based-deal"></a>Criar uma nova oportunidade potencial para um negócio baseado em projetos

Quando uma oportunidade potencial baseada em projetos é qualificada, é criada uma oportunidade e uma conta. Uma oportunidade baseada em projetos é o ponto de partida para as atividades de seguimento de vendas na fase Oportunidade. As oportunidades baseadas em projetos têm capacidades exclusivas que são necessárias para vender o trabalho do projeto. Estas capacidades incluem:

- Métodos de faturação Tempo e material e Preço Fixo
- Listas de preços em vigor em várias datas para recursos humanos, despesas e material incorridos em projetos.

Para uma oportunidade potencial qualificada criar automaticamente uma oportunidade, defina o atributo **Tipo** como **Baseado em trabalho** quando cria a oportunidade potencial. Se escolher um tipo diferente, a oportunidade potencial não criará uma oportunidade baseada em projetos quando é qualificada. Se a oportunidade baseada em projetos não for criada, as capacidades específicas do projeto não estarão disponíveis nos processos de vendas a jusante.

A tabela seguinte inclui informações de campos importantes para uma oportunidade potencial e as implicações a jusante desses campos.

| **Campo** | **Localização** | **Descrição** | **Impacto a jusante** |
| --- | --- | --- | --- |
| Tópico | Separador Geral | Este campo de texto deve conter uma breve descrição do negócio. | O tópico da oportunidade potencial assume por predefinição o tópico da Oportunidade e o contrato Nome da Proposta e do Projeto. |
| Tipo | Separador Geral | Este campo do conjunto de opções tem as seguintes opções:</br>- Baseado em trabalho (disponível apenas quando o Project Operations está instalado)</br>- Baseado em item (disponível apenas quando o Project Operations e o Sales estão instalados)</br>- Baseado em manutenção do serviço (disponível quando o Field Service estiver instalado) | Quando o valor deste campo é definido como **Baseado em trabalho** na oportunidade potencial, a oportunidade potencial é qualificada para criar uma Oportunidade Baseada em Projetos. É necessária uma oportunidade baseada em projetos para ativar todas as funcionalidades e extensões específicas do projeto no processo de vendas a jusante para este negócio. |
| Nome próprio | Separador Geral | Nome próprio do contrato do potencial interessado | Quando a oportunidade potencial é qualificada, é criada uma conta, um contacto e uma oportunidade. O nome próprio do contacto é o valor aqui definido. |
| Apelido | Separador Geral | Apelido do contrato do potencial interessado | Quando a oportunidade potencial é qualificada, é criada uma conta, um contacto e uma oportunidade. O apelido do contacto é o valor aqui definido. |
| Empresa | Separador Geral | Nome da empresa do cliente potencial | Quando a oportunidade potencial é qualificada, é criada uma conta, um contacto e uma oportunidade. O nome da conta criada é o valor aqui definido. |
| Moeda | Separador Detalhes | Moeda do cliente do potencial interessado | Quando a oportunidade potencial é qualificada, é criada uma conta, um contacto e uma oportunidade. A moeda da conta criada é o valor aqui definido. |

## <a name="qualify-a-new-project-based-lead"></a>Qualificar uma nova oportunidade potencial baseada em projetos

As oportunidades potenciais que têm o valor **Tipo** definido como **Baseado em trabalho** são chamadas oportunidades potenciais baseadas em projetos. Quando uma oportunidade potencial baseada em projetos é qualificada, é criado o seguinte:

- Uma conta que utiliza o campo **Empresa** a partir da oportunidade potencial.
- Um registo de contacto associado à conta baseado nos valores nos campos **Nome Próprio** e **Apelido** na oportunidade potencial.
- Uma oportunidade baseada em projetos que tem o campo **Tipo** definido como **Baseado em trabalho**.

Para obter informações mais detalhadas sobre como qualificar oportunidades potenciais, consulte [Qualificar ou converter oportunidades potenciais](https://docs.microsoft.com/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales).

## <a name="business-process-flow-for-project-based-deals"></a>Fluxo do processo de negócio para as oportunidades potenciais baseadas em projetos

Os seguintes fluxos do processo de negócio são suportados para as oportunidades potenciais baseadas no projeto no Project Operations:

- Processo de negócio da Oportunidade Potencial à Oportunidade
- Processo de vendas da Oportunidade

O processo de negócio Da Oportunidade Potencial à Oportunidade suporta as seguintes fases:

| Nome da fase | Entidade mapeada | Funcionalidade |
| --- | --- | --- |
| Qualificar | Oportunidade Potencial | Qualifique a oportunidade potencial para criar uma conta, um contacto e uma oportunidade. |
| Desenvolver | Oportunidade | Desenvolva a oportunidade para adicionar mais informações sobre o trabalho envolvido, os principais intervenientes e a concorrência. |
| Propor | Oportunidade | Desenvolva a proposta e obtenha a aprovação da equipa de revisão interna. |
| Fechar | Oportunidade | Ganhe a oportunidade de fechar o negócio. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]