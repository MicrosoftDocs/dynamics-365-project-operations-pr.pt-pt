---
title: Copiar propostas baseadas em projetos
description: Este tópico fornece informações sobre como copiar propostas baseadas em projetos no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e4e70ed1451c1076f72ef5d7200b918c626ab23c
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181826"
---
# <a name="copy-project-based-quotes"></a>Copiar propostas baseadas em projetos

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Pode criar facilmente uma nova Proposta de projeto ao copiar uma existente. 

- Para copiar uma Proposta de projeto, na página da lista **Propostas de Projeto** ou na página de detalhes **Proposta de Projeto**, selecione a Proposta de projeto que pretende copiar e, em seguida, selecione **Copiar**.

Isto abrirá uma página de diálogo onde poderá introduzir os parâmetros da cópia. A tabela seguinte lista os campos incluídos na página de diálogo. Consoante os valores que selecionar, o processo de cópia poderá mudar.

| **Campo** | **Descrição** | **Impacto a jusante** |
| --- | --- | --- |
| Tópico | Introduza o tópico relevante, ou o nome, da proposta-alvo. Quando a caixa de diálogo é aberta, o sistema irá defini-la para o tópico da proposta de origem com **-copy** anexado. | |
| Cliente Potencial | Referência ao registo da conta ou empresa do cliente. Quando a caixa de diálogo é aberta, o sistema irá defini-la para a conta na proposta de origem. | Este campo é o cliente principal na proposta. |
| Unidade de Contratação | A unidade organizacional que é responsável pela entrega dos projetos associados a este negócio.
Quando a caixa de diálogo é aberta, o sistema irá defini-la para a unidade de contratação da proposta de origem. | A unidade de contratação é a divisão da empresa que executará os projetos após o fecho do negócio. Cada unidade de contratação tem uma moeda. A moeda é utilizada para reportar os custos estimados e reais incorridos durante a execução do projeto. |
| Moeda | Esta é a moeda em que o negócio é transacionado. Quando a caixa de diálogo é aberta, o sistema irá defini-la para a moeda da proposta de origem. Isto pode ser modificado e, se for alterado, o campo **Copiar Definição de Preços** é sempre definido como **Não**. Isto porque as listas de preços na proposta de origem já não são relevantes. | A moeda é utilizada para assumir por predefinição uma lista de preços, para criar uma estimativa financeira sobre a proposta e, eventualmente, para faturar o cliente quando o negócio é ganho. |
| Data de Entrega Pretendida | Esta é a data de entrega solicitada pelo cliente. | Isto é utilizado como a data final ao criar datas de faturação ao longo de uma frequência específica. |
| Copiar definição de preços | Um valor Sim/Não indica se o preço na proposta deve ser copiado a partir do pedido de origem. | Se **Sim** for selecionado, a lista de preços do projeto e as referências da lista de preços do produto são copiadas da proposta de origem para a proposta-alvo. Se **Não** for selecionado, as listas de preços voltam a assumir um valor predefinido baseado nas listas de preços mais recentes que foram criadas nos parâmetros da conta ou do projeto. |

Quando seleciona **OK** na página de diálogo, o sistema cria uma cópia da proposta do projeto baseado nos parâmetros selecionados no diálogo. A nova proposta do projeto é aberta. 

> [!NOTE]
> As seguintes informações não são copiadas a partir da proposta de Origem para Destino:
>
> - Agendas de faturação
> - Clientes de proposta e linha de proposta
> - Referência de projeto no projeto, Linhas da proposta baseada, Informações do orçamento do cliente
>
>Como esta informação é muito específica de cada proposta, estes campos e registos não são copiados. São copiadas as linhas de proposta para projetos e produtos, as estimativas sobre os detalhes da linha de proposta e os valores que não devem ser ultrapassados a nível da proposta. As predefinições de preço e taxa de custo dependem da opção **Copiar definição de preços** selecionada na página de diálogo **Copiar parâmetros**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]