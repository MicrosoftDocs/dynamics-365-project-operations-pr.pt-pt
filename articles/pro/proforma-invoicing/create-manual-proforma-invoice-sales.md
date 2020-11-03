---
title: Criar uma fatura pró-forma manual
description: Este tópico fornece informações sobre a criação de uma fatura pró-forma manual no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5e93206737507bf6698a9746815c790d3dfc904
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/20/2020
ms.locfileid: "4082633"
---
# <a name="creating-a-manual-proforma-invoice"></a>Criar uma fatura pró-forma manual

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

No Dynamics 365 Project Operations, as faturas pró-forma podem ser criadas manualmente, conforme necessário. Pode criar manualmente uma fatura pró-forma a partir da página da lista **Contratos do Projeto** ou na página de detalhes **Contrato do Projeto**.

##  <a name="project-contracts-list-page"></a>Página de lista Contratos do Projeto

A partir da página da lista **Contratos do Projeto** , selecione um ou mais contratos de projeto e crie faturas para todos os registos selecionados.

O sistema verifica qual dos contratos de projeto selecionados tem uma tarefa pendente de **Pronto a Faturar** datado anterior à data de hoje. A partir desses contratos, o sistema cria faturas pró-forma de rascunho. Se um contrato de projeto tiver vários clientes, pode haver uma fatura criada por cliente, e várias faturas por contrato de projeto.

Todas as faturas do projeto criadas estão disponíveis na página **Fatura** na secção **Faturação** da área de **Vendas**.

## <a name="project-contract-details-page"></a>Página de detalhes Contrato do Projeto

Uma fatura pró-forma também pode ser criada a partir da página de detalhes **Contrato do Projeto** , que cria a fatura para esse contrato específico do projeto. O sistema verifica se o contrato de projeto tem uma tarefa pendente de **Pronto a Faturar** que esteja com data anterior à de hoje. A partir destes contratos, o sistema cria faturas pró-forma de rascunho com base no número de clientes em cada item de contrato.

Quando há uma única fatura pró-forma criada, a página **Fatura** abre. Se houver várias faturas criadas para esse contrato de projeto, então a página da lista **Faturas** abre para mostrar todas as faturas criadas.
