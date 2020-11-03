---
title: Gerir vários clientes em propostas do projeto
description: Este tópico fornece informações sobre como trabalhar em propostas com vários clientes que irão financiar o projeto. (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 656418ab99db46455195f70c38b6f5fa13c30755
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082304"
---
# <a name="managing-multiple-customers-on-project-quotes-sales"></a>Gerir vários clientes em propostas do projeto (Vendas)

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

As propostas do projeto suportam o cenário em que a proposta envolve vários clientes que irão financiar o negócio. O separador **Resumo** da Proposta tem o campo **Cliente potencial** , que identifica o cliente principal do negócio. Podem ser configurados outros clientes para a oportunidade potencial no separador **Clientes** da proposta do projeto.

Todos os clientes da proposta no separador **Clientes** da proposta do projeto são assumidos por predefinição como clientes de linha de proposta em quaisquer **novas** linhas de proposta baseadas em projetos criadas para a proposta. Quaisquer linhas de proposta baseadas em projetos existentes não vão herdar novos registos de clientes de proposta criados depois deles.

As linhas de proposta baseadas no produto são associadas automaticamente ao cliente principal que também é o cliente no campo **Cliente Potencial** no separador **Resumo** da proposta.

Os clientes da proposta e os clientes da linha de proposta podem ser adicionados, atualizados ou eliminados em qualquer altura antes de a proposta ser ganha.

## <a name="concept-of-a-primary-customer"></a>Conceito de um cliente principal

O cliente no separador Resumo da proposta de projeto como cliente potencial é o cliente principal da proposta. Quando tenta eliminar o cliente principal da lista de clientes na proposta, receberá um erro a indicar que não é possível eliminar um registo de cliente principal numa proposta.

O cliente principal não deve ser atualizado a partir da lista de clientes na proposta. No entanto, pode influenciar o cliente principal ao alterar o cliente potencial no separador **Resumo** da proposta. Quando este campo é atualizado no **Resumo da Proposta** , o cliente potencial selecionado recentemente é adicionado como um novo cliente de proposta com o sinalizador de privacidade **Principal**. O antigo cliente potencial continuará a ser um cliente na proposta.

## <a name="create-update-or-delete-a-quote-customer-record"></a>Criar, Atualizar ou Eliminar um registo de cliente de proposta

Um cliente de proposta pode ser criado, atualizado ou eliminado do separador **Clientes da Proposta** na página **Proposta**. Os campos listados na tabela seguinte estão no registo de cliente da proposta de uma proposta de projeto.

| **Campo** | **Localização** | **Relevância, finalidade e orientação** | **Impacto a jusante** |
| --- | --- | --- | --- |
| Conta | Grelha editável no separador **Clientes da Proposta** e os formulários **Principal** e **Criação Rápida** para um cliente de proposta. | Lista todas as contas ativas. Este campo é bloqueado após a criação do registo. Se pretende atualizá-lo, elimine o registo e volte a criá-lo. Se registou valores reais, ou se o registo do cliente de proposta for um cliente principal, terá permissão para eliminar o registo. | Os clientes de proposta são copiados como clientes da linha de proposta quando uma linha de proposta é criada. Os clientes de proposta também são copiados para os clientes do contrato de projeto quando uma proposta é ganha. |
| Percentagem de divisão de faturação | Grelha editável no separador **Clientes da Proposta** e os formulários **Principal** e **Criação Rápida** para um cliente de proposta. | Representa a percentagem de cada transação de vendas não faturada que será atribuída a este cliente de proposta. | Copiada para as novas linhas de proposta e para os clientes do contrato de projeto. |
| Nome do Contacto Para Faturação | Grelha editável no separador **Clientes da Proposta** e os formulários **Principal** e **Criação Rápida** para um cliente de proposta. | Este é um campo de texto e deve ser usado para identificar a pessoa de contato da Fatura para este cliente. Assumem o valor predefinido a partir do registo de conta relacionado | Copiado para os clientes do contrato de projeto quando uma Proposta é ganha e, por sua vez, para o campo Nome do Contacto Para Faturação na Fatura que é gerada para este cliente. |
| Nome para Faturação | Grelha editável no separador **Clientes da Proposta** e os formulários **Principal** e **Criação Rápida** para um cliente de proposta. | Este campo de texto deve ser utilizado para identificar a pessoa de contato da fatura para este cliente. | Copiado para os clientes do contrato de projeto quando uma proposta é ganha e, por sua vez, para o campo **Nome do Contacto Para Faturação** na fatura que é gerada para este cliente. |
| Termos de Pagamento | Grelha editável no separador **Clientes da Proposta** e os formulários **Principal** e **Criação Rápida** para um cliente de proposta. | Trata-se de um conjunto de opções com valores que assumem por predefinição o registo de conta relacionado. | Copiado para os clientes do contrato de projeto quando uma proposta é ganha e, por sua vez, para o campo **Nome do Contacto Para Faturação** na fatura que é gerada para este cliente. |
| É Arredondamento | Grelha editável no separador **Clientes da Proposta** e os formulários **Principal** e **Criação Rápida** para um cliente de proposta. | Indica se este cliente é um cliente de arredondamento predefinido para este negócio. | Copiado para os clientes do contrato de projeto quando uma proposta é ganha. |
| Limite a não exceder | Grelha editável no separador **Clientes da Proposta** e os formulários **Principal** e **Criação Rápida** para um cliente de proposta. | Indica se existe um limite negociado ou um máximo para o valor global que será faturado a este cliente para este compromisso | Copiado para os clientes do contrato de projeto quando uma proposta é ganha. |

## <a name="editing-billing-split-percentages"></a>Editar percentagens de divisão de faturação

Pode editar as percentagens de divisão de faturação através da experiência de edição da grelha em linha. Quando as percentagens de divisão de faturação não totalizam 100%, ocorre um erro. Depois de atualizar as percentagens de divisão de faturação, atualize a página para remover o erro.

Também pode tentar selecionar **Distribuir Uniformemente** na subgrelha dos clientes da proposta. Esta ação distribui divisões de faturação por todos os clientes da proposta. Se existir algum fator de arredondamento, ele será adicionado ao cliente arredondamento. Um dos clientes de proposta é sempre identificado como o cliente de arredondamento. Isto significa que o registo de cliente de proposta tem o sinalizador **Arredondamento** definido como **Sim**. Normalmente, este é o cliente principal da proposta, mas isso pode ser alterado.
