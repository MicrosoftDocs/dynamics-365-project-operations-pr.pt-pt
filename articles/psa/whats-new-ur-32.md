---
title: Novidades ou alterações na Versão da Atualização 32 do Project Service Automation, V3
description: Este tópico lista as funcionalidades e correções disponíveis no Project Service Automation V3, Versão da Atualização 32, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 11bf451ef4f24e2301ffde4f86a556a8a4fe30b0
ms.sourcegitcommit: 886102894244887d72e5a6213071e8d8a52c9d48
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129680"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a>Novidades ou alterações na Versão da Atualização 32 do Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente para a aplicação Microsoft Dynamics 365 Project Service Automation. Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização. É compatível com o Dynamics 365, versão 9.x. Para atualizar para esta versão, visite a página de soluções online do Centro de Administração do Dynamics 365 e instale a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este tópico lista as funcionalidades e correções novas ou alteradas para o Project Service Automation V3, Versão da Atualização 32. Esta versão tem um número de compilação V3.10.53.108 e está geralmente disponível através de uma atualização automática em junho de 2021.

## <a name="update-release-32"></a>Versão da Atualização 32

### <a name="bug-fixes"></a>Correções de erros

#### <a name="general"></a>Geral

- Quando uma atualização principal falha, apenas os principais pontos de entrada da aplicação devem ser bloqueados, para garantir que as entidades partilhadas ainda estão acessíveis.

#### <a name="time-and-expense"></a>Tempo e Despesa

Foram corrigidos os seguintes problemas:

- **TimeEntriesImportFromResourceAsignment** não mantém as horas de início e fim do setor de perfil de atribuição de recursos.
- Quando seleciona **Abrir Entrada** na grelha **Entrada de Hora**, poderá ser impedido de selecionar outras formas.
- Enquanto importa atribuições para entradas de tempo, a consulta de código do cliente pode gerar um URL longo que falha a consulta.
- Na grelha **Entrada de Hora**, depois de um valor ser eliminado de uma célula, o foco não permanece na grelha.
- O botão **Rejeitar** foi removido da vista **Processamento de aprovações** para aprovações modernas.
- A estabilidade e o desempenho da aprovação em massa de entradas de tempo são afetados por impasses e por uma falha no processamento adequado de personalizações relacionadas com a entidade **Entrada de Tempo**.

#### <a name="project-planning"></a>Planeamento de Projeto

- Uma exceção de referência nula é gerada quando atualiza um projeto que tem um valor nulo no campo **Unidade de Contratação**.
- **Atualiza Totais do Projeto** calcula incorretamente o custo restante e as vendas restantes num projeto.
- Os cálculos de preços redundantes afetam o desempenho relacionado com atualizações nos perfis de atribuição de recursos.

#### <a name="resource-management"></a>Gestão de Recursos

O seguinte problema foi corrigido:

- Quando a capacidade de calendário de um recurso reservável é superior a 1, o Project Service Automation reconhece incorretamente a capacidade como 0 (zero). Portanto, ocorre um ciclo infinito na vista da agenda.

#### <a name="sales"></a>Vendas

Foram corrigidos os seguintes problemas:

- Quando uma linha do diário é criada com um tipo de transação personalizada, ocorre a seguinte exceção de referência nula: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.
- As funções e categorias que estão inativas antes de uma proposta ser copiada não devem ser adicionadas a funções e categorias faturáveis da proposta recentemente copiada.
- A data do documento e a data da gestão contabilística não estão alinhadas com a data de início que é fornecida no detalhe da linha de uma fatura que é criado diretamente numa fatura de rascunho.
- As exceções de referência nulas são geradas em cenários relacionados com a inativação de funções e categorias antes de uma proposta ser copiada.
- A ação **Atualizar Preços** na página **Projetos** não atualiza as estimativas de despesas e estimativas de materiais.
