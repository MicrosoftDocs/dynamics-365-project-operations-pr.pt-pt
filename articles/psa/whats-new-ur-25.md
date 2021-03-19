---
title: Novidades ou alterações na Versão da Atualização 25 do Project Service Automation, V3
description: Este tópico lista as funcionalidades e correções disponíveis no Project Service Automation V3, Versão da Atualização 25, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: 30822ec64b31e110202a587dd941bdff60116712
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280457"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a>Novidades ou alterações na Versão da Atualização 25 do Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a mais recente atualização à aplicação Project Service Automation para Dynamics 365. Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização. Esta versão é compatível com o Dynamics 365 9.x. Para atualizar esta versão, visite o Centro de Administração para o Dynamics 365 online e aceda à página de soluções para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Este tópico lista as funcionalidades e correções novas ou alteradas para o Project Service Automation V3, Versão de Atualização 25 – esta versão tem um número de compilação V 3.10.43.76 e está geralmente disponível através de uma atualização automática em outubro de 2020.

## <a name="update-release-25"></a>Versão da Atualização 25

### <a name="bug-fixes"></a>Correções de erros

**Tempo e Despesa**

O seguinte problema foi corrigido:

- Gráfico de entrada de tempo que mostra dados adicionais baseados num intervalo demasiado grande a ser obtido.

**Gestão de Recursos**

O seguinte problema foi corrigido:

- Código do Package Deployer adicionado para ignorar a importação do patch do Universal Resource Scheduling se já existir uma versão do patch mais alta.

**Gestão de Projetos**

Foram corrigidos os seguintes problemas:

- Discrepâncias de arredondamento e taxas de câmbio corrigidas, resultando num custo planeado incorreto na grelha de monitorização do projeto.
- Suporte a capacidade de exibir duas ou mais grelhas de reação no formulário **Projeto**.
- Fornecida a validação para resolver a capacidade de atribuir uma tarefa para além da data de fim do calendário, o que resulta numa atribuição falhada de recursos.
- Manuseamento de erros melhorado para resolver Exceção de Referência nula gerada a partir do seguinte:

    - Plug-in **PreValidateProjectTeamMemberCreate**
    - **PreValidateProjectTaskCreate** quando uma tarefa de projeto é criada sem um projeto associado
    - Plug-in **PreProjectTeamMemberCreate**
    - Plug-in **PostProjectTeamMemberDelete**
    - Plug-in **PreValidateProjectTaskDelete**

**Sales**

Foram corrigidos os seguintes problemas:

- Manuseamento de erros melhorado para resolver Exceções de Referência Nulas geradas pelo **Copiar Projeto: Estimativa de Gestão do HelperResource**.
- **Não está pronto a Faturar** num **Registo de Tarefas Pendentes de Faturação de Tempo e Material** não limpa o estado da faturação.
- Corrigida a colocação errada de etiquetas dos botões **Preços** no separador **Preço de Função** e **Itens de Catálogo**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]