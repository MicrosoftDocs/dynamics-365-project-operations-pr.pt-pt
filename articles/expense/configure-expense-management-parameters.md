---
title: Configurar parâmetros de gestão de despesas
description: Este tópico descreve os parâmetros que controlam o comportamento geral na Gestão de despesas.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 8ecbd0abc16d0a29eea47d6bd1653a204a83de4c
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897285"
---
# <a name="configure-expense-management-parameters"></a>Configurar parâmetros de gestão de despesas

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Este tópico descreve os parâmetros que controlam o comportamento geral na Gestão de despesas.

## <a name="general"></a>Geral

| Campo                                                    | Descrição |
|----------------------------------------------------------|-------------|
| Tarifa de quilometragem padrão                                 | Introduza a taxa de reembolso para despesas de quilometragem. Esta taxa é multiplicada pela quilometragem que é introduzida para as despesas para calcular o montante que é reembolsado pelas despesas de viagem. |
| Validar o objetivo da despesa                                 | Ative esta opção para limitar os utilizadores a um conjunto de valores existente que está configurado no campo **Objetivo do relatório de despesas** quando criam relatórios de despesas. |
| Despesas pessoais pagas por                                | Selecione quem é responsável pelo pagamento de quaisquer montantes de transação de cartão de crédito que sejam categorizados como pessoais. |
| Apresentar o relatório de despesas completo no retorno               | Selecione esta opção para mostrar todas as despesas de um relatório de despesas quando os detalhes do documento original são vistos para um voucher específico que foi gerado quando o relatório de despesas foi lançado. |
| A pré-autorização de viagem é obrigatória                 | Selecione esta opção para exigir que uma requisição de viagem seja submetida e aprovada antes de um colaborador poder submeter um relatório de despesas. |
| Permitir a edição de distribuições antes do lançamento            | Selecione se as distribuições de um relatório de despesas podem ser editadas antes de serem lançadas. |
| Avaliar as políticas de gestão de despesas                     | Selecione quando as despesas são avaliadas para determinar se uma política de despesas foi violada. As despesas podem ser avaliadas por violações quando a entrada de despesas é introduzida e guardada, ou quando as despesas são submetidas para aprovação. As regras da política para os recibos que são necessários serão avaliadas quando a linha de despesas for guardada. |
| Permitir linhas de despesas entre empresas                         | Selecione se as despesas para outras entidades jurídicas podem ser introduzidas num relatório de despesas. |
| Permitir a edição da taxa de câmbio para as despesas de cartão de crédito | Selecione esta opção para permitir ao utilizador editar a taxa de câmbio para as despesas de cartão de crédito importadas. |
| Campos hierárquicos de vários níveis a apresentar                  | Selecione os campos de aprovador que são mostrados quando o tipo de atribuição de fluxos de trabalho está definido como uma hierarquia e a seleção **Hierarquia** é definida para utilizar a hierarquia de aprovação e a aprovação de despesas com vários níveis. Quando a hierarquia de aprovação de vários níveis for utilizada para um fluxo de trabalho, os campos selecionados serão mostrados no relatório de despesas e poderão ser editados. |
| Introduzir o número do cartão de crédito do colaborador                        | Selecione se um número de 15 caracteres ou 16 caracteres pode ser introduzido e guardado no campo **ID do cartão** na página **Cartões de crédito** para um colaborador. |
| Validar o objetivo da requisição de viagem                      | Ative esta opção para limitar os utilizadores a um conjunto de valores existente que está configurado no campo **Objetivo do relatório de despesas** quando criam requisições de viagem. |

## <a name="financial"></a>Atividades Financeiras

| Campo                                                                                    | Descrição |
|------------------------------------------------------------------------------------------|-------------|
| Nome do diário do livro razão                                                                | Selecione o nome do diário do livro razão no qual os relatórios de despesas aprovados são lançados. |
| Ativar a recuperação de impostos das despesas                                                        | Selecione esta opção para ativar a recuperação de impostos de despesas para as despesas elegíveis. Esta opção não pode ser selecionada se as regras do imposto sobre a utilização e o imposto sobre as vendas dos EUA estiverem ativadas. |
| Lançar adiantamentos de tesouraria imediatamente                                                           | Selecione esta opção para lançar um adiantamento de tesouraria aprovado quando o processo Pagar e transferir for concluído. Se esta opção não for selecionada, o processo Pagar e transferir gera um diário geral não lançado. |
| Data Contabilística correta durante o lançamento                                                   | Selecione esta opção para atualizar a data contabilística quando as despesas são lançadas, caso o período atual esteja em espera ou fechado. A data contabilística será definida para o período aberto seguinte. |
| Permitir o agrupamento de transações baseado na conta de compensação especificada no método de pagamento       | Selecione esta opção para resumir as transações de despesas para um relatório de despesas, baseado na conta de compensação que está especificada no método de pagamento para as despesas. |
| Imposto incluído                                                                             | Selecione esta opção para incluir o imposto sobre as vendas no montante das despesa por predefinição. |
| Libertar hipotecas ao fechar as requisições de viagem                                      | Selecione esta opção para libertar os fundos onerados quando uma requisição de viagem aprovada é fechada. |
| Permitir a submissão da requisição de viagem com o orçamento excedido para o registo do orçamento e o orçamento do projeto | Selecione esta opção para permitir aos colaboradores submeterem pedidos de viagem para aprovação, apesar de excederem o orçamento permitido que está definido no registo do orçamento ou o orçamento permitido para um projeto. |
| Permitir a submissão do relatório de despesas com o orçamento excedido para o registo do orçamento e o orçamento do projeto     | Selecione esta opção para permitir aos colaboradores submeterem relatórios de despesas para aprovação, apesar de excederem o orçamento permitido que está definido no registo do orçamento ou o orçamento permitido para um projeto. |
| Permitir a aprovação do relatório de despesas com o orçamento excedido apenas para o registo do orçamento                 | Selecione esta opção para permitir que os aprovadores aprovem relatórios de despesas que excedam o orçamento permitido que está definido no registo do orçamento. |

## <a name="per-diem"></a>Diária

| Campo                                 | Descrição |
|---------------------------------------|-------------|
| Mínimo de horas para subsídio diário            | Introduza o número mínimo de horas que um colaborador tem de trabalhar num dia para ser elegível para receber um subsídio diário pelas despesas relacionadas com viagens. Este valor é utilizado como um valor predefinido apenas para o campo **Mínimo de horas** para os níveis de tarifas de subsídio diário. |
| Percentagem para refeições                          | Introduza a percentagem predefinida do subsídio diário para refeições que são utilizadas no primeiro e no último dia da despesa relacionada com a viagem quando o campo **Calcular redução de refeição por** é definido como **Tipo de refeição por dia** ou **Número de refeições por dia**. O dia de trabalho no primeiro e último dia pode ser mais curto do que num dia de trabalho normal. Assim, o montante do subsídio por dia nesses dias pode ser diferente do valor padrão. Se a percentagem for definida como **0** (zero), as deduções do primeiro e último dia será de 0,00. |
| Percentagem do hotel                         | Introduza a percentagem predefinida do subsídio diário para hotéis que é utilizada no primeiro e último dia da despesa relacionada com a viagem. O dia de trabalho no primeiro e último dia pode ser mais curto do que num dia de trabalho normal. Assim, o montante do subsídio por dia nesses dias pode ser diferente do valor padrão. Se a percentagem for definida como **0** (zero), as deduções do primeiro e último dia será de 0,00. |
| Outras percentagens                         | Introduza a percentagem predefinida do subsídio diário para despesas diversas que é utilizada no primeiro e último dia da despesa relacionada com a viagem. O dia de trabalho no primeiro e último dia pode ser mais curto do que num dia de trabalho normal. Assim, o montante do subsídio por dia nesses dias pode ser diferente do valor padrão. Se a percentagem for definida como **0** (zero), as deduções do primeiro e último dia será de 0,00. |
| Redução da percentagem para o pequeno-almoço | Introduza o montante pelo qual o subsídio diário é reduzido para o pequeno-almoço. Por exemplo, se um colaborador receber um pequeno-almoço gratuito, poderá querer reduzir o montante do subsídio por dia em 10%. |
| Redução da percentagem para o almoço     | Introduza o montante pelo qual o subsídio diário é reduzido para o almoço. Por exemplo, se um colaborador receber um almoço gratuito, poderá querer reduzir o montante do subsídio por dia em 15%. |
| Redução da percentagem para o jantar    | Introduza o montante pelo qual o subsídio diário é reduzido para o jantar. Por exemplo, se um colaborador receber um jantar gratuito, poderá querer reduzir o montante do subsídio por dia em 25%. |
| Calcular a redução da refeição por           | Especifique como o sistema deve calcular a redução de refeições do subsídio diário ao selecionar se a redução se baseia no tipo de refeição por viagem ou por dia, ou se se baseia no número de refeições que é permitido por dia. |
| Arredondamento do subsídio diário                     | Selecione o tipo de arredondamento que é utilizado para as despesas do subsídio diário. Se selecionar o arredondamento normal, qualquer despesa do subsídio por dia com um montante de 0,5 será arredondado para 1, e qualquer despesa do subsídio por dia com um valor inferior a 0,5 é arredondada para 0. |
| Basear o cálculo do subsídio por dia em          | Selecione se um montante de subsídio por dia se baseia num dia do calendário ou num período de 24 horas. |

## <a name="fax-cover-pages"></a>Páginas de rosto de fax

| Campo                          | Descrição |
|--------------------------------|-------------|
| Instruções                   | Introduza as instruções que os colaboradores têm de seguir quando criam uma página de rosto para um fax que é utilizado para enviar recibos que estejam relacionados com um relatório de despesas. Para introduzir texto específico do idioma que será mostrado, consoante o idioma do utilizador, selecione **Traduções**. |
| ID de utilizador (Informações do código da barras) | Selecione esta opção para armazenar o identificador exclusivo de um colaborador no código de barras que é utilizado na página de rosto do fax. |
| Código de barras                       | Selecione o código de barras que é utilizado na página de rosto do fax. Os códigos de barras 39 e 128 são suportados na Gestão de despesas. |

## <a name="anti-corruption"></a>Anticorrupção

| Campo                                 | Descrição |
|---------------------------------------|-------------|
| Apresentar declaração anticorrupção   | Selecione esta opção para mostrar o texto anticorrupção quando um relatório de despesas é criado. Em seguida, podem ser ativadas categorias de despesas específicas que exigirão que a declaração anticorrupção seja selecionada no relatório de despesas. Por exemplo, uma categoria de ofertas relacionada com uma despesa de funcionário público pode exigir que o colaborador confirme que a despesa cumpra a política da empresa que está relacionada com funcionários públicos. |
| Mensagem anticorrupção para o submissor | Introduza o texto que deve ser mostrado a um colaborador que está a criar um relatório de despesas. Para introduzir texto específico do idioma que será mostrado, consoante o idioma do utilizador, selecione **Traduções**. |
| Mensagem anticorrupção para o aprovador  | Introduza o texto que deve ser mostrado ao aprovador quando um relatório de despesas é criado. Para introduzir texto específico do idioma que será mostrado, consoante o idioma do utilizador, selecione **Traduções**. |
