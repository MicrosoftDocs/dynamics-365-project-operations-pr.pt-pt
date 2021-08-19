---
title: Novidades de julho de 2021 - Project Operations para cenários baseados em recursos/não armazenados
description: Este tópico fornece informações sobre as atualizações de qualidade disponíveis na versão de julho de 2021 do Project Operations para cenários baseados em recursos/não armazenados.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 69507427521466335df9cbbaba79db1cfc7be91386b8b2ded5b1c384555946ee
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008060"
---
# <a name="whats-new-july-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades de julho de 2021 - Project Operations para cenários baseados em recursos/não armazenados

*Aplica-se A: Project Operations para cenários baseados em recursos/não armazenados*

Este tópico aplica-se aos seguintes componentes e versões do Dynamics 365 Project Operations:

   - Project Operations na versão de ambiente 4.12.0.148 ou 4.12.0.152 do Microsoft Dataverse.
   - Gestão de projetos e contabilística na versão 10.0.20 do ambiente Dynamics 365 Finance.

## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versão

Estão incluídas nesta versão as seguintes funcionalidades:

- Capacidade para os administradores verem registos PSS e registos do Conjunto de Operações a partir do menu de definições. Os registos são armazenados durante 90 dias.

## <a name="project-operations-dual-write-maps-updates"></a>Atualizações de mapas de escrita dupla do Project Operations

Não existem atualizações para os mapas de escrita dupla do Project Operations nesta versão.

Para obter uma lista atual e as versões dos mapas de escrita dupla do Project Operations, consulte [Versões do mapa de escrita dupla do Project Operations](../environment/resource-dual-write-maps.md).

Execute sempre a versão mais recente do mapa no seu ambiente e ative todos os mapas de tabelas relacionados à medida que atualiza a sua solução do Project Operations Dataverse e a versão da solução Finance. Certas funcionalidades e capacidades podem não funcionar corretamente se a versão mais recente do mapa não estiver ativada. Pode ver a versão ativa do mapa na página **Escrita dupla** na coluna **Versão**. Ative uma nova versão do mapa ao selecionar **Versões do mapa de tabelas**, selecionar a versão mais recente e, em seguida, guardar a versão selecionada. Se tiver personalizado um mapa de tabela fora da caixa, reaplique as alterações. Para mais informações, consulte [Gestão do ciclo de vida da aplicação](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se encontrar um problema ao iniciar o mapa, siga as instruções na secção [Problema de colunas de tabela em falta nos mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) no guia de resolução de problemas de escrita dupla.

## <a name="quality-updates"></a>Atualizações de qualidade

### <a name="project-operations-on-dataverse"></a>Project Operations no Dataverse

| **Área de funcionalidades**              | **Número de referência** | **Atualização de qualidade**                                                                                                                                                                                             |
|-------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Faturação e Preços           | 2224046              | O campo **Classe de Transação** é editável no separador **Detalhes de Linha de Proposta**, mas é bloqueado se estiver a trabalhar na página **Detalhes de Linha de Proposta**.                                                                     |
| Faturação e Preços           | 2224400              | A ação **Fechar Proposta como Ganha** falha quando uma proposta não tem marcos de data.                                                                                                                                    |
| Faturação e Preços           | 2234089              | Quando introduz manualmente uma descrição de produto, esta é limpa depois de introduzir uma quantidade para uma estimativa de material.                                                                                                                         |
| Faturação e Preços           | 2234100              | A grelha **Configuração de Faturação de Tarefas** não inclui a coluna **Material** e o respetivo valor no separador **Faturação de Tarefas** do projeto.                                                                                                       |
| Faturação e Preços           | 2277409              | O ID de produto não está disponível no detalhe do item do contrato para uma linha de tipo de material.                                                                                                                                        |
| Faturação e Preços           | 2281728              | A criação de um item de contrato reavalia desnecessariamente os valores reais ao causar aumentos significativos no volume de dados, o que afeta o desempenho.                                                                                |
| Faturação e Preços           | 2298668              | As linhas do diário associadas a uma despesa recuperada e eliminada não são removidas.                                                                                                                                     |
| Faturação e Preços           | 2300192              | Quando vários utilizadores estão a editar uma fatura, é possível criar um novo detalhe da linha de fatura numa fatura confirmada.                                                                                   |
| Faturação e Preços           | 2301569              | As faturas não podem ser corrigidas se tiver sido aplicado um sinal de \$0.                                                                                                                                        |
| Faturação e Preços           | 2307965              | É apresentado um erro se um preço de categoria for criado com valores em falta.                                                                                                                           |
| Faturação e Preços           | 2326870              | Ocorre um erro em **Microsoft.Dynamics.ProjectService.Plugins.PostInvoiceLineDelete** se **producttypecode** for nulo.                                                                            |
| Faturação e Preços           | 2332732              | É apresentado um erro se um marco do item de contrato for criado sem uma linha de encomenda.                                                                                                                |
| Planeamento e Monitorização de Projetos | 2181094              | A API Agendamento de Projetos suporta agora Registos PSS e Registos de Conjuntos de Operações que são armazenados durante 90 dias.                                                                                                                  |
| Planeamento e Monitorização de Projetos | 2254201              | A etiqueta **Modo de Agendamento** é atualizada com detalhes que descrevem a lógica de predefinição.                                                                                                                                      |
| Planeamento e Monitorização de Projetos | 2300252              | A cache de resposta **openProject** é atualizada e inclui o proprietário do token na chave da cache, **URL Base** e **URL do Segmento** para o **URL do Pedido** poder ser sempre recriado se o **URL Base** for alterado. |
| Planeamento e Monitorização de Projetos | 2301312              | **msdyn_membershipstatus** foi removido da vista **Membro da Equipa do Projeto**.                                                                                                                                        |
| Planeamento e Monitorização de Projetos | 2302759              | Os produtos são desnecessariamente obtidos nos separadores **Atribuições de Recursos**, **Estimativas** e **Estimativas de Despesas**.                                                                                                        |
| Planeamento e Monitorização de Projetos | 2308050              | **CopyProject** falha com o erro: "Falha ao obter o token para falar com o serviço remoto".                                                                                                                           |
| Planeamento e Monitorização de Projetos | 2322650              | A vista **Lista de Tarefas do Projeto** foi atualizada para apresentar a data da tarefa por predefinição.                                                                                                            |
| Planeamento e Monitorização de Projetos | 2327266              | **CopyProject** gera o erro "Chave não encontrada no dicionário" ao copiar as estimativas.                                                                                                      |
| Planeamento e Monitorização de Projetos | 2328123              | **CopyProject** gera o erro: "Falha ao obter o token para falar com o serviço remoto".                                                                                                                          |
| Planeamento e Monitorização de Projetos | 2336258              | **CopyProject** copia incorretamente os nomes de posição dos recursos.                                                                                                                                                 |
| Faturação e Preços           | 2224476              | O campo **Recurso Reservável** não assume corretamente por predefinição o utilizador com sessão iniciada na página **Utilização de Material**.                                                                                                            |
| Gestão de Recursos           | 2277249              | Ocorre um erro quando um requisito de recursos não baseado no projeto é atualizado.                                                                                                            |
| Gestão de Recursos           | 2323869              | A utilização de recursos não reconhece corretamente os recursos filtrados.                                                                                                                                             |
| Tempo e Despesa              | 2176538              | São aplicados operadores de filtro incorretos ao controlo **Entrada de Hora**.                                                                                                                                                   |
| Tempo e Despesa              | 2177462              | A eliminação de uma entrada de hora na grelha não atualiza o estado do botão **Submeter**, **Recuperar**, **Eliminar** e **Editar Entrada** conforme esperado.                                                                                        |
| Tempo e Despesa              | 2299985              | **TimeEntriesImportFromResourceAssignment** não mantém a hora de início/fim a partir dos perfis de atribuição.                                                                                                  |
| Tempo e Despesa              | 2318426              | Após a submissão de uma entrada de hora, os campos bloqueados ainda podem ser editados.                                                                                                                                   |
| Tempo e Despesa              | 2323749              | Ocorre um erro quando uma despesa é criada a partir do separador **Relacionada** de um recurso reservável.                                                                                                      |
| Tempo e Despesa              | 2327678              | Quando cria uma entrada de hora a partir do separador **Relacionada** de um recurso reservável, o recurso principal não é transmitido para o controlo de entrada de hora.                                                                            |
| Geral                       | 2296857              | Seguimento do progresso para tarefas de execução prolongada.                                                                                                                                                                        |
| Geral                       | 2253682              | A solução de escrita dupla do Project Operations não deve ser instalada quando o núcleo de escrita dupla é instalado num ambiente sem a solução de orquestração de escrita dupla.                                                |
| Geral                       | 2316420              | O aprovisionamento do núcleo do Project Service falha se a unidade do utilizador da aplicação for alterada.                                                                                                                     |
| Geral                       | 2376405              | Problema de atualização orientada por fabricante fixo (A atualização de qualidade está disponível na versão 4.12.0.152)                                                                                                                     |
### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Gestão de projetos e contabilística no Dynamics 365 Finance

| Área de funcionalidades                      | Número de referência | Atualização de qualidade                                                                                                                                                                                                                                                                                                                |
|-----------------------------------|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Gestão de projetos e contabilística | 4620267          | Não é possível personalizar formulários para adicionar um campo **Finalidade** às páginas **Transação lançada no projeto**, **Criação de propostas de fatura** e **Proposta de fatura**.                                                                                                                                                                                         |
| Gestão de projetos e contabilística | 4613449          | Quando seleciona um ID de contrato de Projeto no Finance, o ambiente integrado do Project Operations abre a página para criar um novo registo, em vez da página para os contratos do projeto já criados.                                                                                                                                           |
| Gestão de projetos e contabilística | 4614445          | Na implementação do cenário integrado do Project Operations, não é possível editar o campo **Grupo de impostos sobre vendas de artigos** na proposta de fatura que é importada a partir da transição. O grupo de impostos sobre vendas de artigos deve ser editável para uma proposta de fatura aberta de todos os tipos de transações, incluindo conta, horas, despesas, taxas e artigos. |
| Gestão de projetos e contabilística |                  | Não é possível lançar uma proposta de fatura que resulte de uma correção de transação de tempo negativa.                                                                                                                                                                                                                                              |
| Gestão de projetos e contabilística |                  | As linhas da proposta da fatura são duplicadas devido a múltiplos processos periódicos **Importar a partir da tabela de transição** em execução em simultâneo.                                                                                                                                                                                                                |

