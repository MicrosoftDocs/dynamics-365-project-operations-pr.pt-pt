---
title: Atualizar atributos de plug-in para incluir novas dimensões de definição de preços
description: Este tópico fornece informações sobre a atualização de atributos de plug-in para dimensões de definição de preços.
author: Rumant
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: d04561fb6bcbc64f6ad3ea922bff1912824be64c6bb2b18cddd95e9b1b5c7850
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988800"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a>Atualizar atributos de plug-in para incluir novas dimensões de definição de preços

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> Se não estiver a utilizar as funcionalidades de Criação de Propostas e Contratação do Project Service Automation (PSA), pode ignorar este tópico.

Este tópico pressupõe que concluiu os procedimentos nos tópicos, [Criar campos e entidades personalizados](create-custom-fields-entities.md), [Adicionar campos personalizados às entidades de configuração de preços e transacionais](field-references.md) e [Configurar campos personalizados como dimensões de definição de preços](set-up-pricing-dimensions.md). Se não tiver concluído esses procedimentos, volte a concluí-los e, em seguida, volte a este tópico.

Quando é criado um detalhe de linha de proposta na página **Linha de Proposta** para uma linha de proposta do projeto, o sistema cria duas linhas de estimativa em segundo plano -- uma linha para o lado do custo da estimativa e outra para o lado das vendas. É o mesmo para os itens de contrato do projeto.

Quando altera uma quantidade ou um campo no lado do custo, essa alteração é propagada para o lado das vendas. Isto é possível devido aos seguintes plug-ins que devem ser registados novamente após uma alteração nas dimensões de definição de preços.

- PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.
- PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.

Os seguintes passos explicam-lhe o processo de registo dos plug-ins.

1. Abra o **PluginRegistrationTool** e ligue-se à sua instância online.
2. Clique em **Procurar** e procure o plug-in a ser atualizado.

 ![Captura de ecrã da árvore de pesquisa.](media/PRT-1.png)

3. Depois de o plug-in ser encontrado, selecione-o e, em seguida, clique em **Selecionar no Formulário Principal**.

4. Selecione o passo do plug-in a atualizar, clique com o botão direito do rato e, em seguida, selecione **Atualizar**.

 ![Captura de ecrã do plug-in a ser atualizado.](media/PRT-2.png)
 
5. Na janela de atualização, clique nas reticências (**...**) nos atributos de filtragem.

 ![Captura de ecrã das informações de configuração Atualizar passo existente.](media/PRT-3.png)
 
6. Selecione as caixas de verificação do atributo de definição de preços.

 ![Captura de ecrã que mostra a seleção da caixa de verificação para atributos de definição de preços.](media/PRT-4.png)

7. Clique em **OK** para fechar a página e, em seguida, selecione **Atualizar Passo**.

 ![Captura de ecrã que mostra o botão "Atualizar Passo".](media/PRT-5.png)
 
8. Repita este processo para o segundo plug-in, **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.

9. Feche o Plug-in Registration Tool.



[!INCLUDE[footer-include](../includes/footer-banner.md)]