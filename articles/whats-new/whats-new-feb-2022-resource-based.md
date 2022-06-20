---
title: Novidades em fevereiro de 2022 – Project Operations para cenários baseados em Recursos/Não Armazenados
description: Este artigo fornece informações sobre as atualizações de qualidade disponíveis na versão de fevereiro de 2022 do Project Operations para cenários baseados em recursos/itens não existentes em stock.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b036c0a3c39c52cb15277293679ef88906cae2c4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933000"
---
# <a name="whats-new-february-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades em fevereiro de 2022 – Project Operations para cenários baseados em Recursos/Não Armazenados

*Aplica-se A: Project Operations para cenários baseados em recursos/não armazenados*

Este artigo aplica-se aos seguintes componentes e versões do Microsoft Dynamics 365 Project Operations:

- Project Operations num ambiente Dataverse, versão 4.28.0.120
- Gestão de projetos e contabilidade num ambiente do Dynamics 365 Finance versão 10.0.24

## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versão

- A partir desta versão, pode adicionar até 300 membros de equipa a um único projeto. Anteriormente, o limite para o número de membros de equipa era 150. Para obter mais informações, consulte [Limites do projeto](../project-management/create-wbs.md#project-limitations).

## <a name="project-operations-dual-write-map-updates"></a>Atualizações ao mapa de escrita dupla do Project Operations

A lista seguinte mostra os mapas de escrita dupla que foram modificados ou adicionados na versão de fevereiro de 2022 do Project Operations.

| Mapa da entidade | Versão atualizada | Comentários |
| --- | --- | --- |
| Entidade de exportação de despesas do projeto de integração com o Project Operations (msdyn\_expenses) | 1.0.0.3 | Expandido para a sincronização de atividades de projeto com o Dataverse. |

Para ver a lista e versões atuais de mapas de escrita dupla no Project Operations, consulte [versões de mapa de escrita dupla no Project Operations](../environment/resource-dual-write-maps.md).

Execute sempre a versão mais recente do mapa no seu ambiente e ative todos os mapas de tabelas relacionados à medida que atualiza a sua solução do Project Operations Dataverse e a versão da solução Finance. Algumas funcionalidades e capacidades podem não funcionar corretamente se a versão mais recente do mapa não estiver ativada. Pode ver a versão ativa do mapa na coluna **Versão** na página **Escrita Dupla**. Para ativar uma nova versão do mapa, selecione **Versões do mapa de tabela** , selecione a versão mais recente e, em seguida, guarde a versão selecionada. Se tiver personalizado um mapa de tabela de origem, volte a aplicar as alterações. Para mais informações, consulte [Gestão do ciclo de vida da aplicação](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se ocorrer um problema quando iniciar o mapa, siga as instruções na secção [Problema de colunas de tabela em falta nos mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) do guia de resolução de problemas do serviço Escrita dupla.

## <a name="quality-updates"></a>Atualizações de qualidade

### <a name="project-operations-on-dataverse"></a>Project Operations no Dataverse

| Área de funcionalidades | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Faturação e preços | 2415109 | O valor predefinição no campo **Termos de pagamento das operações** tem de ser o registo do cliente do contrato do projeto e o registo da fatura pro-forma. |
| Faturação e preços | 2497369 | A correção de material tem de seguir o valor da data nos parâmetros **Correção**. |
| Faturação e preços | 2498697 | Melhorou a configuração de segurança para a **Revocação de entrada de tempo**. |
| Faturação e preços | 2513824 | Para cenários baseados em recursos, o ID de categoria de transação não pode exceder os 28 caracteres no Project Operations. |
| Faturação e preços | 2517455 | A ação **Atualizar transações de linha da fatura** não deve ter permissão para ser acionada várias vezes em simultâneo para a mesma fatura. |
| Faturação e preços | 2517465 | A ação **Desativar detalhes da linha de fatura** está bloqueada porque não é suportada. |
| Faturação e preços | 2556660 | Corrigida a verificação de efetividade da data que está feita na lista de preços anexada a um registo de parâmetros do projeto. |
| Gestão de oportunidades | 2369202 | Corrigida a lógica de negócio que verifica que as listas de preços que têm datas de efetividade sobrepostas podem ser anexadas ao mesmo contrato do projeto. |
| Gestão de oportunidades | 2385965 | Corrigido o comportamento no separador **Clientes** da página **Contrato do projeto** quando seleciona **Guardar e fechar**. |
| Tempo e despesa | 2538503 | Uma tarefa de projeto tem de estar disponível na entidade **Valores reais do projeto** depois de um relatório de despesas ser publicado. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Gestão de projetos e contabilidade no Dynamics 365 Finance

| Área de funcionalidades | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Gestão de projetos e contabilística | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | Durante a importação de notas de crédito do fornecedor, ocorre um erro. A mensagem de erro declara: "O montante a reter não pode ser mais do que o montante líquido restante". |
| Gestão de projetos e contabilística | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | Se uma proposta de fatura incluir quaisquer transações de taxa de montante zero que sejam valores reais de vendas não faturadas, não é possível faturar. |
| Gestão de projetos e contabilística | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | O custo publicado não é correto após a atualização do preço de compra e **Ativar gestão de alterações** ser ativada.|
| Gestão de projetos e contabilística | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | A estimativa de publicação para um projeto de preços fixos utiliza a moeda e o montante incorreto no voucher de estimativa, mesmo quando a funcionalidade **Ativar moeda de contrato do projeto para cálculo da estimativa** estar ativa. |
| Gestão de projetos e contabilística | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | O **ProjDMFDataPoation\_Extension** não deve fazer uma chamada para permitir a monitorização de alterações sem abrir exceções para entidades que tenham chaves de configuração que não estão ativadas. |
| Gestão de projetos e contabilística | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | A tarefa em lote é fixa quando são publicados vários diários avançados e ocorre um erro. |
| Viagem e Despesa | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | Devido a um problema de liquidação que está relacionado com os relatórios de despesas, o montante do imposto não é incluído como parte do adiantamento. |
| Viagem e Despesa | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | As informações sobre o imposto de vendas não estão incluídas no relatório **Despesas - Transações Publicadas**. |
| Viagem e Despesa | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | A violação da política de despesas **Recibos necessários** mostra incorretamente um aviso sobre os relatórios de despesas. |
| Viagem e Despesa | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | Uma transação do projeto não inclui o imposto de vendas não-recuperável no montante total das vendas quando a transação é resultado de uma despesa de quilometragem. |
| Viagem e Despesa | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | Quando uma linha que é colocada em item tem imposto, não pode alterar a data de colocação em item e ocorre um erro de estado do documento de origem. |

## <a name="removed-and-deprecated-features"></a>Funcionalidades removidas e preteridas

O artigo [Funcionalidades removidas ou preteridas no Project Operations](removed-depreciated-features-project.md) descreve as funcionalidades que foram removidas ou preteridas para o Dynamics 365 Project Operations.

- Uma funcionalidade removida já não está disponível no produto.
- Uma funcionalidade preterida não está no desenvolvimento ativo e poderá ser removida numa atualização futura.

Um anúncio de preterido irá aparecer no artigo [Funcionalidades removidas ou preteridas no Project Operations](removed-depreciated-features-project.md) 12 meses antes de qualquer funcionalidade ser removida do produto.

Para alterações de última hora que afetem apenas o tempo de compilação, mas que sejam binários compatíveis com sandbox e ambientes de produção, o tempo de depreciação será inferior a 12 meses. Normalmente, estas alterações são atualizações funcionais que têm de ser feitas ao compilador.
