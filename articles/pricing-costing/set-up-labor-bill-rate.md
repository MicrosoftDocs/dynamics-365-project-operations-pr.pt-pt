---
title: Configurar taxas de faturação de mão de obra
description: Este tópico fornece informações sobre como configurar taxas de faturação de mão de obra no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 501458510efca6434a51577aacd1f09d1a4faa25
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180721"
---
# <a name="set-up-labor-bill-rates"></a>Configurar taxas de faturação de mão de obra

_ **Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados

Cada lista de preços tem um conjunto de preços de função ou de taxas de mão de obra que estão vigentes com o contexto e a data de efetividade incluídos no cabeçalho da lista de preços. As taxas de faturação para tempo no Dynamics 365 Project Operations podem ser configuradas em apenas uma moeda, que é a moeda no cabeçalho da lista de preços.

1. Para configurar as taxas de faturação de mão de obra para uma lista de preços de vendas, crie uma lista de preços com base no cabeçalho da lista de preços. 
2. No separador **Preços de Função**, na subgrelha, selecione **+ Novo Preço de Função**. 
3. No painel **Criação Rápida**, insira a combinação de função e unidade de organização para a qual precisa de configurar a taxa de fatura.

   A tabela a seguir inclui os campos no separador **Geral** e o painel **Criação Rápida** de uma linha de preço de função que precisa de ter em mente à medida que cria preços de função numa lista de preços de vendas:

    | Campo | Localização | Descrição | Impacto a jusante |
    | --- | --- | --- | --- |
    | Função | Separador **Geral** e painel **Criação Rápida** | Selecione a função para a qual está a definir a taxa de fatura. | A função na estimativa de entrada ou real será igualada contra esta linha para assumir a predefinição da taxa de fatura da função. |
    | Empresa de Recursos | Separador **Geral** e painel **Criação Rápida** | Selecione a empresa ou entidade legal a que função pertence. Por exemplo, um programador da Fabrikam India ou um programador da Fabrikam USA. | A empresa de atribuição de recursos na estimativa de entrada ou real será igualada contra esta linha para assumir a predefinição da taxa de fatura da função. |
    | Unidade de Atribuição de Recursos | Separador **Geral** e painel **Criação Rápida** | Selecione a unidade organizacional ou divisão da empresa de onde esta função pertence. Por exemplo, um programador da divisão de Robótica da Fabrikam India ou um programador da divisão de Software da Fabrikam USA. | A unidade de atribuição de recursos na estimativa de entrada ou real será igualada contra esta linha para assumir a predefinição da taxa de fatura da função. |
    | Preço | Separador **Geral** e painel **Criação Rápida** | Configurar a taxa de fatura para a empresa de atribuição de recursos da função e combinação de unidade de atribuição de recursos. Por exemplo, um programador da Fabrikam India tem uma taxa de fatura de 100 USD ou um programador da Fabrikam USA tem uma taxa de fatura de 150 USD. | Este preço é a taxa de fatura predefinida no preço por unidade da estimativa de entrada ou linha real para a classe de transação Tempo. |
    | Moeda | Separador **Geral** e painel **Criação Rápida**| Por predefinição, o valor cambial provém da moeda no cabeçalho da lista de preços de vendas. Numa lista de preços de vendas, a moeda não pode ser substituída. | Esta moeda é a moeda predefinida no preço por unidade de entrada de linha de vendas real para a classe de transação Tempo. |
    | Agenda de Unidades | Separador **Geral** e painel **Criação Rápida** | Esta agenda de unidade assume a predefinição Tempo e não pode ser alterada na entidade de preço Função porque é usado para expressar taxas por unidades de tempo. | Este campo não tem impacto a jusante. |
    | Unidade | Separador **Geral** e painel **Criação Rápida** | O valor da unidade provém do campo **Unidade de Tempo** no cabeçalho da lista de preços de vendas. Mas o valor pode ser substituído. Por exemplo, um programador da Fabrikam India tem uma taxa de fatura de 1000 USD por **Dia na Índia**. Um programador da Fabrikam USA tem uma taxa de fatura de 1500 USD por **Dia nos EUA**. | Quando o preço por unidade assume a predefinição de uma estimativa de entrada ou linha de valor real, o sistema utiliza o sistema de unidades e a conversão em unidades base para calcular um preço por unidade. Por exemplo, a estimativa é de 10 **Dias na Índia** no valor de trabalho para um Programador na Índia, e a unidade Dia na Índia é definido como 10 horas. Ao fixar o preço desta linha de estimativa, a aplicação calcula o preço unitário na estimativa como 1000 USD/10 horas = 100 USD por hora. |

## <a name="transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions"></a>Preços de transferência ou configurar taxas de faturação para recursos a partir de outras divisões ou unidades organizacionais 

As empresas baseadas em projetos usam frequentemente colaboradores de diferentes entidades jurídicas e diferentes divisões dentro da entidade legal para trabalhar em projetos. Os projetos podem ser executados a partir de uma determinada entidade legal e divisão, enquanto os colaboradores ou consultores que trabalham nos projetos podem vir da mesma entidade legal e divisão ou de outra. O projeto poderia também ser constituído por uma combinação de pessoas de diferentes entidades jurídicas e divisões. No Project Operations, a entidade legal que detém a entrega do projeto é chamada de **Empresa Proprietária** e a divisão que detém a entrega é chamada de **Unidade Contratante**. Todas as outras entidades jurídicas que fornecem recursos são chamadas de **Empresas de Atribuição de Recursos** e as divisões que fornecem recursos são chamadas de **Unidades de Atribuições de Recursos**. Devido às diferenças nos custos de mão de obra em várias geografias e mercados de trabalho em todo o mundo, as taxas de faturação da mão de obra também são criadas de forma diferente para diferentes geografias.

Por exemplo, um programador da divisão de Robótica da Fabrikam India que trabalha no projeto dos EUA é faturado à taxa de 100 USD por hora. Um programador da divisão de Robótica da Fabrikam US que trabalha no Projeto dos EUA é faturado a 150 USD por hora. 

### <a name="example-set-up-a-bill-rate"></a>Exemplo: Configurar uma taxa de fatura 

1. Crie uma lista de preços de vendas chamada *Taxas de Faturação da Fabrikam US* e estabeleça a data de efetividade.
2. No lista de preços de vendas, introduza as seguintes informações de taxas:

    | Função | Empresa de recursos | Unidade de atribuição de recursos | Taxa de faturação |
    | --- | --- | --- | --- |
    | Programador | Fabrikam India | Fabrikam India – Robótica | 100€ |
    | Programador | Fabrikam Philippines | Fabrikam Philippines – Robótica | 90 $ |
    | Programador | Fabrikam US | Fabrikam US – Robótica | 150 $ |

3. Anexar a lista de preços de vendas, **Taxas de faturação da Fabrikam US** para a lista de preços do projeto do contrato do projeto ou a uma determinada conta.
