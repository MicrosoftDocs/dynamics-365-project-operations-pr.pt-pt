---
title: Utilizar recurso reservável como uma dimensão de definição de preços
description: Este tópico fornece informações sobre a utilização de um recurso reservável como uma dimensão de definição de preços.
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
ms.openlocfilehash: d3f5ed7da5972cec5b22524bdcb3dc34a83eee28
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290958"
---
# <a name="use-bookable-resource-as-a-pricing-dimension"></a>Utilizar recurso reservável como uma dimensão de definição de preços

[!include [banner](../includes/psa-now-project-operations.md)]

Este tópico fornece informações sobre a utilização de um recurso reservável como uma dimensão de definição de preços. Antes de começar, se ainda não tiver criado uma solução de dimensão de definição de preços, terá de criar uma nova. Se já tiver uma solução de dimensão de definição de preços, poderá efetuar as alterações nessa solução. Se não tiver criado uma nova solução de dimensão de definição de preços para a sua organização, conclua os procedimentos no tópico [Criar campos e entidades personalizados](create-custom-fields-entities.md).

## <a name="add-bookable-resource-to-forms-and-views"></a>Adicionar recurso reservável a formulários e vistas
Para tornar os campos visíveis na IU na solução de dimensão de definição de preços, terá de percorrer todos os formulários e vistas das entidades principais do Project Service e adicionar estes campos aos formulários e às vistas dessas entidades.
A tabela seguinte é uma lista abrangente de formulários e vistas fornecidos com o programa, listados por entidade, que terão de ser atualizados. Se existirem formulários ou vistas adicionais nas suas personalizações nestas entidades, adicione os campos novos aos mesmos.
Abra o Solution Explorer para a solução de dimensão de definição de preços e, em seguida, clique em **Publicar Todas as Personalizações**.


|   Entidade        | Formulários   |Vistas        |
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

## <a name="set-up-bookable-resource-as-a-pricing-dimension"></a>Configurar recurso reservável como uma dimensão de definição de preços

1. Na interface Web, aceda a **Project Service** > **Definições** > **Parâmetros**. Na página **Parâmetro**, no separador **Dimensões de Definição de Preços Baseada no Montante**, note que a grelha no separador mostra os registos na entidade de dimensões de definição de preços. 
2. Adicione o **Recurso Reservável** a esta lista de dimensões de definição de preços como **msdyn_bookableresource**. 
3. Indique o contexto em que o recurso reservável funciona como a dimensão de definição de preços e defina os valores **Aplicável ao custo** e **Aplicável às vendas**.
4. No campo **Tipo de Dimensão**, selecione **Baseada no Montante**. 
5. Selecione a prioridade de custo e vendas para o recurso reservável. Normalmente, quando é incluído como uma dimensão de definição de preços, um recurso reservável tem a prioridade mais elevada, por isso definindo isto como **1** (ou **0** dependendo de como contabiliza a prioridade) irá assegurar esse comportamento.

## <a name="set-up-pricing-dimension-field-names"></a>Configurar nomes dos campos de dimensão de definição de preços

Quando o nome do campo de uma dimensão de definição de preços na tabela **Preço da Função** é diferente do respetivo nome de campo em qualquer uma das outras entidades em que as necessidades de predefinição de preços têm de funcionar, o registo de dimensão de definição de preços tem de tomar conhecimento dos diferentes nomes.    
Para o recurso reservável, a entidade **Membros da Equipa do Projeto** tem um nome de campo ligeiramente diferente (**msdyn_bookableresourceid**) do que é chamado na entidade **Preço da função** (**msdyn_bookableresource**). O registo de dimensão de definição de preços para **msydn_bookableresource** tem de tomar conhecimento disto. 
1. Para tal, faça duplo clique na linha da grelha **Dimensões de Definição de Preços** para abrir a página de dimensão de **msdyn_bookableresource**.
2. Na página de dimensão, no separador **Relacionado**, clique em **Nomes dos Campos de Dimensão de Definição de Preços**.

 ![Separador Nomes dos campos de dimensão de definição de preços](media/PD-fieldname.png)

4. Na vista associada que é aberta, clique em **Adicionar Novo Nome do Campo de Dimensão de Definição de Preços**.

 ![Adicionar Novos Nomes dos Campos de Dimensão de Definição de Preços](media/Add-NewPD-fieldname.png)


Esta ação abre a página **Novo nome do campo de dimensão de definição de preços** para **msdyn_bookableresource**. 

5. Adicione **msdyn_projectteam** ao campo **Nome Lógico da Entidade** e **msdyn_bookableresourceid** ao campo **Nome do Campo**. Guarde o registo.

 ![Formulário Novo nome do campo de dimensão de definição de preços](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]