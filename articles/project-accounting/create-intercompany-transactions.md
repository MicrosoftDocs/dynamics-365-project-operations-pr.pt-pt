---
title: Criar transações interempresa
description: Este tópico fornece informações sobre como criar transações interempresa.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0e396f0d08fd166e7acd6f8ec8f32353a7679dd8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013365"
---
# <a name="create-intercompany-transactions"></a>Criar transações interempresa

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

As transações interempresa são transações de tempo e despesas de um contrato de projeto que pertencem a uma empresa ou unidade organizacional, enquanto os recursos no contrato de projeto fazem parte de uma empresa ou unidade organizacional diferente.

Quando uma transação interempresa é aprovada, as seguintes transações reais são criadas

| **Tipo de transação** | **Lista de preços aplicada** | **Moeda da transação** |
| --- | --- | --- |
| Custo | Lista de preços de custo de unidade de contratação | Moeda na linha de preços |
| Vendas não faturadas. Estes são criados apenas para os valores reais que estão associados a um item de contrato com o tipo de faturação, tempo e material. | Lista de preços de vendas de projeto do contrato | Moeda do contrato |
| Custo de unidade de atribuição de recursos | Lista de preços de custo de unidade de atribuição de recursos | Moeda na linha de preços |
| Vendas de unidades interorganizacionais | Lista de preços de custo de unidade de contratação | Moeda na linha de preços |

O custo, o custo de unidade de atribuição de recursos e os preços e a moeda de transação de vendas de unidades interorganizacionais são impulsionados pela **unidade organizacional**. Isto é importante lembrar ao decidir como estruturar empresas e unidades organizacionais na sua implementação.

Quando cria oportunidades, propostas, contratos de projeto e registos de projetos, o sistema verifica que a moeda da unidade contratante corresponde à moeda contabilística da empresa contratante. Quando não são os mesmos, estes registos não podem ser criados. A moeda da unidade organizacional é definida no Dynamics 365 Project Operations indo a **Dataverse** > **Definições** > **Unidades organizacionais**. A moeda contabilística de uma empresa é definida no Dynamics 365 Finance indo a **Livro razão geral** > **Configuração do livro razão** > **Livro razão**. A moeda é sincronizada ao seu ambiente do Dataverse utilizando o mapa de Escrita Dupla de Livros Razão.

O sistema cria o custo de unidade de atribuição de recursos e os valores reais das vendas de unidades interorganizacionais nas seguintes situações:

  - Quando a unidade de atribuição de recursos difere da unidade de contratação
  - Quando a empresa de atribuição de recursos difere da empresa de contratação

No entanto, apenas as transações que tenham uma empresa de atribuição de recursos diferente da empresa contratante serão transferidas para o ambiente do Dynamics 365 Finance para contabilidade adicional.

A contabilística de valores reais de projeto é registada no diário de integração do Project Operations no Finance. O sistema cria as seguintes linhas do diário.

| **Tipo de transação** | **Entidade legal** | **Cria transação de projeto quando publicado** | **Dimensões financeiras predefinidas de** | **Grupo de impostos sobre vendas de faturação e grupo de impostos sobre vendas de artigos de faturação predefinidos** |
| --- | --- | --- | --- | --- |
| Custo | Não é adicionado ao diário de integração | N/A | N/A | N/A |
| Vendas não faturadas | O diário de integração de entidades legais de contração | Sim | Project | **Grupo de imposto sobre vendas de faturação**: com base no **cliente do contrato** <br/> **Grupo de imposto sobre vendas de artigos de faturação**: da atual categoria de projeto de entidade legal na linha do diário |
| Custo de unidade de atribuição de recursos | O diário de integração de entidades legais de concessão | No | Cliente interempresa | **Grupo de imposto sobre vendas de faturação**: com base no **cliente interempresa** <br/> **Grupo de imposto sobre vendas de artigos de faturação**: da atual categoria de projeto de entidade legal na linha do diário |
| Vendas interorganizacionais | O diário de integração de entidades legais de concessão | No | Cliente interempresa | **Grupo de imposto sobre vendas de faturação**: com base no **cliente interempresa** <br/> **Grupo de imposto sobre vendas de artigos de faturação**: da atual categoria de projeto de entidade legal na linha do diário |

### <a name="example-intercompany-transactions"></a>Exemplo: transações interempresa

Eduarda Lopes, programadora empregada na GBPM, regista 10 horas de trabalho num projeto USPM Adventure Works, que é aprovado pelo gestor do projeto. O custo do programador no GBPM é de 88 GBP por hora. A GBPM faturará a USPM 120 USD por hora de programação. A USPM faturará o cliente Adventure Works, 200 USD pelo trabalho realizado pelo recurso GBPM. Para mais informações, consulte [Configurar faturação interempresa](configure-intercompany-invoicing.md).

1. No Project Operations, vá a **Recursos** e selecione **Eduarda Lopes** da lista. No separador **Agendamento**, no campo **Empresa**, selecione **GBPM**.
2. Vá a **Vendas** > **Clientes** e selecione **Novo** para criar um novo registo de cliente para a Adventure Works.
    1. Defina a empresa como **USPM**.
    2. Defina o **Tipo de relação** como **Cliente**.
    3. Selecione **Grupo de clientes 10 – Doméstico**.
    4. Defina moeda como **USD**.
    5. Guarde o registo.
3. Vá a **Vendas** > **Contratos de Projeto** e crie um novo contrato de projeto para a Adventure Works.
    1. Configurar a empresa proprietária para **USPM** e a unidade contratante para **Contoso Robotics US**.
    2. Selecione Adventure Works como o cliente.
    3. Selecione uma lista de preços do produto e guarde o registo.
    4. No separador **Itens de Contrato**, crie um novo item de contrato. Defina qualquer nome e selecione **Tempo e Materiais** como o método de faturação.
    5. Crie um novo projeto e associe-o a este item de contrato.
4. Inicie sessão como o recurso, **Eduarda Lopes**. Vá a **Projetos** > **Entradas de hora** e crie uma entrada de hora para o projeto Adventure Works.
5. Inicie sessão como Gestor de projetos. Vá a **Projetos** > **Aprovações** e aprove a transação de entrada de hora registada por Eduarda Lopes.
6. Navegue para o projeto Adventure Works e selecione **Relacionado** > **Valores reais**. São criados os seguintes valores reais de transações.

| **Tipo de transação** | **Preço** | **Moeda da transação** | **Montante** |
| --- | --- | --- | --- |
| Custo | 120 | USD | 1200 |
| Vendas não faturadas | 200 | USD | 2000 |
| Custo de unidade de atribuição de recursos | 88 | GBP | 880 |
| Vendas de unidades interorganizacionais | 120 | USD | 1200 |

7. Iniciar sessão como um contabilista da USPM. Abra a instância do Finance do Project Operations e selecione a empresa **USPM**. 
8. Vá à **Gestão de projetos e contabilística** > **Periódico** > **Project Operations no Customer Engagement** > **Importar a partir de teste** e selecione para executar o processo periódico. Este processo periódico preencherá o diário de Integração do Project Operations.
9. Vá a **Gestão de projetos e contabilística** > **Diários** > **Diário de integração do Project Operations** e reveja as linhas do diário. O sistema cria a seguinte linha.

    | **Tipo de transação** | **Preço** | **Moeda da transação** | **Montante** |
    | --- | --- | --- | --- |
    | Vendas não faturadas | 200 | USD | 2000 |

    Se o sistema for configurado para imputar receitas para este projeto, é publicado o seguinte:

    - Débito: Projeto – 200 USD de valor de vendas WIP
    - Crédito: Projeto – 200 USD de Receitas Imputadas

    Esta venda não faturada está agora pronta para faturação. A fatura para o cliente Adventure Works pode ser publicada financeiramente quando necessário.

10. Inicie sessão como o contabilista da **GBPM**. Abra a instância do Finance do Project Operations e abra a empresa **GBPM**. 
11. Vá à **Gestão de projetos e contabilidade** > **Periódico** > **Integração de Project Operations** > **Importar da mesa de teste** e executar o processo periódico para preencher o diário de Integração do Project Operations.
12. Vá a **Gestão de projetos e contabilística** > **Diários** > **Diário de integração do Project Operations** e reveja as linhas. O sistema cria as seguintes linhas.

    | **Tipo de transação** | **Preço** | **Moeda da transação** | **Montante** |
    | --- | --- | --- | --- |
    | Custo de unidade de atribuição de recursos | 88 | GBP | 880 |
    | Vendas de unidades interorganizacionais | 120 | USD | 1200 |

    A publicação destes registos resulta nas seguintes transações de cupão:

    - Débito: 88 GBP de custo do projeto
    - Crédito: 88 GBP de alocação de vencimentos

    Se o sistema for configurado para imputar receitas interempresa, é publicado o seguinte:

    - Débito: Projeto – 120 USD de valor de vendas WIP
    - Crédito: Projeto – 120 USD de Receitas Imputadas

    O sistema está agora pronto para criar uma fatura de cliente interempresa.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
