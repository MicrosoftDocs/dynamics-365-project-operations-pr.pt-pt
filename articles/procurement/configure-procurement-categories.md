---
title: Utilizar categorias de aquisição com encomendas de compra de projeto e faturas de fornecedor pendentes
description: Este artigo descreve como configurar categorias de aquisição que podem ser utilizadas com encomendas de compra de projeto e faturas de fornecedor pendentes.
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 7d774631a4712de9b29ddedfee2ea3fc4a2d436f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927434"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Utilizar categorias de aquisição com encomendas de compra de projeto e faturas de fornecedor pendentes

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Os profissionais das compras podem criar e manter catálogos dos itens e serviços que podem ser utilizados em encomendas de compra de projeto e faturas de fornecedores pendentes. [Os catálogos de materiais](/dynamics365/supply-chain/procurement/procurement-catalogs) facilitam a categorização de compras sem ter de configurar e utilizar um catálogo de produtos lançados. Cada categoria de aquisição pode ser mapeada para uma categoria do projeto para transações de tempo, despesas ou itens. Depois da publicação de uma fatura de fornecedor pendente que utilize uma categoria de aquisição, o sistema irá criar valores reais de tempo, despesas ou materiais do projeto, transações do projeto e entradas auxiliares.

## <a name="minimum-version-requirements"></a>Requisitos mínimos da versão

As versões seguintes são necessárias para utilizar categorias de aquisição com encomendas de compra de projeto para cenários sem stock/baseados em recursos do Microsoft Dynamics 365 Project Operations:

- Versão da solução do Project Operations Dataverse 4.41.0.45 ou posterior
- Versão 10.0.26 ou posterior do ambiente Finanças e Operações

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Executar mapas de escrita dupla para suporte de categorias de aquisição

Certifique-se de o mapeamento para a **Entidade de exportação da linha da fatura de fornecedor do projeto de integração do Project Operations msdyn\_projectvendovoicelines** utiliza a versão 1.0.0.4 ou posterior.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Ativar a chave de funcionalidades para categorias de aquisição

Siga estes passos para ativar a funcionalidade de utilização de categorias de aquisição com encomendas de compra de projeto.

1. No Dynamics 365 Finance, abra a área de trabalho **Gestão de funcionalidades**.
1. Na lista de funcionalidades, encontre a funcionalidade **Usar categorias de aquisição no Project Operations para cenários baseados em recursos/sem stock** e, em seguida, selecione **Ativar**.

> [!IMPORTANT]
> Como pré-requisito, também tem de ativar a funcionalidade **Ativar faturas pendentes de fornecedor no Project Operations para cenários baseados em recursos/sem stock**.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Mapear categorias de projeto na hierarquia de categorias de Aquisição

Siga estes passos para mapear categorias de projeto para categorias de aquisição na **Hierarquia de categorias de aquisição**:

1. Aceda a **Aquisição e fornecimento \> Categorias de aquisição**.
1. Selecione **Editar hierarquia de categorias**.
1. Selecione o nó de hierarquia desejado e, em seguida, no separador **Atribuir categorias do projeto**, associe o nó à categoria do projeto a partir da categoria **Tempo**, **Despesa** ou **Projeto de item** (ou seja, a categoria **Tempo Predefinido** ou **Despesa Predefinida**).
1. Selecione **Guardar**.
1. Feche a página.

> [!NOTE]
> O mapeamento de uma categoria de aquisição para uma categoria de projeto é opcional. Se uma categoria de conteúdo não for mapeada, o sistema irá utilizar o valor definido no campo **Item** na secção **Predefinições de categoria do projeto** no separador **Dynamics 365 Customer Engagement no Project Operations** da página **Parâmetros de gestão de projeto e contabilidade**.
