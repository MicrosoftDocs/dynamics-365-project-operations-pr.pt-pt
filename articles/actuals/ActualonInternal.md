---
title: Impacto dos valores reais para um projeto interno
description: Este tópico fornece informações sobre o impacto na tabela Valores Reais em vários eventos para um projeto interno no Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 66a9ac4d2f56ae95313ed6731c3e51926105cff7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579780"
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
