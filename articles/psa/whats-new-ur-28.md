---
title: Novidades ou alterações na Versão da Atualização 28 do Project Service Automation, V3
description: Este tópico lista as funcionalidades e correções disponíveis no Project Service Automation V3, Versão da Atualização 28, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 079679302b2d8dac3074732b2392a7b811ac9711
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280232"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>Novidades ou alterações na Versão da Atualização 28 do Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a mais recente atualização à aplicação Project Service Automation para Dynamics 365. Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização. Esta versão é compatível com o Dynamics 365 9.x. Para atualizar esta versão, visite o Centro de Administração para o Dynamics 365 online e aceda à página de soluções para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Este tópico lista as funcionalidades e correções novas ou alteradas para o Project Service Automation V3, Versão de Atualização 28 – esta versão tem um número de compilação V3.10.46.32 e está geralmente disponível através de uma atualização automática em janeiro de 2021.

## <a name="update-release-28"></a>Versão da Atualização 28

### <a name="bug-fixes"></a>Correções de erros

**Tempo e Despesa**

Foram corrigidos os seguintes problemas:

- Os utilizadores podem utilizar a **Edição a granel** para atualizar as entradas de tempo que foram aprovadas e submetidas.

**Gestão de Projetos**

Foram corrigidos os seguintes problemas:

- Nos casos em que a tarefa GUID é interpretada como um número, as tarefas não podem ser abertas para edição utilizando **Editar tarefa** no friso da página **Estrutura de hierárquica do trabalho**.

**Sales**

Foram corrigidos os seguintes problemas:

- Uma exceção de referência nula é gerada quando o plug-in **GetEstimatesForProject** é invocado.
- **Marcar como pronta para faturar** na grelha de marca apenas atualiza parcialmente os atributos, com exceção do atributo **Estado de fatura** que é atualizado.



[!INCLUDE[footer-include](../includes/footer-banner.md)]