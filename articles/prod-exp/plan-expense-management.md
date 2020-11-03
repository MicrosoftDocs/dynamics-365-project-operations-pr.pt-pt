---
title: Configurar gestão de despesas
description: Este artigo descreve as considerações e as decisões que deve tomar durante o processo de planeamento antes de configurar a gestão de Despesas no Microsoft Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2291515cc154fb5b34ca5802135791958bea1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082552"
---
# <a name="configure-expense-management"></a>Configurar gestão de despesas

[!include [banner](../includes/banner.md)]

Este tópico descreve as considerações e as decisões que deve tomar durante o processo de planeamento antes de configurar a gestão de Despesas. Na gestão de Despesas, pode armazenar informações sobre métodos de pagamento, requisições de viagem, relatórios de despesas, políticas, e assim por diante.

Porque muitas das decisões que toma quando planeia a sua configuração para a gestão de Despesas são baseadas na hierarquia e estrutura financeira da sua organização, deve consultar os documentos de planeamento dessas áreas.

## <a name="intercompany-expenses"></a>Despesas entre empresas

Quando permite Despesas entre empresas, permite que entidades jurídicas e colaboradores incorram em despesas em nome de outra entidade legal, e cobrem o pagamento da entidade legal de trabalho dentro da sua organização. Por exemplo, um colaborador na entidade legal A completa um projeto para a entidade legal B, e o projeto incorre em despesas relacionadas com viagens. Se as Despesas entre empresas forem ativadas, o trabalhador pode então apresentar um relatório de despesas que irá registar a despesa para a entidade legal B, e as despesas devem então ser pagas pela entidade legal A. Se a sua organização não tem várias entidades jurídicas, não tem de ativar Despesas entre empresas.

**Decisão:** Deseja ativar Despesas entre empresas?

## <a name="financial-management"></a>Gestão financeira

A gestão de despesas está fortemente integrada na gestão financeira da sua organização. Muitas das suas configurações para a gestão de Despesas serão baseadas nas decisões que tomou sobre as finanças da sua organização. As seguintes secções descrevem as várias áreas que requerem planeamento e decisões, com base nas decisões financeiras da sua organização e orientação da sua equipa de liderança.

### <a name="per-diems"></a>Subsídios diários

Deve definir o funcionário por dias que a sua organização fornece. Como os dias são normalmente usados para cobrir despesas como refeições, alojamento e outras despesas incidentais, pode criar regras para os subsídios por dia que a sua organização oferece. as tarifas de subsídio diário podem basear-se na época do ano, na localização da viagem ou em ambas. Ao definir uma regra de subsídio diário, pode especificar que uma percentagem da tarifa do subsídio diário será retida se um trabalhador receber refeições ou serviços gratuitos. Também pode definir um níveis de tarifas diárias para definir o número mínimo e máximo de horas para as quais a tarifa do subsídio por dia pode ser aplicada à viagem de um trabalhador.

**Decisões:**

- Regras diárias predefinidas para o primeiro e último dia:

    - Qual é o número mínimo de horas que um trabalhador pode solicitar por um dia e ainda receber um por dia?
    - Existe uma redução na quantidade que é oferecida para as refeições para o primeiro dia e último dia? Se houver uma redução, qual é a percentagem da redução?
    - Existe uma redução na quantidade que é oferecida para um hotel para o primeiro dia e último dia? Se houver uma redução, qual é a percentagem da redução?
    - Existe uma redução na quantidade que é oferecida para outras despesas incorridas no primeiro dia e último dia? Se houver uma redução, qual é a percentagem da redução?

- Regras por dia predefinidas:

    - Existe uma redução percentual do subsídio por dia por refeição se, por exemplo, a refeição for gratuita? Se houver uma redução, qual é a percentagem da redução para cada refeição?
    - A redução da refeição é calculada por dia, por viagem ou pelo número de refeições por dia?
    - As quantidades por da devem ser arredondadas da forma regular ou arredondada?
    - Os diários são calculados num período de 24 horas ou num dia de calendário?

- Regras por dia que são baseadas na localização:

    - As tarifas por dia variam de acordo com a localização? Quais as localizações incluídas?
    - Se as tarifas por dia variarem em função da localização, para cada local, qual o montante percentual fornecido para os seguintes tipos de despesas:

        - Refeições
        - Hotel
        - Outras despesas

### <a name="expense-management-journals-and-accounts"></a>Diários e contas de gestão de despesas

A gestão de despesas requer que utilize vários diários e contas. Deve decidir, por exemplo, se a mesma conta é usada para adiantamentos de dinheiro e litígios com cartão de crédito.

**Decisões:**

- Em que livro razão são publicados os relatórios de despesas aprovados?
- Que conta é usada para adiantamentos de dinheiro?
- Os adiantamentos em dinheiro devem ser publicados imediatamente?

### <a name="payment-methods"></a>Métodos de pagamento

Quando permite que os colaboradores incorram em despesas em nome do seu negócio, tem de definir os métodos de pagamento que os colaboradores podem utilizar. Por exemplo, pode permitir que os colaboradores utilizem dinheiro ou um cartão de crédito corporativo. Também pode permitir que os colaboradores utilizem cartões de crédito pessoais e, em seguida, reembolsa os empregados. Deve tomar as seguintes decisões por cada método de pagamento que permitir.

**Decisões:**

- Que métodos de pagamento são permitidos?
- Quem é o proprietário das despesas do método de pagamento?
- Existe um tipo de conta compensada? Se houver um tipo de conta de compensação, o que é?
- Se houver um tipo de conta de compensação, o que é a conta?
- Se o método de pagamento for um cartão de crédito, o método de pagamento deve ser utilizado apenas com transações importadas?

### <a name="expense-categories-and-shared-categories"></a>Categorias de despesas e categorias partilhadas

Quando os colaboradores criam um relatório de despesas, cada despesa que registam tem de ser associada a uma categoria de despesas. As categorias de despesas são derivadas das categorias partilhadas que podem ser partilhadas pelas entidades legais na sua organização. Estas categorias também podem ser partilhadas na gestão e contabilidade do Projeto, dependendo da forma como a sua organização é definida. Com base na definição da sua organização e na orientação da equipa de implementação, tem de determinar se as categorias que são utilizadas na Gestão de despesas serão utilizadas apenas na gestão de Despesas ou se devem ser partilhadas entre a gestão do Projeto e a contabilidade e gestão de Despesas. Note que estas categorias podem ser partilhadas entre a Gestão de projeto, e Despesas ou Projeto e Produção, mas não entre Despesas e Produção. Deve tomar as seguintes decisões para cada categoria de despesas.

**Decisões:**

- O que é uma categoria de despesa? Os exemplos incluem categorias para voos, hotel ou quilometragem.
- A categoria de despesa também pode ser utilizada na Gestão de projetos e contabilística?
- O que é um tipo de despesa?
- Qual o método de pagamento predefinido para a categoria de despesa?
- As despesas na categoria de despesa têm de ser discriminadas?
- Qual a conta predefinida principal para a categoria de despesa?
- Qual o grupo de impostos sobre as vendas de artigos predefinido para a categoria de despesa?
- São permitidos métodos de pagamento adicionais para a categoria de despesa? Se forem permitidos métodos de pagamento adicionais, quais são?
- Existem subcategorias nesta categoria de despesa? Se existirem subcategorias, também tem de tomar as seguintes decisões:

    - Alguma das subcategorias está excluída da recuperação de impostos?
    - Qual o grupo impostos sobre vendas de artigos das subcategorias?

Se a categoria de despesas também for utilizada na gestão e contabilidade do Projeto, responda às restantes questões. Caso contrário, passe para a próxima secção.

- Que contas de custos serão utilizadas para as seguintes despesas?

    - Custo
    - Alocação de vencimentos
    - Valor do custo WIP
    - Item de custo
    - Item de valor de custo WIP
    - Perdas acumuladas
    - Perdas acumuladas WIP

- Que contas de receitas serão utilizadas para o seguinte?

    - Receitas faturadas
    - Valor das vendas de receitas acumuladas
    - Valor de vendas WIP
    - Produção de receitas acumuladas
    - Produção WIP
    - Lucros de receitas acumuladas
    - Lucros WIP
    - Subscrição de receitas acumuladas
    - Subscrição WIP

### <a name="taxes"></a>Impostos

Para tarifas relacionadas com despesas, deve determinar o que está incluído ou ativado nos relatórios de despesas.

**Decisões:**

- O imposto sobre as vendas está incluído nos montantes das despesas?
- A recuperação de impostos deve ser ativada para as despesas?

    > [!NOTE]
    > Quando estava a planear o livro razão geral, se decidisse aplicar o imposto de vendas dos EUA e usar as regras fiscais, não pode ativar a recuperação de impostos nas despesas. (Para aplicar o imposto sobre vendas dos EUA e usar as regras fiscais, defina a opção **Aplicar impostos sobre vendas** como **Sim**.)

## <a name="policies"></a>Políticas

Ao criar políticas de relatório de despesas, pode ajudar a sua organização a economizar tempo e dinheiro quando os colaboradores incorrerem em despesas em seu nome. As políticas ajudam a garantir que os colaboradores permaneçam no orçamento, forneçam todas as informações necessárias e gastem dinheiro apenas quando assim o exigirem. Deve tomar as seguintes decisões para cada política de relatório de despesas e cada política de aprovação de relatório de despesas que criar.

**Decisões:**

- O que é o nome da política?
- Para que serve a política de despesas?
- Se já decidiu ativar Despesas entre empresas, a que empresas da sua organização se aplicará esta política?
- Quando é que a política entra em vigor?
- Quando expira a política?
- Qual é a regra da política?
- O que é o resultado da regra da política?
