---
title: Copiar oportunidades baseadas em projetos
description: Este tópico fornece informações sobre como copiar oportunidades baseadas em projetos no Project Operations.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ae724d18e768b838f388b6fd089bfa657c937da1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013455"
---
# <a name="copy-project-based-opportunities"></a>Copiar oportunidades baseadas em projetos

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_


As oportunidades de projeto podem ser facilmente copiadas para criar novas oportunidades de projeto. 

1. Vá à página da lista **Oportunidades de Projeto** e selecione uma oportunidade da lista. Ou abra a página de detalhes de uma oportunidade específica. 
2. A partir de qualquer uma das páginas, selecione **Copiar**. Será aberta uma página de diálogo que contém as seguintes informações de campo. Consoante os valores que selecionou neste diálogo, o processo de cópia poderá mudar.

    | **Campo** | **Descrição** | **Impacto a jusante** |
    | --- | --- | --- |
    | Tópico | Introduza o tópico relevante da oportunidade-alvo. Quando a caixa de diálogo é aberta, o sistema irá defini-la para o tópico da oportunidade de origem com **-cópia** anexado. | Este campo não tem impacto a jusante. |
    | Conta | Referências ao registo da conta ou empresa do cliente. Quando a caixa de diálogo é aberta, o sistema irá defini-la para a conta na oportunidade de origem. | Este campo é o cliente principal na oportunidade. |
    | Unidade de Contratação | A unidade organizacional responsável pela entrega dos projetos associados a este negócio. Quando a caixa de diálogo é aberta, o sistema irá defini-la para a unidade de contratação da oportunidade de origem. | A unidade de contratação é a divisão da empresa que executa os projetos após o fecho do negócio. Todas as unidades de contratação têm uma moeda, e esta moeda é utilizada para reportar os custos estimados e reais incorridos durante o projeto. |
    | Moeda | A moeda em que o negócio é transacionado. Quando a página de diálogo é aberta, o sistema irá defini-la para a moeda da oportunidade de origem. | A moeda é usada para assumir a predefinição de uma lista de preços e para criar estimativas financeiras na proposta. Eventualmente, a moeda é usada para faturar o cliente quando o negócio é ganho. |
    | Copiar definição de preços | Um valor Sim/Não que indique se o preço na oportunidade deve ser copiado da oportunidade de origem. | Se **Sim** for selecionado, as listas de preços são copiadas da origem para a oportunidade-alvo. Se **Não** for selecionado, as listas de preços assumem um valor predefinido baseado nas listas de preços mais recentes que foram configuradas. |

3. Selecione **OK**. O sistema cria uma cópia da oportunidade do projeto com base nos parâmetros selecionados e a nova oportunidade de projeto é aberta.


[!INCLUDE[footer-include](../includes/footer-banner.md)]