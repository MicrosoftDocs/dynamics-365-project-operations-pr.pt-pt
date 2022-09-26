---
title: Novidades ou alterações na Versão da Atualização 47 do Project Service Automation, V3
description: Este artigo lista as funcionalidades e correções disponíveis na Versão 47 da Atualização do Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/14/2022
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
ms.openlocfilehash: 08e8fa9c41bdd77d93e4d5207266115022fba1b2
ms.sourcegitcommit: 498a5d5a33c47cab788fac4215fc47662042155a
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/14/2022
ms.locfileid: "9477241"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-47-v3"></a>Novidades ou alterações na Versão da Atualização 47 do Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente para a aplicação Microsoft Dynamics 365 Project Service Automation. Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização. É compatível com o Dynamics 365, versão 9.x. Para atualizar para esta versão, visite a página de soluções online do Centro de Administração do Dynamics 365 e instale a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este artigo lista as funcionalidades e correções novas ou alteradas para a Versão 45 da Atualização do Project Service Automation, V3. Esta versão tem o número de compilação V3.10.78.8 e está em disponibilidade geral através de uma auto-atualização em julho de 2022.

## <a name="update-release-47"></a>Versão da Atualização 47

### <a name="bug-fixes"></a>Correções de erros

Foram corrigidos os seguintes problemas.

**Gestão de Recursos**
- Uma validação foi atualizada para garantir que os utilizadores não podem acionar uma exceção de referência null quando tentam criar um Membro da Equipa do Projeto sem um **Recurso Reservável**.
