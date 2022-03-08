---
title: Processos de vendas
description: Este tópico fornece informações sobre os processos de vendas básicos.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 58d5aa68dd5af7fc2b39caac429948e55bbc94c39dfb7fc9ae15a37cc3c92ce6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000545"
---
# <a name="sales-processes"></a>Processos de vendas

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Os processos de vendas utilizados numa organização baseada em projetos diferem dos processos de vendas utilizados numa organização baseada em produtos. Esta diferença ocorre porque os ciclos de vendas para as organizações baseadas em projetos são mais demorados e necessitam de técnicas de estimativa personalizadas para analisar e criar propostas para cada negócio. O Dynamics 365 Project Service Automation utiliza algumas das mesmas funcionalidades utilizadas no processo de vendas do Dynamics 365 Sales. Seguem-se alguns exemplos:

- Uma entidade Oportunidade Potencial é utilizada para monitorizar o processo de vendas.
- As oportunidades potenciais qualificadas são monitorizadas como oportunidades. O processo de vendas também pode começar com a oportunidade.
- Todos os artefactos relacionados para uma oportunidade são acedidos. Estes artefactos incluem a equipa de vendas, os intervenientes, a rentabilidade, a classificação, as fases de vendas e os processos de negócio.
- São criadas várias propostas para uma oportunidade.
- Uma proposta é marcada **Fechada como ganha** para criar uma ordem de venda. No PSA, a ordem de venda é personalizada e é chamada de contrato do projeto.

A ilustração seguinte mostra um processo de vendas típico numa organização baseada em projetos.

> ![Processo de vendas numa organização baseada em projetos.](media/basic-guide-1.png)

## <a name="estimating-a-sale"></a>Estimar uma venda
O valor de uma venda pode ser estimado com base em projetos que tenham sido fornecidos anteriormente e na complexidade dos projetos. No caso dos projetos que envolvem extensões para os projetos anteriores, ou os projetos em que a experiência do fornecedor é alta e os modelos de trabalho conhecidos são utilizados, pode utilizar um processo de estimativa mais simples. Normalmente, os projetos mais complexos têm um processo de compra maior. Consequentemente, existem mais fases no processo de estimativa de vendas. No início do processo, a equipa de vendas utiliza a introdução de gestores de contas e especialistas no assunto (SMEs) para começar a criar uma estimativa de alto nível para cada componente distinto do trabalho que é proposto. Estes componentes de trabalho são representados por linhas de proposta. 

Pode criar uma estimativa de alto nível da proposta. Eventualmente, esta estimativa de alto nível será substituída por uma estimativa mais detalhada baseada num plano do projeto criado através da utilização dos modelos de projeto padrão. Estes modelos ajudam-no a criar uma agenda e a determinar os valores monetários na proposta e nos respetivos componentes (linhas de proposta). 

É possível criar várias propostas para um projeto e agrupá-las sob um único tipo de entidade Oportunidade. Eventualmente, uma dessas propostas é marcada **Fechada como Ganha** e é criado um contrato do projeto ou uma declaração de trabalho (SOW). Um contrato do projeto contém o valor contratado de cada componente (item de contrato) que é aceite pelo cliente para entrega. Normalmente, uma SOW é criada como um documento Microsoft Word. Todas as faturas enviadas ao cliente ao longo da entrega do projeto fazem referência ao contrato do projeto ou à SOW.

Também pode criar propostas alternativas sob um tipo de entidade Oportunidade ou configurar o sistema para que um contrato do projeto seja criado quando uma proposta for ganha. Neste caso, pode anexar um documento do Word que representa a SOW ao registo de contrato do projeto.

![Fechar uma proposta para criar um contrato do projeto.](media/basic-guide-2.png)

## <a name="configuring-the-sales-process"></a>Configurar o processo de vendas
Pode utilizar fluxos do processo de negócio (BPFs) no Microsoft Dynamics 365 para configurar o processo de vendas. Os BPFs fornecem ao pessoal de vendas uma interface visual assistida que pode ser utilizada para mover os negócios pelas fases típicas para a sua empresa.

Por exemplo, a sua empresa poderá ter as seis fases seguintes no processo de vendas:

1. Qualificar
2. Estimativa
3. Revisão interna
4. Contrato
5. Entregar
6. Fechar

Estas seis fases são representadas por divisas (\>) que seleciona para expandir em cada tipo de entidade Oportunidade que criar.

![Configuração do processo de negócio no Dynamics 365.](media/basic-guide-3.png)
 
A sua organização poderá utilizar entidades diferentes para representar o mesmo negócio à medida que evoluir. No início do processo de vendas, um negócio é representado pela entidade Oportunidade. À medida que o tempo passa e surgem mais detalhes, poderá utilizar estimativas de alto nível para criar uma ou mais propostas. Se uma destas propostas for revista por intervenientes internos e dos clientes, a entidade Proposta representa o negócio. Depois de o cliente aceitar a proposta, um contrato do projeto ou uma SOW representa o negócio. Para suportar este comportamento, os BPFs são estruturados de modo a que cada fase no processo esteja associada a uma tabela de base de dados diferente.

A fase **Qualificar** no processo de vendas pode ser apoiada por uma entidade Oportunidade. As fases **Estimativa** e **Revisão Interna** podem ser apoiadas por uma entidade Proposta. As fases **Contrato**, **Entrega** e **Fechar** podem ser apoiadas por uma entidade Contrato do Projeto.

À medida que os negócios avançam pelas fases, é-lhe pedido para criar o registo de entidade apropriado para o ajudar e orientar ao longo do processo. As fases podem ser condicionais. Por exemplo, se necessitar de uma revisão interna de uma proposta apenas se a proposta utilizar uma lista de preços personalizada, poderá configurar essa condição na fase apropriada do processo de negócio. A fase **Revisão Interna** é mostrada apenas para as propostas que utilizam uma lista de preços personalizada. Para todos os outros negócios e propostas, a fase **Estimativa** é seguida pela fase **Contrato**.

> [!NOTE]
> O PSA tem páginas específicas para as entidades Oportunidade, Proposta, Encomenda e Fatura. Tem de criar oportunidades de serviço do projeto, propostas, encomendas e faturas utilizando as páginas de informação do projeto para estas entidades. Se utilizar outra página para criar um registo, não conseguirá abrir o registo a partir da página **Informações do Projeto**. Se pretender abrir um registo a partir da página **Informações do Projeto**, tem de eliminar o registo e recriá-lo utilizando a página **Informações do Projeto**. Na página **Informações do projeto**, a lógica de negócio para cada um destes tipos de entidade assegura que o campo **Tipo** do registo está definido corretamente e que todos os conceitos obrigatórios são inicializados corretamente.

> ![Informações do projeto para uma nova encomenda.](media/basic-guide-4.png)
 
## <a name="differences-between-project-service-automation-and-sales"></a>Diferenças entre o Project Service Automation e o Sales
Apesar de o processo de vendas no PSA utilizar as capacidades básicas do processo de vendas do Sales, tem algumas diferenças importantes devido às variações nas práticas de negócio das organizações baseadas em projetos. Seguem-se alguns exemplos:

- **Propostas do Projeto** – No Project Service Automation, uma proposta é fechada após um contrato do projeto ser criado a partir de uma proposta. No Sales, pode manter uma proposta aberta depois de a ganhar. A razão para esta diferença deve-se ao facto de uma correspondência entre uma proposta e um contrato do projeto ser melhor para as organizações baseadas em projetos. 
- **Ativação e revisões** – No PSA, a ativação e as revisões não são suportadas para propostas do projeto. No Sales, é possível bloquear uma proposta para impedir edições adicionais.
- **Fechar uma proposta como perdida ou ganha** - No PSA, quando uma proposta do projeto é fechada como ganha ou perdida, a oportunidade permanece aberta. Todas as outras propostas na oportunidade são fechadas como perdidas. No Sales, quando uma proposta é fechada como ganha ou perdida, é-lhe pedido que o utilizador execute uma ação na oportunidade. Consoante a entrada do utilizador, a oportunidade subjacente poderá ser fechada ou deixada aberta.

## <a name="tracking-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Monitorizar revisões de propostas e planos do projeto no ciclo de vendas
No PSA, não é possível monitorizar as revisões efetuadas numa proposta. Em vez disso, tem de marcar a proposta existente **Fechada como Perdida** e, em seguida, criar uma nova proposta. Pode copiar uma proposta ou clonar uma proposta baseada em projetos utilizando o PSA.

## <a name="tracking-comments-and-approvals-of-quotes-and-project-contracts"></a>Monitorizar comentários e aprovações de propostas e contratos do projeto
Pode gerir a revisão e aprovação de propostas e contratos do projeto utilizando a mural de registo e as publicações. A sua organização pode criar fluxos de trabalho e plug-ins personalizados para atribuir, redirecionar, escalar e gerir notificações de itens de trabalho de revisão e aprovação.


[!INCLUDE[footer-include](../includes/footer-banner.md)]