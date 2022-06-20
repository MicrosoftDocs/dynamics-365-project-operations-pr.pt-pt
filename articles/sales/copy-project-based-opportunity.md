---
title: Copiar oportunidades baseadas em projetos
description: Este artigo fornece informações sobre copiar oportunidades baseadas em projetos no Project Operations.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: cc772391de97f4b2de6e9e29f97a6af4d5514319
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926146"
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