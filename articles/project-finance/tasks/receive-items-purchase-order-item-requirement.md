---
title: Receber itens na nota de encomenda a partir do requisito do item
description: Este tópico explica como receber itens numa nota de encomenda a partir de um requisito de item.
author: KimANelson
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.assetid: c61e3a5e-da3d-4f4c-87fa-03dea19f6936
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5ed287aa24aff647ef1dc625f9e9f5f086ee662
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754471"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a>Receber itens na nota de encomenda a partir do requisito do item

[!include [task guide banner](../../includes/task-guide-banner.md)]

Este tópico explica como receber itens numa nota de encomenda a partir de um requisito de item.

Ao utilizar um requisito de item em vez de uma transação de item, pode planear a entrega imediatamente antes de o item ser realmente utilizado, criar uma nota de encomenda, incluir o item no quadro do acordo comercial e incluir o requisito de item no planeamento da produção. 

Esta tarefa utiliza o conjunto de dados USSI.

1. No painel de navegação, vá para **Módulos > Gestão de projetos e contabilística > Projetos > Todos os projetos**.
2. Na lista, selecione a ligação na linha pretendida.
3. No Painel de Ação, selecione **Plano**.
4. Selecione **Requisitos do item**.
5. Selecione **Novo**.
6. Na nova linha, introduza ou selecione um valor no campo **Número de item**.
7. No campo **Quantidade**, introduza um número.
8. Selecione **Guardar**.
9. No Painel de Ação, selecione **Gestor**.
10. Selecione **Funções**.
11. Selecione **Criar nota de encomenda**.
12. Selecione a caixa de verificação **Incluir tudo**.
13. No campo **Conta de fornecedores**, introduza ou selecione um valor.
14. Selecione **OK**.
15. No painel de navegação, vá para **Módulos > Contas a pagar > Notas de encomenda > Todas as notas de encomenda**.
16. Na lista, selecione a ligação na linha pretendida.
17. No Painel de Ação, selecione **Compra**.
18. Selecione **Confirmar**.
19. No Painel de Ação, selecione **Receber**.
20. Selecione **Receção de produto**.
21. No campo **Receção de produto**, digite um valor.
22. Selecione **OK**.

