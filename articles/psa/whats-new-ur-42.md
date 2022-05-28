---
title: Novidades ou alterações na Versão da Atualização 42 do Project Service Automation, V3
description: Este tópico lista as funcionalidades e correções que estão disponíveis na Versão de Atualização 42 do Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/05/2022
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
ms.openlocfilehash: 32cb7a4c5fc29d5c0dcec37dd395ae69037435a2
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589210"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-42-v3"></a>Novidades ou alterações na Versão da Atualização 42 do Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente para a aplicação Microsoft Dynamics 365 Project Service Automation. Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização. É compatível com o Dynamics 365, versão 9.x. Para atualizar para esta versão, visite a página de soluções online do Centro de Administração do Dynamics 365 e instale a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este tópico lista as funcionalidades e correções novas ou alteradas para o Project Service Automation V3, Versão da Atualização 42, V3. Esta versão tem o número de compilação V3.10.73.61 e está geralmente disponível através de uma atualização automática em abril de 2022.

## <a name="update-release-42"></a>Versão da Atualização 42

### <a name="bug-fixes"></a>Correções de erros

Foram corrigidos os seguintes problemas.

**Tempo e Despesa**

- Quando uma folha de ponto é rejeitado, o utilizador que a rejeitou é identificado incorretamente como **Sistema**.
- Quando as entradas de tempo são importadas, o valor **Categoria do recurso** está em falta.
- Os aprovadores do projeto podem aprovar projetos submetidos quando as suas permissões não estão definidas especificamente como **Pode Aprovar**.

**Vendas**

- Quando os valores reais são registados em tarefas de nível não raiz, os custos reais são agregados incorretamente.
