---
title: Eliminar uma estimativa do projeto
description: Este tópico fornece informações sobre a eliminação de uma estimativa do projeto após a sua conclusão.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: a4ad06bef7ed66a626c6d2ad7ef01ba5b99d1c0f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006930"
---
# <a name="eliminate-a-project-estimate"></a>Eliminar uma estimativa do projeto

[!include [banner](../includes/banner.md)]

As estimativas do projeto fornecem a vista financeira do trabalho estimado e agendado para um projeto. Para trabalhar com estimativas para um projeto, é necessário anexar o projeto a um projeto de estimativa. Um projeto de estimativa baseia-se sempre num projeto existente, no entanto, vários projetos podem referir-se a um único projeto de estimativa. Apenas os projetos de preço fixo e de investimento podem ser associados a projetos de estimativa, devendo esses projetos pertencer ao mesmo grupo de projetos que o projeto de estimativa.

Para eliminar um projeto de estimativa, tem de estar completo. Os seguintes passos explicam como eliminar uma estimativa.

1. Vá para **Gestão de projetos e contabilística** > **Todos os Projetos** e abra o projeto. 
2. No separador **Gerir**, selecione **Estimativas** e, na página **Estimativa**, selecione **Eliminar**.
3. Na página **Eliminar estimativa** no separador **Geral**, defina as seguintes opções:

   - **Código do período**: selecione o código do período para escolher os projetos de estimativa adequados. 
   - **Data de estimativa**: selecione a data de estimativa adequada para a eliminação.
   - **Eliminar com avisos WIP**: ative esta opção para fornecer notificação quando uma estimativa que está associada a um trabalho em curso (WIP) será eliminada. Quando esta opção não está ativada, a eliminação não pode continuar se existirem transações não estimadas. 
   > [!NOTE]
   > Esta opção só está disponível quando a eliminação é aplicada a um projeto de estimativa. Não está disponível se estiver a utilizar publicações periódicas. Esta definição funciona com as definições no separador **Estimativa** na página **Parâmetros do projeto**, no grupo de campos **Permitir a eliminação quando existem transações não estimadas**.
   - **Definir fase para Terminada**: ative esta opção para definir a fase do projeto de estimativa para **Terminado** depois de executar a eliminação.
   - **Imprimir lista de estimativas**: selecione as informações a incluir quando a lista de estimativas for impressa.
   - **Mostrar Infolog**: ative esta opção para exibir o Infolog.
   - **Data da publicação**: escolha a data de publicação do livro razão da estimativa.

4.  Selecione **OK**.
5. Após o processo de eliminação estar concluído, o projeto de estimativa eliminado é apresentado com um valor negativo. 

Se não pretendeu eliminar uma estimativa, pode selecionar a estimativa eliminada e selecionar **Reverter eliminação**.   


[!INCLUDE[footer-include](../includes/footer-banner.md)]