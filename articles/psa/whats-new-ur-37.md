---
title: Novidades ou alterações na Versão da Atualização 37 do Project Service Automation, V3
description: Este tópico lista as funcionalidades e correções que estão disponíveis na Versão de Atualização 37 do Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 11/01/2021
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
ms.openlocfilehash: e8696d84aaca019c2e12d852e669df71146484b3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593488"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-37-v3"></a>Novidades ou alterações na Versão da Atualização 37 do Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente para a aplicação Microsoft Dynamics 365 Project Service Automation. Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização. É compatível com o Dynamics 365, versão 9.x. Para atualizar para esta versão, visite a página de soluções online do Centro de Administração do Dynamics 365 e instale a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este tópico lista as funcionalidades e correções novas ou alteradas para o Project Service Automation V3, Versão da Atualização 37, V3. Esta versão tem um número de compilação de V3.10.58.120 e está em disponibilidade geral através de uma atualização automática em novembro de 2021.

## <a name="update-release-37"></a>Versão da Atualização 37

### <a name="bug-fixes"></a>Correções de erros

Foram corrigidos os seguintes problemas.

**Tempo e Despesa**
- Os utilizadores não conseguem eliminar uma entrada de tempo ao limpar a célula.
- A vista **A minha aprovação com falhas** contém apenas as aprovações de projetos com o estado de **Submetido**.

**Gestão de projetos**
- Os utilizadores recebem um erro de exceção de referência nulo ao abrir um projeto no suplemento de ambiente de trabalho da Microsoft se o nome do cargo do membro da equipa do Projeto estiver vazio.
- Não existe um botão **Guardar** na página **Tarefa de Projeto**, pelo que os utilizadores não podem guardar as alterações aos registos de tarefas.
- Os utilizadores não podem eliminar um projeto com uma tarefa associada a uma proposta com o estado **Ganha**.

**Vendas**
- O campo **Moeda** na página **Projeto** é atualizado para corresponder à moeda do modelo aplicado.
- O custo é calculado incorretamente em tarefas com várias moedas.
