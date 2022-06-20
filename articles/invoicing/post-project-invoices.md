---
title: Vista geral do processo de faturação
description: Este artigo fornece uma descrição geral do processo de faturação no Project Operations para cenários baseados em recursos/não abastecidos.
author: sigitac
ms.date: 01/29/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 6b285a88be14a5972e9a4604713d7d35a3a442b6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923110"
---
# <a name="invoicing-process-overview"></a>Vista geral do processo de faturação

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

O Project Operations para cenários baseados em recursos/não armazenados oferece capacidades abrangentes adaptadas às necessidades tanto do gestor do Projeto como do contabilista de contas a receber. Para o processo de faturação, o gestor do Projeto gere o atraso na faturação do projeto e o responsável/contabilista de contas a receber cria um documento de fatura compatível e preciso virado para o cliente.

![Diagrama do fluxo de faturação.](./media/invoicing-flow.png)

A linha de contrato do projeto define o método de faturação para as transações de projetos associadas. Quando o gestor do Projeto aprova transações de tempo e despesas, o sistema regista as transações na entidade **Valores reais do projeto** e envia as informações para o módulo de **Gestão de projetos e contabilidade** no Dynamics 365 Finance. Em seguida, o contabilista do Projeto revê e publica os registos utilizando o [diário de integração do Project Operations](../project-accounting/project-operations-integration-journal.md). Este diário inclui detalhes contabilísticos importantes para os valores reais do projeto, tais como faturação, grupo de impostos sobre vendas, grupo de imposto de venda de item de faturação, e dimensões financeiras.

O gestor do Projeto pode rever as transações de vendas não faturadas utilizando o método de faturação de tempo e material no tempo e o atraso de [faturação de material](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) e a faturação fixa de preços em [marcos de preço fixo](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones). Estas vistas permitem filtrar e selecionar transações que precisam de ser incluídas no próximo ciclo de faturação e, em seguida, marcá-las como **Pronto a faturar**.

Pode [criar manualmente uma fatura proforma](../proforma-invoicing/create-manual-proforma-invoice.md) ou utilizar um [processo periódico](../proforma-invoicing/configure-automated-invoice-creation.md). O gestor do Projeto pode [ajustar uma fatura proforma](../proforma-invoicing/manage-proforma-invoice.md) conforme necessário e, em seguida, confirmá-la.

A fatura proforma confirmada é enviada para o **Módulo de gestão e contabilidade do projeto** em Finanças. O Projeto de Contabilista forma e atualiza a proposta de fatura do projeto e, em seguida, publica e imprime o documento. As faturas do projeto registadas são registadas no livro geral, bem como nos sub-livros razão de clientes e projetos.


[!INCLUDE[footer-include](../includes/footer-banner.md)]