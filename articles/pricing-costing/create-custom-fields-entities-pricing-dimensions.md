---
title: Criar campos e entidades personalizados como dimensões de definição de preços
description: Este tópico fornece informações sobre como criar conjuntos de opções ou entidades personalizados.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 2000f7e710267560fe2bd52b0e33024617d108ea
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898275"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Criar campos e entidades personalizados como dimensões de definição de preços

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Conclua os seguintes passos sempre que pretender criar um conjunto de opções ou uma entidade personalizada.

> [!IMPORTANT]
> Recomendamos que efetue todas as alterações de dimensões de definição de preços personalizadas numa solução separada. Essa melhor prática importante fornece flexibilidade no futuro para atualizar ou remover as alterações, conforme necessário, ajudará na reutilização do seu trabalho e facilita a portabilidade destas alterações para outra instância. Depois de ter efetuado todas as alterações necessárias, exporte esta solução como uma **Solução Gerida** e importe-a para outras instâncias para reutilizar a configuração de preços.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Criar uma solução personalizada para dimensões de definição de preços
1. Aceda a **Definições** > **Soluções** e, em seguida, selecione **Novo** para criar uma nova solução. 
2. Atribua um nome à solução, **\<your organization name> dimensões de definição de preços**, introduza as informações necessárias restantes e, em seguida, selecione **Guardar**.
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Criar campos personalizados e conjuntos de opções na solução de dimensão de definição de preços

Uma dimensão de definição de preços pode ser uma conjunto de opções ou uma entidade. Ambos têm de ser criados na solução de definição de preços. Os passos neste procedimento explicam como criar dimensões baseadas em entidades e dimensões baseadas em conjuntos de opções.

### <a name="entity-based-dimensions"></a>Dimensões baseadas em entidades

1. Aceda a **Definições** > **Soluções** e, de seguida, faça clique duplo nas dimensões de preços do **\<your organization name>**.
2. No Explorador de Soluções, no painel de navegação esquerdo, selecione **Entidades**.
3. Selecione **Novo** para criar uma nova entidade chamada **Título Padrão**. 
4. Introduza as informações necessárias restantes e selecione **Guardar**.


### <a name="option-set-based-dimensions"></a>Dimensões baseadas em conjuntos de opções 
Pode criar duas dimensões baseadas em conjuntos de opções. Utilize **Localização do Trabalho do Recurso** para monitorizar o preço do trabalho da localização **Principal** e o trabalho **No Local** e utilize **Horas de Trabalho do Recurso** com os valores **Normais** e **Horas Extraordinárias** para aplicar uma margem de lucro quando o trabalho estiver concluído.


1. Aceda a **Definições** > **Soluções** e faça clique duplo nas dimensões de preços do **\<your organization name>**. 
2. No Explorador de Soluções, no painel de navegação esquerdo, selecione  **Conjuntos de Opções**. 
3. Selecione **Novo** para criar um novo conjunto de opções, introduza as informações necessárias restantes e, em seguida, selecione **Guardar**.

## <a name="create-data-for-entity-based-dimensions"></a>Criar dados para as dimensões baseadas em entidades

Pode criar manualmente dados para as dimensões baseadas em entidades ou através da utilização de chamadas de importação ou de serviço do Microsoft Excel. Utilize os passos indicados neste procedimento para criar dois títulos padrão, o **Engenheiro de Sistemas** e o **Engenheiro de Sistemas Sénior** a partir da dimensão baseada em entidades, **Título Padrão**. Se os dados que pretende criar forem pequenos, como no exemplo seguinte, pode utilizar um formulário padrão.

1. Selecione **Pesquisa avançada**, selecione o **Título padrão** da entidade e, em seguida, selecione **Resultados**. Serão mostradas todas as linhas na entidade **Título Padrão**.
2. Selecione **Novo**, e no campo **Nome**, introduza "Engenheiro de Sistemas" e selecione **Guardar**.
3. Fechar o formulário. 
4. Repita os passos 1 a 3 para criar outro título padrão para o "Engenheiro de Sistemas Sénior".

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Adicionar todas as entidades obrigatórias e componentes relacionados necessários à Solução de Dimensão de Definição de Preços
Terá de adicionar as seguintes entidades à Solução de Definição de Preços. Utilize os passos indicados neste procedimento para efetuar algumas alterações de esquema importantes na solução de definição de preços, para que as entidades tomem conhecimento das novas dimensões de definição de preços.

1. Selecione **Definições** > **Soluções** e faça clique duplo nas dimensões de preços do **\<your organization name>**. 
2. No Explorador de Soluções, no painel de navegação esquerdo, selecione **Adicionar Existente** > **Entidades**.
3. Na caixa de diálogo **Componentes da Solução**, selecione as seguintes entidades:

  - Real
  - Recurso Reservável
  - Linha de Estimativa
  - Detalhe de Linha de Fatura
  - Linha do Diário
  - Detalhe de Item de Contrato do Projeto
  - Membro da Equipa do Projeto
  - Detalhe de Linha de Proposta
  - Margem de Lucro do Preço da Função
  - Preço da Função 
  - Entrada de Hora 


> [!NOTE]
> Certifique-se de que inclui todos os formulários e vistas para cada uma das entidades selecionadas.

4. Quando lhe for pedido para incluir entidades dependentes relativas às entidades selecionadas acima, selecione **Não**.

