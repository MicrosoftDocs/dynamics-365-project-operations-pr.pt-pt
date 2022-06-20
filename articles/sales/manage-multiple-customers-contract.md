---
title: Gerir vários clientes em contratos de projetos
description: Este artigo fornece informações sobre como gerir vários clientes num contrato de projeto.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 78ee117c1068e7af4674cc3b21e1055fd05bb43a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928354"
---
# <a name="manage-multiple-customers-on-project-contracts"></a>Gerir vários clientes em contratos de projetos

Este artigo fornece informações sobre como gerir vários clientes num contrato de projeto. Pode usar um contrato de projeto quando um acordo contratual para vários clientes é necessário para financiar um negócio. Na página **Contrato de Projeto**, o separador **Resumo** inclui informações sobre o cliente principal para um negócio. Outros clientes que participam no negócio podem ser adicionados ao separador **Clientes**.

Todos os clientes contratados no separador **Clientes** do contrato de contrato assumem a predefinição como clientes do item de contrato em quaisquer novos itens de contrato baseados em projeto criados para o contrato do projeto. Quaisquer itens de contrato baseados em projetos existentes não herdam novos registos de clientes de contrato que são criados posteriormente.

É possível adicionar, atualizar ou eliminar clientes do contrato ou do item de contrato a qualquer momento antes do contrato ser ganho. Um cliente no contrato do projeto tem de ser configurado como um cliente na empresa proprietária ou entidade legal na página **Clientes**. As entidades legais são configuradas no módulo **Gestão de projetos e contabilística** do Dynamics 365 Project Operations e estão disponíveis como empresas nos módulos **Vendas do Projeto** e **Entrega** do Project Operations.

## <a name="primary-customers"></a>Clientes principais

O cliente potencial no separador **Resumo** do contrato do projeto é o cliente principal do contrato. Não é possível atualizar o cliente principal da lista de cliente do contrato. Se tentar eliminar o cliente principal de uma lista de clientes no contrato, ocorrerá uma mensagem de erro que o informa que um registo de cliente principal num contrato não pode ser eliminado. Em vez disso, o cliente potencial no campo **Campo Potencial**, no separador **Resumo** do contrato do projeto. Quando atualiza este campo, o cliente recém-selecionado é adicionado como um novo cliente de contrato com o sinalizador **Principal** definida como **Sim**. O cliente principal anterior ainda é um cliente no contrato, no entanto já não é o cliente principal.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Criar, atualizar ou eliminar um registo de cliente do contrato

É possível criar, atualizar ou eliminar um cliente do contrato do separador **Clientes do Contrato** na página **Contrato**. Os seguintes campos estão incluídos no registo do cliente do contrato de um contrato de projeto.

| **Campo** | **Localização** | **Descrição** | 
| --- | --- | --- | 
| Conta | Grelha editável no separador **Clientes do Contrato** e as páginas Principal e Criação Rápida para um cliente do contrato. | Lista todas as contas ativas. Este campo é bloqueado após a criação do registo. Para atualizar o registo, tem de o eliminar e, em seguida, voltar a criá-lo. Se tiver registado algum valor real, ou se o registo do cliente do contrato for um cliente principal, não pode eliminar o registo. Quando o item de contrato é criado, os clientes do contrato são copiados como clientes do item de contrato. |
| Percentagem de Divisão de Faturação | Grelha editável no separador **Clientes do Contrato** e as páginas Principal e Criação Rápida para um cliente do contrato. | Representa a percentagem de cada transação de vendas não faturadas atribuída ao cliente do contrato. Quando são criadas novos itens de contrato de projeto, a percentagem de divisão de faturação é copiada para quaisquer novos itens de contrato criados e para clientes de item de contrato do projeto. |
| Nome do Contacto Para Faturação | Grelha editável no separador **Clientes do Contrato** e as páginas Principal e Criação Rápida para um cliente do contrato. | Este campo de texto deve ser utilizado para identificar a pessoa de contacto da fatura para o cliente. O valor predefinido provém do registo de conta relacionado. O nome do contacto é copiado para **Faturar para Nome do Contrato** na fatura gerada para o cliente. |
| Nome para Faturação | Grelha editável no separador **Clientes do Contrato** e as páginas Principal e Criação Rápida para um cliente do contrato. | Utilize este campo para identificar a pessoa de contacto da fatura para o cliente. O valor predefinido provém do registo de conta relacionado. O nome é copiado para o campo **Faturar para Nome do Contrato** na fatura gerada para o cliente. |
| Termos de Pagamento | Grelha editável no separador **Clientes do Contrato** e páginas Principal e Criação Rápida para um cliente do contrato. | O valor predefinido provém do registo de conta relacionado. O termos são copiados para **Faturar para Nome do Contrato** na fatura gerada para o cliente. |
| Empresa Proprietária | Grelha editável no separador **Clientes do Contrato do Projeto** e as páginas Principal e Criação Rápida para um cliente do contrato do projeto. | A entidade legal em que o cliente é configurado no módulo **Gestão de projetos e contabilística**. Este campo é apenas de leitura e está definido para a empresa proprietária do contrato do projeto.</br>A lista de clientes a adicionar no campo **Conta** já está filtrada para a lista da empresa proprietária no módulo **Gestão de projetos e contabilística** do Project Operations. A empresa proprietária é igual à entidade legal no módulo **Gestão de projetos e contabilística** no Project Operations. Todos os custos e receitas provenientes do projeto são contabilizados no livro razão geral da empresa proprietária. |
| É Arredondamento | Grelha editável no separador **Clientes do Contrato** e as páginas Principal e Criação Rápida para um cliente do contrato. | Indica se o cliente é um cliente de arredondamento predefinido para o negócio. Só pode haver um cliente de arredondamento num contrato de projeto. Quando o custo e as vendas não faturados se dividem em quantidade e conduzem a uma diferença de arredondamento, essa diferença é aplicada ao valor real que mapeia para o cliente. |
| Limite a não exceder | Grelha editável no separador **Clientes do Contrato** e as páginas Principal e Criação Rápida para um cliente do contrato. | Indica se existe um limite ou limite negociado para o montante global que será faturado ao cliente para o compromisso. A configuração do limite a não exceder ao nível do cliente do contrato é avaliada com base em valores reais de vendas não faturados que referenciam o cliente do contrato. |

## <a name="edit-billing-split-percentages"></a>Editar percentagens de divisão de faturação

É possível editar as percentagens de divisão de faturação ao editar na grelha. Quando as percentagens de divisão de faturação não totalizam 100 por cento, ocorre um erro. Depois de editar um percentagem de divisão de faturação, atualize a página **Contrato do Projeto** para remover o erro.

Também pode selecionar **Distribuir Uniformemente** na subgrelha de clientes do contrato do projeto. As divisões de faturação são alocadas uniformemente por todos os clientes do contrato do projeto. Se houver algum fator de arredondamento, o fator será adicionado ao cliente de arredondamento. Um dos clientes do contrato tem sempre o sinalizador **Arredondar** definida como **Sim**. Esse cliente é o cliente de arredondamento. Normalmente, o cliente de arredondamento é também o principal cliente do contrato, mas isso não é necessário.


[!INCLUDE[footer-include](../includes/footer-banner.md)]