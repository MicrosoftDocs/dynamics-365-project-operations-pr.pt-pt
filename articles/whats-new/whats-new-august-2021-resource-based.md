---
title: Novidades de agosto de 2021 - Project Operations para cenários baseados em recursos/não armazenados
description: Este tópico fornece informações sobre as atualizações de qualidade disponíveis na versão de agosto de 2021 do Project Operations para cenários baseados em recursos/não armazenados.
author: sigitac
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 26861472d3af20c58b3d01142b834d535cf99715
ms.sourcegitcommit: 083e3d219cd5126eecb74debb1b70b361680b1f6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/18/2021
ms.locfileid: "7501385"
---
# <a name="whats-new-august-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades de agosto de 2021 - Project Operations para cenários baseados em recursos/não armazenados

*Aplica-se A: Project Operations para cenários baseados em recursos/não armazenados*

Este tópico aplica-se aos seguintes componentes e versões do Dynamics 365 Project Operations:

   - Project Operations na versão de ambiente 4.13.0.152 do Microsoft Dataverse.
   - Gestão de projetos e contabilística na versão 10.0.20 do ambiente Dynamics 365 Finance.

## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versão

Estão incluídas nesta versão as seguintes funcionalidades:

- **Conjuntos de aprovações**: Os conjuntos de aprovações agrupam os pedidos de aprovação de utilização de tempo, despesa ou material em subconjuntos menores de operações. Este agrupamento permite que as aprovações sejam processadas por projeto, numa ordem específica, e permite repetições e sequenciações. O agrupamento de pedidos melhora a fiabilidade e a rastreabilidade do processamento de aprovações no caso de grandes volumes de aprovações. Para mais informações, consulte [Conjuntos de aprovações](../approvals/approval-sets.md).

## <a name="project-operations-dual-write-maps-updates"></a>Atualizações de mapas de escrita dupla do Project Operations

Não existem atualizações para os mapas de escrita dupla do Project Operations nesta versão.

Para obter uma lista atual e as versões dos mapas de escrita dupla do Project Operations, consulte [Versões do mapa de escrita dupla do Project Operations](../environment/resource-dual-write-maps.md).

Execute sempre a versão mais recente do mapa no seu ambiente e ative todos os mapas de tabelas relacionados à medida que atualiza a sua solução do Project Operations Dataverse e a versão da solução Finance. Certas funcionalidades e capacidades podem não funcionar corretamente se a versão mais recente do mapa não estiver ativada. Pode ver a versão ativa do mapa na página **Escrita dupla** na coluna **Versão**. Ative uma nova versão do mapa ao selecionar **Versões do mapa de tabelas**, selecionar a versão mais recente e, em seguida, guardar a versão selecionada. Se tiver personalizado um mapa de tabela fora da caixa, reaplique as alterações. Para mais informações, consulte [Gestão do ciclo de vida da aplicação](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se encontrar um problema ao iniciar o mapa, siga as instruções na secção [Problema de colunas de tabela em falta nos mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) no guia de resolução de problemas de escrita dupla.

## <a name="quality-updates"></a>Atualizações de qualidade

### <a name="project-operations-on-dataverse"></a>Project Operations no Dataverse

| **Área de funcionalidades** | **Número de referência** | **Atualização de qualidade** |
| --- | --- | --- |
| Faturação e preços | 2295625 | O nome do marco deve ser copiado da agenda de faturação para o detalhe da linha de fatura. |
| Faturação e preços | 2316323 | O desconto não deve ser editável numa fatura pró-forma no Project Operations para cenários baseados em recursos. |
| Gestão de oportunidades | 2338619 | As regras de negócio **Oportunidade** e **Proposta** só devem ser invocadas nas páginas. |
| Gestão de recursos | 2316523 | A utilização de **Enviar Pedido** a partir de um requisito de recurso que tem uma função anexada não deve apresentar um erro. |
| Gestão de recursos | 2326885 | A criação de um requisito de recurso através de um projeto não deve apresentar um erro. |
| Tempo e despesa | 2335584 | Fluxos de tarefas preteridos na entrada de hora. |
| Tempo e despesa | 2336884 | O botão de entrada de hora **Copiar Semana** deve funcionar para algo mais do que apenas o utilizador atual. |


### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Gestão de projetos e contabilística no Dynamics 365 Finance

| Área de funcionalidades | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Viagem e despesa | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Os montantes incorretos de transações de fornecedores e de transações de impostos sobre vendas são registados quando uma despesa é criada a partir de uma transação com cartão de crédito. |
| Viagem e despesa | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | A liquidação incorreta são as linhas criadas quando o diário de pagamentos é gerado. |
| Viagem e despesa | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Os montantes incorretos de transações de impostos sobre vendas são registados quando uma despesa é criada a partir de uma transação com cartão de crédito. |
| Viagem e despesa | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | A eliminação de uma linha de despesa pode demorar muito tempo. |
| Gestão contabilística do projeto | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | O sistema não suporta a configuração de sequenciação contínua de números quando regista uma estimativa depois de aplicar o 4619395 da BDC. |
| Gestão contabilística do projeto | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | O registo da fatura do fornecedor pode falhar com a mensagem de erro: "As transações no voucher não apresentam saldo em 17/05/2021. (moeda contabilística: 0,00 - moeda de relatório: 0,01)" |
