---
title: Descrição geral do processo de vendas
description: Este tópico fornece informações sobre processos de vendas básicos.
author: rumant
ms.date: 10/29/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: ed9731193e83eebd35e979adffcea529a289b9c5
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368355"
---
# <a name="sales-process-overview"></a>Descrição geral do processo de vendas

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Os processos de vendas utilizados numa organização baseada em projetos diferem dos processos de vendas utilizados numa organização baseada em produtos. Esta diferença deve-se ao facto dos ciclos de vendas para as organizações baseadas em projetos são mais demorados e necessitam de técnicas de estimativa personalizadas para analisar e criar propostas para cada negócio. O Dynamics 365 Project Operations utiliza algumas das seguintes funcionalidades que são utilizadas num processo de venda:

- Um registo de uma Oportunidade Potencial é utilizado para monitorizar o processo de vendas.
- As oportunidades potenciais qualificadas são monitorizadas como oportunidades.
- Todos os artefactos relacionados para uma oportunidade são acessíveis. Estes artefactos incluem a equipa de vendas, os intervenientes, a rentabilidade, a classificação, as fases de vendas e os processos de negócio.
- São criadas várias propostas para uma oportunidade.
- Uma proposta é marcada como **Fechada como ganha** para criar uma ordem de venda. Nas Operações do projeto, a ordem de venda é personalizada e chamada de contrato do projeto.

## <a name="estimate-a-sale"></a>Estimar uma venda
O valor de uma venda pode ser estimado com base em projetos que tenham sido fornecidos anteriormente e na complexidade dos projetos. No caso dos projetos que envolvem extensões para os projetos anteriores, ou os projetos em que a experiência do fornecedor é alta e os modelos de trabalho conhecidos são utilizados, pode utilizar um processo de estimativa mais simples. Normalmente, os projetos mais complexos têm um processo de compra maior. Consequentemente, existem mais fases no processo de estimativa de vendas. No início do processo, a equipa de vendas utiliza a introdução de gestores de contas e especialistas no assunto (SMEs) para criar uma estimativa de alto nível para cada componente distinto do trabalho que é proposto. Estes componentes de trabalho são representados por linhas de proposta. 

Pode criar uma estimativa de alto nível da proposta. Eventualmente, esta estimativa de alto nível será substituída por uma estimativa mais detalhada baseada num plano do projeto criado através da utilização dos modelos de projeto padrão. Estes modelos ajudam-no a criar uma agenda e a determinar os valores monetários na proposta e nos respetivos componentes (linhas de proposta). 

É possível criar várias propostas para um projeto e agrupá-las sob um único registo de Oportunidade. Eventualmente, uma das propostas é marcada **Fechada como Ganha** e é criado um contrato do projeto ou uma declaração de trabalho (SOW). Um contrato do projeto contém o valor contratado de cada componente (item de contrato) que é aceite pelo cliente para entrega. Normalmente, uma SOW é criada como um documento Microsoft Word. Todas as faturas enviadas ao cliente ao longo da entrega do projeto fazem referência ao contrato do projeto ou à SOW.

Também pode criar propostas alternativas sob um registo de Oportunidade ou configurar o sistema para que um contrato do projeto seja criado quando uma proposta for ganha. Neste caso, pode anexar um documento do Word que representa a SOW ao registo de contrato do projeto.

## <a name="configure-the-sales-process"></a>Configurar o processo de vendas
Pode utilizar fluxos do processo de negócio para configurar o processo de vendas. Estes fluxos fornecem uma interface visual guiada para avançar com as fases do processo de venda.

Por exemplo, a sua empresa poderá ter as seis fases seguintes no processo de vendas:

1. Qualificar
2. Estimativa
3. Revisão interna
4. Contrato
5. Entregar
6. Fechar
 
A sua organização poderá utilizar entidades diferentes para representar o mesmo negócio à medida que evoluir. No início do processo de vendas, um negócio é representado pela entidade Oportunidade. À medida que o tempo passa e surgem mais detalhes, poderá utilizar estimativas de alto nível para criar uma ou mais propostas. Se uma destas propostas for revista por intervenientes internos e dos clientes, a entidade Proposta representa o negócio. Depois de o cliente aceitar a proposta, um contrato do projeto ou uma SOW representa o negócio. Para suportar este comportamento, os BPFs são estruturados de modo a que cada fase no processo esteja associada a uma tabela de base de dados diferente.

A fase **Qualificar** no processo de vendas pode ser apoiada por uma entidade Oportunidade. As fases **Estimativa** e **Revisão Interna** podem ser apoiadas por uma entidade Proposta. As fases **Contrato**, **Entrega** e **Fechar** podem ser apoiadas por uma entidade Contrato do Projeto.

À medida que os negócios avançam pelas fases, é-lhe pedido para criar o registo de entidade apropriado para o ajudar e orientar ao longo do processo. As fases podem ser condicionais. Por exemplo, se necessitar de uma revisão interna de uma proposta apenas se a proposta utilizar uma lista de preços personalizada, poderá configurar essa condição na fase apropriada do processo de negócio. A fase **Revisão Interna** é mostrada apenas para as propostas que utilizam uma lista de preços personalizada. Para todos os outros negócios e propostas, a fase **Estimativa** é seguida pela fase **Contrato**.

> [!NOTE]
> As Operações do projeto têm páginas específicas para registos de oportunidades, propostas, encomendas e entidades de fatura. Tem de criar estes registos utilizando as páginas de informação do projeto para estas entidades. Caso contrário, não poderá abrir os registos a partir da página de **informações do Projeto**. Se pretender abrir um registo a partir da página de **informações do projeto**, deve apagar o registo e recriá-lo utilizando a página de **informações do projeto**, onde a lógica de negócio para cada um destes tipos de entidades garante que o campo **Tipo** do registo é definido corretamente, e todos os conceitos obrigatórios são devidamente iniciados.


## <a name="track-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Monitorizar revisões de propostas e planos do projeto no ciclo de vendas
Nas Operações do projeto, não é possível monitorizar as revisões efetuadas numa proposta. Em vez disso, tem de marcar a proposta existente **Fechada como Perdida** e, em seguida, criar uma nova proposta. Pode copiar uma proposta ou clonar uma proposta baseada em projetos utilizando.

## <a name="track-comments-and-approvals-of-quotes-and-project-contracts"></a>Monitorizar comentários e aprovações de propostas e contratos do projeto
Pode gerir a revisão e aprovação de propostas e contratos do projeto utilizando a mural de registo e as publicações. A sua organização pode criar fluxos de trabalho e suplementos personalizados para atribuir, redirecionar, escalar e gerir notificações de itens de trabalho de revisão e aprovação.


[!INCLUDE[footer-include](../includes/footer-banner.md)]