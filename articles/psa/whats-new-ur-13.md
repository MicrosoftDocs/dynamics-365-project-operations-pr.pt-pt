---
title: Novidades ou alterações na Versão da Atualização 13 do Project Service Automation, V3
description: Esta tópico fornece informações sobre o que há de novo na Versão da Atualização 13 do Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 7287054c470a44ed1fdc243018ec935fe21a6c4f
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147262"
---
# <a name="project-service-automation-update-release-13-v3"></a>Versão da Atualização 13 do Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente para a aplicação Dynamics 365 Project Service Automation (PSA). Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização. Esta versão é compatível com o Dynamics 365 9.x. Para atualizar esta versão, visite o Centro de Administração para o Dynamics 365 online e aceda à página de soluções para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Este tópico lista as funcionalidades e correções novas ou alteradas para o Project Service Automation V3, Versão da Atualização 13. Esta versão tem um número de compilação de V3.10.3.18 e está disponível na seguinte agenda:

- **Disponibilidade geral (Atualização automática):** novembro de 2019
- **Atualização automática:** dezembro de 2019


## <a name="update-release-13"></a>Versão da Atualização 13 

### <a name="bug-fixes"></a>Correções de erros

- Tempo e Despesa

     - Corrigido: a funcionalidade de pesquisa na página **Aprovação de despesas** não funciona quando a pesquisa por finalidade de despesa é efetuada.

- Gestão de Recursos

     - Corrigido: os números na reconciliação foram atualizados para serem justificados à direita.
     - Corrigido: os Recursos Nomeados não podem ser atribuídos a tarefas através do separador **Agenda**.

- Gestão de Projetos

     - Corrigido: exceção de referência nula ao atribuir um membro da equipa quando o **TransactionType** não contém informações de configuração para **Unidade** e **DefaultGroup**.

- Sales

     - Corrigido: os registos do tipo de transação duplicados devolvem um erro quando são criados registos de preço de função.
     - Corrigido: Botões adicionais para **Nova Oportunidade**, **Proposta**, **Linha de Encomendas** e **Adicionar Produto** estão visíveis nos comandos de Oportunidades, Propostas, Produtos de Encomenda e a subgrelha das Linhas baseadas em projetos.


