---
title: Novidades ou alterações na Versão da Atualização 29 do Project Service Automation, V3
description: Este artigo lista as funcionalidades e correções disponíveis na Versão 29 da Atualização do Project Service Automation, V3.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 733bbad53933b2de62222e78e3c5c919543c59e9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915383"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a>Novidades ou alterações na Versão da Atualização 29 do Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a mais recente atualização à aplicação Project Service Automation para Dynamics 365. Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização. Esta versão é compatível com o Dynamics 365 9.x. Para atualizar esta versão, visite o Centro de Administração para o Dynamics 365 online e aceda à página de soluções para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este artigo lista as funcionalidades e correções novas ou alteradas para a Versão 29 da Atualização do Project Service Automation V3. Esta versão tem um número de compilação V3.10.47.7 e está geralmente disponível através de uma atualização automática em fevereiro de 2021.

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
