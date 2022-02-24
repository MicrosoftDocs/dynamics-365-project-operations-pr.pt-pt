---
title: Definição de preços do catálogo de produtos
description: Este tópico fornece informações sobre a forma como a definição de preços do catálogo de preços funciona no Dynamics 365 Project Service Automation (PSA).
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
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
ms.openlocfilehash: 3fb9b51d58cbe3b0db6dad902461b90ac04cc42f
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151222"
---
# <a name="product-catalog-pricing"></a>Definição de preços do catálogo de produtos 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


As listas de preços e as entidades de itens da lista de preços oferecem suporte à definição de preços do catálogo de produtos. Na maioria das vezes, esta funcionalidade é utilizada para linhas baseadas no catálogo em propostas e contratos de projetos.

Para linhas baseadas em projetos, um contrato representa o negócio depois de ser ganho. Como o processo de negociação geralmente precede o ganho, o preço anexado à proposta é sempre copiado como está para uma nova lista de preços e anexado ao contrato. Esta nova lista de preços não pode ser alterada fora do âmbito do contrato. Esta limitação ajuda a proteger o cartão de taxas negociado face a quaisquer alterações de preço que ocorram na lista de preços principal.

Os produtos devem ser configurados de modo a que tenham listas de custos e preços predefinidas no catálogo de produtos. Deve utilizar o preço de lista, o custo padrão e o custo atual para configurar o custo predefinido e os preços de lista. Os preços de lista predefinidos são utilizados numa linha de proposta ou num item de contrato do projeto apenas quando o sistema não consegue localizar uma linha da lista de preços para esse produto na lista de preços do produto para a proposta ou o contrato do projeto.

O preço de custo das linhas do catálogo de produtos pode ser alterado entre aspas. Esta capacidade é importante, porque se não monitorizar com precisão os custos, não poderá determinar os lucros operacionais das cativações de projetos. Por predefinição, o custo padrão do produto é utilizado como o preço de custo. No entanto, o preço de custo predefinido pode ser atualizado na linha de proposta se existir um preço de custo diferente para essa proposta.

## <a name="price-list-items"></a>Itens da lista de preços

Pode adicionar produtos de um catálogo de produtos a listas de preços diferentes. As linhas da lista de preços para produtos referenciam sempre uma unidade específica. Os preços de um produto nos itens da lista de preços podem ser configurados como um montante de moeda. Em alternativa, pode ser configurado como uma função do preço de lista, custo atual ou custo padrão.

O PSA suporta várias opções de arredondamento quando os preços são configurados como uma função do preço de lista, custo padrão ou custo atual. Além de tirar partido de vários métodos de definição de preços e opções de arredondamento, pode associar listas de descontos aos itens da lista de preços. 

> ![Adicionar produtos de um catálogo a listas de preços diferentes](media/basic-guide-16.png)

Quando cria uma nova lista de preços personalizada para uma proposta selecionando **Criar Lista de Preços Personalizada** na página **Proposta do Projeto**, o PSA faz uma cópia da lista de preços e o campo **Entidade** no cabeçalho da nova lista de preços é definido como **Entidade de Vendas**. O nome da nova lista de preços é anexado ao nome da proposta e um carimbo de data/hora. Também pode utilizar o nome da nova lista de preços e o nome da proposta em fluxos de trabalho personalizados para acionar a análise e as aprovações adicionais para as propostas que utilizam preços personalizados.

 
## <a name="default-product-price-list"></a>Lista de preços do produto predefinida
Cada registo de cliente tem um campo **Lista de Preços Predefinida**, onde pode especificar uma lista de preços que corresponda à moeda do cliente. No PSA, um valor predefinido não é introduzido automaticamente neste campo. Quando existe um contrato de preços personalizado com um cliente específico, pode utilizar este campo para associar uma lista de preços a esse cliente.

As entidades Oportunidade, Proposta e Contrato do Projeto utilizam a seguinte ordem para introduzir listas de preços de produtos predefinidas. A mesma ordem é utilizada para as listas de preços do projeto.

1.  Proposta
2.  Oportunidade
3.  Cliente
4.  Definições globais para PSA

Por predefinição, o campo **Produto** na linha de proposta lista todos os produtos ativos na lista de preços do produto da proposta. Se um produto tiver sido inativado, ou se for um produto de rascunho, o mesmo não está listado, mesmo que esteja na lista de preços. 

As linhas do catálogo de produtos são adicionadas como linhas de fatura na primeira fatura que é criada para um contrato do projeto. Numa fatura de rascunho, essas linhas de fatura podem ser eliminadas. Neste caso, as linhas serão apresentadas numa fatura subsequente até serem faturadas, ou até a fatura ser enviada para o cliente. No PSA, não é possível faturar uma quantidade parcial de uma linha de fatura do produto. Quando as linhas de produto do contrato do projeto são faturadas, os valores reais são criados. No entanto, esses valores reais não estão associados à entidade do projeto relacionada. Por outras palavras, os itens de contrato do projeto baseados em produtos são independentes de qualquer utilização baseada no projeto. O PSA não monitoriza o consumo de material nos projetos.
