---
title: Faturar um sinal ou um adiantamento – lite
description: Este tópico fornece informações sobre como faturar um sinal ou um adiantamento no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9013529b615026eab92177c9fd9fb84c50d66f4f
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180566"
---
# <a name="invoice-a-retainer-or-an-advance---lite"></a>Faturar um sinal ou um adiantamento – lite

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

O Dynamics 365 Project Operations suporta contratos baseados em sinais e adiantamentos únicos. Num contrato de projeto, pode registar uma agenda de sinais ou adiantamento único. No entanto, o registo ao nível do contrato do projeto não disponibiliza imediatamente um sinal ou adiantamento para utilização. Para utilizar um sinal ou adiantar uma fatura que realmente cobra ao cliente, o sinal ou adiantamento deve ser faturado primeiro.

Conclua os seguintes passos para faturar um sinal ou um adiantamento.

1. Selecione **Vendas** > **Faturação** > **Sinais e Adiantamentos**. 
2. Na página **Adiantamentos e Sinais**, utilize o filtro para selecionar o sinal específico ou adiantamento a faturar e marque-o como **Pronto a Faturar**.
3. Crie uma fatura manualmente a partir da lista **Contrato do Projeto** ou da página de detalhes. O sinal ou adiantamento é mostrado na fatura de rascunho na secção **Adiantamentos e Sinais** na página **Fatura**.
4. Confirme a fatura. Isto irá disponibilizar o sinal ou adiantamento para utilização. Pode verificar a fatura na página de lista **Sinais e Adiantamentos**. Para um Adiantamento ou Sinal faturado, o valor disponível é indicado na grelha.

## <a name="create-a-retainer-or-advance-from-the-invoice-grid"></a>Criar um sinal ou adiantamento a partir da grelha de fatura

Pode criar um sinal ou um adiantamento diretamente numa fatura.

1. Numa fatura de rascunho, na subgrelha **Adiantamento e Sinais**, selecione **Novo** para criar um novo sinal ou adiantamento. 
2. Na página **Criação Rápida**, adicione as informações necessárias e, em seguida, selecione **Guardar**. O sinal ou adiantamento é criado no contrato do projeto relacionado com a fatura. O sinal ou adiantamento é automaticamente marcado como **Pronto a Faturar** e, em seguida, adicionado à subgrelha **Adiantamentos e Sinais** na página **Fatura**.

## <a name="reconcile-an-invoiced-retainer-or-advance"></a>Reconciliar um sinal ou adiantamento faturado

Após a faturação de um sinal ou adiantamento, podem ser utilizados ou reconciliados numa fatura com tempo, despesas, marcos ou outros encargos baseados em projetos. O cliente verá o valor da fatura reduzido pelo montante do sinal ou do adiantamento utilizado nesta fatura.

Em cada fatura gerada para um contrato de projeto que tenha faturado sinais ou adiantamentos, o Project Operation aplica automaticamente o sinal ou adiantamento na fatura.

Isto pode ser visto na grelha **Sinais e Adiantamentos Aplicados** na página **Fatura**. A tabela seguinte fornece informações sobre os campos na grelha **Sinais e Adiantamentos Aplicadas** da página **Fatura do Projeto**.

| Campo | Localização | Descrição | Impacto a jusante |
| --- | --- | --- | --- |
| Descrição | Grelha **Adiantamentos e Sinais Aplicados** na página **Fatura do Projeto** |Este campo só de leitura fornece uma descrição do sinal ou adiantamento utilizado nesta fatura. Não é possível alterar este valor na fatura. Este valor pode ser atualizado na subgrelha na página **Contrato do Projeto**. | Este campo pode ser apresentado ao cliente na fatura impressa para indicar qual o sinal ou adiantamento que é aplicado na fatura. |
| Entregue Em | Grelha **Adiantamentos e Sinais Aplicados** na página **Fatura do Projeto**  | Este campo só de leitura fornece a data de faturação do sinal ou adiantamento utilizado nesta fatura. Não é possível alterar este valor na fatura. Este valor pode ser atualizado na subgrelha na página **Contrato do Projeto**. | Este campo pode ser apresentado ao cliente na fatura impressa para indicar a data em que o sinal ou adiantamento foi faturado pela primeira vez ao cliente. |
| Montante | Grelha **Adiantamentos e Sinais Aplicados** na página **Fatura do Projeto**  | Este campo só de leitura fornece o montante do sinal ou adiantamento utilizado nesta fatura. Não é possível alterar este valor na fatura. Este valor pode ser atualizado na subgrelha na página **Contrato do Projeto**. | Este campo pode ser apresentado ao cliente na fatura impressa para indicar o montante original em que o sinal ou adiantamento que foi pago pelo cliente. |
| Montante usado | Grelha **Adiantamentos e Sinais Aplicados** na página **Fatura do Projeto**  | Este campo apenas de leitura fornece o valor calculado que resume a quantidade utilizada do sinal ou adiantamento. | Este campo pode ser apresentado ao cliente na fatura impressa para indicar o montante deste sinal ou adiantamento que já foi utilizado. |
| Montante Total | Grelha **Adiantamentos e Sinais Aplicados** na página **Fatura do Projeto**  | Este campo editável fornece o montante do sinal ou adiantamento que está a ser utilizado nesta fatura de projeto. Este montante não pode ser mais do que o que está disponível no adiantamento. O sistema calcula-o automaticamente como a diferença entre os campos **Montante** e **Montante Utilizado** na grelha. Pode diminuir este valor para usar menos do que o disponível, mas não pode aumentar a quantidade para usar mais do que o que está disponível. | Este campo pode ser apresentado ao cliente na fatura impressa para indicar o montante deste sinal ou adiantamento que está a ser utilizado na fatura. |
| Montante do Saldo do Sinal. | Grelha **Adiantamentos e Sinais Aplicados** na página **Fatura do Projeto**  | Este campo apenas de leitura fornece o valor de quanto do sinal ou adiantamento será deixado após a confirmação da fatura. | Este campo pode ser apresentado ao cliente na fatura impressa para indicar o montante que será deixado deste sinal ou adiantamento após a fatura ser confirmada e paga. |
