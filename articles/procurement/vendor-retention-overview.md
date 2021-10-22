---
title: Descrição geral da retenção de fornecedores
description: Esta tópico fornece uma descrição geral das capacidades de retenção de fornecedores.
author: sigitac
ms.date: 10/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5f89904af5fb00eac46de834a438f412b371e74e
ms.sourcegitcommit: 098ea345ecfaf4445520094c32f5511b67e7953c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/02/2021
ms.locfileid: "7594617"
---
# <a name="vendor-retention-overview"></a>Descrição geral da retenção de fornecedores

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

A sua organização pode querer reter uma parte dos pagamentos a fornecedores que trabalham nos respetivos projetos. Por exemplo, antes de pagar ao seu fornecedor, pode pretender certificar-se de que os itens e os serviços fornecidos correspondem às suas expectativas.

Quando negoceia compras para projetos com fornecedores, pode especificar os termos de retenção de fornecedores que incluem a percentagem ou o montante a reter. À medida que o fornecedor entrega os itens e os serviços, deduz a percentagem de retenção especificada ou o montante do seu pagamento ao fornecedor. Quando o projeto ficar concluído ou atingir uma fase intermédia conforme especificado no contrato do fornecedor, liberta o montante retido e cria um pagamento ao fornecedor.

## <a name="vendor-retention-example"></a>Exemplo de retenção do fornecedor

O exemplo a seguir mostra como uma percentagem do montante da fatura do fornecedor é retida com base na percentagem de conclusão do projeto.

A Contoso Robotics USA contratou o fornecedor Fabrikam para entregar 100 horas de formação para o projeto de renovação de equipamentos. O valor total do contrato é de 30.000 USD com um preço de compra acordado de 300 USD por hora.

A formação será entregue em três fases com a seguinte agenda:

- Fase 1: 50 horas ou 50 por cento do projeto
- Fase 2: 30 horas ou 80 por cento do projeto no total
- Fase 3: 20 horas ou 100 por cento do projeto

A tabela a seguir lista os termos de retenção.

| **Percentagem de unidades entregues** | **Percentagem a reter** | **Percentagem a libertar** |
| --- | --- | --- |
| 50% | 20% | 0% |
| 80% | 10% | 10% |
| 100% | 0% | 100% |

As transações resultam nos seguintes montantes:

- Fase 1:
  - O montante a pagar é de 50 x 300 ou 15.000.
  - 20 por cento do montante ou 3000 são retido e serão libertados numa fase posterior.
  - O montante pago ao fornecedor é de 12.000.
- Fase 2:
  - O montante a pagar é de 30 x 300 ou 9000.
  - 10 por cento quantia ou 900 são retidos.
  - 10 por cento dos 3000 que foram retidos na Fase 1 ou 300 são libertados.
  - O montante pago ao fornecedor é de 8400. Este montante é de 9000 menos a retenção de 900 mais os 300 libertados da retenção na Fase 1.
- Fase 3:
  - O montante a pagar é de 20 x 300 ou 6000.
  - Nenhum montante é retido.
  - O valor libertado é de 3600. Este montante consiste nos 3000 retidos na Fase 1, menos os 300 da Fase 1 libertados na Fase 2, mais os 900 retidos na Fase 2.
  - O montante pago ao fornecedor é de 9600. Este montante consiste no montante retido de 3600 mais os 6000 para a conclusão da Fase 3.

O montante total pago ao fornecedor após a conclusão das três fases é de 30.000, ou seja, o montante total da nota de encomenda (15.000 + 9000 + 6000).
