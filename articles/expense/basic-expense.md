---
title: Entrada de despesas (lite)
description: Este tópico fornece informações sobre como trabalhar com a entrada de despesas numa implementação leve.
author: stsporen
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 48bf86a5cee475708f93462dc154e21b36240023f0a94cf31c49e9a096951736
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007835"
---
# <a name="expense-entry-lite"></a>Entrada de despesas (lite)

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

A gestão de despesas básica ou leve é a capacidade de registar as despesas simples. Pode registar as despesas num projeto e, em seguida, o aprovador do projeto irá revê-los e aprová-los.

Para obter mais informações sobre as capacidades de despesas no Dynamics 365 Project Operations, consulte [Descrição geral de Despesas](expense-overview.md).

## <a name="capture-a-basic-expense"></a>Capturar uma despesa básica

Pode capturar as suas despesas para poder submetê-las ao aprovador.

1. Vá para **Despesas** e selecione **Novo**.
2. Na página **Nova Despesa**, introduza as informações da despesa necessárias e, em seguida, selecione **Guardar**.

## <a name="submit-a-basic-expense"></a>Submeter uma despesa básica

Depois de concluir a captura de todas as suas despesas, e quando estiver pronto para aprová-las, tem de submetê-las.

1. Vá para **Despesas** e selecione uma despesa. Ou selecione todas as despesas através da caixa de verificação no cabeçalho.
2. Selecione **Submeter**. O sistema processa as entradas selecionadas e, em seguida, cria pedidos de aprovação de despesas.

## <a name="add-an-attachment"></a>Adicionar um anexo

Poderá ter de fornecer ao aprovador documentação adicional sobre as suas despesas. Pode anexar um recibo na linha cronológica da entrada de despesas. Selecione **Editar** e a secção **Linha Cronológica** e, em seguida, selecione o ícone de clipe de papel para anexar o seu recibo.

## <a name="recall-a-basic-expense"></a>Recuperar uma despesa básica

Quando submete uma despesa por engano, podes recuperá-la. O tempo necessário para recuperar uma entrada de despesa depende da sua fase de aprovação.  Se o aprovador ainda não tiver aprovado a entrada, a recuperação poderá ocorrer imediatamente. No entanto, se a entrada já tiver sido aprovada, é pedido ao aprovador para aprovar a recuperação e reverter as transações.

1. Vá para **Despesas** e, depois, na lista de despesas, selecione a despesa a recuperar.
2. Selecione **Recuperar**. Se a entrada de despesa ainda não tiver sido aprovada, o sistema recupera-a imediatamente. Se a entrada de despesa já tiver sido aprovada, é criado um pedido de recuperação para notificar o aprovador que pretende reverter a despesa. Em seguida, o aprovador confirmará que a reversão pode ser feita e a entrada será devolvida.

## <a name="delete-a-basic-expense"></a>Eliminar uma despesa básica

As despesas que ainda não foram submetidas podem ser eliminadas. Para eliminar uma despesa que já foi submetida, primeiro tem de recuperá-la.

## <a name="see-also"></a>Consulte também

- [Descrição geral das aprovações](../approvals/approvals-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]