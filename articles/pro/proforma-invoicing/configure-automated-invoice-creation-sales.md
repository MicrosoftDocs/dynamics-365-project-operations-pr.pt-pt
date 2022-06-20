---
title: Configurar a criação automática de faturas
description: Este artigo fornece informações sobre a preparar e configurar a criação automática de faturas proforma.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c5160b22bd0d8a738c31a5105d83bd15cf136fab
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911748"
---
# <a name="set-up-automatic-invoice-creation"></a>Configurar criação automática de faturas 
 
_**Aplica-se a:** Implementação leve - negociar à faturação pró-forma, Project Operations para cenários baseados em recursos/não armazenados_

Pode configurar a criação automática de faturas no Dynamics 365 Project Operations. O sistema cria uma fatura pró-forma de rascunho com base na agenda de faturação de cada contrato de projeto e item de contrato. As agendas de faturação são configuradas ao nível do item de contrato. Cada item de um contrato pode ter uma agenda de faturação distinta, ou a mesma agenda de faturação pode ser incluída em todos os itens do contrato.

Quando cria uma fatura, o sistema cria sempre, pelo menos, uma fatura por contrato de projeto. Em alguns casos, podem haver várias faturas criadas. Por exemplo, se o contrato tiver vários clientes, o mesmo número de faturas será criado como o número de clientes que têm transações faturadas nesse contrato de projeto.

## <a name="understand-how-transactions-are-included-on-an-invoice"></a>Entenda como as transações são incluídas numa fatura 

Por vezes, cada item de contrato baseado em projeto especifica uma agenda de faturação separada. Por exemplo, os serviços de implementação do contrato Adatum têm os seguintes itens contratuais:

- Trabalho protótipo que é um preço fixo com dois marcos criados manualmente.
- Trabalho de implementação que inclui Tempo e será faturado quinzenalmente às segundas-feiras.
- Despesas incorridas que precisam de ser faturadas mensalmente na primeira segunda-feira de cada mês.

As agendas das faturas definidas em cada uma destes dois itens de linha parecem-se com a seguinte tabela:

| Item de contrato | Data de execução da fatura | Data limite da transação | Data do marco | Montante do marco |
| --- | --- | --- | --- | --- |
| Trabalho de protótipo | 5 de outubro, segunda-feira | - | 5 de outubro, segunda-feira | 5000 USD |
| - | 3 de novembro, terça-feira | - | 3 de novembro, terça-feira | 12,000 USD |
| Trabalho de implementação | 5 de outubro, segunda-feira | 4 de outubro, domingo | - | - |
| - | 19 de outubro, segunda-feira | 18 de outubro, domingo | - | - |
| - | 2 de novembro, segunda-feira | 1 de novembro, domingo | - | - |
| - | 16 de novembro, segunda-feira | 15 de novembro, domingo | - | - |
| Despesas incorridas | 5 de outubro, segunda-feira | 4 de outubro, domingo | - | - |
| - | 2 de novembro, segunda-feira | 1 de novembro, domingo | - | - |

Neste exemplo, quando a faturação automática é executada a:

- **4 de outubro ou qualquer data anterior**: não é gerada qualquer fatura para este contrato porque a tabela **Agenda de Faturação** para cada um destes itens de contrato não convoca 4 de outubro, domingo, como data de execução da fatura.
- **5 de outubro, segunda-feira**: uma fatura é gerada para:

    - Trabalho de protótipo que inclui o marco, se estiver marcado como **Pronto a Faturar**.
    - Trabalho de implementação que inclui todas as transações de Tempo criadas antes da data de validade da transação de 4 de outubro, domingo, que está marcada como **Pronto a Faturar**.
    - Despesas incorridas que incluem todas as transações de Despesas criadas antes da data de validade da transação de 4 de outubro, domingo, que está marcada como **Pronto a Faturar**.
  
- **A 6 de outubro ou qualquer data anterior a 19 de outubro**: não é gerada qualquer fatura para este contrato porque a tabela **Agenda de Faturação** para cada um destes itens de contrato não convoca 6 de outubro ou qualquer data anterior a 19 de outubro, como data de execução da fatura.
- **19 de outubro, segunda-feira**: é gerada uma fatura para trabalho de implementação que inclui todas as transações de Tempo criadas antes da data de validade da transação de 18 de outubro, domingo, que está marcada como **Pronto a Faturar**.
- **2 de novembro, segunda-feira**: uma fatura é gerada para:

    - Trabalho de implementação que inclui todas as transações de Tempo criadas antes da data de validade da transação de 1 de novembro, domingo, que está marcada como **Pronto a Faturar**.
    - Despesas incorridas que incluem todas as transações de Despesas criadas antes da data de validade da transação de 1 de novembro, domingo, que está marcada como **Pronto a Faturar**.

- **3 de novembro, terça-feira**: é gerada uma fatura para o trabalho de protótipo que inclui o marco para 12.000 USD, se estiver marcado como **Pronto a Faturar**.

## <a name="configure-automatic-invoicing"></a>Configurar faturação automática

Conclua os seguintes passos para configurar a execução de fatura automatizada.

1. Em **Project Operations**, aceda a **Definições** > **Configuração de Fatura Recorrente**.
2. Crie uma tarefa de lote e atribua-lhe o nome **Criar faturas no Project Operations**. O nome da tarefa de lote tem de incluir as palavras "criar faturas".
3. No campo **Tipo de Tarefa**, selecione **Nenhum**. Por predefinição, os campos **Frequência Diária** e **Está Ativo** estão definidas como **Sim**.
4. Selecione **Executar Fluxo de Trabalho**. Na caixa de diálogo **Pesquisar Registo**, verá três fluxos de trabalho:

- ProcessRunCaller
- ProcessRunner
- UpdateRoleUtilization

5. Selecione **ProcessRunCaller** e, em seguida, selecione **Adicionar**.
6. Na caixa de diálogo seguinte, selecione **OK**. Um fluxo de trabalho de **Suspensão** é seguido por um fluxo de trabalho do **Processo**. 

> [!NOTE]
> Também pode selecionar **ProcessRunner** no passo 5. Em seguida, quando selecionar **OK**, um fluxo de trabalho do **Processo** é seguido por um fluxo de trabalho de **Suspensão**.

Os fluxos de trabalho **ProcessRunCaller** e **ProcessRunner** criam faturas. O **ProcessRunCaller** chama o **ProcessRunner**. **ProcessRunner** é o fluxo de trabalho que, na realidade, cria as faturas. O fluxo de trabalha passa por todos os itens de contrato para os quais é necessário criar faturas e cria faturas para essas linhas. Para determinar os itens de contrato para os quais devem ser criadas faturas, a tarefa examina as datas de execução da fatura para os itens de contrato. Se os itens de contrato que pertencem a um contrato tiverem a mesma data de execução da fatura, as transações são combinadas numa fatura que tem duas linhas de fatura. Se não houver transações para as quais criar faturas, a tarefa ignora a criação de uma fatura.

Depois de **ProcessRunner** ter terminado a execução, chama o **ProcessRunCaller**, fornece a hora de fim e é fechado. **ProcessRunCaller** em seguida, inicia um temporizador que funciona durante 24 horas a partir da hora de fim especificada. No final do temporizador, o **ProcessRunCaller** é fechado.

A tarefa de processamento em lote para criar faturas é uma tarefa recorrente. Se este processamento em lote for executado muitas vezes, são criadas várias instâncias da tarefa e causam erros. Consequentemente, deverá iniciar o processamento em lote apenas uma vez e, em seguida, reiniciar se parar de ser executado.

> [!NOTE]
> A faturação do lote no Project Operations só funciona para itens de contrato do projeto que são configurados por horários da fatura. Uma linha de contrato com um método de faturação de preço fixo tem de ter marcos configurados. Uma linha de contrato de projeto com um método de faturação de tempo e material necessitará de uma configuração de agenda de faturamento baseado em datas.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
