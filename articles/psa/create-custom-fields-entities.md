---
title: Criar campos e entidades personalizados
description: Este tópico explica como criar conjuntos de opções e entidades na sua própria solução na plataforma Power Apps.
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
ms.openlocfilehash: b9e32c8871a8986ba827f742baf4e4d5cd9dd235
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144877"
---
# <a name="create-custom-fields-and-entities"></a>Criar campos e entidades personalizados 

[!include [banner](../includes/psa-now-project-operations.md)]

Conclua os seguintes passos sempre que pretender criar um conjunto de opções ou uma entidade personalizada na plataforma Power Apps.  
Os procedimentos existentes neste tópico devem ser concluídos utilizando a interface Web do Project Service Automation (PSA).

> [!IMPORTANT]
> Recomendamos que efetue todas as alterações de dimensões de definição de preços personalizadas numa solução separada. Essa melhor prática importante fornece flexibilidade no futuro para atualizar ou remover as alterações, conforme necessário, ajudará na reutilização do seu trabalho e facilita a portabilidade destas alterações para outra instância. Depois de ter efetuado todas as alterações necessárias, exporte esta solução como uma **Solução Gerida** e importe-a para outras instâncias para reutilizar a configuração de preços.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Criar campos personalizados e conjuntos de opções na solução de dimensão de definição de preços

Uma dimensão de definição de preços pode ser uma conjunto de opções ou uma entidade. Ambos têm de ser criados na solução de definição de preços. Os passos neste procedimento explicam como criar dimensões baseadas em entidades e dimensões baseadas em conjuntos de opções.

### <a name="entity-based-dimensions"></a>Dimensões baseadas em entidades

1. Em PSA, clique em **Definições** > **Soluções** e, em seguida, faça clique duplo nas dimensões de preços do **\<your organization name>**.
2. No Explorador de Soluções, no painel de navegação esquerdo, selecione **Entidades**.
3. Clique em **Novo** para criar uma nova entidade chamada **Título Padrão**. Introduza as informações necessárias restantes e clique em **Guardar**.

> ![Definição da entidade de título padrão](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Dimensões baseadas em conjuntos de opções 
Pode criar duas dimensões baseadas em conjuntos de opções. Utilize **Localização do Trabalho do Recurso** para monitorizar o preço do trabalho da localização **Principal** e o trabalho **No Local** e utilize **Horas de Trabalho do Recurso** com os valores **Normais** e **Horas Extraordinárias** para aplicar uma margem de lucro quando o trabalho estiver concluído.


1. Em PSA, clique em **Definições** > **Soluções** e, em seguida, faça clique duplo nas dimensões de preços do **\<your organization name>**. 
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


