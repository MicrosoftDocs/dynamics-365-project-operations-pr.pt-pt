---
title: Unidades organizacionais avançadas
description: Este artigo fornece informações sobre unidades organizacionais no Dynamics 365 Project Service Automation.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/04/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: dd9de490b7d6d847e3226b371e06ac671a7836a8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927112"
---
# <a name="about-organizational-units"></a>Sobre unidades organizacionais 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

O Dynamics 365 Project Service Automation, uma unidade organizacional é um grupo ou uma divisão distinta numa empresa de serviços profissionais que emprega recursos faturáveis que têm taxas de custo.

Para empresas de serviços profissionais que empregam recursos técnicos em várias áreas de prática ou linhas de negócios, o custo para desempenhar uma função numa área de prática ou linha de negócios pode diferir do custo para desempenhar uma função em outra área de prática ou linha de negócios. As unidades organizacionais de conceito ajudam neste cenário fornecendo uma forma de agrupar um conjunto de funções faturáveis numa divisão de uma empresa que tenha uma estrutura de custo distinta para estas funções.

## <a name="key-attributes-and-associations-of-organizational-units"></a>Atributos de chave e associações de unidades organizacionais

No PSA, uma unidade organizacional no PSA tem uma moeda específica e listas de preços de custo específicas.

A moeda de uma unidade organizacional é a moeda primária que é utilizada para monitorizar os custos.

É possível anexar uma ou mais listas de preços de custo a cada unidade organizacional. O PSA coloca as seguintes limitações nas listas de preços que podem ser associadas a uma unidade organizacional:

- As listas de preços têm de estar na moeda da unidade organizacional
- As listas de preços têm de ser listas de preços de custo

Além disso, existe um atributo para a unidade organizacional na entidade Recurso. Cada recurso só pode ser atribuído a uma unidade organizacional.

## <a name="roles-of-organizational-units"></a>Funções das unidades organizacionais

A unidade organizacional desempenha duas funções no PSA:

- **Unidade de contratação** – A unidade organizacional que representa o grupo ou a divisão da empresa, responsável principalmente pela vitória da venda e gestão da entrega de trabalho e serviços ao cliente. A unidade de contratação é identificada pelo campo **Unidade de Contratação** na secção do cabeçalho das páginas **Oportunidade**, **Proposta**, **Contrato do Projeto** e **Projeto**.
- **Unidade de atribuição de recursos** – A unidade organizacional a que um recurso pertence ou é atribuído. Esta unidade organizacional pode fornecer os seus recursos para algumas funções em declarações de trabalho (SOWs) e projetos que são propriedade da unidade de contratação.

> ![Unidades de contratação e unidades de atribuição de recursos.](media/advanced-1.png)

## <a name="organizational-unit-faqs"></a>FAQs sobre unidades organizacionais

Seguem-se algumas respostas às perguntas mais frequentes sobre as unidades organizacionais.

### <a name="how-is-the-organizational-unit-entity-in-psa-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Como está a entidade Unidade Organizacional no PSA relacionada com a entidade Organização que já existe no Dynamics 365?

A entidade Organização no Microsoft Dynamics 365 representa o nome de uma instância global do Dynamics 365. Este nome é, normalmente, o nome da empresa global.

A entidade Unidade Organizacional representa um grupo ou uma divisão na empresa global. Este grupo ou divisão tem um conjunto de funções e uma lista de preços de custo para essas funções, sendo que essas funções e a lista de preços diferem das funções e da lista de preços de outros grupos ou divisões na empresa.

Quando o PSA é instalado, é criada uma unidade organizacional predefinida baseada na organização. Todos os recursos existentes são atribuídos à unidade organizacional predefinida. Se novos utilizadores ou recursos do Active Directory forem importados para o Dynamics 365, o processo de importação de utilizadores atribui os mesmos à unidade organizacional predefinida do PSA.
 
### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Como é que a entidade Unidade Organizacional difere da entidade Unidade de Negócio?

No Dynamics 365, a entidade Unidade de Negócio é uma construção de segurança. A associação de um utilizador a uma unidade de negócio determina as entidades e os registos de entidade aos quais o utilizador tem acesso. Também determina as permissões (Criar, Ler, Escrever, Eliminar, Anexar, Anexar a, Atribuir ou Partilhar) que o utilizador tem para esses registos de entidade.

A entidade Unidade Organizacional representa um grupo ou uma divisão da empresa que tem taxas de custo diferentes para os funcionários que estão atribuídos. A associação de um recurso a uma unidade organizacional determina o custo do recurso para uma cativação do projeto.

Quando implementa o Dynamics 365, otimize a autorização de segurança para a hierarquia de unidades de negócio e a atribuição de utilizadores a unidades de negócio. Atribua todos os utilizadores que, normalmente, têm de aceder ao mesmo conjunto de registos à mesma unidade de negócio. A unidade organizacional não tem efeito sobre o acesso ou autorização de segurança.

#### <a name="example-of-organizational-units-and-business-units"></a>Exemplo de unidades organizacionais e unidades de negócio

A Contoso, Ltd. possui uma próspera prática de tecnologia da Microsoft. Gonçalo e Carla são ambos programadores C\#, mas Carla está nos Estados Unidos, enquanto Gonçalo está na Índia. A maioria das cativações de projetos exige recursos da Contoso India e da Contoso US, e Gonçalo e Carla exigem o mesmo nível de acesso de segurança aos projetos nesta área de prática. No entanto, o custo dos programadores da Contoso India difere significativamente do custo dos programadores da Contoso US.

Segue-se uma forma ideal de estruturar este cenário utilizando o Dynamics 365 e o PSA.

1. Crie a prática de tecnologia da Microsoft como uma unidade de negócio e associe Gonçalo e Carla à mesma. Deste modo, o utilizador ajuda a garantir que ambos os empregados tenham o mesmo nível de acesso de segurança a quaisquer projetos nessa área de prática. Ambos poderão verificar o progresso e reportar o tempo, as despesas e as atualizações de tarefas. 
2. Crie duas unidades organizacionais para ajudar a garantir que o custo do projeto seja refletido corretamente. 
3. Associe o Carla à Contoso US e associe Gonçalo à Contoso India.
4. Atribua listas de preços de custo adequadas a ambas as unidades organizacionais. Desta forma, ajuda a garantir que os custos registados no projeto para Gonçalo e Carla reflitam com precisão a diferença de custos entre a Contoso US e a Contoso India.

### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>As unidades organizacionais estão relacionadas com as regiões de vendas no Dynamics 365?

Não há associação ou relação entre as regiões de vendas e as unidades organizacionais. Normalmente, uma região de vendas é uma área geográfica na qual ocorrem as vendas. É possível associar uma lista de preços de vendas a cada região de vendas.

Uma unidade organizacional é um grupo interno ou uma divisão na empresa que monitoriza os custos de um conjunto de funções que vendem a outras divisões ou a clientes externos.

#### <a name="example-of-organizational-units-and-sales-territories"></a>Exemplo de unidades organizacionais e regiões de vendas

A Contoso, Ltd. possui dois centros de desenvolvimento: Contoso US e Contoso India. Os custos dos recursos diferem muito entre estes dois centros de desenvolvimento.

A Contoso vende os seus serviços de TI em muitos mercados internacionais, tais como América Latina, América do Norte, Ásia-Pacífico, Europa Ocidental e o Médio Oriente. As taxas de faturação para as mesmas funções do projeto podem variar amplamente em todos os mercados.

A Contoso US e a Contoso India devem ser configuradas como unidades organizacionais e cada unidade organizacional deve ter a sua própria lista de preços de custo. Ásia-Pacífico, América Latina, América do Norte, Europa Ocidental e Médio Oriente devem ser configurados como regiões de vendas, e cada região de vendas deve ter a sua própria lista de preços de vendas.

### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Por que existe uma restrição na associação de listas de preços às unidades organizacionais? 

Normalmente, os preços de vendas são exclusivos das áreas geográficas ou mercados onde os serviços são vendidos. Normalmente, as divisões internas de uma empresa não têm seus próprios preços de vendas para o mesmo tipo de serviços. No entanto, as divisões internas têm um custo diferente dos produtos vendidos (COGS), dependendo das competências das pessoas que empregam e das condições de trabalho da região onde operam. Como as unidades organizacionais são modeladas como divisões internas de uma empresa, podem ter apenas listas de preços de custo.

### <a name="why-cant-we-associate-sales-price-lists-to-organizational-units"></a>Por que não podemos associar listas de preços de vendas a unidades organizacionais?

No PSA, as listas de preços de vendas podem ser associadas a clientes e regiões de vendas. As entidades transacionais como Oportunidade, Proposta, Contrato do Projeto e Projeto utilizam listas de preços de vendas anexadas à conta do cliente ou à região de vendas para determinar taxas de faturação e receitas potenciais na cativação do projeto.

As listas de preços de custo estão associadas a unidades organizacionais. As entidades transacionais como Oportunidade, Proposta, Contrato do Projeto e Projeto utilizam listas de preços de custo anexadas à unidade de contratação para determinar os custos de uma cativação do projeto.

### <a name="are-organizational-units-hierarchical-in-psa"></a>As unidades organizacionais são hierárquicas no PSA?

Não. Na versão atual do PSA, as unidades organizacionais não são hierárquicas. Isto significa que não é possível:

- Configurar um padrão para predefinir os preços de custo que atravessam uma hierarquia. 
- Reportar as receitas ou os custos acumulados em diferentes níveis da hierarquia de unidades organizacionais.

### <a name="were-a-big-multinational-firm-with-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-make-the-best-use-of-the-organizational-unit-concept-in-this-version-of-the-project-service-app"></a>Somos uma grande empresa multinacional com uma hierarquia complexa e multinível de centros de custos, divisões e escritórios de faturação. Como podemos fazer a melhor utilização do conceito da unidade organizacional nesta versão da aplicação Project Service?

Quando tem uma hierarquia complexa de centros de custos, divisões, escritórios de faturação, etc., configure os nós de folha dessa hierarquia como unidades organizacionais distintas.
O exemplo que se segue mostra uma hierarquia típica:

**Contoso India**

  - Prática SAP 

    - Consultores Técnicos 
    - Consultores Funcionais 
    
  - Prática de Tecnologia da Microsoft 

    - Consultores Técnicos
    - Consultores Funcionais 
    
**Contoso EUA**

 - Prática SAP 

    - Consultores Técnicos 
    - Consultores Funcionais 
    
 - Prática de Tecnologia da Microsoft 

    - Consultores Técnicos 
    - Consultores Funcionais 
 
Se a hierarquia for semelhante, terá de a configurar como uma lista simples, tal como é mostrado aqui:
- Contoso India - Prática SAP - Consultores Técnicos 
- Contoso India - Prática SAP - Consultores Funcionais       
- Contoso India - Prática de Tecnologia da Microsoft - Consultores Funcionais 
- Contoso India - Prática de Tecnologia da Microsoft - Consultores Funcionais 
- Contoso US - Prática SAP - Consultores Técnicos  
- Contoso US - Prática SAP - Consultores Funcionais  
- Contoso US - Prática de Tecnologia da Microsoft - Consultores Técnicos 
- Contoso US - Prática de Tecnologia da Microsoft - Consultores Funcionais

### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-organizational-unit-concept-in-the-current-version-of-psa"></a>Somos uma pequena empresa de serviços profissionais que opera como apenas uma divisão. Como podemos utilizar melhor o conceito da unidade organizacional na versão atual do PSA?

Se a sua empresa operar como uma unidade com uma lista de preços de custo, não terá de configurar unidades organizacionais. Durante a instalação do PSA, o Dynamics 365 cria uma unidade organizacional predefinida que tem o mesmo nome que a organização. Por predefinição, todos os utilizadores são atribuídos a esta unidade organizacional. Sempre que o sistema necessitar que uma unidade organizacional seja selecionada, esta unidade organizacional é selecionada por predefinição.

### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract-what-is-the-default-contracting-unit"></a>Quando um projeto é criado a partir de uma proposta ou de um item de contrato do projeto, a unidade de contrato predefinida provém da proposta ou do contrato do projeto. Se for criado um projeto antes das entidades de vendas, tais como a proposta ou o contrato do projeto, qual é a unidade de contratação predefinida?

Quando um projeto é criado sozinho, a unidade de contratação predefinida do projeto baseia-se no utilizador que o cria. Esse utilizador também é o gestor de projeto predefinido. Se o projeto estiver mapeado para uma entidade de vendas, tal como uma proposta ou um contrato do projeto, a unidade de contratação do projeto será baseada na entidade de vendas. Neste caso, as estimativas do projeto poderão ser recalculadas porque a lista de preços de custo é utilizada para calcular as alterações de estimativa de custos se a unidade de contratação for alterada. A lista de preços de vendas é utilizada para calcular as estimativas de vendas que serão alteradas de modo a serem sincronizadas com a lista de preços do projeto na proposta.

Os campos **Unidade de Contratação** e **Moeda** no projeto estão bloqueados para edição, porque têm de estar em sincronização com os valores na entidade de vendas (proposta ou contrato do projeto) para a qual o projeto está mapeado.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
