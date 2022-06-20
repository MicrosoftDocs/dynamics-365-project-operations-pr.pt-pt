---
title: Novidades ou alterações na Versão da Atualização 12 do Project Service Automation, V3
description: Este artigo inclui informações sobre o que há de novo na Versão 12 da Atualização do Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: 28539b2e1331c8509e40aaf771f4d88d6f54e022
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922650"
---
# <a name="project-service-automation-update-release-12-v3"></a>Versão da Atualização 12 do Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente para a aplicação Dynamics 365 Project Service Automation (PSA). Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização. Esta versão é compatível com o Dynamics 365 9.x. Para atualizar esta versão, visite o Centro de Administração para o Dynamics 365 online e aceda à página de soluções para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este artigo lista as funcionalidades e correções novas ou alteradas para a Versão 12 da Atualização do Project Service Automation V3. Esta versão tem um número de compilação de V3.10.2.34 e está geralmente disponível através de uma Atualização automática em outubro de 2019.

## <a name="update-release-12"></a>Versão da Atualização 12

### <a name="bug-fixes"></a>Correções de erros

- Tempo e Despesa

    - Corrigido: a mensagem de erro de entrada de tempo foi atualizada com um contexto mais relevante.
    - Corrigido: a grelha de hora de entrada e a agenda apresentam corretamente a barra de deslocamento vertical quando necessário.
    - Corrigido: entradas de despesas e de hora submetidas podem ser aprovadas.
    - Corrigido: a mensagem de diálogo Cancelar confirmação de aprovação foi corrigida para refletir o estado da aprovação quando alterado de **Aprovada** para **Submetida**.
    - Corrigido: os campos **Preço**, **Unidade** e **Quantidade** agora estão bloqueados no registo Despesas depois de terem sido aprovados.

- Gestão de Projetos

    - Corrigido: a ação **Nova** no formulário principal **Membro da equipa** foi removida.
    - Corrigido: as atribuições de recursos foram atualizadas para considerar erros de arredondamento imprecisos, que resultavam em mudanças na data de fim de uma tarefa.
    - Corrigido: na grelha de tarefas, os erros relevantes do lado do servidor serão apresentados ao utilizador.
    - Corrigido: o nome do membro da equipa agora é composto no seletor de pessoas da tarefa em vez de no nome da posição.

- Gestão de Recursos

    - Corrigido: os detalhes do requisito de recurso para projetos criados a partir de um modelo agora utilizam o calendário do projeto.
    - Corrigido: as qualificações e competências agora são predefinidas a partir dos dados principais de função para o requisito de recurso criado para essa função.

- Sales

    - Corrigido: IDs de objetos duplicados no formulário **Principal do contrato**.
    - Corrigido: a lógica foi atualizada para tornar visível o separador **Análise de Proposta**, de modo a apresentar a configuração de metadados do separador.
    - Corrigido: a data contabilística do registo real agora provém da data da hora da entrada da hora/despesa e não da data de aprovação.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
