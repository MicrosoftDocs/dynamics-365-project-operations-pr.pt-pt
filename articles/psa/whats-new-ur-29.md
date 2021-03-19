---
title: Novidades ou alterações na Versão da Atualização 29 do Project Service Automation, V3
description: Este tópico lista as funcionalidades e correções disponíveis no Project Service Automation V3, Versão da Atualização 29, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 711255ab66f84fe46d0f16fa72e5a10fe0360394
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/04/2021
ms.locfileid: "5499685"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a>Novidades ou alterações na Versão da Atualização 29 do Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a mais recente atualização à aplicação Project Service Automation para Dynamics 365. Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização. Esta versão é compatível com o Dynamics 365 9.x. Para atualizar esta versão, visite o Centro de Administração para o Dynamics 365 online e aceda à página de soluções para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Este tópico lista as funcionalidades e correções novas ou alteradas para o Project Service Automation V3, Versão da Atualização 29. Esta versão tem um número de compilação V3.10.45.98 e está geralmente disponível através de uma atualização automática em fevereiro de 2021.

## <a name="update-release-29"></a>Versão da Atualização 29

### <a name="bug-fixes"></a>Correções de erros

**Tempo e Despesa**

Foram corrigidos os seguintes problemas:

- Os utilizadores não podem ver horas de trabalho registadas em dias não úteis na grelha de entrada de tempo.
- As entradas de despesas aprovadas podem ser editadas na grelha.

**Gestão de Projetos**

Foram corrigidos os seguintes problemas:

- Lógica de validação em falta para garantir que as horas de esforço de atribuição de recursos não podem ser negativas.
- A ação personalizada **AssignResourcesForTask** atualiza todos os campos em vez de apenas campos alterados.
- Ao copiar um projeto num ambiente com plug-ins ou fluxos de trabalho registados no evento **CreateProject**, o atributo **msdyn_bulkgenerationstatus** não é atualizado se o **CopyWBSToProject** falhar.
- Quando se expande o calendário do projeto, os dias de trabalho não são classificados por ordem ascendente, fazendo com que algumas atualizações de tarefas do projeto falhem.
- Mudar o Gestor de Projeto num projeto existente desencadeia a lógica de incumprimento da unidade organizacional.

**Vendas**

Foram corrigidos os seguintes problemas:

- O separador **Desempenho do Contrato** na página **Contrato** falha silenciosamente durante a inicialização quando não existem linhas contratuais.
