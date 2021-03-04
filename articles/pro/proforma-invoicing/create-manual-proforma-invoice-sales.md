---
title: Criar uma fatura pró-forma manual – lite
description: Este tópico fornece informações sobre a criação de uma fatura pró-forma manual no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5a924de6efc377e28a20e038e7deac04616b95aa
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764517"
---
# <a name="create-a-manual-proforma-invoice---lite"></a>Criar uma fatura pró-forma manual – lite

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

Em Dynamics 365 Project Operations, as faturas proforma podem ser criadas manualmente, conforme necessário. Pode criar manualmente uma fatura pró-forma a partir da página da lista **Contratos do Projeto** ou na página de detalhes **Contrato do Projeto**.

##  <a name="project-contracts-list-page"></a>Página de lista Contratos do Projeto

A partir da página da lista **Contratos do Projeto**, selecione um ou mais contratos de projeto e crie faturas para todos os registos selecionados.

O sistema verifica qual dos contratos de projeto selecionados tem uma tarefa pendente de **Pronto a Faturar** datado anterior à data de hoje. A partir desses contratos, o sistema cria faturas pró-forma de rascunho. Se um contrato de projeto tiver vários clientes, pode haver uma fatura criada por cliente, e várias faturas por contrato de projeto.

Todas as faturas do projeto criadas estão disponíveis na página **Fatura** na secção **Faturação** da área de **Vendas**.

## <a name="project-contract-details-page"></a>Página de detalhes Contrato do Projeto

Uma fatura proforma também pode ser criada a partir da página de detalhes do **Contrato de Projeto**. O sistema verifica que o contrato do projeto tem uma tarefa pendente de **Pronto a Faturar** com data anterior à data de hoje. A partir destes contratos, o sistema cria faturas pró-forma de rascunho com base no número de clientes em cada item de contrato.

Quando há uma única fatura pró-forma criada, a página **Fatura** abre. Se forem criadas várias faturas para esse contrato de projeto, a página da lista de **Faturas** abre-se para mostrar todas as faturas criadas.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]