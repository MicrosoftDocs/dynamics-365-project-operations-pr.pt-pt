---
title: Novidades ou alterações no Project Operations de julho de 2021 para cenários baseados em produção/armazenados
description: Este tópico fornece informações sobre as atualizações de qualidade disponíveis na versão de julho de 2021 do Project Operations para cenários baseados produção/armazenados.
author: andchoi
ms.date: 07/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: db5bb27650d65bb68f45f95cb2562f4b773ddcea
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597076"
---
# <a name="whats-new-or-changed-in-project-operations-july-2021-for-stockedproduction-based-scenarios"></a>Novidades ou alterações no Project Operations de julho de 2021 para cenários baseados em produção/armazenados

_**Aplica-se a:** Project Operations para cenários baseados em stock/produção_

Este tópico aplica-se aos seguintes componentes e versões do Dynamics 365 Project Operations:

- Gestão de projetos e contabilidade no ambiente do Dynamics 365 Finance versão 10.0.20
 
### <a name="quality-updates"></a>Atualizações de qualidade
                                                                                                                                                                                  
| Área de funcionalidades                      | Número de referência| Atualização de qualidade                                                                                                                                                                          |
|-----------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Gestão de projetos e contabilística | [485394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485394) | Os registos de compromisso de custos de uma requisição de compra são limpos assim que a nota da encomenda é lançada a partir do problema da requisição de compra.                                                                           |
| Gestão de projetos e contabilística | [529602](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529602) | A validação do orçamento ocorre duas vezes numa requisição de compra. Esta duplicação significa que não foi possível fechar a requisição e que a nota de encomenda correspondente não foi criada.                                                                                                                        |
| Gestão de projetos e contabilística | [539439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539439) | Não foi possível concluir a regra de faturação **Percentagem sobre a qual faturar** devido a um problema de arredondamento.                                                                              |
| Gestão de projetos e contabilística | [540023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540023) | Quando ajusta a transação e a percentagem tem decimais, o custo e o preço de vendas não são ajustados corretamente.                                      |
| Gestão de projetos e contabilística | [540927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540927) | O explorador de origem contabilística mostra horas para uma única linha de folha de horas para várias linhas de de folha de horas com diferentes atividades.                                      |
| Gestão de projetos e contabilística | [541471](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541471) | As vistas guardadas e a personalização dos detalhes da folha de horas fazem com que o sistema abra sempre os detalhes da primeira folha de horas na lista ao tentar abrir uma folha de horas.  |
| Gestão de projetos e contabilística | [548677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548677) | O nó raiz do projeto desaparece e os registos da estrutura hierárquica do trabalho são eliminados após a importação.                                                                                             |
| Gestão de projetos e contabilística | [548999](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548999) | Quando os itens são recebidos e emitidos parcialmente a partir do requisito do item, o sistema atualiza o saldo de consumo do orçamento errado. |
| Gestão de projetos e contabilística | [550959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550959) | As notas de encomenda de retenção do projeto não estão a mostrar corretamente os totais no painel **Totais** ou a grelha **Fatura pendente**.                                                                  |
| Gestão de projetos e contabilística | [554593](https://fix.lcs.dynamics.com/Issue/Details/?bugId=554593) | Ao fechar o inventário, os ajustes de custos de artigos do projeto são lançados na conta do saldo em vez de na conta de resultados.                                                            |
| Gestão de projetos e contabilística | [557394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557394) | Um voucher de transação lançado no projeto e um voucher de estimativa utilizam USD como moeda de contabilidade, mas o montante está a mostrar aquilo que seria o equivalente em CAD.              |
| Gestão de projetos e contabilística | [560140](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560140) | Os custos consolidados com um requisito de artigo e uma nota de encomenda estão errados no processo de faturação da nota de encomenda com receção e faturação parcial parciais do produto.       |
| Gestão de projetos e contabilística | [560567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560567) | O ajuste do projeto não está a atualizar corretamente o valor das vendas com custos indiretos.                                                                                    |
| Gestão de projetos e contabilística | [561137](https://fix.lcs.dynamics.com/Issue/Details/?bugId=561137) | Falta uma relação definida na tabela **Folha de Horas** com a vista **Trabalhador/Recurso**.                                                                                   |
| Gestão de projetos e contabilística | [563330](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563330) | Não é possível preencher o campo **Número de atividade** quando o seleciona a partir do menu pendente para uma folha de horas entre empresas.                                                                 |
| Gestão de projetos e contabilística | [563840](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563840) | Não é possível adicionar um campo **Finalidade** ou **Descrição da Atividade** às seguintes páginas: **Transação lançada no projeto**, **Criação de propostas de fatura** ou **Fatura do projeto**.  |
| Gestão de projetos e contabilística | [566348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566348) | O controlo de data de entrega errado é fornecido quando cria requisitos de artigos ao utilizar a gestão de dados (**ProjSalesItemRequirementEntity**).                                              |
| Gestão de projetos e contabilística | [566544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566544) | Quando seleciona um ID de contrato de projeto no Finance, o ambiente integrado do Project Operations abre a página para criar um novo registo em vez de abrir o contrato de projeto existente.                                                                                                                 |
| Gestão de projetos e contabilística | [567300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567300) |  A etiqueta, "@SYS4083080" ("Não é possível localizar um registo de Trabalhador exclusivo correspondente aos valores introduzidos”) não está traduzida para dinamarquês.                                |
| Gestão de projetos e contabilística | [569901](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569901) | O campo **Grupo de impostos sobre vendas de artigos** não é editável numa proposta de fatura.                                                                               |
| Gestão de projetos e contabilística | [557049](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557049) | O custo consolidado é sobrestimado com montantes de imposto não dedutíveis.                                                                                                    |
| Gestão de projetos e contabilística | [565080](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565080) | Lançar uma folha de horas entre empresas com vários projetos e diferentes dimensões financeiras gera valores inesperados no razão geral.                             |
| Gestão de projetos e contabilística | [567962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567962) | As linhas da proposta da fatura são duplicadas devido a múltiplas instâncias do processo periódico **Importar a partir da tabela de transição** em execução em simultâneo.                                      |
| Gestão de projetos e contabilística | [571339](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571339) | Ocorreu um erro no lançamento da proposta de fatura da nota de crédito, pelo que as transações no voucher não se equilibram.    |
| Gestão de projetos e contabilística | [573567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573567) | Os custos consolidados do projeto ficam incorretos após o lançamento das faturas pendentes suspensas.                                                                             |
| Gestão de projetos e contabilística | [573886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573886) | Não é possível criar uma nota de crédito para uma ordem de venda do projeto quando o imposto está numa moeda diferente da moeda da empresa.                                      |
| Gestão de projetos e contabilística | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Eliminar um contrato também elimina o endereço associado ao cliente.                                                                                     |
| Gestão de projetos e contabilística | [585811](https://fix.lcs.dynamics.com/Issue/Details/?bugId=585811) | Uma proposta de fatura que resulte de uma correção de transação de tempo negativa não pode ser lançada.                                                                    |
| Viagem e Despesa                  | [532075](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532075) | O imposto é calculado de forma diferente nos relatórios de despesas.                                                                                                                  |
| Viagem e Despesa                  | [546450](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546450) | A atualização de versão **DB72_Expense.updateTrvExpTransProjTransId()** não permite **trvExpTrans.ReferenceDataAreaId** para criar a nova sequência numérica.                    |
| Viagem e Despesa                  | [568805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568805) | O montante apresentado não é mostrado com o campo obrigatório.                                                                                                             |
| Viagem e Despesa                  | [568831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568831) | Melhorias no desempenho ao anexar uma despesa ao relatório de despesas através da interface de utilizador Despesas Reinventados.                                                            |
| Viagem e Despesa                  | [570790](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570790) | Pode eliminar os relatórios de despesas lançados.                                                                                           |
| Viagem e Despesa                  | [571317](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571317) | A Mensagem da política de despesas é apresentada várias vezes.                                                                                                       |
| Viagem e Despesa                  | [573969](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573969) | O campo **Método de pagamento** é incluído no painel **Nova despesa**.                                                                                                      |
| Viagem e Despesa                  | [523557](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523557) | A ferramenta **Repor Estado do documento de despesas** deve repor o estado do relatório de despesas para **Rascunho** se o fluxo de trabalho não tiver sido encontrado. 

### <a name="regulatory-updates"></a>Atualizações regulamentares
Para obter informações sobre atualizações regulamentares para as aplicações de Finanças e Operações, consulte [Atualizações regulamentares](/dynamics365/finance/localizations/regulatory-updates). Também pode iniciar sessão no Lifecycle Services (LCS) e ver as atualizações regulatórias planeadas através da ferramenta Procurar problema. A pesquisa Emitir permite pesquisar por país, tipo de funcionalidade e versão.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
