---
title: Utilizar categoria de transação como uma dimensão de definição de preços
description: Este tópico fornece informações sobre a utilização de uma categoria de transação como uma dimensão de definição de preços.
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
ms.openlocfilehash: 0019571a1d37d3b6a503e7221db3c3b51365c236
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082488"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Utilizar categoria de transação como uma dimensão de definição de preços
Este tópico mostra como utilizar uma categoria de transação como uma dimensão de definição de preços. Antes de começar, se ainda não tiver criado uma solução de dimensão de definição de preços, terá de criar uma nova. Se já tiver uma solução de dimensão de definição de preços, poderá efetuar as alterações nessa solução. Se não tiver criado uma nova solução de dimensão de definição de preços para a sua organização, conclua os procedimentos no tópico [Criar campos e entidades personalizados](create-custom-fields-entities.md).

## <a name="add-transaction-category-to-forms-and-views"></a>Adicionar categoria de transação a formulários e vistas
Para tornar uma categoria de transação visível na IU na solução de dimensão de definição de preços, terá de percorrer todos os formulários e vistas das entidades principais e adicionar estes campos aos formulários e às vistas dessas entidades.
A tabela seguinte é uma lista abrangente de formulários e vistas fornecidos com o programa, listados por entidade, que terão de ser atualizados com os novos campos. Se existirem formulários ou vistas adicionais nas suas personalizações nestas entidades, adicione os campos novos aos mesmos.

|  Entidade        | Formulários     |Vistas        |
| ------------------------------|---------------------------------|----------------------------------|
|  Preço da Função|• Informação |• Preços de Categoria de Recurso Ativos<br> • Vista Associada de Preço de Categoria de Recurso|
|  Margem de Lucro do Preço da Função|• Informação|• Margem de Lucro do Preço da Função Ativa<br>• Vista Associada de Margens de Lucro do Preço da Função|
|  Detalhe de linha de proposta|• Informações do projeto<br>• Criação Rápida de Projeto|• Detalhe de Linha de Proposta Ativo<br>• Detalhes de Linha de Proposta Combinados<br>• Vista associada de Detalhe de Linha de Proposta|
|  Detalhe de Item de Contrato do Projeto|• Informações do projeto<br>• Criação Rápida de Projeto|• Detalhes de Item de Contrato Combinados<br>• Detalhes de Item de Contrato Ativos<br>• Vista associada de Detalhes de Item de Contrato|
|  Tarefa de Projeto|• Informação<br>• Novo Formulário||
|  Membro da Equipa do Projeto|• Informação<br>• Novo Formulário|• Membros da Equipa do Projeto Ativos<br>• Membros da Equipa do Projeto<br>• Vista associada de membros da Equipa do Projeto|
|  Entrada de Hora|• Informação<br>• Criar Entrada de Tempo|• As Minhas Entradas de Tempo por Data<br>• As minhas Entradas de tempo para esta semana<br>• Entradas de tempo para aprovação|
|  Linha do Diário|• Informação<br>• Criação rápida|• Linhas do diário ativas<br>• Vista associada de Linha do Diário|
|  Detalhe de Linha de Fatura|• Informação<br>• Criação rápida|• Detalhes de Linha de Fatura Ativos<br>• Transações de Fatura Faturáveis<br>• Transações de Fatura Grátis<br>• Vista associada de Detalhe de Linha de Fatura<br>• Transações de Fatura Não Faturáveis|
|  Real|• Informação<br>• Valores Reais Ativos|• Vista associada de Valor Real|

## <a name="set-up-transaction-category-as-a-pricing-dimension"></a>Configurar categoria de transação como uma dimensão de definição de preços

1. Na interface Web, aceda a **Project Service** > **Definições** > **Parâmetros**. 
2. Na página **Parâmetros** , no separador **Dimensões de Definição de Preços Baseada no Montante** , note que a grelha no separador mostra os registos na entidade **Dimensões de Definição de Preços**.
3. Adicione **Categoria de Transação** à lista e defina os campos **Aplicável ao Custo** e **Aplicável às Vendas** como **Sim**.
4. No campo **Tipo de Dimensão** , selecione **Baseado no Montante** e, em seguida, selecione a prioridade para a **Categoria de Transação** relacionada com o custo e as vendas.
