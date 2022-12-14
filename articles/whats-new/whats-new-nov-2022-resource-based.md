---
title: Novidades em novembro de 2022 – Project Operations para cenários baseados em Recursos/Não Stock
description: Este artigo fornece informação sobre as atualizações de qualidade que estão disponíveis na versão de novembro de 2022 do Microsoft Dynamics 365 Project Operations para cenários baseados em recursos/sem stock.
author: ryansandness
ms.date: 12/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 509e303aeb0567627590fd89c6888b59a414c6f1
ms.sourcegitcommit: 952fcefe33de192ad48f4108c3adbe658fd7b94f
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831100"
---
# <a name="whats-new-november-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades em novembro de 2022 – Project Operations para cenários baseados em Recursos/Não Stock

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Este artigo aplica-se aos seguintes componentes e versões do Microsoft Dynamics 365 Project Operations:

- Project Operations num ambiente Dataverse, versão 4.58.0.119
- Gestão de projetos e contabilidade num ambiente do Dynamics 365 Finance versão 10.0.30

## <a name="project-operations-dual-write-maps-updates"></a>Atualizações de mapas de escrita dupla do Project Operations

Não existem atualizações para os mapas de escrita dupla do Project Operations nesta versão. Para obter uma lista atual e as versões dos mapas de escrita dupla do Project Operations, consulte [Versões do mapa de escrita dupla do Project Operations](../environment/resource-dual-write-maps.md).

Execute sempre a versão mais recente do mapa no seu ambiente e ative todos os mapas de tabelas relacionados à medida que atualiza a sua solução do Project Operations Dataverse e a versão da solução Finance. Algumas funcionalidades e capacidades podem não funcionar corretamente se a versão mais recente do mapa não estiver ativada. Pode ver a versão ativa do mapa na coluna **Versão** na página **Escrita Dupla**. Para ativar uma nova versão do mapa, selecione **Versões do mapa de tabela** , selecione a versão mais recente e, em seguida, guarde a versão selecionada. Se tiver personalizado um mapa de tabela de origem, volte a aplicar as alterações. Para mais informações, consulte [Gestão do ciclo de vida da aplicação](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se ocorrer um problema quando iniciar o mapa, siga as instruções na secção [Problema de colunas de tabela em falta em mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) do guia de resolução de problemas do serviço Escrita dupla.

## <a name="quality-updates"></a>Atualizações de qualidade

### <a name="project-operations-on-dataverse"></a>Project Operations no Dataverse

| Área de funcionalidades | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Faturação e Preços | 2781818 | A chave não encontrou erros durante a predefinição do preço para o registo de utilização de materiais. |
| Faturação e Preços | 2922373 | Não é possível associar a linha de proposta ao projeto que tenha fechado como proposta perdida. |
| Faturação e Preços | 2943206 | O campo **Item de Contrato** na Entidade do Projeto Deve ser Opcional. |
| Faturação e Preços | 2953182 | Melhorar a mensagem de erro para a correção de faturas.|
| Faturação e Preços | 2959500 | Não é possível associar uma linha de proposta a uma tarefa de projeto que já está associada a uma proposta perdida.|
| Faturação e Preços | 2959560 | Mensagem "Este cliente já está no Contrato do Projeto" recebida durante o encerramento da proposta como ganha em determinadas regiões. |
| Faturação e Preços | 3031727 | As atribuições de recursos falham com o erro Campo "msdyn_Company" obrigatório em falta. |
| Faturação e Preços | 3036905 | A Empresa Proprietária nunca é inicializada no ProjectTeamMember. |
| Gestão de oportunidades | 2763519 | Erro de Referência Nula em EnsureProjectContractAllowsUpdates. |
| Gestão de oportunidades | 2783798 | Quando importa estimativas de projeto na linha de proposta, faltam descrições de tarefas para estimativas de despesas e materiais.|
| Gestão de oportunidades | 2988635 | Melhore a descrição da mensagem de erro ao eliminar Cliente na Proposta. |
| Gestão de oportunidades | 3001191 | Não é possível criar uma proposta a partir de Oportunidade, em que o método de faturação é especificado como nulo. |
| Atualizar | 3012324 | A conversão do projeto falhou num projeto com carateres de controlo, tal como Tab no nome do projeto. || Planeamento e Monitorização de Projetos | 2790384 | O tempo limite do OperationSet Pendente é demasiado curto. |
| Planeamento e Monitorização de Projetos | 3044275 | Localização em falta para: missingProjectSchedulerErrorMessage. |
| Planeamento e Monitorização de Projetos | 3044277 | A grelha de Reconhecimento do Projeto não carrega quando o agendador está por definir.|
| Gestão de Recursos | 2943153 | Atualize o separador Monitorização para mostrar duas casas decimais para Duração.|
| Subcontratos | 2932774 | Fornecedor de Linha de Fatura Só de Leitura a lançar erro incorretamente. |
| Subcontratos | 2939556 | O estado do Cabeçalho da Fatura do Fornecedor não deve estar definido como Rascunho na eliminação de linha se não estiver ativo. |
| Tempo e Despesa | 2939998 | Adoção da nova versão da TESA no ProjOps. |


### <a name="project-management-and-accounting-in-finance"></a>Gestão de projetos e contabilística em Finanças

Para obter informações sobre as correções de erros incluídas nesta atualização, inicie sessão no Microsoft Dynamics Lifecycle Services e consulte o [Artigo BDC](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
