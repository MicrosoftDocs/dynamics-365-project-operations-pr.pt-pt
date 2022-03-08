---
title: Novidades em novembro de 2020 – Project Operations para cenários baseados em Recursos/Não Stock
description: Este tópico fornece informações sobre as atualizações de qualidade disponíveis na versão de novembro de 2020 do Project Operations para cenários baseados em Recursos/Não Stock.
author: sigitac
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9eda9d75f5a4d71e6e4b8bd22dce973270639db3f927ac6a76be5b3c4303fc31
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007970"
---
# <a name="whats-new-november-2020---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades em novembro de 2020 – Project Operations para cenários baseados em Recursos/Não Stock

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Este tópico aplica-se aos seguintes componentes e versões do Dynamics 365 Project Operations:

- Project Operations na versão 4.4.0.70 do ambiente CDS
- Gestão de projetos e contabilística na versão 10.0.14 do ambiente Dynamics 365 Finance

## <a name="updates-to-project-operations-for-resource-non-stocked-based-scenarios"></a>Atualizações ao Project Operations para cenários baseados em Recursos/Não Stock

### <a name="project-operations-on-cds"></a>Project Operations no CDS

| Área de funcionalidades                 | Número de referência | Atualização de qualidade                                                                                                                                                                    |
|------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   Gestão de oportunidades       | 2036993          | As linhas de estimativa e itens de contrato de atribuição de recursos são atualizados em propostas ganhas quando o tipo de linha de proposta for **Todas as tarefas**.                                                 |
| Faturação e preços          | 2070392          | Os itens de contrato do projeto na fatura aumentam sempre que **Atualizar transações de faturas** for selecionado.                                                                         |
| Planeamento de projeto             | 2043336          | Incapaz de eliminar um registo de membro da equipa do projeto.                                                                                                                                  |
| Planeamento de projeto             | 2046013          | Comportamento inconsistente para colunas de etiqueta Estimativas no carregamento vs. na alteração do tipo de fase de tempo.                                                                                   |
| Planeamento de projeto             | 2046647          | As horas de início e de fim estão erradas por uma hora quando os requisitos de recursos são gerados por membros da equipa do projeto.                                                                      |
| Planeamento de projeto             | 2053879          | (Pelo próximo lançamento da versão do CDS) PublishUnassignedAssignments quebra uma tentativa de guardar uma tarefa quando o erro, "O valor passado para ConditionOperator.In está vazio."                       |
| Planeamento de projeto             | 2055501          | Deixar vazia a **Data de Início do Projeto** causa uma falha na agenda.                                                                                                      |
| Planeamento de projeto             | 2066817          | Não é possível criar um recurso genérico utilizando o seletor de pessoas no separador **Tarefas**.                                                                                                   |
| Planeamento de projeto             | 2067034          | **Ver Detalhes** não está disponível na página **Detalhes da Tarefa**.                                                                                                       |
| Gestão de recursos          | 2046667          | Os membros genéricos da equipa não são eliminados, mesmo depois de todos os recursos serem cumpridos.                                                                                                    |
| Entrada de tempo e de despesas rápidas | 2047499          | O botão **Novo** na página Entrada de Tempo abre a página **Nova Assinatura de E-mail**.                                                                                               |
| Entrada de tempo e de despesas rápidas | 2059859          | Pop-up inesperado abre ao criar uma entrada de despesas.                                                                                                                         |
| Outros                        | 2044181          | (Desinstalar uma nota de encomenda) Quando tenta desinstalar msdyn_ProjectServiceCore_Patch e as soluções principais msdyn do Project Service, ocorre o erro "Registo indisponível".  |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Gestão de projetos e contabilística no Dynamics 365 Finance

| Área de funcionalidades        | Número de referência | Atualização de qualidade                                                                                                                                                            |
|---------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Reconhecimento de receitas | [451662](https://fix.lcs.dynamics.com/Issue/Details/?bugId=451662)           | A percentagem de estimativa do projeto completa está errada quando o contrato está a utilizar uma moeda estrangeira e a percentagem de progresso do trabalho para o método completo.                     |
| Reconhecimento de receitas | [469894](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469894)           | Incapaz de publicar estimativas com o método de conclusão de **Custos de valores reais**.                                                                                                    |
| Reconhecimento de receitas | [485439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485439)           | A eliminação falha devido a um erro de desequilíbrio do cupão quando a moeda da empresa e a moeda de transação são diferentes.                                              |
| Gestão de despesas  | [456882](https://fix.lcs.dynamics.com/Issue/Details/?bugId=456822)           | Para os utilizadores não administradores, os valores de pesquisa para colunas de linhas de despesas, como o **ID do Projeto** e a **Categoria de Despesas** não estão a aparecer corretamente na estrutura do conector de dados. |
| Gestão de despesas  | [469300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469300)           | O predefinição da propriedade de linha não está a aparecer para as categorias de Despesas.                                                                                                         |
| Gestão de despesas  | [469302](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469302)           | A integração das despesas deve incluir a propriedade da linha do relatório de despesas.                                                                                             |
| Faturação           | [462499](https://fix.lcs.dynamics.com/Issue/Details/?bugId=462499)           | Não é possível publicar propostas de faturas de projeto por causa de uma mensagem de erro que diz que a combinação de FD não foi validada.                                                    |
| Faturação           | [470614](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470614)           | Não é possível ver transações a partir da página de detalhes da **fatura**.                                                                                                              |
| Faturação           | [480070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480070)           | As linhas de proposta de fatura podem ser eliminadas.                                                                                                                                  |
| Gestão contabilística do projeto  | [470293](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470293)           | Os itens de menu de **previsão** não estão visíveis na página da lista de **Projetos**.                                                                                                   |
| Gestão contabilística do projeto  | [475873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475873)           | Não é possível abrir a **Declaração do projeto**   > **Transações e previsão**.                                                                                                       |
| Gestão contabilística do projeto  | [475879](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475879)           | **Ajustar a contabilidade** não está ativado para transações de projetos faturados.                                                                                                  |
| Gestão contabilística do projeto  | [480962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480962)           | Os detalhes contabilísticos não estão incluídos na tabela **ProjCDSActualsImport** quando o diário de **Integração** é publicado.                                                  |
| Gestão contabilística do projeto  | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558)           | A entrada de previsão do Projeto é duplicada quando remove e, em seguida, lê uma atribuição de recursos.                                                                            |
| Gestão contabilística do projeto  | [502019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=502019)           | A seleção de uma ligação de ID do Projeto não abre o URL de ligação avançada do CDS.                                                                                                         |
| Gestão contabilística do projeto  | [505458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505458)           | Não pode atualizar a data de início de uma tarefa no CDS.                                                                                                                           |
| Gestão contabilística do projeto  | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041)           | Ativar a funcionalidade, vários itens de contrato não são possíveis sem a integração do CDS.                                                                                   |

### <a name="regulatory-updates"></a>Atualizações regulamentares
Para obter informações sobre atualizações regulamentares para aplicações Finance and Operations, consulte [Atualizações regulamentares](/dynamics365/finance/localizations/regulatory-updates). Também pode iniciar sessão no LCS e ver as atualizações regulamentares planeadas utilizando a ferramenta de pesquisa Emitir. A pesquisa Emitir permite pesquisar por país, tipo de funcionalidade e versão.


[!INCLUDE[footer-include](../includes/footer-banner.md)]