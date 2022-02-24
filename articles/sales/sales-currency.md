---
title: Moeda
description: Este tópico fornece informações sobre como adicionar e remover tipos de moeda em Operações de projeto.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 093eaa78b5f88aee364a753374a56c33e20a5ce3
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642287"
---
# <a name="currency"></a>Moeda

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

As moedas determinam os preços dos produtos no catálogo de produtos e o custo das transações, tais como as ordens de venda. Se os clientes se encontram espalhados por várias regiões do globo, adicione as suas moedas para gerir as suas transações. Adicione as moedas que são mais adequadas para as suas necessidades de negócio existentes e futuras.  

> [!NOTE]
> Se o seu ambiente for um ambiente do Common Data Service, está no centro de administração do Power Platform e seleciona a página **Moedas** (**Ambientes** > [selecionar ambiente] > **Definições** > **Negócio** > **Moedas**), a página ficará em branco. Isto deve-se ao facto de a definição de uma moeda não ser suportada em ambientes Common Data Service.

## <a name="add-a-currency"></a>Adicionar uma moeda  
Antes de iniciar este procedimento, verifique se o seu direito de acesso inclui permissões de administração do sistema. 

1. No centro de administração do Power Platform, selecione um ambiente. 
2. Selecione **Definições** > **Negócio**.
3. Selecione **Moedas**.  
4. Selecione **Novo**.  
5. Preencha as informações conforme necessário.  


   |          Campo          |                                                                                                                                                                                                                                                                                                                                                                            Descrição                                                                                                                                                                                                                                                                                                                                                                            |
   |-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |    **Tipo de Moeda**    | - **Sistema** - Selecione esta opção se pretende utilizar as moedas disponíveis nas aplicações condicionadas por modelo no Dynamics 365. Para procurar uma moeda, selecione **Pesquisar** . Quando seleciona um código de moeda, o **Nome da moeda** e o **Símbolo de moeda** são adicionados automaticamente para a moeda selecionada.<br />- **Personalizar** - Selecione esta opção se pretende adicionar uma moeda que não está disponível nas aplicações condicionadas por modelo no Dynamics 365. Neste caso, tem de introduzir manualmente os valores para **Código de moeda**, **Precisão Monetária**, **Nome da moeda**, **Símbolo de moeda** e **Conversão de moeda**. |
   |    **Código de Moeda**    |                                                                                                                                                                                                                                                                                                                                            Forma breve da moeda. Por exemplo, **USD** para o Dólar Norte-americano.                                                                                                                                                                                                                                                                                                                                            |
   | **Precisão Monetária**  |                                                                                                                                                                                  Escreva o número de casas decimais que pretende utilizar para a moeda.  Pode adicionar um valor entre 0 e 4. **Nota:** Se tiver definido um valor de precisão na caixa de diálogo **Definições do Sistema**, esse valor aparecerá aqui.                                                                                                                                                                                  |
   |    **Nome da Moeda**    |                                                                                                                                                                                                                                         Se tiver selecionado um código de moeda da lista de moedas disponíveis nas aplicações condicionadas por modelo no Dynamics 365, o nome da moeda para o código selecionado é apresentado aqui. Se tiver selecionado **Personalizar** como tipo de moeda, escreva o nome de moeda.                                                                                                                                                                                                                                          |
   |   **Símbolo de Moeda**   |                                                                                                                                                                                                                                                                      Se tiver selecionado um código de moeda da lista de moedas disponíveis, o símbolo para a moeda selecionada é apresentado aqui. Se tiver selecionado **Personalizar** como tipo de moeda, introduza o símbolo para a nova moeda.                                                                                                                                                                                                                                                                       |
   | **Conversão de Moeda** |                                                                                                                                                                                                                                     Escreva o valor da moeda selecionada em termos de um dólar americano. Este é o montante com que a moeda selecionada é convertida para a moeda base. **Importante** Certifique-se de que atualiza este valor tão frequentemente quanto necessário para evitar cálculos inexatos nas transações.                                                                                                                                                                                                                                      |


6. Quando tiver terminado, na barra de comandos, selecione **Guardar** ou **Guardar e Fechar**.  

   > [!TIP]
   >  Para editar uma moeda, selecione a moeda e depois introduza ou selecione os novos valores.  

## <a name="delete-a-currency"></a>Eliminar uma moeda  

1. No centro de administração do Power Platform, selecione um ambiente. 
2. Selecione **Definições** > **Negócio**.
3. Selecione **Moedas**.  
4. Da lista de moedas apresentadas, selecione a moeda para eliminar.  
5. Selecione **Eliminar**.  
6. Confirme a eliminação.  

> [!IMPORTANT]
>  Não pode eliminar as moedas que estão em utilização por outros registos; apenas pode desativá-las. A desativação dos registos de moeda não remove as informações de moeda armazenadas nos registos existentes, tais como oportunidades ou encomendas. No entanto, não poderá selecionar a moeda desativada para novas transações.  
