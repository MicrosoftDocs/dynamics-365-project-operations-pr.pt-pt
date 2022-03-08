---
title: Vista geral do processo de faturação
description: Esta tópico fornece uma vista geral do processo de faturação no Project Operations para cenários baseados em recursos/não armazenados.
author: sigitac
manager: Annbe
ms.date: 01/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9dc424cf69abfccc10bf551272a14e5cefb3dff0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275821"
---
# <a name="invoicing-process-overview"></a>Vista geral do processo de faturação

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

O Project Operations para cenários baseados em recursos/não armazenados oferece capacidades abrangentes adaptadas às necessidades tanto do gestor do Projeto como do contabilista de contas a receber. Para o processo de faturação, o gestor do Projeto gere o atraso na faturação do projeto e o responsável/contabilista de contas a receber cria um documento de fatura compatível e preciso virado para o cliente.

![Diagrama do fluxo de faturação](./media/invoicing-flow.png)

A linha de contrato do projeto define o método de faturação para as transações de projetos associadas. Quando o gestor do Projeto aprova transações de tempo e despesas, o sistema regista as transações na entidade **Valores Reais do Projeto** e envia a informação para o módulo de **Gestão e contabilidade do Projeto** em Dynamics 365 Finance. Em seguida, o contabilista do Projeto revê e publica os registos utilizando o [diário de integração do Project Operations](../project-accounting/project-operations-integration-journal.md). Este diário inclui detalhes contabilísticos importantes para os valores reais do projeto, tais como faturação, grupo de impostos sobre vendas, grupo de imposto de venda de item de faturação, e dimensões financeiras.

O gestor do Projeto pode rever as transações de vendas não faturadas utilizando o método de faturação de tempo e material no tempo e o atraso de [faturação de material](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) e a faturação fixa de preços em [marcos de preço fixo](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones). Estas vistas permitem filtrar e selecionar transações que precisam de ser incluídas no próximo ciclo de faturação e, em seguida, marcá-las como **Pronto a faturar**.

Pode [criar manualmente uma fatura proforma](../proforma-invoicing/create-manual-proforma-invoice.md) ou utilizar um [processo periódico](../proforma-invoicing/configure-automated-invoice-creation.md). O gestor do Projeto pode [ajustar uma fatura proforma](../proforma-invoicing/manage-proforma-invoice.md) conforme necessário e, em seguida, confirmá-la.

A fatura proforma confirmada é enviada para o **Módulo de gestão e contabilidade do projeto** em Finanças. O Projeto de Contabilista forma e atualiza a proposta de fatura do projeto e, em seguida, publica e imprime o documento. As faturas do projeto registadas são registadas no livro geral, bem como nos sub-livros razão de clientes e projetos.


[!INCLUDE[footer-include](../includes/footer-banner.md)]