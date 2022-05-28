---
title: Criar um adiantamento ad hoc num contrato
description: Este tópico fornece informações sobre a criação de um adiantamento num contrato, se necessário.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ee97710a9f0229cef3ff9dbfda6a2f108726df20
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8594040"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract"></a>Criar um adiantamento ad hoc num contrato

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

O Microsoft Dynamics 365 Project Operations suporta cenários de faturação que envolvem pré-pagamentos e adiantamentos. O processo de utilização **Adiantamentos** no **Project Operations** é semelhante aos contratos de **Sinal**. 

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]