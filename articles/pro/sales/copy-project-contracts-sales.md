---
title: Copiar contratos de projeto – lite
description: Este artigo fornece informações sobre copiar contratos de projeto no Project Operations.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a1846af677f7cea3ec22fdba4408f2bbd7db8a3c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932632"
---
# <a name="copy-project-contracts---lite"></a>Copiar contratos de projeto – lite

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

Pode facilmente criar novos contratos de projeto fazendo cópias dos contratos existentes de uma de duas formas: 

  - Na página da lista de **Contratos do Projeto**, selecione um contrato do projeto e, em seguida, selecione **Copiar**.
  - Na página de detalhes **Contrato de Projeto**, selecione **Copiar**.

Abrirá uma página de diálogo onde poderá selecionar os parâmetros do contrato copiado. Na caixa de diálogo estão incluídos os seguintes campos. Consoante os valores que selecionar neste diálogo, o processo de cópia poderá mudar.

| **Campo** | **Descrição** | **Impacto a jusante** |
| --- | --- | --- |
| Tópico | Introduza o tópico do contrato-alvo. Quando a página de diálogo é aberta, o sistema irá definir este campo para o nome do contrato de origem com **cópia** anexado. | Este campo não tem impacto a jusante. |
| Cliente | Referência ao registo da conta ou empresa do cliente. Quando a caixa de diálogo é aberta, o sistema irá definir este campo para a conta no contrato de origem. | Este campo é o cliente principal no contrato. |
| Unidade de Contratação | A unidade da Organização que é responsável pela entrega dos projetos associados a este negócio. Quando a página de diálogo é aberta, o sistema irá defini-la para a unidade de contratação do contrato de origem. | A unidade de contratação é a divisão da empresa que executará os projetos após o fecho do negócio. Cada unidade de contratação tem uma moeda. Esta moeda é utilizada para reportar os custos estimados e reais incorridos durante a execução do projeto. |
| Moeda | A moeda em que o negócio é transacionado. Quando a página de diálogo é aberta, o sistema irá definir o campo para a moeda do contrato de origem. Não é possível alterar a moeda. Se for, o campo **Definição de Preços de Cópia** é sempre definido como **Não** porque as listas de preços no contrato de origem já não são relevantes. | A moeda é utilizada para assumir a predefinição de listas de preços para criar estimativas financeiras sobre o contrato e, para faturação, o cliente quando o negócio é ganho. |
| Data de Entrega Pretendida | A data de entrega pedida pelo cliente. | Esta data é utilizada como a data final quando cria datas de faturação ao longo de uma frequência específica. |
| Copiar definição de preços | Indica se o preço no contrato deve ser copiado a partir do contrato de origem. | Se o campo estiver definido como **Sim**, a lista de preços do projeto e as referências da lista de preços do produto são copiadas do contrato de origem para o contrato-alvo. Se **Não** for selecionado, as listas de preços assumem um valor predefinido baseado nas listas de preços mais recentes nos parâmetros da conta ou do projeto. |

Quando seleciona **OK** na página de diálogo, o sistema cria uma cópia do contrato do projeto baseado nos parâmetros selecionados. O novo contrato será aberto.

As seguintes informações não são copiadas a partir da **Origem** para o **Contrato-alvo**:

  - Agendas de faturação
  - Clientes do contrato e do item de contrato
  - Referência do projeto nos itens de contrato baseados em projetos
  - Informações de orçamento do cliente

Como estas informações são específicas de cada contrato, estes campos e registos não são copiados. São copiadas os itens de contrato para projetos e produtos, as estimativas e detalhes de itens de contrato e os valores que não devem ser ultrapassados a nível do contrato. A taxa de preço e custo assume a predefinição consoante a seleção no campo **Copiar definição de preços** na página de diálogo **Copiar Parâmetros**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]