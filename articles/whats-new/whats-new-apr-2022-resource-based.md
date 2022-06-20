---
title: Novidades de abril de 2022 - Project Operations para cenários baseados em recursos/não armazenados
description: Este artigo fornece informação sobre as atualizações de qualidade que estão disponíveis na versão de abril de 2022 do Microsoft Dynamics 365 Project Operations para cenários baseados em recursos/sem stock.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5ea1c96d64309990962f431b1c72ae47bf445bfa
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912392"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades de abril de 2022 - Project Operations para cenários baseados em recursos/não armazenados

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Este artigo aplica-se aos seguintes componentes e versões do Microsoft Dynamics 365 Project Operations:

- Project Operations num ambiente Dataverse, versão 4.41.0.45
- Gestão de projetos e contabilidade num ambiente do Dynamics 365 Finance versão 10.0.26

## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versão

As categorias de aquisição podem ser usadas em encomendas de compra de projeto e faturas de fornecedor pendentes. Para mais informações, consulte [Utilizar categorias de aquisição com encomendas de compra de projeto e faturas de fornecedor pendentes](configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>Atualizações de mapas de escrita dupla do Project Operations

A tabela seguinte mostra os mapas de escrita dupla que foram modificados ou adicionados na versão de março de 2022 do Project Operations.

| Mapa da entidade | Versão atualizada | Comentários |
| -------------- | ------------------- | ------------|
| Entidade de exportação de linhas de faturas de fornecedor do projeto de integração do Project Operations msdyn\_projectvendorinvoicelines | 1.0.0.4 | Este mapa suporta a utilização de categorias de aquisição com encomendas de compra e faturas de fornecedor pendentes. |

Execute sempre a versão mais recente do mapa no seu ambiente e ative todos os mapas de tabelas relacionados à medida que atualiza a sua solução do Project Operations Dataverse e a versão da solução Finance. Algumas funcionalidades e capacidades podem não funcionar corretamente se a versão mais recente do mapa não estiver ativada. Pode ver a versão ativa do mapa na coluna **Versão** na página **Escrita Dupla**. Para ativar uma nova versão do mapa, selecione **Versões do mapa de tabela** , selecione a versão mais recente e, em seguida, guarde a versão selecionada. Se tiver personalizado um mapa de tabela de origem, volte a aplicar as alterações. Para mais informações, consulte [Gestão do ciclo de vida da aplicação](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se ocorrer um problema quando iniciar o mapa, siga as instruções na secção [Problema de colunas de tabela em falta em mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) do guia de resolução de problemas do serviço Escrita dupla.

## <a name="quality-updates"></a>Atualizações de qualidade

### <a name="project-operations-on-dataverse"></a>Project Operations no Dataverse

| Área de funcionalidades | Número de referência | Atualização de qualidade |
| ------------ | ---------------- | -------------- |
| Tempo e despesa | 2573900 | A funcionalidade **Aprovação Moderna** tem de estar ativada por predefinição. |
| Faturação e preços | 2603313 | Corrigiu um erro de registo duplicado que impedia que a cotação e os itens de contrato com um produto fossem adicionados. |
| Implementação e configuração | 2611368 | Os clientes têm de conseguir adicionar até cinco entidades personalizadas à solução utilizando o estruturador de aplicações moderno. |
| Tempo e despesa | 2628285 | Corrigido um problema que afetava a capacidade de definir a categoria de recurso correta durante a importação de entrada de tempo. |
| Gestão de oportunidades| 2628815 | Atualize o limite de caracteres da descrição detalhada da linha de proposta para corresponder ao limite de caracteres do assunto da tarefa, para que a importação tenha êxito para tarefas em que o assunto tenha mais de 100 caracteres. |
| Tempo e despesa| 2629547 | O campo **Submetido por** das aprovações do projeto tem de apontar para o utilizador que submeteu o registo. |
| Tempo e despesa| 2629865 | O campo **Copiar categoria** em tarefas quando os projetos são copiados. |
| Tempo e despesa| 2636463 | Corrigido os filtros nas aprovações em formulários de aprovação moderna. |
| Planeamento e monitorização de projetos | 2648300 | Corrigido um problema que impede que o proprietário do projeto seja alterado. |
| Faturação e preços | 2563000 | Linhas do diário para uma venda não faturada em que a moeda seja diferente da moeda de contrato não deve ser permitida. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Gestão de projetos e contabilidade no Dynamics 365 Finance

Para obter informações sobre as correções de erros incluídas nesta atualização, inicie sessão no Microsoft Dynamics Lifecycle Services (LCS) e consulte o [Artigo BDC](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
