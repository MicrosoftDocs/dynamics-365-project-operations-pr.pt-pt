---
title: Gerir vários clientes em itens de contrato do projeto
description: Este artigo fornece informações sobre a gestão de vários clientes em itens de contrato baseados em projetos.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ec8457fd32a5c215bbc2056b02b2ab3527c4ab1f
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825955"
---
# <a name="manage-multiple-customers-on-project-contract-lines"></a>Gerir vários clientes em itens de contrato do projeto

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

Os itens de contrato baseados em projetos podem incluir uma lista de clientes responsáveis pelo pagamento. Esta lista de clientes no item de contrato baseado no projeto pode ser a mesma que a lista de clientes no contrato, mas isso não é necessário. Quando uma proposta do projeto é ganha e um contrato de projeto é criado, a lista de clientes na linha de proposta é copiada para o item de contrato correspondente. Os clientes na proposta são copiados para o contrato.

Quando o contrato do projeto é faturado, a lista de clientes no item de contrato baseado em projetos tem prioridade sobre a lista de clientes no contrato. A lista de clientes no contrato do projeto só é usada para predefinir novos itens de contrato.

Todos os clientes contratados no separador **Clientes** do contrato de contrato assumem a predefinição como clientes do item de contrato em quaisquer novos itens de contrato criados para o contrato do projeto. Quaisquer itens de contrato existentes não herdarão os novos registos de clientes do contrato criados após eles.

## <a name="create-update-or-delete-a-contract-line-customer-record"></a>Criar, atualizar ou eliminar um registo de cliente do item de contrato

Pode criar, atualizar ou eliminar um cliente do item de contrato a partir do separador Clientes do Item de Contrato na página Item de Contrato baseado no Projeto. Quando um novo cliente é adicionado ao item de contrato baseado no projeto, eles também são adicionados no contrato global como um cliente contratado com uma percentagem de faturação padrão dividida de zero por cento. A percentagem de faturação dividida no contrato global é copiada para novos itens de contrato e para o eventual contrato de projeto. No entanto, ao faturar a partir do contrato, é a percentagem de divisão da faturação ao nível do item de contrato que é usada e não a percentagem de divisão da faturação a nível global do contrato.

Abaixo estão os campos no registo do cliente do item de **Contrato** de um item de contrato baseado em projetos para ter em mente como está a trabalhar com ele:

| Campo | Localização | Descrição | Impacto a jusante |
| --- | --- | --- | --- |
| **Conta** | Grelha editável no separador **Clientes do Contrato** e os formulários **Principal** e **Criação Rápida** para um cliente do contrato. | Todas as contas ativas. Este campo é bloqueado após a criação do registo. Para atualizar o campo, elimine o registo e crie um novo registo. Se registou algum valor real, não pode eliminar o registo. No entanto, pode marcar a percentagem de divisão de faturação como zero para essa conta. Quando o registo é marcado como zero, qualquer custo e receitas futuras que sejam atribuídas ou divididas a este cliente são impactadas. | Quando escolhe uma conta da lista principal de contas para adicioná-las e guardá-las, o cliente do item de contrato também é adicionado como cliente contratado. Os clientes do item de contrato são utilizados quando as faturas são geradas. |
| **Percentagem de Divisão de Faturação** | Grelha editável no separador **Clientes do Contrato** e os formulários **Principal** e **Criação Rápida** para um cliente do contrato. | Este campo representa a percentagem de cada transação de vendas não faturadas que será atribuída a este cliente do item de contrato. | Os clientes do item de contrato e as percentagens de divisão de faturação são utilizados quando os valores reais são criados após aprovação e quando a fatura é gerada. |
| **Limite a Não Exceder** | Grelha editável no separador **Clientes do Contrato** e os formulários **Principal** e **Criação Rápida** para um cliente do contrato. | Indica se existe um limite ou limite negociado para o montante global que será faturado a este cliente para o item de contrato. | O limite a não exceder para o cliente do item de contrato é usado quando os valores reais são criados e as faturas são geradas. |
| **É Arredondamento** | Grelha editável no separador **Clientes do Contrato** e os formulários **Principal** e **Criação Rápida** para um cliente do item de contrato. | Este campo indica se este cliente é um cliente de arredondamento predefinido para este item de contrato baseado em projetos. | Quando se gera uma percentagem de divisão real de faturação, pode haver algumas diferenças arredondamentos. Este cliente é atribuído às diferenças de arredondamento neste caso. |

## <a name="edit-billing-split-percentages"></a>Editar percentagens de divisão de faturação

As faturação de percentagens divididas pode ser editada na grelha. Quando as percentagens de divisão de faturação não totalizam 100 por cento, ocorrerá um erro. Depois de editar as percentagens de divisão de faturação, atualize a página para remover o erro.

Também pode selecionar **Distribuir Uniformemente** na subgrelha do cliente do item de contrato. Esta ação atribui igualmente divisões de faturação a todos os clientes do item de contrato. Se houver algum fator de arredondamento, será adicionado ao cliente de arredondamento. Um cliente do item de contrato é sempre etiquetado como cliente de **Arredondamento** com a bandeira **Arredondamento** definida como **Sim**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
