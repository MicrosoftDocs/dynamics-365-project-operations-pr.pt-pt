---
title: Utilizar Categoria de Transação como dimensão de preços
description: Este tópico fornece informações sobre como utilizar um campo de Categoria de Transação como uma dimensão de preços.
author: rumant
manager: tfehr
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bace11455d34fdda95e08be1a7cc37850a0cf589
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 11/12/2020
ms.locfileid: "4514014"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Utilizar Categoria de Transação como dimensão de preços


_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_


Este tópico explica como utilizar o campo **Categoria de Transação** como uma dimensão de preços. 

## <a name="prerequisites"></a>Pré-requisitos
Antes de completar os procedimentos neste tópico, deve ter uma nova solução de dimensão de preços para a sua organização. Se ainda não criou uma, consulte [Criar campos e entidades personalizados como dimensões de preços](create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-transaction-category-field-to-forms-and-views"></a>Adicionar o campo Categoria de Transação a formulários e vistas
Para tornar o campo **Categoria de Transação** visível na solução de dimensão de preços, é necessário adicionar o campo a todos os formulários e vistas como uma entidade.

A tabela que se segue lista todos os formulários e vistas de origem, por entidade. Também terá de adicionar o novo campo a quaisquer formulários ou vistas adicionais nas suas entidades personalizadas.

|  Entity        | Formulários     |Visualizações        |
| ------------------------------|---------------------------------|----------------------------------|
|  Preço da Função| Informações |- Preços de Categoria de Recurso Ativos<br> - Preço de Categoria de Recurso Associado |
|  Margem de Lucro do Preço da Função| Informações|- Margem de Lucro do Preço da Função Ativa<br>- Margem de Lucro do Preço da Função Associada |
|  Detalhe de Linha de Proposta|- Informações do Projeto<br>- Criação Rápida de Projeto| - Detalhe de Linha de Proposta Ativo<br>- Detalhes de Linha de Proposta Combinados<br>- Detalhe de Linha de Proposta Associado |
|  Detalhe de Item de Contrato do Projeto|- Informações do Projeto<br>- Criação Rápida de Projeto|- Detalhes de Item de Contrato Combinados<br>- Detalhes de Item de Contrato Ativos<br>- Detalhes de Item de Contrato Associados |
|  Tarefa de Projeto|- Informações<br>- Novo Formulário| &nbsp; |
|  Membro da Equipa do Projeto|- Informações<br>- Novo Formulário|- Membros da Equipa do Projeto Ativos<br>- Membros da Equipa do Projeto<br>- Membros da Equipa do Projeto Associados |
|  Entrada de Hora|- Informações<br>- Criar Entrada de Hora|- As Minhas Entradas de Hora por Data<br>- As Minhas Entradas de Hora para esta Semana<br>- Entradas de Hora para Aprovação|
|  Linha do Diário|- Informações<br>- Criação Rápida|- Linhas do Diário Ativas<br>- Linha do Diário Associada|
|  Detalhe de Linha de Fatura|- Informações<br>- Criação Rápida|- Detalhes de Linha de Fatura Ativos<br>- Transações de Fatura Faturáveis<br>- Transações de Fatura Grátis<br>- Detalhe de Linha de Fatura Associado <br>- Transações de Fatura Não Faturáveis|
|  Valor Real|- Informações<br>- Valores Reais Ativos| – Valor Real Associado |

## <a name="set-up-the-transaction-category-field-as-a-pricing-dimension"></a>Configurar o campo Categoria de Transação como uma dimensão de preços

1. Aceda a **Definições** > **Parâmetros**. 
2. Na página **Parâmetros**, no separador **dimensões de preços Baseada no Montante**, verifique que a grelha no separador mostra os registos na entidade **dimensões de preços**.
3. Adicione **Categoria de Transação** à lista e defina os campos **Aplicável ao Custo** e **Aplicável às Vendas** como **Sim**.
4. No campo **Tipo de Dimensão**, selecione **Baseado no Montante** e, em seguida, selecione a prioridade para a **Categoria de Transação** que se relaciona com o custo e as vendas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]