---
title: Linhas de oportunidade baseadas em projetos – lite
description: Este artigo fornece informações sobre linhas de oportunidade baseadas em projetos. (Pro)
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8b5a8fc32ca903d7da2e090137bed358b364902a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914278"
---
# <a name="project-based-opportunity-lines---lite"></a>Linhas de oportunidade baseadas em projetos – lite

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

As linhas de oportunidade baseadas em projetos só estão disponíveis nas oportunidades baseadas em projetos. Os registos de oportunidade baseados em projetos têm o valor do campo **Tipo** definido como **Baseado em trabalho**.

As linhas de oportunidade baseadas em projetos são os itens que serão entregues ao cliente através de um projeto. No entanto, um projeto não pode ser associado a uma linha de oportunidade baseada em projetos. Os projetos podem ser associados a itens a partir da fase **Proposta** e reencaminhados, porque normalmente a oportunidade está numa fase inicial no ciclo de vida de um negócio. A determinação do número de projetos serão utilizados para entregar o trabalho ao cliente é uma decisão que é tomada mais tarde na fase de vendas. Pode utilizar a fase de oportunidade para identificar os componentes de entrega discretos ao cliente. As decisões relacionadas com o número real de projetos utilizados para entregar estes componentes podem ser adiadas até se serem conhecidas mais informações sobre o trabalho em si.

Abaixo são mostrados os campos numa linha de oportunidade baseada em projetos:

| **Campo** | **Localização** | **Descrição** | **Impacto a jusante** |
| --- | --- | --- | --- |
| Tipo de Produto | Separador Geral (oculto) | Pode selecionar uma das seguintes opções:</br>- Serviço baseado em projetos (disponível apenas quando o Dynamics 365 Project Operations estiver instalado)</br>- Produto (disponível apenas quando o Project Operations e o Dynamics 365 Sales estão instalados) | O valor deste campo está definido como **Serviço baseado em projetos** quando cria uma linha de oportunidade baseada em projetos a partir da grelha de linhas baseada em projetos na Oportunidade. <br> Se alterar ou substituir este valor, a funcionalidade do projeto não será ativada nos itens baseados em projetos. |
| Oportunidade | Separador Geral | Este campo é só de leitura e referencia o registo de Oportunidade principal a que este item pertence. | Este campo não tem impacto a jusante. |
| Nome | Separador Geral | Este campo de texto editável pode ser usado para atribuir uma identidade curta ao item. | Este valor é transportado para a linha de proposta quando cria uma proposta a partir desta oportunidade. |
| Orçamento do Cliente | Separador Geral | Este campo de moeda editável pode ser utilizado para monitorizar o montante que o cliente está disposto a gastar para este item. | Este valor é transportado para o campo correspondente na linha de proposta quando cria uma proposta a partir desta oportunidade. |
| Método de Faturação | Separador Geral | Este campo editável tem os seguintes valores:</br>- Tempo e Material</br>- Preço Fixo | Este valor é transportado para o campo correspondente na linha de proposta quando cria uma proposta a partir desta oportunidade. Após a criação da linha de proposta, o campo é bloqueado e não pode ser alterado. Atribua este valor de campo com a maior precisão possível. Se precisar de alterar o valor deste campo na linha de proposta, elimine e volte a criar a linha de proposta. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]