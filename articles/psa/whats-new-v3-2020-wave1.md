---
title: Novidades ou alterações no Project Service Automation versão 3.x, vaga 1 de 2020
description: Este tópico inclui informações sobre o que há de novo e o que foi alterado no Project Service Automation versão 3, vaga 1 de 2020.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 16b51995f863d9ee54172625dacbf081c51c8556
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082350"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Novidades ou alterações no Project Service Automation versão 3, vaga 1 de 2020
O tópico realça as principais considerações de atualização quando migrar para a versão mais recente do Project Service Automation (PSA) versão 3.x, vaga 1 de 2020.

## <a name="time-entry"></a>Entrada de tempo
A experiência de entrada de tempo foi prorrogada para fornecer capacidades para expandir a introdução de tempo a mais cenários de clientes. Isto inclui a capacidade de adicionar tipos de entrada, que agora direcionam o comportamento específico com base no nome do esquema do campo **Definições de entrada de tempo** , apresentado como **Origem da Hora**. Foi adicionada uma nova solução, chamada Tempo, Despesa, Estados e Aprovações (TESA) para suportar esta funcionalidade.

### <a name="upgrade-consideration"></a>Considerações sobre a atualização
Para suportar esta funcionalidade, as funções existentes no PSA foram atualizadas para incluir novos privilégios. Estes privilégios concedem acesso de leitura à nova entidade **Definições de Entrada de Hora**.

Os utilizadores que necessitam da capacidade de registar a hora devem receber a função de utilizador **Utilizador de Entrada de Tempo** , para além das funções existentes. Esta função inclui a nova funcionalidade e assegura que a entrada de tempo continuará a funcionar.

Além disso, se tiver algum módulo de aplicação personalizado que inclua todos os formulários para a entidade de entrada de tempo, será necessário remover o **Formulário de Criação Rápida de Entrada de Tempo TESA** do módulo.

### <a name="currently-extended-time-entry-changes"></a>Alterações a entradas de tempo expandidas atualmente
Para minimizar o impacto sobre os utilizadores atuais da entrada de tempo, esta alteração de função é a única exigência básica necessária para continuar a utilizar a entrada de tempo. Se tiver criado vistas personalizadas ou experiências de entrada de tempo separadas, tem de definir os campos **Definição de Entrada de Tempo** para o valor correto do PSA.