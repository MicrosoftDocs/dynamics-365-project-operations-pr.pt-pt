---
title: Novidades ou alterações na Versão da Atualização 39 do Project Service Automation, V3
description: Este artigo lista as funcionalidades e correções disponíveis na Versão 39 da Atualização do Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/20/2022
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
ms.openlocfilehash: d5b5938762d98acaead9e26c47bce07e0059faf6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922466"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-39-v3"></a>Novidades ou alterações na Versão da Atualização 39 do Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente para a aplicação Microsoft Dynamics 365 Project Service Automation. Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização. É compatível com o Dynamics 365, versão 9.x. Para atualizar para esta versão, visite a página de soluções online do Centro de Administração do Dynamics 365 e instale a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este artigo lista as funcionalidades e correções novas ou alteradas para a Versão 39 da Atualização do Project Service Automation, V3. Esta versão tem um número de compilação de V3.10.60.170 e está geralmente disponível através de uma Atualização automática em janeiro de 2022.

## <a name="update-release-39"></a>Versão da Atualização 39

### <a name="bug-fixes"></a>Correções de erros

Foram corrigidos os seguintes problemas.

**Geral**

- Foram feitos vários melhoramentos ao mapa do site para tradução árabe.

**Gestão de Projetos**

- Ocorre um erro quando altera o gestor do projeto num projeto para um utilizador que já é membro da equipa no projeto.

**Vendas**

- O proprietário da **Lista de preços do contrato do Projeto** está incorreto quando a lista de preços é criada automaticamente. 
- A efetividade da data de uma lista de preços não é honrada quando a lista de preços é aplicada ao parâmetro do projeto.
- A unidade de contratação pode não ter o valor predefinido correto ao editar duas cotações separadas.