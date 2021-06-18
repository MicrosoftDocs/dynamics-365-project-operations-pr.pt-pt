---
title: Criar uma solução para dimensões de preços personalizadas
description: Este tópico fornece informações sobre como criar soluções para dimensões de preços personalizadas.
author: Rumant
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 86f4cd2c26ebfca621d1b226b571d220d3b2441e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010350"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a>Criar uma solução para dimensões de preços personalizadas

 _**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_ 

>[!IMPORTANT]
>Todas as alterações às dimensão de preços personalizados devem estar numa solução separada. Esta melhor prática importante permite a flexibilidade para atualizar ou remover as alterações, conforme necessário, ajuda na reutilização do seu trabalho e facilita a portabilidade de alterações para outras instâncias. Depois de efetuar as alterações necessárias, exporte esta solução como uma solução **Gerida** e, em seguida, importe-a para outras instâncias para reutilização.

## <a name="create-a-solution-for-custom-pricing-dimensions"></a>Criar uma solução para dimensões de preços personalizadas

1.  Selecione **Definições** > **Soluções** e, em seguida, selecione **Nova**.
2.  Nomeie a solução, *Dimensões de preços de <your organization name>*.
3. Introduza as informações necessárias restantes e selecione **Guardar**.

  ![Criação de uma solução de dimensões de preços personalizadas](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Adicionar todas as entidades obrigatórias e componentes relacionados necessários à Solução de dimensão de preços

Adicione as seguintes entidades do Project Service à sua solução de preços para fazer alterações importantes na solução de preços. Depois de concluído este procedimento, as entidades reconhecerão as novas dimensões de preços.

1.  Selecione **Definições** > **Soluções** e faça duplo clique no **<*nome da sua organização*> dimensões de preços**.
2.  No Explorador de Soluções, no painel de navegação esquerdo, selecione **Adicionar Existente** > **Entidades**.
3.  Na caixa de diálogo **Componentes da Solução**, selecione as seguintes entidades:
 
   - **Valor Real**
   - **Recurso Reservável**
   - **Linha de Estimativa**
   - **Tarefa de Projeto**
   - **Detalhe de Linha de Fatura**
   - **Linha do Diário**
   - **Detalhe de Item de Contrato do Projeto**
   - **Membro da Equipa do Projeto**
   - **Detalhe de Item de Proposta**
   - **Margem de Lucro do Preço da Função**
   - **Preço da Função**
   - **Entrada de Hora**
 
   ![Adicionar solução de dimensão de preços personalizados de entidades existentes](./media/Existing-entities-to-PD-solution.png)
 
 4. Para cada entidade, reveja os componentes a ser adicionados e a lista final de ativos de entidade para cada entidade. 

   >[!NOTE]
   > Inclua todos os formulários e vistas para cada uma das entidades selecionadas.

  ![Entidades adicionadas](./media/solution-component-selection.png)


5.  Quando solicitado para incluir quaisquer entidades dependentes para as entidades selecionadas, selecione **Não, não incluir componentes necessários.**

    ![Incluindo entidades dependentes](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]