---
title: Verificação de faturas de fornecedor com valores reais aprovados
description: Este artigo explica como o Microsoft Dynamics 365 Project Operations permite que os gestores de projeto verifiquem as faturas dos fornecedores com os valores reais que foram aprovados como contratantes durante o trabalho e tempo registados, bem como as despesas e materiais que foram utilizados pelos membros da equipa do projeto.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 43f47a44260d1a47437846f2764b56f680d4b682
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914232"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Verificação de faturas de fornecedor com valores reais aprovados

[!include [banner](../../includes/dataverse-preview.md)]

_ **Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma

O Microsoft Dynamics 365 Project Operations permite que os gestores de projeto verifiquem as linhas de fatura de fornecedor das seguintes maneiras:

- Utilize o campo **Estado de verificação** nas linhas de fatura do fornecedor.
- Se as linhas de fatura do fornecedor se referem a um item de subcontrato, ligue os valores reais da atividade do subcontratante àquelas linhas da fatura do fornecedor. A ligação é criada associando os valores reais de custo às linhas da fatura do fornecedor.

    > [!NOTE]
    > Embora seja possível monitorizar o estado de verificação das linhas de fatura do fornecedor que não se referem a um subcontrato, os custos reais não podem ser associados a essas linhas da fatura do fornecedor.

## <a name="verification-status"></a>Estado da verificação

O campo **Estado de verificação** numa linha de fatura do fornecedor indica esse estado da verificação. São suportados os seguintes estados:

1. Não iniciada
2. Em Curso
3. Concluir

As linhas da fatura do fornecedor que têm o estado de verificação **Não iniciada** podem ser editadas.

As linhas da fatura do fornecedor que têm o estado de verificação **Em progresso** já não podem ser editadas. No caso de uma linha da fatura de fornecedor se referir a um subcontrato, o estado de verificação é automaticamente definido como **Em progresso**, assim que o primeiro custo real é associado à linha da fatura do fornecedor.

As linhas da fatura do fornecedor que têm o estado de verificação **Concluída** já não podem ser editadas. Quando todas as linhas na fatura de um fornecedor têm este estado de verificação, a fatura do fornecedor pode ser confirmada.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Associar custos reais às linhas da fatura do fornecedor

A correspondência dos valores reais de custo ajuda com o processo de verificação na linha da fatura de fornecedor. Para associar o custo real a uma linha de fatura do fornecedor, siga estes passos.

1. Abra a linha de fatura do fornecedor e selecione o separador **Valores reais de custo não associados**. Surge uma grelha que mostra uma lista dos custos reais que se referem ao mesmo item de subcontrato que a linha de fatura do fornecedor.
2. Selecione um ou mais valores reais de custo e, em seguida, selecione **Associar** na barra de ferramentas acima da grelha. O sistema valida se é possível corresponder os valores reais de custo selecionados. Após a validação ser aprovada, os valores reais de custo serão associados à linha de fatura do fornecedor.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Critérios de validação utilizados para ligar os custos reais a linhas da fatura do fornecedor

Durante o processo de correspondência, só é possível estabelecer uma ligação entre um custo real e uma linha de fatura do fornecedor se ambas as condições seguintes for cumpridas:

- O campo **Estado de ajuste** para cada custo real de custo selecionado tem de estar em branco. Por outras palavras, o custo real não pode ter sido substituído por outros custos reais durante um processo de revocação, cancelamento de aprovação ou diário de correção.
- Os valores dos seguintes campos são associados entre a linha da fatura do fornecedor e o custo real selecionado. Se algum campo não estiver definido na linha de fatura do fornecedor, não é considerado para correspondência.

    - Contrato do projeto
    - Item de contrato do projeto
    - Classe de transação
    - Project
    - Tarefa
    - Categoria de recursos
    - Categoria de transação
    - Produto
    - Item de subcontrato
    - Recurso reservável

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Desassociar valores de custo reais de uma linha de fatura do fornecedor

A não associação dos valores reais de custo também pode ajudar com o processo de verificação numa fatura de fornecedor, permitindo que as ligações anteriormente estabelecidas sejam removidas. Os valores de custo reais podem ser desassociados apenas das linhas da fatura do fornecedor que têm o estado de verificação **Em progresso**. Para desassociar o custo real de uma linha de fatura do fornecedor, siga estes passos.

1. Abra a linha de fatura do fornecedor e selecione o separador **Valores reais de custo associados**. Surge uma grelha que mostra uma lista dos custos reais que se referem ao mesmo item de subcontrato que a linha de fatura do fornecedor.
2. Selecione um ou mais valores reais de custo e, em seguida, selecione **Desassociar** na barra de ferramentas acima da grelha.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
