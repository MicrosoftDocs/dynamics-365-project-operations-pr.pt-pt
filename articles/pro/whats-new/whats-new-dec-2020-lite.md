---
title: Novidades de dezembro de 2020 – Implementação do Project Operations Lite – negócio para faturação pró-forma
description: Este tópico fornece informações sobre as atualizações de qualidade disponíveis na versão de dezembro de 2020 da implementação do Project Operations Lite – negócio para faturação pró-forma.
author: sigitac
manager: Annbe
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6a001cea56411865599a5c0a41fe47682dad35c2
ms.sourcegitcommit: 5791f6347e800fc4f6c76e7460947cb6824edebe
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 12/08/2020
ms.locfileid: "4700830"
---
# <a name="whats-new-december-2020---project-operations-lite-deployment---deal-to-proforma-invoicing"></a>Novidades de dezembro de 2020 – Implementação do Project Operations Lite – negócio para faturação pró-forma

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

Este tópico aplica-se aos seguintes componentes e versões do Dynamics 365 Project Operations:

  - Project Operations na versão 4.5.0.134 do ambiente Dataverse 

A tabela que se segue lista as atualizações para o Project Operations na versão 4.4.0.70 do ambiente Dataverse.

| **Área de funcionalidades** | **Número de referência** | **Atualização de qualidade** |
| --- | --- | --- |
| Faturação e Preços | 1986009 | As linhas do diário criadas manualmente têm um desempenho inconsistente quando confirmado antes do projeto ser associado ou desassociado a um item de contrato. |
| Faturação e Preços | 2014153 | Os produtos não são faturados quando são executados a partir da agenda da fatura. |
| Faturação e Preços | 2014159 | Os produtos não são puxados quando a fatura é atualizada para transações. |
| Faturação e Preços | 2028174 | As atualizações a detalhes da linha de fatura devem seguir a lógica do diário de correção. |
| Faturação e Preços | 2028315 | Correções de comportamento de grelha aninhada editáveis. |
| Faturação e Preços | 2031070 | Ajustar o detalhe da linha de fatura corretiva deve seguir a lógica do diário de correção. |
| Faturação e Preços | 2034186 | Deve ser capaz de atualizar um projeto num item de contrato. |
| Faturação e Preços | 2034206 | O estado de ajustamento deve ser definido durante a reversão real, ao mesmo tempo que desassocia um projeto de um item de contrato. |
| Faturação e Preços | 2040871 | Permitir atualizações de células de Unidade e de Grupo de Unidades na grelha de estimativas Despesas. |
| Faturação e Preços | 2053754 | Os valores reais criados a partir de edições de fatura não são marcados com o estado de ajuste e estado de faturação. |
| Faturação e Preços | 2057874 | Ligação de transação correta criada durante a edição de detalhes da linha de fatura. |
| Faturação e Preços | 2057875 | Origens de transação correta criada durante a edição de detalhes da linha de fatura. |
| Faturação e Preços | 2057944 | Estado Não exceder definido como Comprometido para valores reais que não estão prontos para faturar de uma correção de fatura. |
| Faturação e Preços | 2057963 | Divida o privilégio Create\_Product do privilégio Create\_ProjectContract. |
| Faturação e Preços | 2067622 | O ícone de processamento deve ser mostrado ao gerar marcos. |
| Faturação e Preços | 2067624 | O montante contratado deve ser marcado como Negócio recomendado ao gerar marcos. |
| Faturação e Preços | 2086880 | Oculte o botão **Sugestão** na fita para linhas de proposta baseadas em projeto. |
| Implementação e Configuração | 2101152 | Novo ambiente criado usando o modelo do Project Operations a partir do Centro de Administração do Power Platform deve ter todas as operações pós-instalação realizadas. |
|   Gestão de oportunidades | 2022204 | A grelha de faturação baseada em projetos no separador **Faturação de tarefas** na página **Projeto** deve ocultar a grelha baseada no projeto se não houver uma linha de proposta/item de contrato com **Todas as tarefas** e vice-versa. |
|   Gestão de oportunidades | 2086601 | As funções e categorias desativadas não devem ser copiadas para funções Faturáveis e a lista de categorias Faturável em linhas de proposta e itens de contrato. |
| Planeamento e Monitorização de Projetos | 1949065 | A visibilidade dos dados funciona corretamente com zoom a 200% |
| Planeamento e Monitorização de Projetos | 2046317 | Capacidade de renomear a entidade do projeto no Project Operations |
| Planeamento e Monitorização de Projetos | 2057171 | Mensagem de erro atualizada quando o campo **Data de Início do Projeto** estiver vazio na página **Projeto**. |
| Planeamento e Monitorização de Projetos | 2057197 | A cópia da linha de estimativa com referência de tarefa não é suportada. |
| Planeamento e Monitorização de Projetos | 2060687 | O aviso de fuso horário agora desaparece após uma duração específica. |
| Gestão de recursos | 1832887 | O ID da categoria de recursos predefinida tem de ser estático para garantir cargas de dados repetíveis para os ambientes do Dataverse e do Finance. |
| Tempo e despesa | 2034882 | O botão **Novo** aparece duas vezes na barra de comando para entradas de hora quando o Dynamics 365 Field Service é instalado. |
| Tempo e despesa | 2056028 | Atualize a página **Edição de Tempo** para incluir linha de tempo. |
| Tempo e despesa | 1983747 | Gráfico de entrada de hora mostra dados adicionais. |
