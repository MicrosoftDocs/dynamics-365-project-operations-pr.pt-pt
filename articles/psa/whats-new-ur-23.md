---
title: Novidades ou alterações na Versão da Atualização 23 do Project Service Automation, V3
description: Este tópico lista as funcionalidades e correções disponíveis no Project Service Automation V3, Versão da Atualização 23, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: ec27d2344f14e61a50be2771ee3d7952f16abd736927de7c3c5a019351a3e067
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996630"
---
# <a name="project-service-automation-update-release-23-v3"></a>Versão da Atualização 23 do Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a mais recente atualização à aplicação Project Service Automation para Dynamics 365. Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização. Esta versão é compatível com o Dynamics 365 9.x. Para atualizar esta versão, visite o Centro de Administração para o Dynamics 365 online e aceda à página de soluções para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este tópico lista as funcionalidades e correções novas ou alteradas para o Project Service Automation V3, Versão da Atualização 23. Esta versão tem um número de compilação de V 3.10.34.30 e está geralmente disponível através de uma Atualização automática em agosto de 2020.

## <a name="update-release-23"></a>Versão da Atualização 23

### <a name="bug-fixes"></a>Correções de erros

**Tempo e Despesa**

Foram corrigidos os seguintes problemas:
- Lidar com o caso da borda em **Eliminação de Membro da Equipa de Projeto** para fornecer uma exceção significativa.
- A importação de atribuição resulta num ecrã de remoção em branco.

**Gestão de Recursos**

Foram corrigidos os seguintes problemas:

- O **Cartão de recursos da grelha de utilização de recursos** mostra dados incorretos quando a escala de tempo é superior a cinco dias.
- Quando os clientes criam um recurso reservado, o plug-in falha intermitentemente ao adicionar automaticamente o recurso a um grupo do Microsoft Office 365.
- A vista **Reconciliação** apresenta contornos manuais incorretamente na vista **Semana** ou **Mês**.

**Gestão de Projetos**

Foram corrigidos os seguintes problemas:

- Um número excessivo de entidades **RetrieveMultiple para usersettings** está a causar um desempenho degradado para aprovações de projetos e outras operações.
- A pesquisa de recursos da grelha **Planeamento de Tarefas** está limitada a apenas cinco membros da equipa do projeto. 
- A pesquisa de recursos da grelha **Planeamento de Tarefas** não filtra recursos inativos.
- O modo manual não está a funcionar como esperado na estrutura hierárquica do trabalho de planeamento do projeto.
- A grelha **Planeamento de Tarefas** mostra **Categorias de Transação Inativas**.
- A grelha **Atribuição de Recursos** arredonda incorretamente quando uma tarefa tem várias atribuições.
- Os valores de arredondamento são diferentes entre o custo planeado e o custo real para uma única tarefa.

**Sales**

Foram corrigidos os seguintes problemas:

- Clicar duas vezes em **Obter Todas as Categorias de Transações** cria várias linhas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]