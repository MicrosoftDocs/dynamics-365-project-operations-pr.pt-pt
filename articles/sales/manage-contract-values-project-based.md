---
title: Trabalhar com itens de contrato baseados em projetos
description: Este tópico fornece informações sobre itens de contrato baseados em projetos.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c1c935a998cba8bd42ba2f11c8310d41e72de94adac7c2cb83f4c7224127b10b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6990060"
---
# <a name="work-with-projectbased-contract-lines"></a>Trabalhar com itens de contrato baseados em projetos

Os itens de contrato baseados em projetos no Dynamics 365 Project Operations destinam-se a manter os contratos de estimativa e faturação para componentes específicos do trabalho do projeto num compromisso. A estrutura de um item de contrato baseado em projetos é alargado para estimativas de projetos e cenários de faturação com os seguintes conceitos:

- Método de faturação
- Mapeamento de projetos e tarefas
- Classes de transações incluídas
- Limite a não exceder
- Configuração da exigibilidade
- Estimativas que usam detalhes do item de contrato
- Clientes do item de contrato

Os seguintes campos estão incluídos no separador **Geral** dos itens de contrato baseados em projetos. Estes campos ajudam a configurar a base para uma estimativa detalhada e de raiz, bem como os acordos de faturação dos trabalhos baseados em projetos.

| Campo | Descrição | Impacto a jusante |
| --- | --- | --- |
| **Nome** | O nome do item de contrato que identifica a componente discreta do contrato que está a ser estimado. Para um contrato de projeto criado a partir de uma proposta, este valor é copiado de um valor correspondente da linha de proposta baseada em projetos. | O valor do campo é copiado para a linha de fatura do projeto que é criada a partir deste item de contrato quando a fatura é criada. |
| **Método de Faturação** | Num contrato de projeto criado a partir de uma proposta, este valor é copiado do campo correspondente na linha de proposta. Trata-se de um conjunto de opções que representa os dois principais modelos de contratação suportados pelo Project Operations:</br>- **Preço Fixo**</br>- **Tempo e Material** | Com base no método de faturação do item de contrato referenciado, a transação real será processada. Se o item de contrato referenciado pelo valor real tiver um método de faturação de tempo e material, é criado um registo de valor real de custos e vendas não faturados. Se o item de contrato referenciado pelo valor real tiver um método de faturação de preço fixo, apenas é criado um valor real de custo. |
| **Project** | Utilize este campo para identificar o projeto que será usado para entregar o trabalho neste compromisso. | O valor neste campo será utilizado em conjunto com campos **Tarefas Incluídas** e **Classes de Transações Incluídas** para resolver a referência do item de contrato num registo de linha de valor real ou de estimativa. |
| **Incluir Tempo** | Uma bandeira indica se as transações de tempo ou os custos de mão de obra no projeto selecionado são incluídos neste item de contrato. Um valor **Não** indica que as transações de tempo ou os custos de mão de obra não serão incluídos neste item de contrato. Um valor **Sim** indica que serão. | Este valor de campo é utilizado em conjunto com o projeto para resolver a referência do item de contrato num registo de linha de valor real ou de estimativa. |
| **Incluir Despesa** | Uma bandeira indica se os custos de despesas no projeto selecionado serão incluídos neste item de contrato. Um valor **Não** indica que os custos de despesas não serão incluídos neste item de contrato. Um valor **Sim** indica que serão. | Este valor de campo é utilizado em conjunto com o projeto para resolver a referência do item de contrato num registo de linha de valor real ou de estimativa. |
| **Incluir Taxa** | Uma bandeira indica se as taxas no projeto selecionado serão incluídas neste item de contrato. Um valor **Não** indica que as taxas não serão incluídos neste item de contrato. Um valor **Sim** indica que serão. | Este valor de campo é utilizado em conjunto com o projeto para resolver a referência do item de contrato num registo de linha de valor real ou de estimativa. |
| **Montante Contratado** | Num item de contrato de preço fixo, este é o valor acordado que será faturado ao cliente por todos os componentes de trabalho associados com este item de contrato. Num item de contrato de tempo e material, este montante é um valor estimado do que será faturado ao cliente por todos os componentes de trabalho associados a este item de contrato. Num contrato de projeto criado a partir de uma proposta, este valor é copiado do campo correspondente na linha de proposta. Quando um item de contrato baseado em projetos tem detalhes de linha, este campo está bloqueado para edição e é resumido a partir do montante nos detalhes do item de contrato. | Quando o item de contrato tem detalhes de linha, este valor pode ser modificado alterando os montantes nos detalhes da linha. Num item de contrato de preço fixo, este valor é utilizado para gerar o montante antes dos impostos sobre os marcos periódicos de faturação. |
| **Imposto Estimado** | O utilizador pode editar este campo para inserir o montante estimado do imposto no item de contrato. Quando um item de contrato baseado em projetos tem detalhes de linha, este campo está bloqueado para edição e é resumido a partir do montante de impostos nos detalhes do item de contrato. | Quando o item de contrato tem detalhes de linha, este valor pode ser modificado alterando os montantes de impostos nos detalhes da linha. Num item de contrato de preço fixo, este valor é utilizado para gerar o imposto sobre os marcos periódicos de faturação. |
| **Montante Contratado após o Imposto** | O montante do item de contrato após o imposto. Este campo é apenas de leitura e é calculado como **Montante Contratado + Imposto**. | Num item de contrato de preço fixo, este valor é utilizado para gerar os marcos periódicos de faturação. |
| **Limite a Não Exceder** | O utilizador pode editar este campo e só está disponível em itens de contrato baseados em projetos que tenham um método de faturação de tempo e material. | O utilizador pode editar este campo. Quando um valor real de tempo ou de despesas referencia este item de contrato por tempo e material, o montante sobre o valor real é avaliado em relação ao limite a não exceder neste item de contrato depois de contabilizar os montantes já gastos e comprometidos. |
| **Orçamento do Cliente** | Este campo é editável e é copiado do campo correspondente na linha de proposta se o contrato foi criado a partir de uma proposta. | Este campo é utilizado apenas para informações e não tem qualquer significado a jusante. |

## <a name="validation-rule-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Regra de validação das opções no separador Geral dos itens de contrato baseados em projetos

Regra: Um projeto e uma determinada classe de transações só podem ser incluídos num item de contrato baseado em projetos num contrato.

| Contrato | Item de contrato | Project | Incluir tempo | Incluir despesa | Incluir taxa | Válido/não válido | Razão                                                                                                                                                                                                  |
|----------|---------------|---------|--------------|-----------------|-------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| C1       | CL1           | P1      | Sim          | Sim             | Sim         | Não é válido       | Viola a regra. O tempo, as despesas e as taxas no projeto P1 estão incluídos em ambos os itens de contrato, CL1 e CL2.                                                                                       |
| C1       | CL2           | P1      | Sim          | Sim             | Sim         | Não é válido       | Viola a regra. O tempo, as despesas e as taxas no projeto P1 estão incluídos em ambos os itens de contrato, CL1 e CL2.                                                                                       |
| C1       | CL1           | P1      | Sim          | No              | Sim         | Não é válido       | Viola a regra. O tempo e as despesas no projeto P1 estão incluídos em ambos os itens de contrato, CL1 e CL2.                                                                                                   |
| C1       | CL2           | P1      | Sim          | Sim             | Sim         | Não é válido       | Viola a regra. O tempo e as despesas no projeto P1 estão incluídos em ambos os itens de contrato, CL1 e CL2.                                                                                                   |
| C1       | CL1           | P1      | Sim          | No              | Sim         | Válido           | O tempo e as taxas do projeto P1 estão incluídos no CL1. As Despesas no projeto P1 estão incluídas no CL2. </br>   Não há sobreposição no que está a ser incluído em cada item de contrato e, por conseguinte, é válido.  |
| C1       | CL2           | P1      | No           | Sim             | No          | Válido           | O tempo e as taxas do projeto P1 estão incluídos no CL1. As Despesas no projeto P1 estão incluídas no CL2. </br>   Não há sobreposição no que está a ser incluído em cada item de contrato e, por conseguinte, é válido.  |
| C1       | CL1           | P1      | Sim          | Sim             | Sim         | Não é válido       | Viola a regra. O tempo, as despesas e as taxas no projeto P1 estão incluídos nos itens dos dois contratos.                                                                                               |
| CL2      | CL2           | P1      | Sim          | Sim             | Sim         | Não é válido       | Viola a regra. O tempo, as despesas e as taxas no projeto P1 estão incluídos nos itens dos dois contratos.                                                                                               |


[!INCLUDE[footer-include](../includes/footer-banner.md)]