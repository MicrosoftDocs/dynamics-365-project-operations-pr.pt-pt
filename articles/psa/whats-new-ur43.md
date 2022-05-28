---
title: Novidades ou alterações na Versão da Atualização 43 do Project Service Automation, V3
description: Este tópico lista as funcionalidades e correções que estão disponíveis na Versão de Atualização 43 do Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 05/04/2022
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
ms.openlocfilehash: fcf18a24b3bc354a16a415368063133743e79696
ms.sourcegitcommit: 7e419a5f73f80fa887084e3b212c90586fc397dd
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710041"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-43-v3"></a>Novidades ou alterações na Versão da Atualização 43 do Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente para a aplicação Microsoft Dynamics 365 Project Service Automation. Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização. É compatível com o Dynamics 365 9.x. Para atualizar para esta versão, visite a página de soluções online do Centro de Administração do Dynamics 365 e instale a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este tópico lista as funcionalidades e correções novas ou alteradas para o Project Service Automation V3, Versão da Atualização 43, V3. Esta versão tem o número de compilação V3.10.74.200 e está geralmente disponível através de uma atualização automática em maio de 2022.

## <a name="update-release-43"></a>Versão da Atualização 43

### <a name="bug-fixes"></a>Correções de erros

Foram corrigidos os seguintes problemas.


**Tempo e Despesa**

- Quando importa entradas de tempo a partir de reservas ou atribuições de recursos, a referência ao recurso a reservar relacionado não é mantida.
- Quando a grelha de entrada de tempo é expandida para ecrã inteiro, navegar na grelha com a chave do separador não funciona.
- Quando submete uma entrada de tempo criada por outro utilizador, o campo **Submetido Por** é povoado incorretamente com o utilizador que criou a folha de ponto.
