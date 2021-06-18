---
title: Utilizar um recurso reservável como dimensão de preços
description: Este tópico fornece informações sobre como utilizar um recurso reservável como uma dimensão de preços.
author: Rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d46d4659a5f60226f80b29f3dd8607249cb91ac2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011205"
---
# <a name="use-a-bookable-resource-as-a-pricing-dimension"></a>Utilizar um recurso reservável como dimensão de preços

 _**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_ 

Este tópico fornece informações sobre como utilizar um recurso reservável como uma dimensão de preços. Se a sua estratégia de preços for configurada para que cada recurso reservável tenha um preço ou taxa de custo específicos, use um recurso reservável como uma dimensão de preços.

## <a name="prerequisites"></a>Pré-requisitos
Antes de completar os procedimentos neste tópico, deve ter uma nova solução de dimensão de preços para a sua organização. Se ainda não criou uma, consulte [Criar campos e entidades personalizados](../pricing-costing/create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-bookable-resource-field-to-forms-and-views"></a>Adicionar o campo Recurso Reservável a formulários e vistas
Para tornar o campo **Recurso Reservável** visível na solução de dimensão de preços, é necessário adicionar o campo a todos os formulários e vistas como uma entidade.

A tabela que se segue lista todos os formulários e vistas de origem, por entidade. Também terá de adicionar o novo campo a quaisquer formulários ou vistas adicionais nas suas entidades personalizadas.

|   Entity        | Formulários   |Visualizações        |
| ------------------------------|---------------------------------|----------------------------------|
|  Preço da Função| Informações | - Preços de Categoria de Recurso Ativos<br> - Preço de Categoria de Recurso Associado |
|  Margem de Lucro do Preço da Função| Informações| - Margem de Lucro do Preço da Função Ativa<br>- Margem de Lucro do Preço da Função Associada |
|  Detalhe de linha de proposta| - Informações do Projeto<br>- Criação Rápida de Projeto| - Detalhe de Linha de Proposta Ativo<br>- Detalhes de Linha de Proposta Combinados<br>- Detalhe de Linha de Proposta Associado |
|  Detalhe de Item de Contrato do Projeto| - Informações do Projeto<br>- Criação Rápida de Projeto| - Detalhes de Item de Contrato Combinados<br>- Detalhes de Item de Contrato Ativos<br>- Detalhes de Item de Contrato Associados |
|  Tarefa de Projeto| - Informações<br>- Novo Formulário| &nbsp; |
|  Membro da Equipa do Projeto| - Informações<br>- Novo Formulário| - Membros da Equipa do Projeto Ativos<br>- Membros da Equipa do Projeto<br>- Membros da Equipa do Projeto Associados |
|  Entrada de Hora| - Informações<br>- Criar Entrada de Hora| - As Minhas Entradas de Hora por Data<br>- As Minhas Entradas de Hora para esta Semana<br>- Entradas de Hora para Aprovação|
|  Linha do Diário| - Informações<br>- Criação Rápida| - Linhas do Diário Ativas<br>- Linha do Diário Associada |
|  Detalhe de Linha de Fatura| - Informações<br>- Criação Rápida| - Detalhes de Linha de Fatura Ativos<br>- Transações de Fatura Faturáveis<br>- Transações de Fatura Grátis<br>- Detalhe de Linha de Fatura Associado <br>- Transações de Fatura Não Faturáveis|
|  Valor Real| - Informações<br>- Valores Reais Ativos| – Valor Real Associado |

## <a name="set-up-a-bookable-resource-as-a-pricing-dimension"></a>Configurar um recurso reservável como uma dimensão de preços
Para configurar um recurso reservável como uma dimensão de preços, siga estes passos:

1. Aceda a **Definições** > **Parâmetros**. 
2. Na página **Parâmetro**, no separador **Dimensões de Definição de Preços Baseada no Montante**, verifique que a grelha no separador mostra os registos na entidade **Dimensões de Definição de Preços**. 
2. Adicione o **Recurso Reservável** a esta lista de dimensões de definição de preços como **msdyn_bookableresource**. 
3. Em **Aplicável ao custo** e **Aplicável às vendas**, selecione um valor.
4. Em **Tipo de Dimensão**, selecione **Baseada no Montante**. 
5. Selecione a prioridade de custo e vendas para o recurso reservável. Normalmente, um recurso reservável tem a maior prioridade quando incluído como uma dimensão de preços. Defina a prioridade para **1** (ou **0** dependendo da forma como conta a prioridade) para garantir este comportamento.

## <a name="set-up-pricing-dimension-field-names"></a>Configurar nomes dos campos de dimensão de definição de preços

Quando o nome do campo de uma dimensão de definição de preços na tabela **Preço da Função** é diferente do nome de campo em qualquer uma das outras entidades em que o preço predefinido é utilizado, o registo de dimensão de preços tem de ser notificado dos diferentes nomes.  

Para um recurso reservável, a entidade **Membros da Equipa do Projeto** tem um nome de campo ligeiramente diferente do que é chamado na entidade **Preço da Função**: 

 - Entidade **Membros da Equipa do Projeto** = **msdyn_bookableresourceid**
 - Entidade **Preço de Função** = **msdyn_bookableresource**

O registo de dimensão de preços para **msydn_bookableresource** tem de ser notificado desta diferença.

1. Faça duplo clique na linha da grelha **Dimensões de Definição de Preços** para abrir a página de dimensão de **msdyn_bookableresource**.
2. Na página de dimensão, no separador **Relacionado**, selecione **Nomes dos Campos de Dimensão de Preços**.

  ![Separador Nomes dos campos de dimensão de definição de preços](media/PD-fieldname.png)

3. Na vista associada que é aberta, selecione **Adicionar Novo Nome do Campo de Dimensão de Preços**.

  ![Adicionar Novos Nomes dos Campos de Dimensão de Definição de Preços](media/Add-NewPD-fieldname.png)

  Esta ação abre a página **Novo nome do campo de dimensão de definição de preços** para **msdyn_bookableresource**. 

4. Na página **Novo Nome de Campo de Dimensão de Preços**, adicione **msdyn_projectteam** ao **Nome Lógico da Entidade**.
5. Adicione **msdyn_bookableresourceid** ao **Nome do Campo**.

 ![Formulário Novo nome do campo de dimensão de definição de preços](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]