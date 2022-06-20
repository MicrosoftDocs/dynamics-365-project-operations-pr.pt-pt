---
title: Novidades ou alterações na Versão da Atualização 28 do Project Service Automation, V3
description: Este artigo lista as funcionalidades e correções disponíveis na Versão 28 da Atualização do Project Service Automation, V3.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 56a87bce55c560e541e20709b10d38b9512ffcee
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930608"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>Novidades ou alterações na Versão da Atualização 28 do Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a mais recente atualização à aplicação Project Service Automation para Dynamics 365. Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização. Esta versão é compatível com o Dynamics 365 9.x. Para atualizar esta versão, visite o Centro de Administração para o Dynamics 365 online e aceda à página de soluções para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este artigo lista as funcionalidades e correções que são novas ou foram alteradas para o Project Service Automation V3, Atualização de Versão 28 Esta versão tem um número de compilação de V3.10.46.32 e, geralmente, está disponível através de uma atualização automática em janeiro de 2021.

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
