---
title: Propostas e linhas de proposta
description: Este artigo fornece informações sobre propostas e linhas de proposta.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 4c59f018adc7ee439fd77a819e2fb7620941e958
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933368"
---
# <a name="quotes-and-quote-lines"></a>Propostas e linhas de proposta

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

No Dynamics 365 Project Service Automation, existem dois tipos de propostas: propostas do projeto e propostas de vendas. Os dois tipos diferem das seguintes formas:

- Numa proposta de vendas, existe apenas uma grelha para itens de linha. Numa proposta de projeto, existem duas grelhas para itens de linha: uma para as linhas de projeto e outra para as linhas de produto.
- Uma proposta de vendas suporta a ativação e revisões. Uma proposta de projeto não suporta esses processos.
- Pode anexar várias encomendas a uma proposta de vendas. Só pode anexar um contrato de projeto a uma proposta do projeto.
- Pode ganhar uma proposta de vendas e manter a oportunidade relacionada aberta. Depois de uma proposta de projeto ser ganha, a oportunidade relacionada é fechada.
- Uma proposta de vendas não inclui alguns campos e conceitos que estão incluídos numa proposta de projeto com campos. Os campos incluem **Unidade de Contratação**, **Gestor de Contas** e **Nome do Contacto para Faturação**.  
- As propostas de vendas e as propostas do projeto também são identificadas por um campo baseado no conjunto de opções com o nome **Tipo**. Para uma proposta de vendas, este campo tem o valor **Baseado em item**. Para uma proposta do projeto, tem o valor **Baseado em trabalho**.

Este artigo irá concentrar-se nos detalhes das propostas do projeto.

Uma proposta do projeto no PSA pode ter múltiplos itens de linha ou linhas de proposta. Na verdade, uma proposta do projeto tem duas grelhas para os itens de linha. Uma grelha destina-se às linhas baseadas em projetos que permitem estimativas detalhadas. A outra grelha destina-se às linhas baseadas em produtos que utilizam um preço unitário simples e uma abordagem baseada em quantidade.

- **Baseado em projetos** – O montante (valor proposto) é determinado depois de estimar a quantidade de trabalho necessária. Pode estimar o trabalho num nível alto ou pode estimá-lo diretamente como detalhes de linha por baixo de cada linha de proposta. Por fim, pode estimar o trabalho com base em estimativas de raiz, utilizando um projeto e um plano do projeto. As linhas de proposta baseadas em projeto só são encontradas em propostas baseadas em projeto criadas através do Project Service Automation. Este tipo de linha de proposta é um formulário personalizado das linhas de proposta acrescentadas manualmente disponíveis no Microsoft Dynamics 365 Sales.
- **Baseado em produto** – O montante (valor proposto) é determinado com base na quantidade de unidades que são vendidas e no preço de venda unitário do produto. O produto numa linha baseada em produto pode provir de um catálogo de produtos em Vendas ou pode ser um produto que defina. Este tipo de linha de proposta também está disponível nas propostas baseadas em projeto criadas através da utilização de PSA.

O montante numa proposta é o total nas linhas baseadas em produto e nas linhas baseadas em projetos.

> [!NOTE]
> As propostas e as linhas de proposta não são necessárias no PSA. Pode iniciar o processo do projeto com um contrato de projeto (projeto vendido). No entanto, uma oportunidade é sempre necessária, quer tenha iniciado com uma proposta ou um contrato do projeto.

## <a name="project-based-quote-lines"></a>Linhas de proposta baseadas em projetos

Um item de proposta baseado em projetos no PSA tem os seguintes métodos de faturação:

- Tempo e material
- Preço fixo

### <a name="time-and-material"></a>Tempo e material

O método de faturação de tempo e material é baseado no consumo. Quando seleciona este método de faturação, o cliente é faturado à medida que o projeto incorre em custos. As faturas são criadas numa frequência periódica baseada na data. Durante o processo de vendas, o valor proposto de um componente de tempo e material fornece apenas uma estimativa do custo final ao cliente. O fornecedor não se compromete a concluir o projeto exatamente com o valor proposto. Os componentes de tempo e material aumentam o risco do cliente. Os clientes poderão pretender negociar cláusulas adicionais a não exceder para minimizar o risco. O PSA não suporta a definição de cláusulas a não exceder.

### <a name="fixed-price"></a>Preço fixo

No método de faturação de preços Fixos, um fornecedor compromete-se a entregar o projeto a um custo fixo ao cliente. Ao cliente é faturado o valor proposto da linha de proposta de preço fixo, independentemente dos custos que o fornecedor incorre para entregar essa linha de proposta. O valor da linha de proposta de preço fixo é faturado de uma das seguintes formas: 

- Como um montante único no início ou no final do projeto, ou quando um marco do projeto é atingido. 
- Numa frequência baseada em datas de prestações iguais do valor fixo na linha de proposta. Estas prestações são conhecidas como marcos periódicos.
- Em prestações com um valor monetário alinhado com o progresso do trabalho ou com marcos específicos alcançados no projeto. Neste caso, o valor de cada prestação pode ser diferente, mas tem de ser adicionado ao valor fixo na linha de proposta.

O PSA suporta os três tipos de agendas de faturação para as linhas de proposta de preço fixo.

## <a name="transaction-classification"></a>Classificação de transação

Normalmente, as organizações de serviços profissionais propõem e faturam os seus clientes por classificação de custos. No PSA, os custos são representados pelas seguintes classificações de transação:

- **Tempo** – Esta classificação representa o custo de trabalho ou o tempo dos recursos humanos num projeto.
- **Despesa**: – Esta classificação representa todos os outros tipos de despesas num projeto. Uma vez que as despesas podem ser amplamente classificadas, a maioria das organizações cria subcategorias, tais como viagens, aluguer de automóveis, hotel ou material de escritório.
- **Taxa** – Esta classificação representa despesas gerais diversas, penalizações e outros itens que são cobrados ao cliente. 
- **Imposto** – Esta classificação representa os montantes de imposto que os utilizadores adicionam enquanto introduzem as despesas.
- **Transação de material** – Esta classificação representa os valores reais a partir de linhas de produto numa fatura do projeto confirmada.
- **Marco** – Esta classificação é utilizada pela lógica de faturação de preço fixo no PSA.

Uma ou mais destas classificações de transação podem ser associadas a cada linha de proposta. Depois de uma proposta ser ganha, o mapeamento entre a classificação de transação e a linha de proposta é transferido para o item de contrato.
 
> ![Captura de ecrã do mapeamento de tipos de transação para itens de contrato e linhas de proposta.](media/basic-guide-5.png)
  
Por exemplo, uma proposta poderá conter as seguintes duas linhas de proposta: 
- Trabalho de consultadoria que utiliza um método de faturação de tempo e material em que as classificações de transação de tempo e taxas são aplicáveis. Por exemplo, todas as transações de tempo e taxa para o projeto de exemplo de **Implementação do Dynamics AX** são faturadas ao cliente com base no tempo e nos materiais que são utilizados. 
- Despesas de viagens relacionadas que utilizam um método de faturação de preço Fixo. Por exemplo, todas as despesas de viagem para o projeto de exemplo de **Implementação do Dynamics AX** são faturadas a um valor monetário fixo.

> [!NOTE]
> A combinação das classificações de projeto e transação de **Tempo**, **Despesa** e **Taxa** que estão associadas a uma linha de proposta ou item de contrato tem de ser exclusiva. Se a mesma combinação de projeto e classe de transação estiver associada a mais de um item de contrato ou linha de proposta, o PSA não funciona corretamente.

## <a name="billing-types"></a>Tipos de faturação

O campo **Tipo de Faturação** define o conceito de exigibilidade no PSA. Trata-se de um conjunto de opções que tem os seguintes valores possíveis:

- **Faturável** – O custo acumulado por esta função/categoria é um custo direto que conduz à execução do projeto e que o cliente irá pagar por este trabalho. O pagamento pode ser administrado como uma disposição de tempo e material ou de preço fixo. No entanto, o funcionário que passar este tempo receberá o crédito correspondente pela sua utilização faturável.
- **Não Faturável** – O custo acumulado por esta função/categoria é considerado um custo direto que conduz à execução do projeto, mesmo que o cliente não reconheça esse facto e não pague por este trabalho. O funcionário que passar este tempo não será creditado com a utilização faturável.
- **Grátis** – O custo acumulado por esta função/categoria é considerado um custo direto que conduz à execução do projeto e o cliente reconhece este facto. O funcionário que passar este tempo será creditado com a utilização faturável. No entanto, este custo não é cobrado ao cliente.
- **Não disponível** – Os custos incorridos nos projetos internos que não necessitam de monitorização das receitas são monitorizados através da utilização desta opção.

## <a name="invoice-schedule"></a>Agenda de faturação

Uma agenda de faturação é uma série de datas durante a faturação de um projeto. Opcionalmente, pode criar uma agenda de faturação numa linha de proposta no PSA. Cada linha de proposta pode ter a sua própria agenda de faturação. Para criar uma agenda de faturação, tem de fornecer os seguintes valores de atributo:

- Uma data de início da faturação 
- Uma data de entrega que representa a data de fim da faturação no projeto
- Uma frequência de faturação

O PSA utiliza estes três valores de atributo para gerar um conjunto de datas provisórias para estabelecer a faturação.

## <a name="invoice-frequency"></a>Frequência da Fatura

A frequência de faturação é uma entidade que armazena valores de atributos que ajudam a expressar a frequência da criação de faturas. Os seguintes atributos expressam ou definem a entidade de frequência de faturação:

- **Período** - São suportados períodos mensais, quinzenais e semanais. 
- **Execuções por período** - Para períodos semanais e quinzenais, pode definir apenas uma execução por período. Para períodos mensais, pode definir entre uma e quatro execuções por período. 
- **Dias de execução** – Os dias em que a faturação deve ser executada. Pode configurar este atributo de duas maneiras:
  - **Dias da semana** - Por exemplo, pode especificar que a faturação é executada a cada segunda-feira ou a cada segunda segunda-feira. Os clientes que têm de definir a faturação a ser executada num dia de trabalho podem preferir este tipo de configuração. 
  - **Dias do calendário** - Por exemplo, pode especificar que a faturação seja executada no sétimo e no vigésimo primeiro dias de cada mês. Algumas organizações poderão pretender este tipo de configuração, uma vez que ajuda a garantir que a faturação é executada numa agenda fixa a cada mês.
  
### <a name="invoice-schedule-for-a-fixed-price-quote-line"></a>Agenda de faturação para uma linha de proposta de preço fixo

Para uma linha de proposta de preço fixo, pode utilizar a grelha **Agenda de Faturação** para criar marcos de faturação que sejam iguais ao valor da linha de proposta.

- Para criar marcos de faturação igualmente divididos, selecione uma frequência de faturação, introduza a data de início da faturação na linha de proposta e selecione **Data de Conclusão Pretendida** para a proposta na secção **Resumo** do cabeçalho da proposta. Em seguida, selecione **Gerar Marcos Periódicos** para criar marcos igualmente divididos com base na frequência de faturação selecionada. 
- Para criar um marco de faturação de montante único, crie um marco e, em seguida, introduza o valor da linha de proposta como o montante do marco.
- Para criar marcos de faturação baseados em tarefas específicas no plano do projeto, crie um marco e mapeie-o para o elemento de agenda do projeto na IU do marco de faturação.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
