---
title: Descrição geral da faturação interempresa
description: Este tópico fornece informações e exemplos sobre a faturação interempresa para projetos.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 670b5d15ecf1ef7dcc034064e625814cbe6d54b0
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595531"
---
# <a name="intercompany-invoicing-overview"></a>Descrição geral da faturação interempresa

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

A sua organização pode ter múltiplas divisões, subsidiárias e outras entidades jurídicas que transferem produtos e serviços entre si para projetos. A entidade legal que presta o serviço ou produto é denominada *entidade legal de concessão*. A entidade legal que recebe o serviço ou produto é denominada *entidade legal de contração*.

A seguinte ilustração mostra um cenário típico em que duas entidades legais, a Contoso Robotics USA (entidade legal de contração) e a Contoso Robotics UK (entidade legal de concessão) partilham recursos para entregar um projeto para o cliente, a Adventure Works. Para este cenário, a Contoso Robotics USA está contratada para entregar o trabalho à Adventure Works.

![Faturação entre empresas](./media/IntercompanyScenario.png) 

O Dynamics 365 Project Operations utiliza o seguinte fluxo para processar transações interempresa:

1. Os recursos da entidade legal de concessão registam o tempo ou as transações de despesas interempresa através da reserva de tempo e despesas contra projetos na entidade legal de contração.
2. Os custos de tempo e despesa são registados na empresa de concessão utilizando a lista de preços de custo de unidade da empresa de contração.
3. As transações de venda não faturadas interempresa são registadas na empresa de concessão utilizando a lista de preços de custo de unidade da empresa de contração.
4. As receitas não faturadas são registadas na empresa de contração utilizando a lista de preços de vendas do contrato de projeto. O cliente pode ser cobrado quando as receitas não faturadas são registadas. O cliente não tem de esperar até que o processamento da faturas interempresa esteja completo.
5. As faturas de clientes interempresa são criadas periodicamente na empresa de concessão. As faturas são criadas manualmente ou utilizando um processo automatizado periódico. Uma única fatura pode ser criada para cada entidade legal de contração ou faturas separadas podem ser criadas por projeto.
6. Quando a fatura de cliente interempresa é publicada na entidade legal de concessão, a fatura de fornecedor correspondente é criada na entidade legal de contração. Os custos na fatura de fornecedor pendente serão registados no sub-livro razão do projeto quando a fatura for publicada.

O diagrama que se segue ilustra a faturação interempresa no que diz respeito a eventos contabilísticos e publicações esperadas no livro razão geral.

![Fluxo interempresa](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a>Recursos adicionais

- [Configurar faturação interempresa](configure-intercompany-invoicing.md)
- [Registar transações interempresa](create-intercompany-transactions.md)
- [Criar faturas de clientes e fornecedores interempresa](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]