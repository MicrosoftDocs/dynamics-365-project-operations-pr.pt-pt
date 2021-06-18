---
title: Novidades ou alterações na Versão da Atualização 30 do Project Service Automation, V3
description: Este tópico lista as funcionalidades e correções disponíveis no Project Service Automation V3, Versão da Atualização 30, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 3b6b7dba9c2a22587d27006b9972c950fbb454f2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010440"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a>Novidades ou alterações na Versão da Atualização 30 do Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a mais recente atualização à aplicação Project Service Automation para Dynamics 365. Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização. Esta versão é compatível com o Dynamics 365 9.x. Para atualizar esta versão, visite o Centro de Administração para o Dynamics 365 online e aceda à página de soluções para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution.md).

Este tópico lista as funcionalidades e correções novas ou alteradas para o Project Service Automation V3, Versão da Atualização 30. Esta versão tem o número de compilação V3.10.51.61 e está geralmente disponível através de uma atualização automática em abril de 2021.

## <a name="update-release-30"></a>Versão da Atualização 30

### <a name="bug-fixes"></a>Correções de erros

**Tempo e Despesa**

Foram corrigidos os seguintes problemas:

- Ocorre um erro quando cria e guarda uma entrada de tempo na página **Criação rápida** se o campo **Função** for removido.
- O filtro Entrada de Tempo aplica o operador de filtro errado.
- As folhas de tempo copiadas não são exibidas automaticamente quando seleciona **Copiar semana** no controlo de entrada de tempo.

**Gestão de Recursos**

Foram corrigidos os seguintes problemas:

- Quando prolonga uma reserva, o estado de reserva atribuído à reserva dura está incorreto. O alargamento de uma reserva respeita o estado de reserva definido como **Comprometido** nos metadados de configuração de reserva.
- Quando um estado de reserva válido não é especificado, a mensagem de erro não é corretamente localizada.

**Gestão de Projetos**

Foram corrigidos os seguintes problemas:

- Os projetos não podem ser criados numa moeda e incluem tarefas relacionadas noutra moeda.

**Vendas**

Foram corrigidos os seguintes problemas:

- Quando uma lista de preços é copiada, os preços não são atualizados.
- Fechar uma proposta como ganha falha quando o detalhe de custos tem um valor de origem.
- Na entidade de **Tarefa do projeto**, **Custo estimado** foi renomeado para **Custo Planeado (Base)**.
- Uma exceção de referência nula é gerada quando as faturas são criadas ou eliminadas.
