---
title: Adicionar campos personalizados obrigatórios às entidades de configuração de preços e transacionais
description: Esta tópico fornece informações sobre como adicionar referências de campo personalizadas necessárias às entidades e a formulários e vistas.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: a7268eb33c80f5e35d2ef21a8f4c7ed7ba322e27
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000585"
---
# <a name="add-required-custom-fields-to-price-setup-and-transactional-entities"></a>Adicionar campos personalizados obrigatórios às entidades de configuração de preços e transacionais

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Este tópico parte do princípio de que concluiu os procedimentos no tópico [Criar campos e entidades personalizados para utilizar como dimensões de preços](create-custom-fields-entities-pricing-dimensions.md). Se não tiver concluído esses procedimentos, volte a concluí-los e, em seguida, volte a este tópico. 

Neste tópico, os procedimentos irão mostrar-lhe como adicionar as referências de campo personalizado necessárias a entidades e aos elementos da interface de utilizador (IU), tais como formulários e vistas.

## <a name="add-custom-pricing-dimension-fields"></a>Adicionar campos de dimensão de preços personalizados 
Depois de os campos e as entidades personalizados terem sido criados, o passo seguinte consiste em que as entidades de configuração de preços e transacionais tomem conhecimento de quaisquer entidades personalizadas ou conjuntos de opções criando campos de referência. Dependendo de se a lista de dimensões de definição de preços inclui dimensões do conjunto de opções ou dimensões de entidades ou ambas, siga apenas os passos indicados nas **Dimensões de definição de preços personalizadas baseadas em conjuntos de opções** ou nas **Dimensões de definições de preços personalizadas baseadas em entidades**, ou ambas, respetivamente.

### <a name="option-set-based-custom-pricing-dimensions"></a>Dimensões de definição de preços personalizadas baseadas em conjuntos de opções
Quando uma dimensão de definição de preços personalizada é baseada em conjuntos de opções, é adicionada como um campo às entidades principais. No seguinte procedimento, a **Localização de Trabalho do Recurso** e as **Horas de Trabalho do Recurso** são utilizadas como as dimensões de definição de preços baseadas em conjuntos de opções. Estas têm de ser adicionadas primeiro como campos às entidades de definição de preços, **Preço da Função** e **Margem de Lucro do Preço da Função**.

1. Nas operações do Projeto, selecione **Definições** > **Soluções** e faça clique duplo nas dimensões de preços do **\<your organization name>**. 
2. No Explorador de Soluções, no painel de navegação esquerdo, selecione **Entidades > Preço da Função**.
3. Expanda a entidade **Preço da Função** e selecione **Campos**.
4. Selecione **Novo** para criar um novo campo denominado **Localização de Trabalho do Recurso** e selecione **Conjunto de opções** como o tipo de campo. 
5. Selecione **Utilizar um conjunto de opções existente**, selecione o conjunto de opções de **Localização de Trabalho do Recurso** e, em seguida, selecione **Guardar**.
6. Repita os passos 1 a 5 para adicionar este campo à entidade **Margem de Lucro do Preço da Função**. 
7. Repita os passos 1 a 5 para o conjunto de opções de **Horas de Trabalho do Recurso**.

> [!IMPORTANT]
> Quando adicionar um campo a mais de uma entidade, utilize o mesmo nome de campo em todas as entidades. 

> ![Adicionar Localização de Trabalho do Recurso ao Preço da Função](media/RWL-Field.png)

Nas fases de vendas e estimativas de um projeto, as estimativas do esforço de trabalho necessário para concluir o trabalho **Local** e **No Local**, nas **Horas normais** e nas **Horas extraordinárias** são utilizadas para estimar o valor da Proposta/Projeto. Os campos **Localização de Trabalho do Recurso** e **Horas de Trabalho do Recurso** serão adicionados às entidades de estimativa, **Detalhe de Linha de Proposta**, **Detalhe de Item de Contrato**, **Membro da Equipa do Projeto** e **Linha de Estimativa**.

1. Nas operações do Projeto, selecione **Definições** > **Soluções** e, de seguida, faça clique duplo nas dimensões de preços do **\<your organization name>**. 
2. No Explorador de Soluções, no painel de navegação esquerdo, selecione **Entidades > Detalhe de Linha de Proposta**.
3. Expanda a entidade **Detalhe de Linha de Proposta** e selecione **Campos**.
4. Selecione **Novo** para criar um novo campo denominado **Localização de Trabalho do Recurso** e selecione o tipo de campo, **Conjunto de opções**. 
5. Selecione **Utilizar um conjunto de opções existente** e **Localização de Trabalho do Recurso** e, em seguida, selecione **Guardar**.
6. Repita os passos 1 a 5 para adicionar este campo às entidades **Detalhe de Item de Contrato do Projeto**, **Membro da Equipa do Projeto** e **Linha de Estimativa**.
7. Repita os passos 1 a 6 para o conjunto de opções de **Horas de Trabalho do Recurso**. 

> ![Adicionar Localização de Trabalho do Recurso à Linha de Estimativa](media/RWL-Default-Value.png)

Para a entrega e a faturação, o trabalho concluído tem de ter um preço definido com precisão para selecionar se foi efetuado **Localmente** ou **No Local** e se foi concluído durante as **Horas normais** ou nas **Horas Extraordinárias** nos Valores Reais do Projeto. Os campos **Localização de Trabalho do Recurso** e **Horas de Trabalho do Recurso** devem ser adicionados às entidades **Entrada de Tempo**, **Valor Real**, **Detalhe de Linha de Fatura** e **Linha do Diário**.

1. Selecione **Definições** > **Soluções** e, de seguida, faça clique duplo nas dimensões de preços do **\<your organization name>**.
2. No Explorador de Soluções, no painel de navegação esquerdo, selecione **Entidades > Entrada de Tempo**.
3. Expanda a entidade **Detalhe de Linha de Proposta** e selecione **Campos**.
4. Selecione **Novo** para criar um novo campo denominado **Localização de Trabalho do Recurso** e selecione **Conjunto de opções** como o tipo de campo. 
5. Selecione **Utilizar um conjunto de opções existente**, selecione o conjunto de opções de **Localização de Trabalho do Recurso** e, em seguida, selecione **Guardar**.
6. Repita os passos 1 a 5 para adicionar este campo às entidades **Valor Real**, **Detalhe de Linha de Fatura** e **Linha do Diário**.
7. Repita os passos 1 a 6 para o conjunto de opções de **Horas de Trabalho do Recurso**. 

> ![Adicionar Localização de Trabalho do Recurso à Entrada de Tempo](media/RWL-time-entry.png)

Isto conclui as alterações de esquema necessárias para as dimensões personalizadas baseadas em conjuntos de opções.

## <a name="entity-based-custom-pricing-dimensions"></a>Dimensões de definição de preços personalizadas baseadas em entidades

Quando a dimensão de definição de preços personalizada for uma entidade, irá adicionar relações 1:N entre a entidade de dimensão e as entidades principais. Utilizando o exemplo de Título Padrão acima, é razoável esperar que cada funcionário receba um título padrão. Como resultado, irá precisar de uma relação 1:N a partir do Título Padrão para o Recurso Reservável ou de uma relação N:1 se tiver sido criado a partir do Recurso Reservável para o Título Padrão.

1. Nas operações do Projeto, selecione **Definições** > **Soluções** e, de seguida, faça clique duplo nas dimensões de preços do **\<your organization name>**. 
2. No Explorador de Soluções, no painel de navegação esquerdo, selecione **Entidades > Título Padrão**.
3. Expanda a entidade **Título Padrão** e selecione **Relações 1:N**.
4. Selecione **Novo** para criar uma nova relação 1:N denominada **Título Padrão para Recurso Reservável**. Introduza as informações necessárias e selecione **Guardar**.

> ![Adicionar Título Padrão como campo de referência ao Recurso Reservável](media/ST-BR.png)

Também será necessário adicionar o Título Padrão às entidades definição de preços, **Preço da Função** e **Margem de Lucro do Preço da Função**. Esta opção também é concluída através da utilização de relações 1:N entre as entidades **Título Padrão** e **Preço da Função** e as entidades **Título Padrão** e **Margem de Lucro do Preço da Função**.

1. No Explorador de Soluções, no painel de navegação esquerdo, selecione **Entidades > Título Padrão**.
2. Expanda a entidade **Título Padrão** e selecione **Relações 1:N**.
3. Selecione **Novo** para criar uma nova relação 1:N denominada **Título Padrão para Preço da Função**. Introduza as informações necessárias e selecione **Guardar**.
4. Repita os passos 1 a 4 para criar relações 1:N entre as entidades **Título Padrão** e **Margem de Lucro do Preço da Função**.

Nas fases de vendas e estimativa do projeto, para definir o preço da Proposta/Projeto, são necessárias estimativas do esforço de trabalho para cada título padrão. Isto significa que as relações 1:N do Título Padrão para cada uma destas entidades de estimativa são necessárias: 

- **Detalhe de Linha de Proposta**
- **Detalhe de Item de Contrato do Projeto**
- **Membro da Equipa do Projeto**
- **Linha de Estimativa**

5. Repita os passos 1 a 5 para criar relações 1:N a partir do **Título Padrão** para o **Detalhe de Linha de Proposta**, **Detalhe de Item de Contrato do Projeto**, **Membro da Equipa do Projeto** e **Linha de Estimativa**.

> ![Adicionar Título Padrão como campo de referência à Linha de Estimativa](media/ST-Estimate-Line.png)

  Nas fases Entrega e Faturação, o trabalho concluído por cada título padrão deve ter o preço definido com precisão nos Valores Reais do Projeto. Isto significa que precisa de haver relações 1:N a partir das entidades **Título Padrão** para a **Entrada de Tempo**, **Valor Real**, **Detalhe de Linha de Fatura** e **Linha do Diário**.

6. Repita os passos 1 a 6 para criar relações 1:N a partir das entidades **Título Padrão** para a **Entrada de Tempo**, **Valor Real**, **Detalhe de Linha de Fatura** e **Linha do Diário**.

> ![Adicionar Título Padrão como campo de referência à Entrada de Tempo](media/ST-Mapping.png)

### <a name="set-up-dimension-value-defaulting-using-the-mappings-features-of-the-platform"></a>Configurar a predefinição do valor Dimensão utilizando as funcionalidades de mapeamento da plataforma
Para a Entrada de Tempo, seria útil que o sistema predefini-se o título padrão na Entrada de Tempo a partir do Recurso Reservável que está a registar a entrada de tempo. Utilize os seguintes passos para adicionar mapeamentos de campos na relação 1:N a partir do **Recurso Reservável** para a **Entrada de Tempo**.

1. No Explorador de Soluções, no painel de navegação esquerdo, selecione **Entidades > Título Padrão**.
2. Expanda a entidade **Título Padrão** e selecione **Relações 1:N**.
3. Faça duplo clique em **Recurso Reservável para Entrada de Tempo**. Na página **Relação**, selecione **Utilizar mapeamentos de campos**. 
4. Selecione **Novo** para criar um novo mapeamento de campos entre o campo **Título Padrão** na entidade **Recurso Reservável** para o campo de referência **Título Padrão** na entidade **Entrada de Tempo**. 

> ![Configurar mapeamentos de campos para predefinição do Título Padrão a partir do Recurso Reservável para a Entrada de Tempo](media/ST-Mapping2.png)

Isto conclui as alterações de esquema necessárias para as dimensões personalizadas baseadas em entidades.

##  <a name="add-custom-fields-to-forms-views-and-business-rules"></a>Adicionar campos personalizados a formulários, vistas e regras de negócio

Depois de ter efetuado todas as alterações de esquema necessárias, o próximo passo é tornar os campos visíveis na IU adicionando os campos aos formulários e às vistas.

1. Abra o formulário ou a vista. No painel de navegação direito, selecione o campo e arraste-o para a tela do formulário. 
2. Se estiver a editar uma vista, utilize o painel de navegação direito, selecione **Adicionar campos** e na caixa de diálogo **Listagem de Campos**, selecione os campos necessários e selecione **OK**.

A tabela seguinte fornece uma lista abrangente de formulários e vistas fornecidos com o programa, por entidade, que terão de ser atualizados com os novos campos. Se tiver formulários ou vistas adicionais nas suas personalizações nestas entidades, adicione os campos novos aos mesmos.

| Entity        | Formulários que necessitam do novo campo   |Vistas que necessitam do novo campo      |
| ------------------------------|---------------------------------|----------------------------------|
|  Preço da Função|• Informação |• Preços de Categoria de Recurso Ativos<br> • Vista Associada de Preço de Categoria de Recurso|
|  Margem de Lucro do Preço da Função|• Informação|• Margem de Lucro do Preço da Função Ativa<br>• Vista Associada de Margens de Lucro do Preço da Função|
|  Detalhe de linha de proposta|• Informações do projeto<br>• Criação Rápida de Projeto|• Detalhe de Linha de Proposta Ativo<br>• Detalhes de Linha de Proposta Combinados<br>• Vista associada de Detalhe de Linha de Proposta|
|  Detalhe de Item de Contrato do Projeto|• Informações do projeto<br>• Criação Rápida de Projeto|• Detalhes de Item de Contrato Combinados<br>• Detalhes de Item de Contrato Ativos<br>• Vista Associada de Detalhes de Item de Contrato|
|  Membro da Equipa do Projeto|• Informação<br>• Novo Formulário|• Membros da Equipa do Projeto Ativos<br>• Membros da Equipa do Projeto<br>• Vista associada de membros da Equipa do Projeto|
|  Entrada de Hora|• Informação<br>• Criar Entrada de Tempo|• As Minhas Entradas de Tempo por Data<br>• As minhas Entradas de tempo para esta semana<br>• Entradas de tempo para aprovação|
|  Linha do Diário|• Informação<br>• Criação rápida|• Linhas do diário ativas<br>• Vista associada de Linha do Diário|
|  Detalhe de Linha de Fatura|• Informação<br>• Criação rápida|• Detalhes de Linha de Fatura Ativos<br>• Transações de Fatura Faturáveis<br>• Transações de Fatura Grátis<br>• Vista associada de Detalhe de Linha de Fatura<br>• Transações de Fatura Não Faturáveis|
|  Real|• Informação<br>• Valores Reais Ativos|• Vista associada de Valor Real|

Os campos personalizados também poderão ter de ser adicionados às regras de negócio consoante o que tiver definido. Um exemplo fornecido com o programa destina-se à regra de negócio **Capacidade de Edição da Entrada de Tempo baseada no Estado**. Esta regra define quais campos têm de ser bloqueados quando a Entrada de Tempo se encontra num estado não editável, tal como **Aprovado**. Adicione campos a esta regra de negócio, para que os campos fiquem bloqueados para edição quando a Entrada de Tempo estiver num estado diferente de **Rascunho** ou **Devolvido**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]