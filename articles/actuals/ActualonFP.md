---
title: Impacto real numa cativação de preço fixo
description: Este artigo fornece informações sobre o impacto na tabela Valores Reais em vários eventos durante o ciclo de vida de uma cativação de preço fixo no Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 50819d77d56935bfe5438d7d9dae99562bcc0b49
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918142"
---
# <a name="actuals-impact-in-a-fixed-price-engagement"></a>Impacto real numa cativação de preço fixo

_**Aplica-se a:** Project Operations para cenários baseados em recursos/não armazenados, implementação leve - negócio para faturação pró-forma_

A tabela seguinte lista os valores reais de diferentes tipos de transações criados em vários eventos numa cativação de preço fixo.

| Event | Custo real | Valor real de vendas não faturadas | Valor real de vendas faturadas | Exemplo |
|---|---|---|---|---|
| O tempo foi criado. | Não aplicável | Não aplicável | Não aplicável | <p>Roberto Neves, da unidade organizacional Fabrikam US, que tem uma taxa de custo de 100 USD por hora, está a trabalhar num projeto denominado "Instalação Neves na Adatum". Este projeto está mapeado para um método de faturação de preço fixo no item de contrato. Eis uma amostra de entrada de tempo Roberto Neves:</p><p>Roberto Neves - 8 horas</p> |
| O tempo foi submetido. | Não aplicável | Não aplicável | Não aplicável | É criada uma linha do diário de custos para a entrada de tempo. A taxa de custo predefinida foi introduzida na entrada de diário. |
| A entrada de tempo é revocada antes de ser aprovada. | Não aplicável | Não aplicável | Não aplicável | |
| O tempo foi aprovado. | É criado um custo real. | Não aplicável | Não aplicável | <p>No valor real que é criado:</p><ul><li>**Custo real:** Roberto Neves, 8 horas, 800 USD</li></ul> |
| A aprovação do tempo foi cancelada. | <p>O estado de ajuste do valor real do custo original é atualizado para **Ajustado**.</p><p>É criado um valor real de custo que tem um estado de ajuste de **Não ajustável**.</p> | Não aplicável | Não aplicável | <p>Valor real existentes que foi atualizado:</p><ul><li>**Custo real:** Roberto Neves, 8 horas, 800 USD, *Ajustado*</li></ul><p>Novo valor real que foi criado para reverter o impacto financeiro anterior:</p><ul><li>**Custo real:** Roberto Neves, (8 horas), (800 USD), *Não ajustado*</li></ul> |
| A entrada de tempo é revocada depois de ser aprovada. | <p>O estado de ajuste do valor real do custo original é atualizado para **Ajustado**.</p><p>É criado um valor real de custo que tem um estado de ajuste de **Não ajustável**.</p> | Não aplicável | Não aplicável | <p>Valor real existentes que foi atualizado:</p><ul><li>**Custo real:** Roberto Neves, 8 horas, 800 USD, *Ajustado*</li></ul><p>Novo valor real que foi criado para reverter o impacto financeiro anterior:</p><ul><li>**Custo real:** Roberto Neves, (8 horas), (800 USD), *Não ajustado*</li></ul> |
| O contrato está confirmado. | <p>O estado de ajuste dos valores reais de custo antigo é atualizado para **Ajustado**.</p><p>São criados valores reais de custo de reversão que têm um estado de ajuste **Não ajustável**.</p><p>Os novos valores reais de custo são criados após a reavaliação das regras contratuais.</p> | Não aplicável | Não aplicável | <p>Valor real existentes que foi atualizado:</p><ul><li>**Custo real:** Roberto Neves, 8 horas, 800 USD, *Ajustado*</li></ul><p>Novo valor real que foi criado para reverter o impacto financeiro anterior:</p><ul><li>**Custo real:** Roberto Neves, (8 horas), (800 USD), *Não ajustado*</li></ul><p>O novo valor real que é criado para reavaliar o impacto financeiro anterior:</p><ul><li>**Custo real:** Roberto Neves, 8 horas, 800 USD</li></ul> |
| É criada uma fatura. | Não aplicável | Não aplicável | Não aplicável | |
| A fatura é confirmada com um marco. | Não aplicável | Não aplicável | São criados novos valores reais de vendas faturadas baseados em marcos. | <p>Valor real existente que se mantém inalterado:</p><ul><li>**Custo real:** Roberto Neves, 8 horas, 800 USD</li></ul><p>O novo valor real que é criado para gravar os valores de vendas faturados:</p><ul><li>**Vendas reais faturadas:** Marco, 5.000 USD</li></ul> |
| A fatura é corrigida para creditar o marco. | Não aplicável | Não aplicável | São criados valores reais de vendas faturadas de reversão: | <p>Valor real existente que se mantém inalterado:</p><ul><li>**Custo real:** Roberto Neves, 8 horas, 800 USD</li></ul><p>Valor real existentes que foi atualizado:</p><ul><li>**Vendas reais faturadas**: Marco, 5.000 USD, *Ajustado*</li></ul><p>O novo valor real que é criado para reverter os valores de vendas faturados anteriores:</p><ul><li>**Vendas reais faturadas**: Marco, (5.000 USD), *Não ajustado*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
