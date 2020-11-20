---
title: Itens de oportunidade baseados em projetos
description: Este tópico fornece informação sobre como trabalhar com linhas de oportunidade baseadas em projetos.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0ede474e3d8830b420dc5b183f14327206c10288
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181961"
---
# <a name="project-based-opportunity-lines"></a>Itens de oportunidade baseados em projetos

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_


As linhas de oportunidade baseadas em projetos só estão disponíveis nas oportunidades baseadas em projetos. Os registos de oportunidade baseados em projetos têm o valor do campo **Tipo** definido como **Baseado em trabalho**.

As linhas de oportunidade baseadas em projetos são os itens que serão entregues ao cliente através de um projeto. No entanto, um projeto não pode ser associado a uma linha de oportunidade baseada em projetos. Os projetos podem ser associados a itens a partir da fase **Proposta**, porque normalmente a oportunidade ocorre numa fase inicial de um negócio. A determinação do número de projetos serão utilizados para entregar o trabalho ao cliente é uma decisão que é tomada mais tarde na fase de vendas. Utilize a fase de oportunidade para identificar os componentes de entrega discretos ao cliente. As decisões relacionadas com o número real de projetos utilizados para entregar estes componentes podem ser adiadas até se serem conhecidas mais informações sobre o trabalho em si.

Abaixo são mostrados os campos numa linha de oportunidade baseada em projetos:

| **Campo** | **Localização** | **Descrição** | **Impacto a jusante** |
| --- | --- | --- | --- |
| Tipo de Produto | Separador Geral (oculto) | Este é um campo de conjunto de opções. Se tiver o Dynamics 365 Operations instalado, uma das opções disponíveis é **Serviço baseado em projetos**.  | O valor deste campo está definido como **Serviço baseado em projetos** quando cria a linha de oportunidade baseada em projetos a partir da grelha de linhas baseada em projetos na Oportunidade. <br> Se alterar ou substituir este valor, a funcionalidade do projeto não será ativada nos itens baseados em projetos. |
| Oportunidade | Separador Geral | Este campo é só de leitura e referencia o registo de Oportunidade principal a que este item pertence. | Este campo não tem impacto a jusante. |
| Nome | Separador Geral | Este é um campo de texto editável que pode ser usado para dar uma identidade curta a este item | Este valor é transportado para a linha de proposta quando cria uma proposta a partir desta oportunidade |
| Orçamento do Cliente | Separador Geral | Este campo de moeda editável pode ser utilizado para monitorizar o montante que o cliente está disposto a gastar para este item. | Este valor é transportado para o campo correspondente na linha de proposta quando cria uma proposta a partir desta oportunidade |
| Método de Faturação | Separador Geral | Este campo editável tem os seguintes valores:</br>- Tempo e Material</br>- Preço Fixo | Este valor é transportado para o campo correspondente na linha de proposta quando cria uma proposta a partir desta oportunidade. Após a criação da linha de proposta, o campo é bloqueado e não pode ser alterado. Atribua este valor de campo com a maior precisão possível. Se precisar de alterar o valor deste campo na linha de proposta, elimine e volte a criar a linha de proposta. |
