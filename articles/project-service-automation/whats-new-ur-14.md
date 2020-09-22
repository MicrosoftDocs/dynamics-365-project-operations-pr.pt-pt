---
title: Novidades na Versão da Atualização 14 do Project Service Automation, V3
description: Esta tópico fornece informações sobre o que há de novo na Versão da Atualização 14 do Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c69eab3b-0bb9-4b52-b606-e8a96e893471
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 31134756a5f4bff3022fca7df8364c49217b9b55
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754534"
---
# <a name="project-service-automation-v3-update-release-14"></a>Versão da Atualização do Project Service Automation V3, Versão da Atualização 14
Temos o prazer de anunciar a atualização mais recente para a aplicação Dynamics 365 Project Service Automation (PSA). Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização. Esta versão é compatível com o Dynamics 365 9.x. Para atualizar esta versão, visite o Centro de Administração para o Dynamics 365 online e aceda à página de soluções para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Este tópico lista as funcionalidades e correções novas ou alteradas para o PSA V3, Versão da Atualização 14. Esta versão tem um número de compilação de V3.10.4.21 e está disponível na seguinte agenda:

- **Disponibilidade geral (Atualização automática):** janeiro de 2020
- **Atualização automática:** fevereiro de 2020

## <a name="update-release-14"></a>Versão da Atualização 14

### <a name="enhancements"></a>Melhorias

- Sales

     - Os valores de campos personalizados de **Detalhes da Linha da Proposta** são copiados para os **Detalhes do Item de Contrato do Projeto** quando uma proposta é atualizada para **Fechada como ganha**.
     - Os projetos confirmados podem ser **Fechados como perdidos**.

- Gestão de Recursos

     - Ao expandir as reservas, será apresentada aos utilizadores uma caixa de diálogo de confirmação para resumir os resultados da reserva e fornecer uma hiperligação para Manter Reservas.


### <a name="bug-fixes"></a>Correções de erros

- Tempo e Despesa

     - Corrigido: melhorou a experiência do utilizador quando o utilizador não tiver selecionado nenhuma entrada a ser corrigida.

- Gestão de Recursos

     - Corrigido: a reserva de um recurso várias vezes sobrepõem-se ao nome do recurso agendável.

- Sales

     - Corrigido: o preço de vendas total não é calculado até que o utilizador também introduza um preço de custo para estimativa de despesas num projeto.
     - Corrigido: fechar uma proposta como **Ganha** falha se o contrato de projeto associado não estiver num estado de **Rascunho**.

