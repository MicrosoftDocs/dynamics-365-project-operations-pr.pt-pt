---
title: Novidades ou alterações na Versão da Atualização 45 do Project Service Automation, V3
description: Este artigo lista as funcionalidades e correções disponíveis na Versão 45 da Atualização do Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/14/2022
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
ms.openlocfilehash: 98f7c973917d7d6334e6e0aeb15214c538b33143
ms.sourcegitcommit: 36fda4f45ddeb0f81d30bd1e22852727df644754
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169164"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-45-v3"></a>Novidades ou alterações na Versão da Atualização 45 do Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente para a aplicação Microsoft Dynamics 365 Project Service Automation. Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização. É compatível com o Dynamics 365, versão 9.x. Para atualizar para esta versão, visite a página de soluções online do Centro de Administração do Dynamics 365 e instale a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este artigo lista as funcionalidades e correções novas ou alteradas para a Versão 45 da Atualização do Project Service Automation, V3. Esta versão tem o número de compilação V3.10.76.168 e está em disponibilidade geral através de uma auto-atualização em julho de 2022.

## <a name="update-release-45"></a>Versão da Atualização 45

### <a name="bug-fixes"></a>Correções de erros

Foram corrigidos os seguintes problemas.

**Vendas**

- Os utilizadores não podem criar faturas com êxito depois de tentarem criar uma fatura sem vendas não faturadas, se também estão a ver a mesma instância da página e não a atualizem.

**Tempo e Despesa**

- Quando a opção Aprovações Modernas está ativada e uma aprovação do projeto é revocada, a fase do registo é incorretamente atualizada para **Aprovada revocação do pedido**.
- Quando a opção Aprovações Modernas está ativada e os fluxos de cloud estão inativos, o processo de aprovação não é bem-sucedido e os utilizadores submetidos ou aprovados não são notificados.
