---
title: Gerir vários clientes em linhas de proposta baseadas em projetos – lite
description: Este tópico descreve como gerir vários clientes em linhas de proposta baseadas em projetos.
author: rumant
ms.date: 10/06/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a6247c572284a5832cf2953578c98f6454e39dda
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575640"
---
# <a name="manage-multiple-customers-on-project-based-quote-lines---lite"></a>Gerir vários clientes em linhas de proposta baseadas em projetos – lite

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

As linhas de proposta baseadas em projetos suportam cenários em que cada linha de proposta tem uma lista de clientes que a estão a pagar. Esta lista de clientes na linha de proposta baseada em projetos pode ser a mesma que a lista de clientes na proposta. Também pode alterar a lista de clientes para ser diferente. Quando uma proposta do projeto é ganha, a lista de clientes na linha de proposta baseada em projetos é copiada para o item de contrato baseado em projetos correspondente para criar o contrato de projeto eventual. Os clientes na proposta baseada em projetos são copiados para o contrato de projeto.

Quando fatura o contrato de projeto eventual, a lista de clientes no item de contrato baseado em projetos tem prioridade sobre a lista no contrato de projeto. A lista de clientes no contrato de projeto só é utilizada para os valores por predefinição nos novos itens de contrato de projeto.

Todos os clientes da proposta no separador **Clientes** da proposta do projeto são assumidos por predefinição como clientes de linha de proposta em quaisquer novas linhas de proposta baseadas em projetos criadas para a proposta de projeto. Quaisquer linhas de proposta baseadas em projetos existentes não herdam novos registos de clientes de proposta criados depois deles.

## <a name="create-update-or-delete-a-quote-line-customer-record"></a>Criar, atualizar ou eliminar um registo de cliente da linha de proposta

Pode criar, atualizar ou eliminar um cliente de linha de proposta no separador **Clientes da Linha de Proposta** na página **Linha de proposta baseadas em projetos**. Quando adiciona um novo cliente na linha de proposta baseada em projetos, o cliente também é adicionado à proposta global como um cliente de proposta, com uma percentagem de divisão de faturação na proposta global de 0%. A percentagem de divisão de faturação na proposta global é copiada para as novas linhas de proposta e para o eventual contrato de projeto. No entanto, quando fatura a partir do contrato, é utilizada a percentagem de divisão de faturação a nível da linha de proposta, não a percentagem de divisão de faturação a nível do contrato global. 

A tabela seguinte mostra os campos no registo de cliente da linha de proposta de uma linha de proposta baseada em projetos.

| Campo | Localização | Descrição e orientação | Impacto a jusante |
| --- | --- | --- | --- |
| **Conta** | Uma grelha editável no separador **Clientes da Linha de Proposta**, o formulário principal e os formulários de criação rápida para um cliente da linha de proposta. | Lista todas as contas ativas. Este campo é bloqueado após a criação do registo. Se precisar de atualizar o campo, elimine e recrie o registo. Se registou valores reais, não poderá eliminar o registo. | Quando escolhe uma conta a partir da lista de contas principal a adicionar, o cliente da linha de proposta também é adicionado como um cliente de proposta quando o guarda. Quando uma proposta é ganha, os clientes da linha de proposta são copiados para os clientes de item de contrato do projeto. |
| **Percentagem de divisão de faturação** | Uma grelha editável no separador **Clientes da Linha de Proposta**, o formulário principal e os formulários de criação rápida para um cliente da linha de proposta. | Representa a percentagem de cada transação de vendas não faturada que será atribuída a este cliente da linha de proposta. | Copiado para os clientes de item de contrato de projeto. |
| **Limite a não exceder** | Uma grelha editável no separador **Clientes da Linha de Proposta**, o formulário principal e os formulários de criação rápida para um cliente da linha de proposta. | Indica se existe um limite negociado ou um máximo para o valor global que será faturado a este cliente para esta linha de proposta. | Copiado para os clientes de item de contrato de projeto quando uma proposta é ganha. |
| **É arredondamento** | Uma grelha editável no separador **Clientes da Linha de Proposta**, o formulário principal e os formulários de criação rápida para um cliente da linha de proposta. | Indica se este cliente é um cliente de arredondamento predefinido para esta linha de proposta baseada em projetos. | Copiado para os clientes de contrato de projeto quando uma proposta é ganha. |

## <a name="edit-billing-split-percentages"></a>Editar percentagens de divisão de faturação

Pode editar as percentagens de divisão de faturação na linha. Quando as percentagens de divisão de faturação não totalizam 100%, ocorre um erro. Depois de editar as percentagens de divisão de faturação, atualize a página da linha de proposta para remover o erro.

Utilize a ação de distribuição uniforme na subgrelha dos clientes da linha de proposta para alocar divisões de faturação a todos os clientes de linha de proposta. Se existir um fator de arredondamento, ele será adicionado ao cliente arredondamento. Um dos clientes da linha de proposta é sempre sinalizado como o cliente arredondamento, o que significa que o registo do cliente da linha de proposta tem o sinalizador de arredondamento definida como **Sim**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]