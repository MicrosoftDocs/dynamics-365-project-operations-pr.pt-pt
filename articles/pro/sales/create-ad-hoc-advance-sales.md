---
title: Criar um adiantamento ad hoc num contrato – lite
description: Este tópico fornece informações sobre a criação de um adiantamento num contrato, se necessário.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a6bf02c2e2ab2f3c696b1eab1b92a20272187bf5
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181376"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract---lite"></a>Criar um adiantamento ad hoc num contrato – lite

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

O Microsoft Dynamics 365 Project Operations suporte cenários de faturação que envolvem pré-pagamentos e adiantamentos. O processo de utilização **Adiantamentos** no **Project Operations** é semelhante aos contratos de **Sinal**. 

Conclua os seguintes passos para faturar o cliente por um adiantamento.

1. Vá à página **Contrato de Projeto** e, em seguida, selecione o separador **Adiantamentos e Sinais**.
2. Na subgrelha que lista todos os adiantamentos e pré-pagamentos previamente registados, selecione **+ Novo sinal de contrato de projeto**. 

    O formulário **Criação Rápida** abre para a gravação de um pré-pagamento ou adiantamento.
    
3. A tabela abaixo lista os campos para registar um adiantamento e as considerações a ter em conta à medida que cria novos:

    | Campo | Descrição | Impacto a jusante |
    | --- | --- | --- |
    | **Cliente do Contrato do Projeto** | Este campo indica qual o cliente no contrato que será faturado por este adiantamento. | Se tiver vários clientes no contrato e quiser faturar cada um deles por um montante de sinal ou de adiantamento específico, crie um adiantamento para cada cliente individualmente. |
    | **Descrição** | A descrição do propósito ou do momento do adiantamento para ajudar a identificar este adiantamento. | Esta descrição é apresentada na linha de fatura deste adiantamento. |
    | **Montante** | O valor para o pré-pagamento ou adiantamento. | Este montante é apresentado na linha de fatura deste adiantamento. |
    | **Data da Fatura** | A data em que este adiantamento é faturado ao cliente. | Esta é a data para o processo automatizado de criação de faturas criar uma linha de fatura para este adiantamento. |
    | **Estado da Fatura** | Esta é uma definição de opção que indica se este adiantamento é adicionado a uma fatura de rascunho para este cliente. Os valores possíveis são:</br>- **Não está pronto para faturar**</br>- **Pronta para faturar** | Quando um adiantamento ou pré-pagamento é marcado como **Pronto a faturar**, é adicionado como um tempo de linha numa fatura de rascunho. Apenas um adiantamento totalmente faturado pode ser utilizado para conciliar com os custos do projeto para o próximo período de faturação. |

4. Selecione **Guardar e fechar** no diálogo de criação rápida para registar o adiantamento ou o pré-pagamento.
