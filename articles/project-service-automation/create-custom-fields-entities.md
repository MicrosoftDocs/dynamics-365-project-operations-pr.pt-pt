---
title: Criar campos e entidades personalizados
description: Este tópico explica como criar conjuntos de opções e entidades na sua própria solução na plataforma Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754601"
---
# <a name="create-custom-fields-and-entities"></a>Criar campos e entidades personalizados 

Conclua os seguintes passos sempre que pretender criar um conjunto de opções ou uma entidade personalizada na plataforma Power Apps.  
Os procedimentos existentes neste tópico devem ser concluídos utilizando a interface Web do Project Service Automation (PSA).

> [!IMPORTANT]
> Recomendamos que efetue todas as alterações de dimensões de definição de preços personalizadas numa solução separada. Essa melhor prática importante fornece flexibilidade no futuro para atualizar ou remover as alterações, conforme necessário, ajudará na reutilização do seu trabalho e facilita a portabilidade destas alterações para outra instância. Depois de ter efetuado todas as alterações necessárias, exporte esta solução como uma **Solução Gerida** e importe-a para outras instâncias para reutilizar a configuração de preços.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Criar uma solução personalizada para dimensões de definição de preços
1. No PSA, clique em **Definições** > **Soluções** e, em seguida, clique em **Novo** para criar uma nova solução. 
2. Atribua um nome à solução, **\<o nome da sua organização > dimensões de definição de preços**, introduza as informações necessárias restantes e, em seguida, clique em **Guardar**.

> ![Criar uma solução personalizada para dimensões de definição de preços](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Criar campos personalizados e conjuntos de opções na solução de dimensão de definição de preços

Uma dimensão de definição de preços pode ser uma conjunto de opções ou uma entidade. Ambos têm de ser criados na solução de definição de preços. Os passos neste procedimento explicam como criar dimensões baseadas em entidades e dimensões baseadas em conjuntos de opções.

### <a name="entity-based-dimensions"></a>Dimensões baseadas em entidades

1. No PSA, clique em **Definições** > **Soluções** e faça duplo clique no **\<nome da sua organização> dimensões de definição de preços**.
2. No Explorador de Soluções, no painel de navegação esquerdo, selecione **Entidades**.
3. Clique em **Novo** para criar uma nova entidade chamada **Título Padrão**. Introduza as informações necessárias restantes e clique em **Guardar**.

> ![Definição da entidade de título padrão](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Dimensões baseadas em conjuntos de opções 
Pode criar duas dimensões baseadas em conjuntos de opções. Utilize **Localização do Trabalho do Recurso** para monitorizar o preço do trabalho da localização **Principal** e o trabalho **No Local** e utilize **Horas de Trabalho do Recurso** com os valores **Normais** e **Horas Extraordinárias** para aplicar uma margem de lucro quando o trabalho estiver concluído.


1. No PSA, clique em **Definições** > **Soluções** e faça duplo clique no  **\<nome da sua organização> dimensões de definição de preços**. 
2. No Explorador de Soluções, no painel de navegação esquerdo, selecione  **Conjuntos de Opções**. 
3. Clique em **Novo** para criar um novo conjunto de opções, introduza as informações necessárias restantes e, em seguida, clique em **Guardar**.

> ![Dimensão de definição de preços baseada em conjuntos de opções denominada Localização de Trabalho do Recurso ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Dimensão de definição de preços baseada em conjuntos de opções denominada Horas de Trabalho do Recurso ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Criar dados para as dimensões baseadas em entidades

Pode criar manualmente dados para as dimensões baseadas em entidades ou através da utilização de chamadas de importação ou de serviço do Microsoft Excel. Utilize os passos indicados neste procedimento para criar dois títulos padrão, o **Engenheiro de Sistemas** e o **Engenheiro de Sistemas Sénior** a partir da dimensão baseada em entidades, **Título Padrão**. Se os dados que pretende criar forem pequenos, como no exemplo seguinte, pode utilizar um formulário padrão.

1. No PSA, clique em **Localização Avançada**. Selecione a entidade **Título Padrão** e, em seguida, clique em **Resultados**. Serão mostradas todas as linhas na entidade **Título Padrão**.
2. Clique em **Novo**. No campo **Nome**, introduza "Engenheiro de Sistemas" e clique em **Guardar**.
3. Feche o formulário. 
4. Repita os passos 1 a 3 para criar outro título padrão para o "Engenheiro de Sistemas Sénior".

> ![Dados de Exemplo para a Entidade Título Padrão ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a>Adicionar todas as entidades do PSA e componentes relacionados necessários à Solução de Dimensão de Definição de Preços
Terá de adicionar as seguintes entidades do Project Service à Solução de Definição de Preços. Utilize os passos indicados neste procedimento para efetuar algumas alterações de esquema importantes na solução de definição de preços, para que as entidades tomem conhecimento das novas dimensões de definição de preços.

1. No PSA, clique em **Definições** > **Soluções** e faça duplo clique no **\<nome da sua organização> dimensões de definição de preços**. 
2. No Explorador de Soluções, no painel de navegação esquerdo, selecione **Adicionar Existente** > **Entidades**.
3. Na caixa de diálogo **Componentes da Solução**, selecione as seguintes entidades:

- Real
- Recurso Reservável
- Linha de Estimativa
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

4. Quando lhe for pedido para incluir entidades dependentes relativas às entidades selecionadas acima, clique em **Não**.

> ![Não incluir todos os componentes relacionados](media/Do-not-include-required.png)


