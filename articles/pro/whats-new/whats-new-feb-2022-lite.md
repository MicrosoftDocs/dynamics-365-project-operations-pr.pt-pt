---
title: O que há de novo fevereiro de 2022 - Implementação de Project Operations lite
description: Este artigo fornece informações sobre as atualizações de qualidade que estão disponíveis na versão de fevereiro de 2022 da implementação do Project Operations Lite.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1203faa2dd53a8fb82cff0857a1725426ebff19a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922834"
---
# <a name="whats-new-february-2022---project-operations-lite-deployment"></a>O que há de novo fevereiro de 2022 - Implementação de Project Operations lite

_Aplica-se a: Implementação lite – negócio para faturação pró-forma_

Este artigo aplica-se aos seguintes componentes e versões do Microsoft Dynamics 365 Project Operations:

- Project Operations num ambiente Dataverse, versão 4.28.0.120

## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versão

A partir desta versão, pode adicionar até 300 membros de equipa a um único projeto. Anteriormente, o limite para o número de membros de equipa era 150. Para obter mais informações, consulte [Limites do projeto](../../project-management/create-wbs.md#project-limitations).

## <a name="quality-updates"></a>Atualizações de qualidade

| Área de funcionalidades | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Faturação e preços | 2497369 | A correção de material tem de seguir o valor da data nos parâmetros **Correção**. |
| Faturação e preços | 2498697 | Melhorou a configuração de segurança para a **Revocação de entrada de tempo**. |
| Faturação e preços | 2517455 | A ação **Atualizadas transações de linha da fatura** não deve ter permissão para ser acionada várias vezes em simultâneo para a mesma fatura. |
| Faturação e preços | 2517465 | A ação **Desativar detalhes da linha de fatura** está bloqueada porque não é suportada. |
| Faturação e preços | 2556660 | Corrigidas as verificações de efetividade da data que estão feitas na lista de preços anexada a um registo de parâmetros do projeto. |
| Gestão de oportunidades | 2369202 | Corrigida a lógica de negócio que verifica que as listas de preços que têm datas de efetividade sobrepostas podem ser anexadas ao mesmo contrato do projeto. |
| Gestão de oportunidades | 2385965 | Corrigido o comportamento no separador **Clientes** da página **Contrato do projeto** quando seleciona **Guardar e fechar**. |
