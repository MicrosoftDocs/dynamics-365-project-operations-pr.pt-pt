---
title: Gerir vários clientes em contratos do projeto – lite
description: Este tópico fornece informações sobre a gestão de vários clientes em contratos de projetos.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b7010ef75cd71ecdf832abb889db4703baa18fce0adadf3893621c42002fcab9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001760"
---
# <a name="manage-multiple-customers-on-project-contracts---lite"></a>Gerir vários clientes em contratos do projeto – lite

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

Os contratos de projeto no Dynamics 365 Project Operations suportam o cenário em que um acordo contratual envolve vários clientes que estão a financiar um negócio. O separador **Resumo** na página **Contrato de Projeto** inclui o campo **Cliente**. Este campo identifica o principal cliente do negócio. Outros clientes do negócio podem ser configurados no separador **Clientes** da página **Contrato de Projeto**.

Todos os clientes contratados listados no contrato de projeto assumem a predefinição como clientes do item de contrato em quaisquer novos itens de contrato baseados em projetos criados para o contrato do projeto. Os itens de contrato baseados em projetos existentes não herdam novos clientes de contrato, uma vez que novos registos são criados.

Os itens de contrato baseados em produtos estão automaticamente associadas ao cliente principal.

Os clientes do contrato e os clientes do item de contrato podem ser adicionados, atualizados ou eliminados a qualquer momento antes do contrato ser ganho.

## <a name="primary-customer"></a>Cliente principal

O cliente listado no separador **Resumo** do contrato do projeto, uma vez que o cliente potencial é o principal cliente do contrato. Quando tentar eliminar o cliente principal da lista de clientes no contrato, receberá uma mensagem de erro de que um registo de cliente principal num contrato não pode ser eliminado.

O cliente principal não pode ser atualizado da lista de clientes do contrato. Em vez disso, altere o cliente potencial no separador **Resumo** do contrato. Quando este campo é atualizado na página **Resumo do Contrato**, o novo cliente é adicionado como um novo cliente de contrato com a bandeira **Principal** definida. O cliente principal anterior continuará a ser um cliente no contrato.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Criar, atualizar ou eliminar um registo de cliente do contrato

Um cliente do contrato pode ser criado, atualizado ou eliminado do separador **Clientes** na página **Contrato de Projeto**. Os campos na tabela seguinte estão no registo do cliente do contrato de um contrato de projeto e devem ser tidos em conta enquanto está a trabalhar com o contrato.

| Campo | Localização | Descrição | Impacto a jusante |
| --- | --- | --- | --- |
| **Conta** | A grelha pode ser editada no separador **Clientes do Contrato** e os formulários **Principal** e **Criação Rápida** para um cliente do contrato. | Lista todas as contas ativas. Este campo é bloqueado após a criação do registo. Para atualizar a conta, elimine o registo e volte a criá-lo. Se tiver registado algum valor real, ou se o registo do cliente do contrato for um cliente principal, não pode eliminar o registo. | Os clientes do contrato são copiados como clientes do item de contrato quando um item de contrato é criado. |
| **Percentagem de Divisão de Faturação** | A grelha pode ser editada no separador **Clientes do Contrato** e os formulários **Principal** e **Criação Rápida** para um cliente do contrato. | Representa a percentagem de cada transação de vendas não faturadas que é atribuída a este cliente do contrato. | Copiado para novos itens de contrato e para clientes de item de contrato de projeto em novos itens de contrato de projeto. |
| **Nome do Contacto Para Faturação** | A grelha pode ser editada no separador **Clientes do Contrato** e os formulários **Principal** e **Criação Rápida** para um cliente do contrato. | Este campo de texto deve ser utilizado para identificar a pessoa de contato da fatura para este cliente. Este campo assume a predefinição do registo de conta relacionado. | Copiado para o campo **Faturar para Nome do Contrato** na fatura gerada para este cliente. |
| **Nome para Faturação** | A grelha pode ser editada no separador **Clientes do Contrato** e os formulários **Principal** e **Criação Rápida** para um cliente do contrato | Este campo de texto deve ser utilizado para identificar a pessoa de contato da fatura para este cliente. Este campo assume a predefinição do registo de conta relacionado. | Copiado para o campo **Faturar para Nome do Contrato** na fatura gerada para este cliente. |
| **Termos de Pagamento** | A grelha pode ser editada no separador **Clientes do Contrato** e os formulários **Principal** e **Criação Rápida** para um cliente do contrato. | Os valores assumem a predefinição do registo de conta relacionado. | Copiado para o campo **Faturar para Nome do Contrato** na fatura gerada para este cliente. |
| **É Arredondamento** | A grelha pode ser editada no separador **Clientes do Contrato** e os formulários **Principal** e **Criação Rápida** para um cliente do contrato. | Indica se este cliente é um cliente de arredondamento predefinido para este negócio. Só pode haver um cliente de arredondamento num contrato de projeto. | Quando o custo e as vendas não faturados se dividem em quantidade, conduzem a uma diferença de arredondamento, essa diferença é aplicada ao valor real que mapeia para este cliente. |
| **Limite a Não Exceder** | A grelha pode ser editada no separador **Clientes do Contrato** e os formulários **Principal** e **Criação Rápida** para um cliente do contrato | Indica se existe um limite ou limite negociado para o montante global que será faturado ao cliente para este compromisso. | A configuração do **Limite a Não Exceder** ao nível do cliente do contrato será avaliada em **Valores Reais de Vendas Não Faturados** que referenciam este cliente do contrato. |

## <a name="edit-billing-split-percentages"></a>Editar percentagens de divisão de faturação

As faturação de percentagens divididas pode ser editada usando a experiência de edição da grelha inline. Quando as percentagens de divisão de faturação não totalizam 100 por cento, receberá um erro. Depois de editar as percentagens de divisão de faturação, atualize a página para dispensar o erro.

Também pode selecionar **Distribuição Uniformemente** na subgrelha **Clientes do Contrato** para alocar divisões de faturação uniformemente a todos os clientes do contrato. Se houver um fator de arredondamento, será adicionado ao cliente de arredondamento. Um dos clientes do contrato é sempre etiquetado como o cliente de **arredondamento**, o que significa que o registo do cliente do contrato tem a bandeira de arredondamento definida como **Sim**. Normalmente, este é o cliente principal do contrato, mas também pode ser alterado.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]