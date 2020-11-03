---
title: Criar soluções personalizadas para dimensões de preços
description: Este tópico explica como criar uma solução personalizada ao criar dimensões de preços personalizados.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 3e437fce5b9f1fb330a713788e24100a4fe02948
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082413"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a>Criar soluções personalizadas para dimensões de preços

> [!IMPORTANT]
> Todas as alterações às dimensão de preços personalizados devem estar numa solução separada. Essa melhor prática importante fornece flexibilidade no futuro para atualizar ou remover as alterações, conforme necessário, ajudará na reutilização do seu trabalho e facilita a portabilidade destas alterações para outra instância. Depois de efetuar todas as alterações necessárias, exporte esta solução como uma **Solução Gerida** e importe-a para outras instâncias para reutilizar a configuração de preços.

1. Selecione **Definições** > **Soluções** e, em seguida, selecione **Nova**. 
2. Atribua um nome à solução, **\<your organization name> dimensões de definição de preços** , introduza as informações necessárias restantes e, em seguida, selecione **Guardar**.

> ![Criar uma solução personalizada para dimensões de definição de preços](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Adicionar todas as entidades obrigatórias e componentes relacionados necessários à Solução de dimensão de preços
Terá de adicionar as seguintes entidades do Project Service à Solução de Definição de Preços. Conclua os passos indicados neste procedimento para efetuar algumas alterações de esquema importantes na solução de definição de preços, para que as entidades tomem conhecimento das novas dimensões de preços.

1. Selecione **Definições** > **Soluções** e, de seguida, faça clique duplo nas dimensões de preços do **\<your organization name>**. 
2. No Explorador de Soluções, no painel de navegação esquerdo, selecione **Adicionar Existente** > **Entidades**.
3. Na caixa de diálogo **Componentes da Solução** , selecione as seguintes entidades:

- Valor Real
- Recurso Reservável
- Linha de Estimativa
- Tarefa de Projeto
- Detalhe de Linha de Fatura
- Linha do Diário
- Detalhe de Item de Contrato do Projeto
- Membro da Equipa do Projeto
- Detalhe de Item de Proposta
- Margem de Lucro do Preço da Função
- Preço da Função 
- Entrada de Hora 

> ![Adicionar as entidades existentes à solução de dimensões de definição de preços](media/Existing-entities-to-PD-solution.png)

> ![Selecionar componentes da solução](media/Dimension-Components.png)

> [!NOTE]
> Certifique-se de que inclui todos os formulários e vistas para cada uma das entidades selecionadas.

4. Quando lhe for pedido para incluir entidades dependentes relativas às entidades selecionadas, selecione **Não**.

> ![Não incluir todos os componentes relacionados](media/Do-not-include-required.png)


