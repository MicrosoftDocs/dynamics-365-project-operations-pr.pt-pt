---
title: Home page de dimensões de definição de preços e custos
description: Este artigo fornece uma descrição geral das dimensões de preços.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 88c77d90bccaa5f10e8f75d60ae121d699bc0976
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925456"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Home page de dimensões de definição de preços e custos

[!include [banner](../includes/psa-now-project-operations.md)]

As dimensões utilizadas para definir os preços do trabalho e os custos em organizações baseadas em projetos são influenciadas pelos seguintes atributos:

- Pessoas com trabalho semelhante à sua experiência, função ou geografia
- Trabalho a realizar semelhante à sua complexidade ou hora do dia

Dada a natureza típica destes attrubutes do trabalho e das pessoas necessárias para realizar o trabalho, existem dois tipos de valores de dimensão de preços disponíveis no Project Service Automation: 

- **Conjuntos de opções** – atributos que são enumerações fixas para um conjunto de valores.
- **Valores baseados em entidades** – atributos que podem ter um conjunto de valores variado que são finitos mas podem mudar ao longo do tempo.

## <a name="pricing-dimensions"></a>Dimensões de preços

O PSA é fornecido com um conjunto predefinido de dimensões de definição de preços. Pode visualizá-lo acedendo a **Project Service** > **Parâmetros**. No registo de parâmetro, no separador **Dimensões de definição de preços baseadas em montantes**, verifique se a função, **msdyn_resourcecategory** e a unidade organizacional de atribuição de recursos, **msdyn_organizationalunit** têm os campos **Aplicável às vendas** e **Aplicável ao custo** definidos como **Sim**. Isto irá permitir-lhe configurar o preço e o custo de cada combinação de função e unidade organizacional.

![Captura de ecrã dos parâmetros do Project Service com "Aplicável às Vendas" destacado.](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> Se tiver utilizado os campos de função e unidade organizacional fornecidos com o programa como dimensões de definição de preços anteriores à versão 3 do PSA, não haverá nenhuma alteração observável. Pode continuar a utilizar o Project Service normalmente. 

Se precisar de definir o preço ou o custo dos seus recursos utilizando atributos adicionais, poderá criar campos, entidades e dimensões personalizados. Para mais informações, consulte os seguintes artigos, no entanto, note que tem de concluir os procedimentos na ordem listada abaixo:

- [Criar campos e entidades personalizados](create-custom-fields-entities.md)
- [Adicionar campos personalizados às entidades de configuração de preços e transacionais](field-references.md)
- [Configurar campos personalizados como dimensões de definição de preços](set-up-pricing-dimensions.md)
- [Atualizar atributos de plug-in para incluir novas dimensões de definição de preços](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>Definir preço do tempo dos recursos humanos
A forma como uma organização define o preço do tempo de um recurso humano é, normalmente, uma consideração estratégica importante que afeta diretamente a rentabilidade da organização. Trabalhe com as equipas de finanças e pratique os chefes quando a sua organização estiver pronta para identificar como pretende definir taxas de faturação e custo para o tempo de recursos humanos.

As outras considerações para definição de preços incluem a reutilização de campos ou entidades que, no momento, não são dimensões de definição de preços, mas que se aplicam como uma dimensão de definição de preços para a sua organização. Campos como **Categoria de Transação** (**msdyn_transactioncategory**) e **Recurso Reservável** (**bookableresource**) são exemplos de dimensões candidatas. 

Considere se a dimensão de definição de preços deve ser uma tabela ou um conjunto de opções. Se prever alterações nos valores de uma dimensão que excederão 10 ou 12 e necessitar de atributos adicionais nestes valores, criar uma entidade em vez de um conjunto de opções. A manutenção de um conjunto de opções, como a adição ou a remoção de valores, requer um administrador ou programador, ao passo que a adição de novas linhas a uma tabela pode ser efetuada pela maior parte dos utilizadores empresariais.

O exemplo que se segue mostra taxas de faturação que são configuradas com base na função e na unidade organizacional de atribuição de recursos à qual o recurso pertence. Normalmente, as taxas de custo baseiam-se na faixa salarial do funcionário e na unidade organizacional à qual pertencem. Neste exemplo, as tabelas de taxas de faturação e taxas de custo terão o seguinte aspeto:

**Taxas de faturação de exemplo**

| Função        | Unidade Organizacional    |Unidade      |Preço      |Moeda  |
| ------------|-------------|----------|----------:|----------|
| Programador   | Contoso EUA  |Hour | 200|USD     |
| Programador   | Contoso India |Hour|   112|USD     |


**Exemplo de taxas de custo**

| Faixa salarial     | Unidade Organizacional    |Unidade      |Preço      |Moeda  |
| ----------------|-------------|----------|----------:|----------|
| A minha empresa_Faixa 1 | Contoso EUA  |Hour | 145|USD     |
| A minha empresa_Faixa 2 | Contoso India |Hour|   67|USD     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
