---
title: Copiar contratos baseados em projetos
description: Este artigo fornece informações sobre a cópia de contratos de projeto no Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 21994ef6d8f6e6cdf321599d107cc80368c96ecc
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410338"
---
# <a name="copy-project-based-contracts"></a>Copiar contratos baseados em projetos

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Pode facilmente criar novos contratos de projeto, copiando os contratos existentes de uma de duas formas:

- Na página da lista **Contratos do projeto**, selecione um contrato do projeto e, em seguida, selecione **Copiar**.
- Na página de detalhes **Contrato de Projeto**, selecione **Copiar**.

Em ambos os casos, aparece uma caixa de diálogo, onde pode definir os parâmteros do contrato copiado. A caixa de diálogo inclui os seguintes campos. Consoante os valores que selecionar, o processo de cópia poderá mudar.

| Campo | Description | Impacto a jusante |
| --- | --- | --- |
| Tópico | Introduza o tópico do contrato-alvo. Quando a caixa de diálogo é aberta, o sistema define o campo para o nome do contrato de origem, mas com a palavra "cópia" anexada ao mesmo. | Este campo não tem impacto a jusante. |
| Cliente | Uma referência ao registo da conta ou empresa do cliente. Quando a caixa de diálogo é aberta, o sistema define o campo para a conta no contrato de origem. | Este campo é o cliente principal no contrato. |
| Empresa Proprietária | A companhia é responsável pela entrega dos projetos que estão associados a este negócio. Quando a caixa de diálogo é aberta, o sistema define o campo para a empresa proprietária do contrato de origem. | A empresa proprietária é a entidade legal que irá executar o projeto após o negócio ser fechado. A moeda da empresa proprietária deve corresponder à moeda da unidade contratante. |
| Unidade de Contratação | A unidade da organização que é responsável pela entrega dos projetos que estão associados a este negócio. Quando a caixa de diálogo é aberta, o sistema define o campo da unidade contratante do contrato de origem. | A unidade de contratação é a divisão da empresa que executará os projetos após o fecho do negócio. Cada unidade de contratação tem uma moeda. Esta moeda é utilizada para reportar os custos estimados e reais incorridos durante a execução do projeto. |
| Moeda | A moeda em que o negócio é transacionado. Quando a página de diálogo é aberta, o sistema define o campo para a moeda do contrato de origem. Não é possível alterar a moeda. Se for, o campo **Definição de preços de cópia** é sempre definido como **Não**, porque as listas de preços no contrato de origem já não são relevantes. | Esta moeda é utilizada para as listas de preços predefinidas, para gerar estimativas financeiras sobre o contrato e faturar ao cliente quando o negócio é ganho. |
| Data de Entrega Pretendida | A data de entrega que é pedida pelo cliente. | Esta data é utilizada como a data de fim quando cria datas de faturação numa frequência específica. |
| Copiar definição de preços | Um valor que indica se o preço no contrato deve ser copiado a partir do contrato de origem. | Se o campo estiver definido como **Sim**, as referências da lista de preços do projeto e do produto são copiadas do contrato de origem para o contrato de destino. Se estiver definido como **Não**, são usadas as listas de preços predefinidas, baseadas nas listas de preços mais recentes nos parâmetros da conta ou do projeto. |

Quando seleciona **OK** na caixa de diálogo, o sistema cria uma cópia do contrato, baseado nos valores de parâmetro que definiu. Em seguida, o novo contrato é aberto.

As informações seguintes **não** são copiadas do contrato de origem para o contrato de destino, porque são específicas de cada contrato:

- Agendas de faturação
- Clientes do contrato e do item de contrato
- Referência do projeto nos itens de contrato baseados em projetos
- Informações de orçamento do cliente

São copiadas os itens de contrato para projetos e produtos, estimativas nos detalhes de itens de contrato e os valores que não devem ser ultrapassados a nível do contrato. A entrada de preços predefinidos e as taxas de custo dependem da seleção no campo **Copiar definição de preços** na caixa de diálogo **Copiar parâmetros**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
