---
title: Inquérito da Agenda de Despesas de Inquérito de Prémios Federais
description: Este tópico fornece informações sobre o inquérito da Agenda de Despesas de Prémios Federais.
author: velofog
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: johnmichalak
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: b88c97f3dcb1020ccf17788256990485580f6964
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684472"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a>Inquérito da Agenda de Despesas de Inquérito de Prémios Federais

[!include [banner](../includes/banner.md)]

De acordo com o Office of Management and Budget Circular A-133, as agências que recebem fundos federais estão sujeitas a requisitos de auditoria, que também são conhecidas como auditorias únicas. O processo de auditoria é utilizado para reportar, de forma recorrente, as receitas e as despesas das concessões federais. Parte do relatório único de auditoria inclui a Lista de Despesas de Prémios Federais (SEFA).

O inquérito da Agenda de Despesas de Prémios Federais inclui o Título e número do Catálogo de Assistência Interna Federal (CFDA), o número de concessão, o ano da concessão, o nome da agência federal que disponibiliza os fundos, e o nome da entidade pass-through. O inquérito é para um período específico. Tipicamente, esse período é o mesmo que o período da declaração financeira, que é um ano fiscal.

O inquérito inclui concessões que tenham datas de projeção no intervalo de datas selecionadas. A coluna **Agência concessora** do inquérito mostra o cliente da concessão ou, para uma concessão pass-through, a agência concessora. Para uma concessão pass-through, a coluna **Agência pass-through** mostra o cliente da concessão. Se a concessão não for uma concessão pass-through, a coluna **Agência pass-through** está em branco.

## <a name="set-up-the-cfda-clusters"></a>Configurar os clusters CFDA

Tem de configurar os clusters CFDA que podem ser associados aos números CFDA no inquérito da Agenda de Despesas de Prémios Federais.

1. Vá a **Gestão e contabilidade de projetos \> Configurar \> Concessões \> clusters de Catálogo de Apoio Nacional Federal**.
2. Selecione **Novo** para criar um cluster CFDA.
3. Introduza o nome do cluster.
4. Selecione **Guardar** para guardar as alterações.

## <a name="set-up-cfda-numbers"></a>Configurar números CFDA

Tem de configurar os números CFDA que podem ser adicionados a concessões e incluídos no inquérito da Agenda de Despesas de Prémios Federais.

1. Vá a **Gestão e contabilidade de projetos \> Configurar \> Concessões \> números de Catálogo de Apoio Nacional Federal**.
2. Selecione **Novo** para criar um número CFDA.
3. Na coluna **Número**, introduza o número CFDA.
4. Prima a tecla **Tab**.
5. Na coluna **Descrição**, introduza o título CFDA.
6. Prima a tecla **Tab**.
7. Opcional: No campo **Cluster do programa**, adicione o cluster CFDA apropriado.
8. Selecione **Guardar** para guardar as alterações.

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Configurar concessões para reportar para o inquérito de Agenda de Despesas de Prémios Federais

1. Vá a **Gestão e contabilidade de projetos \> Concessões \> Concessões**, e selecione uma concessão existente.
2. No Separador Rápido **Configuração**, no campo **Catálogo de Assistência Doméstica Federal**, atribua o número CFDA. O número do CFDA na concessão determina o cluster CFDA a reportar.
3. No Separador Rápido **Informações de contacto**, insira as informações do concessor seguindo estes passos:

    1. No campo **Cliente da concessão**, insira o cliente responsável pela concessão. Para uma concessão existente, estas informações podem já estar inseridas.
    2. Indique se o cliente da concessão é o financiador. Se o cliente de concessão for o financiador, deixe a caixa de verificação **Pass-through** por selecionar. Se outro cliente for o financiador, e o cliente da concessão for responsável por gastar e monitorizar o dinheiro, selecione a caixa de verificação **Pass-through**.

4. Se selecionou a caixa de verificação **Pass-through** no passo anterior, no campo **Agência concessora**, insira o cliente que forneceu a concessão. A agência concessora e o cliente não podem ser o mesmo cliente.

Aqui está um exemplo de uma concessão pass-through:

O governo federal financiou um projeto de infraestrutura para um estado. O governo federal deu o dinheiro ao estado para gastar. Neste caso, o governo federal é a agência de concessão, e o estado é o cliente da concessão.

> [!NOTE] 
> Quando executar a funcionalidade pela primeira vez, os números CFDA iniciais serão introduzidos utilizando os números existentes nas concessões.

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a>Excluir concessões de relatórios SEFA com base no tipo de concessão

1. Vá para **Gestão e contabilidade de projetos \> Configurar \> Concessões \> Tipos de concessão**.
2. No Separador Rápido **Informações predefinidas**, selecione a caixa de verificação **Excluir da Agenda de Despesas de Prémios Federais**.
3. Selecione **Guardar** para guardar as alterações.

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Execute o inquérito da Agenda de Despesas de Inquérito de Prémios Federais

1. Vá à **Gestão e contabilidade de projetos \> Inquéritos e relatórios \> Inquérito de concessão \> Agenda de Despesas de Prémios Federais**.
2. Na secção **Parâmetros**, siga estes passos:

    1. No campo **Intervalo de datas**, selecione o código para o intervalo de datas. Alternativamente, nos campos **De data** e **Até data**, defina o intervalo de datas.
    2. Opcional: Para incluir apenas as transações faturadas como receita no inquérito, defina a opção **Incluir apenas receitas faturadas** como **Sim**.

## <a name="columns"></a>colunas

A Agenda de Despesas de Prémios Federais inclui as seguintes colunas:

- Nome do cluster do Catálogo de Assistência Nacional Federal
- Agência de concessão
- Agência pass-through
- Nome da concessão
- ID da concessão
- ID da aplicação da concessão
- Catálogo de Assistência Nacional Federal
- Recibos
- Despesas


[!INCLUDE[footer-include](../includes/footer-banner.md)]