---
title: Configurar campos personalizados como dimensões de definição de preços
description: Este tópico fornece informações sobre como configurar as dimensões de definição de preços usando campos personalizados.
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
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3a2a3b48df02853e519a45dc1d37052c8ba2529d
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896610"
---
# <a name="set-up-custom-fields-as-pricing-dimensions"></a>Configurar campos personalizados como dimensões de definição de preços

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Antes de começar, este tópico parte do princípio de que concluiu os procedimentos nos tópicos [Criar campos e entidades personalizados](create-custom-fields-entities-pricing-dimensions.md) e [Adicionar campos personalizados obrigatórios às entidades de configuração de preços e transacionais](add-custom-fields-price-setup-transactional-entities.md). Se não tiver concluído esses procedimentos, volte a concluí-los e, em seguida, volte a este tópico. 

Esta tópico fornece informações sobre a configuração de dimensões de definição de preços personalizadas. Na página **Parâmetros**, o separador **Dimensões de Definição de Preços Baseada no Montante** mostra os registos nas entidades de dimensão de definição de preços. Por padrão, existem duas linhas na grelha neste separador:

- **msdyn_resourcecategory** (Função)
- **msdyn_OrganizationalUnit** (Unidade Organizacional)

> [!IMPORTANT]
> Não elimine estas linhas. No entanto, se não necessitar das mesmas, pode fazer com que as mesmas não se apliquem num contexto específico através da definição de **Aplicável ao Custo**, **Aplicável às Vendas** e **Aplicável à Compra** como **Não**. A definição destes valores de atributo como **Não** tem o mesmo efeito de não ter o campo como uma dimensão de definição de preços.

Para que um campo se torne uma dimensão de definição de preços, tem de ser:

- Criado como um campo nas entidades **Preço da Função** e **Margem de Lucro do Preço da Função**. Para mais informações sobre como fazer isso, consulte [Adicionar campos personalizados às entidades de configuração de preços e transacionais](add-custom-fields-price-setup-transactional-entities.md).
- Criado como uma linha na tabela **Dimensões de Definição de Preços**. Por exemplo, adicione linhas de dimensão de definição de preços, conforme mostrado no gráfico seguinte. 

As horas de Trabalho do Recurso (**msdyn_resourceworkhours**) são adicionadas como uma dimensão baseada na margem de lucro e foram adicionadas à grelha no separador **Dimensão de Definição de Preços Baseada na Margem de Lucro**.

> [!IMPORTANT]
> Qualquer alteração nos dados da dimensão de definição de preços nesta tabela, existente ou nova, é propagada para a lógica de negócio de definição de preços apenas após a atualização da cache. O tempo de atualização da cache poderá demorar até 10 minutos. Aguarde esse período de tempo para ver as alterações na lógica de predefinição de preços que devem resultar das alterações efetuadas nos dados de Dimensão de Definição de Preços.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Atributos da tabela Dimensões de Definição de Preços
As secções seguintes fornecem informações sobre os diferentes atributos na tabela **Dimensões de Definição de Preços**.

### <a name="pricing-dimension-name"></a>Nome da Dimensão de Definição de Preços
Este valor deve ser o mesmo que o nome do esquema do campo que é adicionado à tabela **Preço da Função** para as dimensões de definição de preços personalizadas. Para mais informações sobre a adição de campos à tabela **Preço da Função**, consulte [Adicionar campos personalizados às entidades de configuração de preços e transacionais](add-custom-fields-price-setup-transactional-entities.md).

### <a name="type-of-dimension"></a>Tipo de dimensão
Existem dois tipos de dimensões de definição de preços:
  
  - **Dimensões baseadas no montante**: os valores de dimensão do contexto de entrada correspondem aos valores de dimensão na linha **Preço da Função** e o preço/custo é predefinido diretamente da tabela **Preço da Função**.
  - **Dimensões baseadas na margem de lucro**: são as dimensões nas quais é usado o seguinte processo de 3 passos para obter o preço/custo:
 
    1. Os valores de dimensão não baseados na margem de lucro do contexto de entrada correspondem à linha Preço da Função para obter a taxa base.
    2. Os valores de dimensão do contexto de entrada correspondem à linha **Margem de Lucro do Preço da Função** para obter a percentagem da margem de lucro.
    3. A percentagem de margem de lucro do segundo passo aplica-se à taxa base obtida na tabela **Preço da Função** no primeiro passo para chegar ao preço/custo final.
   
   A tabela seguinte ilustra o cálculo de margens de lucro do preço.
  
| Função        | Unidade Organizacional    |Localização do Trabalho      |Título Padrão      |Horas de Trabalho do Recurso      |  Margem de Lucro|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Contoso India|No Local            |                    |Horas Extraordinárias                 |15     |
|             | Contoso India|Região             |                    |Horas Extraordinárias                 |10     |
|             | Contoso EUA   |Região             |                    |Horas Extraordinárias                 |20     |


Se um recurso da Contoso India, cuja taxa base é de 100 USD, estiver a funcionar no local e registar 8 horas de tempo Normal e 2 horas extraordinárias na entrada de tempo, o motor de definição de preços irá utilizar a taxa base de 100 pelas 8 horas para registar 800 USD. Nas duas horas extraordinárias, uma margem de lucro de 15% será aplicada à taxa base de 100 para obter um preço unitário de 115 USD e irá registar um custo total de 230 USD.

### <a name="applicable-to-cost"></a>Aplicável ao Custo 
Se estiver definido como **Sim**, indica que o valor de dimensão do contexto de entrada deve ser utilizado para corresponder ao **Preço da Função** e **Margem de Lucro do Preço da Função** ao obter as taxas de custo e de margem de lucro.

### <a name="applicable-to-sales"></a>Aplicável às Vendas
Se estiver definido como **Sim**, indica que o valor de dimensão do contexto de entrada deve ser utilizado para corresponder ao **Preço da Função** e **Margem de Lucro do Preço da Função** ao obter as taxas de faturação e de margem de lucro.

### <a name="applicable-to-purchase"></a>Aplicável à Compra
Se estiver definido como **Sim**, indica que o valor de dimensão do contexto de entrada deve ser utilizado para corresponder ao **Preço da Função** e **Margem de Lucro do Preço da Função** ao obter o preço de compra. Os cenários de subcontratação não são suportados, pelo que este campo não é utilizado. 

### <a name="priority"></a>Prioridade
Definir a prioridade da dimensão ajuda os preços a apresentar um preço, mesmo quando não é possível encontrar uma correspondência exata entre os valores da dimensão de entrada e os valores das tabelas **Preço da Função** ou **Margem de Lucro do Preço da Função**. Nesse cenário, os valores nulos são usados para valores de dimensão não correspondidos, ponderando as dimensões por ordem de prioridade.

- **Prioridade ao Custo**: o valor da prioridade de custo de uma dimensão irá indicar o peso dessa dimensão quando comparado com a configuração dos preços de custo. O valor de **Prioridade ao Custo** tem de ser exclusivo nas dimensões **Aplicáveis ao Custo**.
- **Prioridade às Vendas**: o valor da prioridade de vendas de uma dimensão irá indicar o peso dessa dimensão quando comparado com a configuração dos preços de venda ou taxas de faturação. O valor de **Prioridade às Vendas** tem de ser exclusivo nas dimensões **Aplicáveis às Vendas**.
