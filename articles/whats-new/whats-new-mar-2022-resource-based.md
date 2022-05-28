---
title: Novidades em março de 2022 – Project Operations para cenários baseados em Recursos/Não Armazenados
description: Este tópico fornece informações sobre as atualizações de qualidade disponíveis na versão de março de 2022 do Project Operations para cenários baseados em recursos/sem stock.
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: afd5149cda909b5367e7f12382423179d7e19267
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600756"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades em março de 2022 – Project Operations para cenários baseados em Recursos/Não Armazenados

*Aplica-se A: Project Operations para cenários baseados em recursos/não armazenados*

Este tópico aplica-se aos seguintes componentes e versões do Microsoft Dynamics 365 Project Operations:

- Project Operations num ambiente Dataverse, versão 4.30.0.99
- Gestão de projetos e contabilidade num ambiente do Dynamics 365 Finance versão 10.0.25

## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versão

Agora, os per diem são suportados na nova e reinventada área de trabalho de despesas moderna. As empresas que utilizam per diems podem ativar esta funcionalidade para permitir que os utilizadores submetam e sejam reembolsados pelas suas despesas per diem de forma fácil. Para obter mais informações, consulte [Despesas per diem](../expense/per-diem-expenses.md).

## <a name="project-operations-dual-write-maps-updates"></a>Atualizações de mapas de escrita dupla do Project Operations

A lista seguinte mostra os mapas de escrita dupla que foram modificados ou adicionados na versão de março de 2022 do Project Operations.

| **Mapa da entidade** | **Versão atualizada** | **Comentários** |
| --- | --- | --- |
| Entidade de exportação de linhas de faturas de fornecedor do projeto de integração do Project Operations msdyn\_projectvendorinvoicelines | 1.0.0.3 | Mapeamentos atualizados para se alinharem com a entidade de linha de fatura do fornecedor no Dataverse. <br>Não ative a versão de mapeamento 1.0.0.4. Estará pronta a utilizar em conjunto com o ambiente de Finanças versão 10.0.26 na próxima atualização mensal. |

Execute sempre a versão mais recente do mapa no seu ambiente e ative todos os mapas de tabelas relacionados à medida que atualiza a sua solução do Project Operations Dataverse e a versão da solução Finance. Algumas funcionalidades e capacidades podem não funcionar corretamente se a versão mais recente do mapa não estiver ativada. Pode ver a versão ativa do mapa na coluna **Versão** na página **Escrita Dupla**. Para ativar uma nova versão do mapa, selecione **Versões do mapa de tabela** , selecione a versão mais recente e, em seguida, guarde a versão selecionada. Se tiver personalizado um mapa de tabela de origem, volte a aplicar as alterações. Para mais informações, consulte [Gestão do ciclo de vida da aplicação](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se ocorrer um problema quando iniciar o mapa, siga as instruções na secção [Problema de colunas de tabela em falta em mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) do guia de resolução de problemas do serviço Escrita dupla.

## <a name="quality-updates"></a>Atualizações de qualidade

### <a name="project-operations-on-dataverse"></a>Project Operations no Dataverse

| Área de funcionalidades | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Tempo e despesa | 2388011 | Mostrar comentários de rejeição a apresentadores de entrada de tempo durante a aprovação em massa. |
| Planeamento e monitorização de projetos | 2495294 | Os detalhes do projeto não podem ser editáveis na página **Detalhes da tarefa**. |
| Faturação e preços | 2499605 | Os marcos do contrato criados a partir dos marcos das cotações estão incorretamente marcados como só de leitura. |
| Planeamento e monitorização de projetos | 2506050 | O conjunto de operações permanece pendente durante uma hora, caso não haja alterações para guardar. Em seguida, o conjunto será erradamente marcado como **Com falhas**, pelo que deverá ser concluído imediatamente. |
| Faturação e preços | 2507401 | As unidades de contratação predefinida estão incorretamente inseridas em projetos devido à colocação incorreta em cache. |
| Faturação e preços | 2541660 | **Validação de criação de encomendas de venda** em dupla escrita deve ser apenas para encomendas baseadas em projetos. |
| Faturação e preços | 2552745 | O imposto não está dividido entre clientes que tenham configurado regras de faturação divididas. |
| Faturação e preços | 2558859 | Mensagens de erro melhoradas quando as dimensões de preços estão configuradas. |
| Faturação e preços | 2558933 | **Importar de estimativas do projeto** falha quando **msdyn\_project** é adicionado como uma dimensão de preços. |
| Faturação e preços | 2559101 | A eliminação de parâmetros do projeto não está bloqueada e causa problemas. |
| Gestão de oportunidades | 2570390 | O plug-in de escrita dupla força o tipo de conta a ser **Cliente** em cotações, encomendas e oportunidades, mesmo quando esse tipo de conta não está correto. |
| Faturação e preços | 2586097 | Os valores reais de custo dividido faturado não são revertidos quando um projeto é removido de um item de contrato do projeto. |
| Faturação e preços | 2589619 | O imposto sobre material de escrita é propagado para valores reais de vendas não faturadas e para a fatura. |
| Gestão de oportunidades | 2594015 | Não é possível fechar uma cotação se tiver sido ganha para clientes que tenham termos de pagamento **Net60**. |
| Planeamento e monitorização de projetos | 2595841 | No Project for the Web, os utilizadores recebem uma mensagem de erro sobre um **msdyn\_actual** em falta quando criam um novo pedido de recurso. |
| Tempo e Despesa | 2602511 | O campo **Rejeitado por** para entradas de tempo mostra o **Sistema** vez de um utilizador nomeado como o tendo rejeitado. |
| Tempo e Despesa | 2602528 | Um aprovador de projetos pode aprovar tempo em projetos nos quais não se encontra listado como aprovador. |
| Faturação e preços | 2608550 | É possível confirmar uma fatura de correção mesmo que não haja alterações à original. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Gestão de projetos e contabilidade no Dynamics 365 Finance

| Área de funcionalidades | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Gestão de projetos e contabilística | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | Existe uma incompatibilidade entre as Finanças e o Project Operations no comprimento permitido do campo **ID de categoria**. |
| Gestão de projetos e contabilística | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | Não é possível eliminar projetos de preço fixo quando o campo **Faturação em conta** está definido para **Lucro e prejuízo** e é utilizado o princípio **Percentagem concluída**. |
| Gestão de projetos e contabilística | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | É inserido um grupo de impostos de vendas predefinido incorreto a partir da configuração do projeto nas linhas de despesas no diário de integração do Project Operations. |
| Gestão de projetos e contabilística | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | Não pode editar as dimensões do cabeçalho da proposta de fatura do projeto numa implementação integrada com o Project Operations. |
| Gestão de projetos e contabilística | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | As faturas de fornecedor entre empresas não podem ser integradas com o Dataverse. |
| Gestão de projetos e contabilística | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | Existe uma incompatibilidade entre a moeda do balanço do cliente e a moeda de relatório. |
| Gestão de projetos e contabilística | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | Pode publicar uma fatura do projeto mesmo que o cliente esteja em espera para todas as faturas. |
| Gestão de projetos e contabilística | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | O botão **Eliminar todas as linhas** está em falta nas propostas de fatura do projeto que têm as vistas **Cabeçalho** e **Linhas**. |
| Gestão de projetos e contabilística | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | Quando publica uma fatura de fornecedor, ocorre o seguinte erro: "A data de contabilidade para a fatura tem de estar no mesmo ano de contabilidade que a encomenda de compra relacionada. Executar o processo de fim do ano da encomenda de compra ou alterar a data para o ano de contabilidade atual." |
| Viagem e Despesa | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | O custo comprometido de um projeto não é divulgado depois de o custo comprometido da viagem ser lançado. |
| Viagem e Despesa | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | O seguinte erro ocorre quando submete um relatório de despesas: "Rastreio de pilha: a empresa não existe." |
| Viagem e Despesa | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | O **ID do projeto** predefinido não foi inserido nos relatórios de despesas quando o parâmetro **Exigir atividade para o diário** está selecionada no projeto. |
| Viagem e Despesa | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | O botão **Publicar despesas** não funciona corretamente no Project Operations em cenários de recursos/sem stock. |
| Viagem e Despesa | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Existe um problema com a **Taxa por quilometragem** do relatório de despesas de quilometragem que inclui os passageiros. |
| Viagem e Despesa | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | As taxas de quilometragem de despesas dos colaboradores não estão corretamente calculadas quando dois tipos de veículos diferentes são usados na categoria de despesas **Nível de taxa de quilometragem**. |
| Viagem e Despesa | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | A procura para o campo **Projeto** numa linha de pedido de viagem não devolve a lista de projetos correta. |
| Viagem e Despesa | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **Quilometragem em revisão** mostra um aviso sobre os relatórios de despesas. |
| Viagem e Despesa | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | O serviço de receção de reconhecimento de caracteres (OCR) não funciona devido a um problema com o URL do serviço OCR de despesas. |
| Viagem e Despesa | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | Quando a funcionalidade **Capacidade de rapidamente colocar por itens despesas recorrentes** está ativada, os montantes nas linhas de itens nos relatórios de despesas alteram os montantes de cada vez que a página **Colocar por itens** é aberta. |
| Viagem e Despesa | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | Não é possível eliminar um relatório de despesas quando a lista provisória tem mais de um aprovador. |

## <a name="removed-and-deprecated-features"></a>Funcionalidades removidas e preteridas

O tópico [Funcionalidades removidas ou preteridas no Project Operations](removed-depreciated-features-project.md) descreve as funcionalidades que foram removidas ou preteridas para o Dynamics 365 Project Operations.

- Uma funcionalidade removida já não está disponível no produto.
- Uma funcionalidade preterida não está no desenvolvimento ativo e poderá ser removida numa atualização futura.

Um anúncio de preterido irá aparecer no tópico [Funcionalidades removidas ou preteridas no Project Operations](removed-depreciated-features-project.md) 12 meses antes de qualquer funcionalidade ser removida do produto.

Para alterações de última hora que afetem apenas o tempo de compilação, mas que sejam binários compatíveis com sandbox e ambientes de produção, o tempo de depreciação será inferior a 12 meses. Normalmente, estas alterações são atualizações funcionais que têm de ser feitas ao compilador.
