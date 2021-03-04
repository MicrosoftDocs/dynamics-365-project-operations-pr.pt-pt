---
title: Cenários de várias moedas (versão 3.x)
description: Este tópico fornece informações sobre cenários de várias moedas.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/26/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bdb9ccad84e0f510118502d4253f5c83a760f8bb
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145687"
---
# <a name="multiple-currency-scenarios"></a>Cenários de várias moedas

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

O Microsoft Dynamics 365 tem dois conceitos de moedas:

- **Moeda da transação** - A moeda na qual uma transação ocorre. 
- **Moeda base** - A moeda da instância do Dynamics 365. Esta moeda é configurada quando uma instância do Dynamics 365 é aprovisionada. Não é possível alterar.

Por exemplo, a Contoso US venderam 100 t-shirts a um cliente do Reino Unido por 15 libras (GBP) cada. A tabela seguinte mostra como esta transação é registada na entidade Produto da Encomenda.

| Produto | Quantidade | Preço unitário | Moeda | Montante | Câmbio | Preço unitário (Base)| Montante (Base)|
|---------|----------|----------------|----------|--------|---------------|----------------------|--------------|
| T-shirt | 100      | 15             | GBP      | 1500   | 0.94          | 17,25 $               | 1725 $       |

A coluna **Moeda** mostra a moeda da transação, que é a moeda em que a venda ocorreu. A coluna **Câmbio** é o câmbio entre a moeda da transação e a moeda base. A moeda base é dólares norte-americanos (USD). Esta moeda base foi configurada quando uma instância do Dynamics 365 foi aprovisionada.
À medida que a tabela mostra, cada transação é registada na moeda da transação e na moeda base. O Dynamics 365 utiliza o câmbio para calcular os montantes da moeda base.

## <a name="project-service-automation-extensions"></a>Extensões do Project Service Automation

O Dynamics 365 Project Service Automation influencia a moeda da transação, uma vez que, normalmente, as transações comerciais têm dois aspetos: custo e vendas.

As seguintes entidades são consideradas transações comerciais:

- Detalhe de linha de proposta
- Detalhe do item de contrato do projeto
- Linha de estimativa
- Linha do diário
- Detalhe de linha de fatura
- Real

Em cada uma destas entidades, existe um registo que representa o montante de custo ou o montante de vendas. Tal como para qualquer entidade do Dynamics 365 que tenha um campo **Montante**, cada registo inclui montantes na moeda da transação e na moeda base. 

O PSA expande o conceito da moeda da transação para o custo e as vendas das seguintes formas:

- A moeda da transação de custo para as transações de tempo provém sempre da moeda da unidade organizacional que possui ou gere o projeto. Esta unidade organizacional é conhecida como unidade de contratação.
- A moeda da transação de vendas para as transações de tempo e despesas provém sempre da moeda do contrato de projeto.
- A moeda da transação de custo para as despesas provém da moeda em que a entrada de despesas foi criada.

## <a name="multiple-currency-scenario"></a>Cenário de várias moedas

Esta secção descreve um exemplo de um projeto que a Contoso UK fornece a um cliente denominado Fabrikam, Japão. Eis como o cenário foi configurado:

1. A GBP e o iene japonês (JPY) estão configurados em **Definições** \> **Gestão de Negócio** \> **Moedas**. 
2. Uma conta de cliente denominada **Fabrikam - Japão** está configurada e o JPY está selecionado como a moeda na conta.
3. Uma unidade organizacional denominada **Contoso UK** está configurada e a GBP é selecionada como a moeda.
4. É criado um contrato de projeto, em que a **Contoso UK** é especificada como a unidade de contrato e a **Fabrikam – Japão** é especificada como o cliente.
5. Os itens de contrato de projeto são criados, com base nas disposições de faturação para as várias classes de transação no projeto, tal como a faturação para o tempo versus a faturação de despesas.
6. É criado um projeto em que a **Contoso UK** é especificada como a unidade de contratação. Este projeto é criado e mapeado para os itens de contrato do projeto.


Durante a estimativa que utiliza o detalhe de linha de proposta, os detalhes de item de contrato do projeto, ou na linha de estimativa da agenda, são sempre criados dois registos na entidade. Um registo é para o custo e o outro registo é para as vendas.

- Por predefinição, a moeda da transação no registo de custo é definida como a moeda da unidade de contratação do projeto. Neste exemplo, a moeda é GBP.
- Por predefinição, a moeda da transação no registo de vendas é definida como a moeda do contrato do projeto. Neste exemplo, a moeda é JPY.

Quando são criados valores reais para o tempo utilizando a entrada de tempo ou a linha do diário, ocorre o seguinte comportamento:

- Por predefinição, a moeda da transação no registo de custo é definida como a moeda da unidade de contratação do projeto.
- Por predefinição, a moeda da transação no registo de vendas é definida como a moeda do contrato do projeto.

Quando são criados valores reais para as despesas utilizando a entrada de despesa ou a linha do diário, ocorre o seguinte comportamento:

- Pode registar o montante das despesas em qualquer moeda. Selecione a moeda utilizando o seletor de moedas na página **Entrada de Despesas** ou na página **Linha do Diário**. Por predefinição, a moeda da transação para o registo de custo é definida como a moeda na entrada de despesas. 
- Por predefinição, a moeda da transação para o registo de vendas é a moeda do contrato do projeto. Para definir esta moeda, primeiro, o sistema converte o montante da transação na moeda que o utilizador introduziu na moeda base. Em seguida, converte o montante na moeda do contrato do projeto. 

### <a name="computing-roll-ups-when-project-actuals-are-recorded-in-multiple-transaction-currencies"></a>Calcular acumulações quando os valores reais do projeto são registados em moedas de várias transações

O Dynamics 365 processa automaticamente as acumulações de montantes em moedas diferentes. Segue-se um exemplo.

| Classe de transação | Tipo de transação| Date   | Recurso | Categoria de transação | Quantidade | Preço unitário | Montante      | Câmbio | Montante base |
|-------------------|------------------|--------|----------|----------------------|----------|--------------|-------------|---------------|----------------|
| Time              | Vendas não faturadas   | 14 jun | Gonçalo  |                      | 8 horas    | 20.000 JPY    | 160.000 JPY | 123           | 1.300,81 USD    |
| Time              | Vendas não faturadas   | 15 jun | Gonçalo  |                      | 8 horas    | 20.000 JPY    | 160.000 JPY | 123           | 1.300,81 USD    |
| Despesa           | Vendas não faturadas   | 16 jun | Gonçalo  | Hotel                | 1 cada     | 250 EUR      | 250 EUR     | 0.94          | 265,95 USD     |
| Despesa           | Vendas não faturadas   | 17 jun | Gonçalo  | Aluguer de Automóvel           | 1 cada     | 150 EUR      | 150 EUR     | 0.94          | 159,57 USD     |

Para calcular o valor total de vendas não faturadas no projeto, pode criar um campo de acumulação para o campo **Montante** em todos os valores reais de vendas não faturadas relacionados. O campo de acumulação é uma construção do Dynamics 365 que permite fórmulas rápidas sobre os registos relacionados.


[!INCLUDE[footer-include](../includes/footer-banner.md)]