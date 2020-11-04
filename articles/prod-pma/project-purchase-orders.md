---
title: Notas de encomenda para um projeto
description: Este artigo descreve os vários métodos que pode utilizar para criar notas de encomenda para um projeto. O método que utilizar depende do objetivo da nota de encomenda e quando os itens são consumidos e cobrados a um projeto.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd891aec5bcab66c5801a5d9ca8abbbf632d662d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082392"
---
# <a name="purchase-orders-for-a-project"></a>Notas de encomenda para um projeto

[!include [banner](../includes/banner.md)]

Este artigo descreve os vários métodos que pode utilizar para criar notas de encomenda para um projeto. O método que utilizar depende do objetivo da nota de encomenda e quando os itens são consumidos e cobrados a um projeto.

### <a name="methods-for-creating-a-purchase-order"></a>Métodos para criar uma nota de encomenda

Pode utilizar um dos seguintes métodos para criar uma nota de encomenda em Gestão de projetos e contabilística. O objetivo da nota de encomenda é determinar quando nota de encomenda é consumida e, portanto, quando os itens são cobrados a um projeto.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Método</th>
<th>Objetivo</th>
<th>Consumo de itens</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Crie uma nota de encomenda diretamente a partir de um projeto.</td>
<td>Utilize este método para comprar itens a um fornecedor externo para consumo num projeto. Pode criar a nota de encomenda de duas formas:
<ul>
<li>A partir do próprio projeto. Neste caso, o projeto já está definido para a nota de encomenda.</li>
<li>Ao navegar para a nota de encomenda do projeto. Tem de selecionar o fornecedor e o projeto para o qual pretende criar a nota de encomenda.</li>
</ul></td>
<td>Os itens são consumidos quando a fatura do fornecedor é atualizada.</td>
</tr>
<tr class="even">
<td>Crie uma nota de encomenda a partir de uma nota de encomenda.</td>
<td>Utilize este método para comprar itens quando criar uma ordem de venda a partir de um projeto.</td>
<td>Os itens são consumidos quando a ordem de venda é faturada ao cliente.</td>
</tr>
<tr class="odd">
<td>Crie uma nota de encomenda a partir de um requisito de item.</td>
<td>Utilize este método para comprar itens quando criar um requisito de item a partir de um projeto.</td>
<td>Os itens são consumidos quando o recibo de entrega do requisito de item é atualizado.</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> Quando atualiza a fatura do fornecedor ou o recibo de entrega, é-lhe solicitado que atualize o recibo de entrega no requisito de item.

Para mais informações, consulte [Receber itens na nota de encomenda a partir do requisito do item](tasks/receive-items-purchase-order-item-requirement.md).
