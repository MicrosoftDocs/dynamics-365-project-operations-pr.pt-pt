---
title: Trabalhar com o modelo de dados do Project Service Automation
description: Este tópico fornece informações sobre como trabalhar com o modelo de dados.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 9bceb96153f0e9f5c0d40478baf691220de95f27
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642692"
---
# <a name="working-with-the-project-service-automation-data-model"></a>Trabalhar com o modelo de dados do Project Service Automation

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

O Dynamics 365 Project Service Automation expande outras entidades de aplicação e introduz as suas próprias entidades no modelo de dados do Common Data Service. Este tópico descreve algumas das entidades que irá encontrar nos cenários de relatórios PSA comuns.

## <a name="reporting-on-opportunities"></a>Relatórios sobre oportunidades

O Project Service Automation expande a entidade **Oportunidade** do Dynamics 365 Sales adicionando campos que permitem cenários baseados em projetos. Estes campos são identificados por um nome de esquema que tem o prefixo **msdyn\_**. Um novo campo importante para reportar oportunidades do PSA é **Tipo de Encomenda**. Um valor de **Baseado em Trabalho** para este campo indica que a oportunidade é uma oportunidade do PSA. Os outros campos que tenham sido adicionados à entidade incluem a **Organização de Contratação**, que captura a organização que contém a oportunidade e o **Gestor de Contas**, que captura o nome do gestor de contas que é responsável pela oportunidade.

A entidade **Linha de Oportunidade** também inclui campos relacionados com o Project Service. O **Método de Faturação** indica se a linha de oportunidade deve ser faturada com base no tempo e nos materiais ou numa base de preço fixo, e o **Projeto** captura o nome do projeto que está a apoiar a oportunidade. Outros campos que pode reportar sobre custos de captura e valores de orçamento do cliente para o item de linha.

## <a name="reporting-on-quotes"></a>Relatórios sobre propostas

O PSA expande a entidade **Proposta** de Vendas adicionando campos relacionados com o projeto. O **Tipo de Encomenda** distingue propostas PSA de propostas não PSA. Um valor de **Baseado em Trabalho** para este campo indica que a proposta é uma proposta de PSA. Os outros campos que podem ser relevantes para gerar relatórios sobre propostas de PSA incluem campos de montante, tais como **Custos Faturáveis**, **Custos Não Faturáveis**, **Margem Bruta**, **Estimativas** e **Orçamento**. Outros campos úteis indicam se a proposta é lucrativa, se a mesma será concluída na agenda e se a mesma cumpre as expectativas de orçamento do cliente.

O PSA também expande a entidade **Linha de Proposta** de Vendas. Um campo que o PSA adiciona é o **Método de Faturação**, que indica o modo como a linha de proposta será faturada (tempo e materiais ou preço fixo). Outros campos que tenham sido adicionados à entidade capturam o projeto relacionado que está a apoiar a linha de proposta, a faturação, o custo e o orçamento.

O PSA também adiciona novas entidades relacionadas com propostas ao modelo de dados do Dynamics 365. Seguem-se alguns exemplos:

- **Detalhe de Linha de Proposta** – Esta entidade contém os detalhes da estimativa do projeto da linha de proposta. Tem dois registos para cada linha de proposta. Um registo armazena o custo e os detalhes de custo da linha de proposta e o outro registo armazena o montante de vendas e os detalhes de vendas da linha de proposta.
- **Agenda de Faturação de Linha de Proposta** – Esta entidade contém a agenda de faturação para a linha de proposta. Esta agenda é gerada com base na frequência de faturação atribuída à linha de proposta.
- **Marco da Linha de Proposta** – Esta entidade contém os marcos de faturação para linhas de proposta de preço fixo.
- **Divisão de Análise da Linha de Proposta** – Esta entidade contém os detalhes financeiros da linha de proposta. Estes detalhes podem ser úteis para reportar os valores de vendas propostas e custos estimados por diversas dimensões.

As outras entidades que o PSA adiciona às propostas são **Linha de Proposta: Lista de Preços do Projeto**, **Linha de Proposta: Categoria de Recurso** e **Linha de Proposta: Categoria de Transação**.

![Diagrama que mostra as relações entre a proposta, a linha de proposta e o projeto](media/PS-Reporting-image2.png "Diagrama que mostra as relações entre a proposta, a linha de proposta e o projeto")

## <a name="reporting-on-project-contracts"></a>Relatórios sobre contratos do projeto

O PSA expande a entidade **Ordem** de Venda utilizada quando os contratos do projeto são registados. Adiciona um novo campo importante, **Tipo de Encomenda**, que identifica o contrato como um contrato do projeto do PSA em vez de uma ordem de venda. Um valor de **Baseado em Trabalho** para este campo indica que a encomenda é um contrato do projeto do PSA. Outros novos campos que são adicionados à entidade **Encomenda** capturam os detalhes sobre os custos, o estado do contrato do PSA e a organização que é proprietária do contrato.

O PSA também expande a entidade **Linha da Ordem de Venda**. Entre os campos adicionados, estão os que capturam o método de faturação (tempo e materiais ou preço fixo), valores do orçamento do cliente e o projeto subjacente.

O PSA também adiciona novas entidades que foram concebidas para contratos do projeto. Seguem-se alguns exemplos:

- **Detalhe de Item de Contrato do Projeto** – Esta entidade contém os detalhes ao nível da linha que são acumulados até ao montante do item de contrato. Podem ser tão detalhados quanto os itens de linha gerados a partir de uma agenda do projeto ao nível da tarefa.
- **Agenda de Faturação de Item de Contrato** – Esta entidade contém a agenda de faturação gerada com base na frequência da faturação que é atribuída ao item de contrato.
- **Marco do Contrato** – Esta entidade contém os marcos de faturação para os itens de contrato que têm um período de faturação de preço fixo.

As outras entidades que o PSA adiciona aos contratos são **Item de Contrato do Projeto: Lista de Preços do Projeto**, **Item de Contrato do Projeto: Categoria de Recurso** e **Item de Contrato do Projeto: Categoria de Transação**.

![Diagrama que mostra as relações entre a encomenda, a linha de encomenda e o projeto](media/PS-Reporting-image3.png "Diagrama que mostra as relações entre a encomenda, a linha de encomenda e o projeto")

## <a name="reporting-on-projects"></a>Relatórios sobre projetos

A entidade **Projetos** e as suas entidades relacionadas são exclusivas do PSA. **Projeto** é a entidade de nível superior utilizada para capturar o lado do trabalho e do custo das operações. Segue-se uma lista das entidades relacionadas:

- **Membro da equipa do projeto** – Esta entidade contém detalhes sobre os recursos reserváveis que estão atribuídos ao projeto. Estes recursos podem ser recursos reserváveis genéricos ou podem ser nomeados recursos reserváveis que são introduzidos pelo gestor de projeto ou gerados a partir da agenda do projeto.
- **Tarefa do Projeto** – Esta entidade contém as tarefas que compõem o plano ou a agenda do projeto.
- **Atribuição de Recurso** – Esta entidade contém a atribuição de tarefas para o recurso reservável.
- **Requisito de Recurso** – Esta entidade contém os requisitos para quaisquer membros da equipa de recursos genéricos.
- **Estimativa** e **Linha da estimativa** – Estas entidades têm uma relação cabeçalho/linha e contêm estimativas de despesas para o projeto. As estimativas de tarefas são armazenadas na entidade **Estimativa de Recurso**.

![Diagrama que mostra as relações entre o requisito de recurso e o projeto](media/PS-Reporting-image4.png "Diagrama que mostra as relações entre o requisito de recurso e o projeto")

## <a name="reporting-on-resources"></a>Relatórios sobre recursos

Os recursos do projeto utilizam as entidades **Recurso Reservável** a partir do Universal Resource Scheduling (URS) partilhadas com outras aplicações, como o Microsoft Dynamics 365 Field Service. Segue-se uma lista das entidades que poderá ter de utilizar quando reportar sobre recursos do projeto:

- **Recurso Reservável** – Esta entidade representa o utilizador, o contacto, o recurso genérico, a conta, o grupo ou o equipamento utilizado na equipa do projeto.
- **Características de Recurso Reservável** – Esta entidade inclui as competências, certificações ou formação do recurso. As características podem ter valores de classificação definidos pelo modelo de classificação.
- **Categoria de Recurso Reservável** – Esta entidade representa a função do recurso reservável.
- **Reservas de Recursos Reserváveis** – Esta entidade representa o tempo que está reservado nos projetos para o recurso. Cada reserva tem uma entidade de cabeçalho e uma entidade de linha, sendo que cada linha tem um estado que representa o estado da reserva.

![Diagrama que mostra as relações das características de recursos reserváveis](media/PS-Reporting-image5.png "Diagrama que mostra as relações das características de recursos reserváveis")

## <a name="reporting-on-actual-transactions"></a>Relatórios sobre transações reais

Quando aprovar uma folha de horas ou despesa, ou faturar um contrato no PSA, a transação comercial é capturada na entidade **Valor Real**. Esta entidade pode servir como base para quase todos os relatórios relacionados com finanças no PSA. A entidade **Valor Real** captura as transações de custo e vendas para o evento de negócio. Também captura muitos atributos relevantes.

Quando está a trabalhar com a entidade **Valor Real**, é importante que compreenda quais transações ou que transações são registadas na entidade e quando as transações são registadas. Aqui está o fluxo típico quando trabalha com entradas de tempo (o fluxo para entradas de despesa é semelhante):

1. Quando a entrada de tempo é guardada, não são criados registos na entidade **Valor Real**.
2. Quando a entrada de tempo é submetida, não são criados registos na entidade **Valor Real**.
3. Quando a entrada de tempo é aprovada, é criado um registo na entidade **Valor Real** e um segundo registo também pode ser criado. O primeiro registo armazena o custo da entrada de tempo. O segundo registo armazena o montante de vendas não faturadas da entrada de tempo. O segundo registo depende de o projeto ter um cliente, uma proposta ou um item de contrato atribuído.

    | Data do documento | Tipo de transação | Classe de transação | Cliente         | Contrato   | Recurso     | Função do recurso | Tipo de faturação | Quantidade | Preço unitário | Montante |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|--------|
    | 3/2/18        | Custo             | Time              | Alpine ski house | Alpine CRM | Bárbara Araújo | Gestor de projeto   | Faturável   | 8.0      | 50.00      | 400.00 |
    | 3/2/18        | Vendas não faturadas   | Time              | Alpine ski house | Alpine CRM | Bárbara Araújo | Gestor de projeto   | Faturável   | 8.0      | 100.00     | 800.00 |

    Estes dois registos são registos separados mas relacionados. Não são débitos nem créditos.

4. Se um contrato estiver associado ao projeto, quando a entrada de tempo for faturada, mais dois registos são criados na entidade **Valor Real**. Primeiro, é criado um montante negativo para o registo de vendas não faturadas. Este registo basicamente reverte a venda não faturada. Segundo, é criada uma transação para a venda faturada. Novamente, estes registos são registos separados, mas relacionados, e não débitos e créditos.

    | Data do documento | Tipo de transação | Classe de transação | Cliente         | Contrato   | Recurso     | Função do recurso | Tipo de faturação | Quantidade | Preço unitário | Montante   |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|----------|
    | 4/2/18        | Vendas não faturadas   | Time              | Alpine ski house | Alpine CRM | Bárbara Araújo | Gestor de projeto   | Faturável   | - 8,0    | 100.00     | - 800,00 |
    | 4/2/18        | Vendas faturadas     | Time              | Alpine ski house | Alpine CRM | Bárbara Araújo | Gestor de projeto   | Faturável   | 8.0      | 100.00     | 800.00   |

A entidade **Origem da Transação** regista a origem do registo **Valor Real** e a entidade **Ligação da Transação** regista os registos relacionados para o registo **Valor Real**. Além disso, o registo **Valor Real** contém referências ao projeto, ao contrato do projeto (encomenda), ao recurso reservável e ao cliente.

![Diagrama que mostra as relações da ligação, da origem e dos valores reais](media/PS-Reporting-image6.png "Diagrama que mostra as relações da ligação, da origem e dos valores reais")
