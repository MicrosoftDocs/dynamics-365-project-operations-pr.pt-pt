---
title: Gerir oportunidades potenciais
description: Este tópico fornece informações sobre como gerir as oportunidades potenciais baseadas em projetos.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a10be42f4ae1ecc8ae5613ed8fdc669304e0ec72
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898635"
---
# <a name="manage-leads"></a>Gerir oportunidades potenciais

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

As oportunidades potenciais baseadas em projetos podem ser geridas e qualificadas no Project Operations. O processo de gestão de oportunidades potenciais inclui a criação de oportunidades potenciais baseadas no trabalho e a qualificação dessas oportunidades potenciais. 

## <a name="project-sales-leads"></a>Oportunidades potenciais baseadas em projetos

Na secção **Vendas**, no painel de navegação esquerdo, abra a página da lista **Oportunidades Potenciais** para ver uma lista de todos os registos de oportunidades potenciais no sistema. A lista de oportunidades potenciais baseia-se no trabalho e noutros tipos de oportunidades potenciais que podem ser criados se também tiver as aplicações do Dynamics 365 Sales ou do Dynamics 365 Field Service.

Pode criar um vista filtrada para ver apenas as oportunidades potenciais pistas baseadas em projetos ao criar um filtro no valor **Tipo**. Por exemplo, pode selecionar para mostrar apenas as oportunidades potenciais baseadas no trabalho.

## <a name="create-a-new-lead-for-a-project-based-deal"></a>Criar uma nova oportunidade potencial para um negócio baseado em projetos

Quando uma oportunidade potencial baseada em projetos é qualificada, é criada uma oportunidade e uma conta. Uma oportunidade baseada em projetos é o ponto de partida para as atividades de seguimento de vendas na fase Oportunidade. As oportunidades baseadas em projetos têm capacidades exclusivas que são necessárias para vender o trabalho do projeto. Estas capacidades incluem:

- Métodos de faturação Tempo e material e Preço Fixo
- Listas de preços em vigor em várias datas para recursos humanos, despesas e material incorridos em projetos

Para a oportunidade potencial qualificada criar automaticamente uma oportunidade, defina o atributo **Tipo** como **Baseado em trabalho** quando cria a oportunidade potencial. Se escolher um tipo diferente, a oportunidade potencial não criará uma oportunidade baseada em projetos quando é qualificada. Se a oportunidade baseada em projetos não for criada, as capacidades específicas do projeto não estarão disponíveis nos processos de vendas a jusante.

A tabela seguinte inclui informações de campos importantes para uma oportunidade potencial e as implicações a jusante desses campos.
 
| **Campo** | **Localização** | **Relevância, finalidade e orientação** | **Impacto a jusante** |
| --- | --- | --- | --- |
| Tópico | Separador Geral | Este campo de texto deve conter uma breve descrição do negócio. | O tópico da oportunidade potencial assume por predefinição o tópico da Oportunidade e o contrato Nome da Proposta e do Projeto. |
| Tipo | Separador Geral | Este campo do conjunto de opções tem as seguintes opções:</br>- Baseado em trabalho (disponível apenas quando o Project Operations está instalado)</br>- Baseado em item (disponível apenas quando o Project Operations e o Sales estão instalados)</br>- Baseado em manutenção do serviço (disponível quando o Field Service estiver instalado) | Quando o valor deste campo é definido como **Baseado em trabalho** na oportunidade potencial, a oportunidade potencial é qualificada para criar uma Oportunidade Baseada em Projetos. É necessária uma oportunidade baseada em projetos para ativar todas as funcionalidades e extensões específicas do projeto no processo de vendas a jusante para este negócio. |
| Nome próprio | Separador Geral | Nome próprio do contrato do potencial interessado | Quando a oportunidade potencial é qualificada, é criada uma conta, um contacto e uma oportunidade. O nome próprio do contacto é o valor aqui definido. |
| Apelido | Separador Geral | Apelido do contrato do potencial interessado | Quando a oportunidade potencial é qualificada, é criada uma conta, um contacto e uma oportunidade. O apelido do contacto é o valor aqui definido. |
| Empresa | Separador Geral | Nome da empresa do cliente potencial | Quando a oportunidade potencial é qualificada, é criada uma conta, um contacto e uma oportunidade. O nome da conta que criou o valor aqui definido. |
| Moeda | Separador Detalhes | Moeda do cliente do potencial interessado | Quando a oportunidade potencial é qualificada, é criada uma conta, um contacto e uma oportunidade. A moeda da conta criada é o valor aqui definido. |

## <a name="qualify-a-new-project-based-lead"></a>Qualificar uma nova oportunidade potencial baseada em projetos

As oportunidades potenciais que têm o valor **Tipo** definido como **Baseado em trabalho** são chamadas oportunidades potenciais baseadas em projetos. Quando uma oportunidade potencial baseada em projetos é qualificada, é criado o seguinte:

- Uma conta que utiliza o campo **Empresa** a partir da oportunidade potencial.
- Um registo de contacto associado à conta baseado nos valores nos campos **Nome Próprio** e **Apelido** na oportunidade potencial.
- Uma oportunidade baseada em projetos que tem o campo **Tipo** definido como &quot;**Baseado em trabalho**.

Para obter informações mais detalhadas sobre como qualificar oportunidades potenciais, consulte [Qualificar ou converter oportunidades potenciais](https://docs.microsoft.com/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales).

## <a name="lead-qualification-and-legal-entity-information"></a>Qualificação de oportunidades potenciais e informações da entidade legal 

Quando executa o Project Operations através do modo de implementação, Project Operations para cenários baseados em recursos/não armazenados, cada cliente e oportunidade exigirá ter o campo **Empresa Proprietária** definido. A Empresa Proprietária é uma entidade legal da sua organização é proprietária da entrega do projeto. Cada cliente, ou conta com um tipo de relação cliente, tem de ter o valor de campo **Empresa Proprietária** definido para a entidade legal que contrata e negoceia com este cliente. Um cliente só pode estar numa entidade legal.

Quando uma oportunidade potencial é qualificada, os registos de cliente e oportunidade criados terão o campo **Empresa Proprietária** definido para a empresa do registo de recursos reserváveis do utilizador atual.

Se o registo de recursos reserváveis do utilizador atual estiver vazio, então o valor de campo **Empresa Proprietária** no registo de utilizador é utilizado para assumir por predefinição nos registos de cliente e de oportunidade.

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
