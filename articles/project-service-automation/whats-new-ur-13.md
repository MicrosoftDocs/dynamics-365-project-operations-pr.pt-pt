---
title: Novidades na Versão da Atualização 13 do Project Service Automation, V3
description: Esta tópico fornece informações sobre o que há de novo na Versão da Atualização 13 do Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c6f6a5b6-b5bb-467c-b7c7-7fb962504c6d
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5f1b6b3879c94a77ab62082aad1e470a3ba66552
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754535"
---
# <a name="project-service-automation-v3-update-release-13"></a>Versão da Atualização do Project Service Automation V3, Versão da Atualização 13
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
     - Corrigido: os botões adicionais para **Nova Oportunidade**, **Proposta**, **Linha de Proposta** e **Adicionar Produto** são visíveis em comandos para Oportunidades, Propostas, Produtos de Propostas e na subgrelha de linhas baseadas no projeto.


