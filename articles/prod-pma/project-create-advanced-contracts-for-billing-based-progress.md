---
title: Criar contratos avançados para faturação baseada em progresso
description: Este tópico explica como criar contratos de projeto para que possa gerar faturas para os clientes, com base numa percentagem de trabalho concluído.
author: RadhikaRS
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: bdafc2ed2398054d8b0bf42bdd96dfe0eccee93b
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683177"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a>Criar contratos avançados para faturação baseada em progresso
[!include [banner](../includes/banner.md)]

Este tópico explica como criar contratos de projeto para que possa criar faturas para os clientes, com base numa percentagem de trabalho concluído. Os valores da fatura são automaticamente calculados para as categorias orçamentais de trabalho que configura para um projeto. O calendário da fatura é definido quando negoceia o contrato do projeto com o cliente.

Utilize os procedimentos deste tópico para configurar um contrato, um projeto associado e as regras de faturação que calculam os valores da fatura para as categorias orçamentais de trabalho que criou para o projeto.

Depois de ter criado o contrato e o projeto, pode configurar os detalhes do projeto. Por exemplo, pode definir atividades e atribuir trabalhadores ao projeto.

## <a name="example"></a>Exemplo

A sua organização é uma empresa de programação de software. Concorda em programar um pacote de contabilidade de pagamento para um cliente por uma taxa total de 20.000 dólares americanos (USD). A sua organização concorda em faturar o cliente à medida que completa percentagens específicas do projeto. Configura as seguintes categorias de projetos para o trabalho, para que possa usá-las no processo de faturação:

- Consultadoria
- Design
- Instalação

Configura também regras de faturação que calculam automaticamente os montantes da fatura para a percentagem de trabalho do projeto que está concluída em cada categoria.

O gestor orçamental cria um orçamento para as categorias de projeto. O montante do trabalho concluído é calculado automaticamente em percentagem do trabalho efetivo em comparação com os montantes orçamentados.

## <a name="prerequisites"></a>Pré-requisitos

Antes de criar um projeto que utilize regras de faturação, tem de configurar as sequências de números para as regras de faturação e um diário de honorários que é usado para publicar faturações de progresso.

1. Vá para **Gestão de projetos e contabilística** \> **Configurar** \> **Parâmetros da Gestão de projetos e contabilística**.
2. Na página de **Parâmetros da Gestão de projetos e contabilística**, no separador **Sequências de números**, configure a sequência de números que pretende utilizar quando as regras de faturação forem criadas.
3. Vá a **Gestão de projetos e contabilística** \> **Diários** \> **Honorários**.
4. Na página do **Diário de Honorários**, selecione **Novo** e insira o nome do diário.

## <a name="create-a-contract-for-progress-billings"></a>Criar um contrato para faturações de progresso

Utilize este procedimento para criar um contrato de projeto para um projeto de preço fixo. Cria uma fatura de projeto quando o trabalho que está concluído no projeto atinge uma percentagem especificada.

1. Vá a **Gestão de projetos e contabilística** \> **Projetos** \> **Contratos de Projeto**.
2. Na página **Contratos de projeto**, selecione **Novo**.
3. Na caixa de diálogo do **Novo contrato de projeto**, defina os seguintes campos:

    - **Nome**
    - **Tipo de financiamento**
    - **Fonte de financiamento**
    - **Moeda das Vendas** – Por predefinição, esta moeda é utilizada para faturas de clientes associadas ao contrato do projeto. No entanto, pode alterar a moeda de vendas numa fatura específica do cliente.

4. Selecione **OK**. As informações são copiadas para o cabeçalho da página **Contratos de projeto**.
5. Na página **Contratos de projeto**, preencha o resto das informações necessárias para o projeto.

## <a name="create-a-project-for-progress-billings"></a>Criar um projeto para faturações de progresso

Siga estes passos para criar um projeto e quaisquer subprojetos associados a um contrato de projeto.

1. Vá para **Gestão de projetos e contabilística** \> **Projetos** \> **Todos os projetos**.
2. Na página **Todos os projetos**, selecione **Novo**.
3. Na caixa de diálogo **Novo projeto**, no campo **Tipo de projeto**, selecione **Tempo e material**.
4. Selecionar um grupo de projeto. Um grupo de projeto define as informações de publicação para os projetos que são atribuídos ao grupo.
5. Selecione **Criar projeto**.
6. Após a criação do projeto, defina a fase do projeto com **A processar**.

## <a name="create-a-budget-for-a-project"></a>Criar um orçamento para um projeto

Categorias de orçamento são utilizadas para calcular automaticamente os montantes da fatura para a percentagem de trabalho que está concluída para cada categoria. Siga estes passos para criar categorias orçamentais para os custos estimados.

1. Vá para **Gestão de projetos e contabilística** \> **Projetos** \> **Todos os projetos**.
2. Na página **Todos os projetos**, selecione e abra o projeto que deseja.
3. Na página **Projetos**, no Painel de Ação, no separador **Plano**, no grupo **Orçamento**, selecione **Orçamento do projeto**.
4. Na página do **Orçamento do projeto**, insira um custo estimado para cada categoria no projeto.

## <a name="create-billing-rules-for-progress-billings"></a>Criar regras de faturação para faturações de progresso

1. Vá a **Gestão de projetos e contabilística** \> **Projetos** \> **Contratos de Projeto**.
2. Na página **Contratos do projeto**, selecione e abra um contrato do projeto.
3. Na página do contrato do projeto, no Separador Rápido **Regras de faturação**, selecione **Adicionar**.
4. Na página da **Regra de faturação**, no campo **Tipo de linha**, selecione **Progresso**.
5. No Separador Rápido **Detalhes da linha de regra de faturação**, no campo **Valor do contrato**, insira o valor total do contrato.
6. No campo **Categoria**, selecione a categoria para onde publicar a transação de honorários.
7. No campo **Projeto**, selecione o projeto que utiliza esta regra de faturação.
8. Opcional: Atribua a regra de faturação a projetos adicionais. No Separador Rápido **Projeto**, na secção **Projetos disponíveis**, selecione um projeto e, em seguida, selecione o botão de seta para a direita para adicionar o projeto à secção **Projetos selecionados**.
9. Opcional: Calcule o montante percentual que o cliente retém dos pagamentos numa fatura. No Separador Rápido **Termos de sinal de pagamento**, selecione a origem do financiamento e, em seguida, no campo **Percentagem de sinal**, insira a percentagem de sinal.
10. Repita estes passos para criar regras adicionais de faturação para o contrato do projeto.


[!INCLUDE[footer-include](../includes/footer-banner.md)]