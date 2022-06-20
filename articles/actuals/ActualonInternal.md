---
title: Impacto dos valores reais para um projeto interno
description: Este artigo fornece informações sobre o impacto na tabela Valores Reais em vários eventos para um projeto interno no Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: de05714c079fe121ef68e28b1acb82c24bce095e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921362"
---
# <a name="actuals-impact-for-an-internal-project"></a>Impacto dos valores reais para um projeto interno

_**Aplica-se a:** Project Operations para cenários baseados em recursos/não armazenados, implementação leve - negócio para faturação pró-forma_

A tabela seguinte lista os valores reais de diferentes tipos de transações criados em vários eventos numa cativação de projeto interno.

| Event | Custo real | Exemplo |
|---|---|---|
| O tempo foi criado. | Não aplicável | <p>Roberto Neves, da unidade organizacional Fabrikam US, que tem uma taxa de custo de 100 USD por hora, está a trabalhar num projeto denominado "Instalação Neves na Adatum". Este projeto está mapeado para um método de faturação de preço fixo no item de contrato. Eis uma amostra de entrada de tempo Roberto Neves:</p><p>Roberto Neves - 8 horas</p> |
| O tempo foi submetido. | Não aplicável | É criada uma linha do diário de custos para a entrada de tempo. A taxa de custo predefinida foi introduzida na entrada de diário. |
| A entrada de tempo é revocada antes de ser aprovada. | Não aplicável | |
| O tempo foi aprovado. | É criado um custo real. | <p>No valor real que é criado:</p><ul><li>**Custo real:** Roberto Neves, 8 horas, 800 USD</li></ul> |
| A aprovação do tempo foi cancelada. | <p>O estado de ajuste do valor real do custo original é atualizado para **Ajustado**.</p><p>É criado um valor real de custo que tem um estado de ajuste de **Não ajustável**.</p> | <p>Valor real existentes que foi atualizado:</p><ul><li>**Custo real:** Roberto Neves, 8 horas, 800 USD, *Ajustado*</li></ul><p>Novo valor real que foi criado para reverter o impacto financeiro anterior:</p><ul><li>**Custo real:** Roberto Neves, (8 horas), (800 USD), *Não ajustado*</li></ul> |
| A entrada de tempo é revocada depois de ser aprovada. | <p>O estado de ajuste do valor real do custo original é atualizado para **Ajustado**.</p><p>É criado um valor real de custo que tem um estado de ajuste de **Não ajustável**.</p> | <p>Valor real existentes que foi atualizado:</p><ul><li>**Custo real:** Roberto Neves, 8 horas, 800 USD, *Ajustado*</li></ul><p>Novo valor real que foi criado para reverter o impacto financeiro anterior:</p><ul><li>**Custo real:** Roberto Neves, (8 horas), (800 USD), *Não ajustado*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
