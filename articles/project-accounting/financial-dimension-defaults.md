---
title: Dimensão financeira predefinida
description: Este tópico fornece informações sobre como configurar predefinições de dimensão financeira.
author: sigitac
ms.date: 12/14/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 8c1eb71d13ca7fc59118d15fef7ac914577b3b0e
ms.sourcegitcommit: fe5610464fdb5be756aa6a6a5b3c9a991dea0ed8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 12/15/2021
ms.locfileid: "7922952"
---
# <a name="financial-dimension-defaults"></a>Dimensão financeira predefinida

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

O Dynamics 365 Project Operations utiliza a estrutura de [Dimensões financeiras](/dynamics365/finance/general-ledger/financial-dimensions) no Dynamics 365 Finance para fornecer informações adicionais sobre as transações do sub-livro razão e livro razão geral.

As dimensões financeiras predefinidas podem ser definidas num cliente, fonte de financiamento de projetos, marco, item de contrato de projeto ou projeto.

## <a name="define-default-financial-dimensions-for-a-customer"></a>Predefinir dimensões financeiras para um cliente

As predefinições da dimensão do cliente são especificados no Finance. Conclua os seguintes passos para predefinir a dimensão.

1. Vá a **Contas a receber** > **Clientes** > **Todos os clientes**.
2. Na página **Clientes**, no separador **Dimensões financeiras**, defina os valores de dimensão financeira para o cliente específico.

## <a name="define-default-financial-dimensions-for-project-contracts"></a>Predefinir dimensões financeiras para contrato de projeto

Os contratos de projeto são criados e mantidos no Common Data Service (CDS). Os atributos contabilísticos para os contratos de projeto são definidos no módulo **Gestão de projetos e contabilística** no Finance.

### <a name="set-financial-dimensions-for-a-project-funding-source"></a>Definir dimensões financeiras para uma fonte de financiamento de projetos

1. Vá a **Gestão de projetos e contabilística** > **Projetos** > **Contratos de Projeto**.
2. Selecione o registo que pretende atualizar e, no separador **Contrato do projeto**, selecione **Mostrar contabilidade predefinida**.
3. Expanda **Informações relacionadas** e selecione o separador **Fontes de financiamento**.
4. Defina as predefinições da dimensão financeira. Note que as dimensões financeiras assumem a predefinição da conta do cliente.

### <a name="set-financial-dimensions-for-a-project-contract-line"></a>Definir dimensões financeiras para um item de contrato de projeto

1. Vá a **Gestão de projetos e contabilística** > **Projetos** > **Contratos de Projeto**.
2. Selecione o registo que pretende atualizar e, no separador **Contrato do projeto**, selecione **Mostrar contabilidade predefinida**.
3. Expanda **Informações relacionadas** e selecione o separador **Itens de contrato**.
4. Defina as predefinições da dimensão financeira. As predefinições da dimensão financeira são aplicáveis e só podem ser utilizadas com itens de contrato de Preço fixo (marco).

Estas predefinições são utilizadas em transações em conta de projetos relacionados e linhas de fatura.

## <a name="define-default-financial-dimensions-for-projects"></a>Predefinir dimensões financeiras para projetos

Os projetos são criados e mantidos no CDS. Os atributos contabilísticos para os projetos são definidos no módulo **Gestão de projetos e contabilidade** no Finance.

1. Vá para **Gestão de projetos e contabilística** > **Projetos** > **Todos os projetos**.
2. Selecione o registo que pretende atualizar e, no separador **Projeto**, selecione **Mostrar contabilidade predefinida**.
3. Expanda **Informações relacionadas** e selecione o separador **Configurar**.
4. Defina as predefinições da dimensão financeira. Note que as dimensões financeiras assumem a predefinição da conta do cliente. Se o projeto estiver associado a um item de contrato com vários clientes de contratos de projeto, o cliente principal é utilizado para predefinir dimensões financeiras.

As dimensões financeiras predefinidas do projeto são usadas para predefinir linhas de diário para tempo, despesas e transações de taxas no **Diário de Integração do Project Operations** e em linhas de fatura de projeto relacionadas.

## <a name="apply-financial-dimensions-for-project-time-entries"></a>Aplicar dimensões financeiras a entradas de tempo do projeto
Para aplicar dimensões financeiras a entradas de tempo do projeto, note que o valor de dimensão predefinido se baseia na seguinte ordem:

1. recurso
2. Project
3. Fonte de financiamento

Por exemplo, se a dimensão predefinida for especificada num recurso, será aplicada sobre uma predefinição especificada no projeto. Da mesma forma, uma dimensão de projeto predefinida será aplicada sobre a predefinição especificada na origem do financiamento.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
