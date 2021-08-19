---
title: Novidades de julho de 2021 - implementação leve do Project Operations
description: Este tópico fornece informações sobre as atualizações de qualidade disponíveis na versão de julho de 2021 da implementação leve do Project Operations.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6992498df5beb97d4e7197e301f093320dc28a23
ms.sourcegitcommit: 3abf1e67938d91bd826b025ae3187cd313f556b9
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 07/07/2021
ms.locfileid: "6433667"
---
# <a name="whats-new-july-2021---project-operations-lite-deployment"></a>Novidades de julho de 2021 - implementação leve do Project Operations

_Aplica-se a: Implementação lite – negócio para faturação pró-forma_

Este tópico aplica-se aos seguintes componentes e versões do Dynamics 365 Project Operations:

  - Project Operations na versão 4.12.0.148 do ambiente Dataverse.

## <a name="quality-updates"></a>Atualizações de qualidade
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