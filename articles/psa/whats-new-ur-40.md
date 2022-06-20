---
title: Novidades ou alterações na Versão da Atualização 40 do Project Service Automation, V3
description: Este artigo lista as funcionalidades e correções disponíveis na Versão 40 da Atualização do Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/31/2022
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
ms.openlocfilehash: dca7f340b8d544b183aa0390ac3c11a38f536ed0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912806"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-40-v3"></a>Novidades ou alterações na Versão da Atualização 40 do Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente para a aplicação Microsoft Dynamics 365 Project Service Automation. Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização. É compatível com o Dynamics 365, versão 9.x. Para atualizar para esta versão, visite a página de soluções online do Centro de Administração do Dynamics 365 e instale a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este artigo lista as funcionalidades e correções novas ou alteradas para a Versão 40 da Atualização do Project Service Automation, V3. Esta versão tem um número de compilação V3.10.61.61 e está geralmente disponível através de uma atualização automática em fevereiro de 2022.

## <a name="update-release-40"></a>Versão da Atualização 40

### <a name="features"></a>Funcionalidades
Fase 1 da atualização do Project Service Automation para o Project Operations - A implementação Lite será lançada em fevereiro de 2022 para todos os clientes. Para confirmar a sua eligibilidade, consulte [Atualizar do Project Service Automation para o Project Operations](upgrade-project-operations-non-stocked.md). Se a aplicação não aparecer na sua instância no Centro de Administração Power Platform, contacte o suporte e solicite que a disponibilização como piloto seja ativada para os seus ambientes. O seu pedido tem de incluir uma lista de ID do ambiente em que a disponibilização como piloto tem de ser ativada.

### <a name="bug-fixes"></a>Correções de erros

Foram corrigidos os seguintes problemas.

**Tempo e Despesa**
- Falta uma entrada de nota quando uma entrada de tempo é rejeitada ou cancelada. 

**Vendas**

- Quando atualiza o custo ou as estimativas de vendas utilizando plug-ins de instalação inicial, tem incorretamente permissão para enviar cargas úteis JSON que não sejam válidas fora da interface de utilizador.
- Quando atualiza linhas de proposta utilizando a vista rápida, tem permissão para ativar propostas.
