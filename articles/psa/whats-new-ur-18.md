---
title: Novidades ou alterações na Versão da Atualização 18 do Project Service Automation, V3
description: Este tópico lista as funcionalidades e correções disponíveis no Project Service Automation V3, Versão da Atualização 18, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: 1d7ea200531dd24d56a829f879e3a2532a9b38dc
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082358"
---
# <a name="project-service-automation-update-release-18-v3"></a>Versão da Atualização 18 do Project Service Automation, V3

Temos o prazer de anunciar a mais recente atualização à aplicação Project Service Automation para Dynamics 365. Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização. Esta versão é compatível com o Dynamics 365 9.x. Para atualizar esta versão, visite o Centro de Administração para o Dynamics 365 online e aceda à página de soluções para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Este tópico lista as funcionalidades e correções novas ou alteradas para o Project Service Automation V3, Versão da Atualização 18. Esta versão tem o número de compilação V3.10.8.12 e está geralmente disponível através de uma atualização automática em abril de 2020.

## <a name="update-release-18"></a>Versão da Atualização 18

### <a name="bug-fixes"></a>Correções de erros

**Tempo e Despesa**

- Corrigido: os fluxos **Revocar** , **Pedir** e **Cancelar Aprovação** lançam exceções com mensagens de erro ambíguas.
- Corrigido: quando **Cancelar Aprovação** falha para uma despesa, um erro de exceção relevante não é lançado.
- Corrigido: a grelha Entrada de Hora processa incorretamente dias não úteis na Austrália após a mudança para a hora de verão (DST) em outubro.
- Corrigido: a lógica de definição incorreta impede o envio de despesas.
- Corrigido: quando a aprovação da entrada de hora falha, a aprovação permanece num estado de **Pendente**.
- Corrigido: erros SQL em aprovações em massa (impasse/tempo limite).
- Corrigido: problemas de desempenho significativos na experiência do utilizador causados pela atualização de membros da equipa durante a aprovação das entradas de hora.

**Gestão de Projetos**

- Corrigido: a notificação de fuso horário moveu-se da vista **Reconciliação** para o formulário principal **Projeto**.
- Corrigido: o modelo de calendário não é predefinido corretamente quando é aberto um novo formulário de projeto.
- Corrigido: para browsers baseados em chromium, os utilizadores não conseguem selecionar facilmente as tarefas predecessoras a eliminar.
- Corrigido: a criação ou copia do **Projeto a partir de Modelo Vazio** obtém atribuições não relacionadas.
- Corrigido: em casos específicos do Edge, a criação de uma nova atribuição a partir da grelha de tarefas resulta na criação de registos duplicados.
- Corrigido: no modo manual, os utilizadores não conseguem atualizar as datas de início das tarefas para serem posteriores à data atual guardada.

**Gestão de Recursos**

- Corrigido: a linha de subtotal da vista de **Reconciliação** calcula incorretamente a variância das reservas após a extensão de reservas.
- Corrigido: a vista de **Reconciliação** apresenta incorretamente as atribuições de recursos quando o recurso que é agendado tem um calendário que não corresponde ao calendário do projeto.

**Sales**

- Corrigido: quando as entradas de hora são reaprovadas ( **Aprovar > Cancelar >** são aprovadas novamente), é criado um valor real não cobrável duplicado.