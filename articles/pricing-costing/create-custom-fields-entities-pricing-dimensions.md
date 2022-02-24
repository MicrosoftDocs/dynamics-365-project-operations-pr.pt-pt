---
title: Criar campos e entidades personalizados como dimensões de definição de preços
description: Este tópico fornece informações sobre como criar conjuntos de opções ou entidades personalizados.
author: rumant
manager: AnnBe
ms.date: 11/18/2020
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
ms.openlocfilehash: fc5917856b8f28d36dc55593a68eba7823a00b36
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642827"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Criar campos e entidades personalizados como dimensões de definição de preços

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Conclua os seguintes passos quando pretender criar um conjunto de opções ou uma entidade personalizados para utilizar como dimensão de preços. Para mais informações, consulte [Descrição geral de dimensões de preços](pricing-dimensions-overview.md).  

> [!IMPORTANT]
> Recomendamos que efetue todas as alterações de dimensões de definição de preços personalizadas numa solução separada. Esta importante melhor prática proporciona flexibilidade no futuro para atualizar ou remover as alterações, se necessário. Isto também ajudará na reutilização do seu trabalho e facilitará a portabilidade destas alterações para outra instância; depois de ter feito todas as alterações necessárias, exporte esta solução como **Solução gerida** e importe-a para outras instâncias para reutilizar a sua configuração de preços.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Criar campos personalizados e conjuntos de opções na solução de dimensão de definição de preços

Uma dimensão de definição de preços pode ser uma conjunto de opções ou uma entidade. Ambos têm de ser criados na solução de definição de preços. Os passos neste procedimento explicam como criar dimensões baseadas em entidades e dimensões baseadas em conjuntos de opções.

### <a name="entity-based-dimensions"></a>Dimensões baseadas em entidades
Para criar dimensões baseadas em entidades, siga estes passos:

1. Aceda a **Definições** > **Soluções** e, de seguida, faça clique duplo nas dimensões de preços do **\<your organization name>**.
2. No Explorador de Soluções, no painel de navegação esquerdo, selecione **Entidades**.
3. Selecione **Novo** para criar uma nova entidade chamada **Título Padrão**. 
4. Introduza as informações necessárias restantes e selecione **Guardar**.

> ![Definição da entidade de título padrão](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a>Dimensões baseadas em conjuntos de opções 
Pode criar duas dimensões baseadas em conjuntos de opções. 

- Utilize **Localização de Trabalho de Recursos** para monitorizar o preço do trabalho de localização **Doméstica** e o trabalho **No local**. 
- Utilize **Horas de trabalho de recursos** com valores **Regulares** e **Horas Extraordinárias** para aplicar uma margem de lucro quando o trabalho estiver concluído.

O gráfico a seguir proporciona uma vista da dimensão de **Localização de Trabalho de Recursos**. 

> ![Dimensão de definição de preços baseada em conjuntos de opções denominada Localização de Trabalho do Recurso](media/Option-set-PD-called-Resource-Work-Location.png)

O gráfico a seguir proporciona uma vista da dimensão de **Horas de Trabalho de Recursos**. 

> ![Dimensão de definição de preços baseada em conjuntos de opções denominada Horas de Trabalho do Recurso](media/Option-set-PD-called-Resource-Work-Hours.png)

1. Aceda a **Definições** > **Soluções** e faça clique duplo nas dimensões de preços do **\<your organization name>**. 
2. No Explorador de Soluções, no painel de navegação esquerdo, selecione **Conjuntos de Opções**. 
3. Selecione **Novo** para criar um novo conjunto de opções, introduza as informações necessárias restantes e, em seguida, selecione **Guardar**.

## <a name="create-data-for-entity-based-dimensions"></a>Criar dados para as dimensões baseadas em entidades

Pode criar manualmente dados para as dimensões baseadas em entidades ou através da utilização de chamadas de importação ou de serviço do Microsoft Excel. Utilize os passos indicados neste procedimento para criar dois títulos padrão, o **Engenheiro de Sistemas** e o **Engenheiro de Sistemas Sénior** a partir da dimensão baseada em entidades, **Título Padrão**. Se os dados que pretende criar forem pequenos, como no exemplo seguinte, pode utilizar um formulário padrão.

1. Selecione **Localização Avançada**.
2. Selecione a entidade **Título Padrão** e, em seguida, selecione **Resultados**. Serão mostradas todas as linhas na entidade **Título Padrão**.
3. Selecione **Novo**, e no campo **Nome**, introduza "Engenheiro de Sistemas" e selecione **Guardar**.
4. Feche a página. 
5. Repita os passos 1 a 3 para criar outro título padrão para o "Engenheiro de Sistemas Sénior".

> ![Dados de exemplo para a entidade Título Padrão](media/ST-data.png)
