---
title: Descrição geral das dimensões de preços
description: Este tópico fornece informações sobre as dimensões de preços no Dynamics 365 Project Operations.
author: rumant
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 4b3b71c0b64a24f6914c70c4383eee654e7d4947ececaf9b4e6394f45a081a4c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001985"
---
# <a name="pricing-dimensions-overview"></a>Descrição geral das dimensões de preços

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

As dimensões utilizadas nos recursos humanos para definir preços e custos enquadram-se em duas categorias:

- Pessoas
- Trabalho planeado

Por esse motivo, existem dois tipos de valores de dimensão de definição de preços disponíveis:

- **Conjuntos de opções**: Dimensões que são enumerações fixas para um conjunto de valores.
- **Valores baseados em entidades**: Dimensões que podem ser um conjunto de valores variado.

## <a name="pricing-dimensions"></a>Dimensões de preços

O Dynamics 365 Project Operations é fornecido com um conjunto predefinido de dimensões de preços. Pode visualizar estas dimensões de preços ao aceder a **Operações do projeto** > **Parâmetros**. No registo de parâmetro, no separador **Dimensões de definição de preços baseadas em montantes**, verifique se a função, **msdyn_resourcecategory** e a unidade organizacional de atribuição de recursos, **msdyn_organizationalunit** têm os campos **Aplicável às vendas** e **Aplicável ao custo** definidos como **Sim**. Com estes campos ativados, pode configurar o preço e o custo de cada combinação de função e unidade organizacional.

![Captura de ecrã dos parâmetros do Project Service com "Aplicável às Vendas" destacado.](media/PS-OOB-parameters.png)

Se precisar de definir o preço ou o custo dos seus recursos utilizando atributos adicionais, poderá criar campos, entidades e dimensões personalizados. Para obter mais informações, consulte os seguintes tópicos. 
  
  > [!NOTE]
  > Os procedimentos têm de ser concluídos na ordem em que estão listados.

1. [Criar uma solução para dimensões de preços personalizadas](../sales/create-solution-custompd.md)
2. [Criar campos e entidades personalizados](create-custom-fields-entities-pricing-dimensions.md)
3. [Adicionar campos personalizados às entidades de configuração de preços e transacionais](add-custom-fields-price-setup-transactional-entities.md)
4. [Configurar campos personalizados como dimensões de definição de preços](set-up-custom-fields-pricing-dimensions.md)
5. [Atualizar atributos de plug-in para incluir novas dimensões de definição de preços](update-plugin-attributes-pd.md)


## <a name="pricing-human-resource-time"></a>Definir preço do tempo dos recursos humanos
A forma como uma organização define o preço do tempo de um recurso humano é, normalmente, uma consideração estratégica importante que afeta diretamente a rentabilidade da organização. Trabalhe com as equipas de finanças e pratique os chefes quando a sua organização estiver pronta para identificar como pretende definir taxas de faturação e custo para o tempo de recursos humanos.

As outras considerações para definição de preços incluem a reutilização de campos ou entidades que, no momento, não são dimensões de definição de preços, mas que se aplicam como uma dimensão de definição de preços para a sua organização. Campos como **Categoria de Transação** (**msdyn_transactioncategory**) e **Recurso Reservável** (**bookableresource**) são exemplos de dimensões candidatas. 

Considere se a dimensão de definição de preços deve ser uma tabela ou um conjunto de opções. Se prever alterações nos valores de uma dimensão que excederão 10 ou 12 e necessitar de atributos adicionais nestes valores, poderá criar uma entidade em vez de um conjunto de opções. A manutenção de um conjunto de opções, como a adição ou a remoção de valores, requer um administrador ou programador, ao passo que a adição de novas linhas a uma tabela pode ser efetuada pela maior parte dos utilizadores.

O exemplo que se segue mostra taxas de faturação que são configuradas com base na função e na unidade organizacional de atribuição de recursos à qual o recurso pertence. Normalmente, as taxas de custo baseiam-se na faixa salarial do funcionário e na unidade organizacional à qual pertencem. Neste exemplo, as tabelas de taxas de faturação e taxas de custo terão o seguinte aspeto:

**Taxas de faturação de exemplo**

| Função        | Unidade Organizacional    |Unidade      |Preço      |Moeda  |
| ------------|-------------|----------|----------:|----------|
| Programador   | Contoso E.U.A.  |Hora | 200|USD     |
| Programador   | Contoso India |Hora|   112|USD     |


**Exemplo de taxas de custo**

| Faixa salarial     | Unidade Organizacional    |Unidade      |Preço      |Moeda  |
| ----------------|-------------|----------|----------:|----------|
| A minha empresa_Faixa 1 | Contoso E.U.A.  |Hora | 145|USD     |
| A minha empresa_Faixa 2 | Contoso India |Hora|   67|USD     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]