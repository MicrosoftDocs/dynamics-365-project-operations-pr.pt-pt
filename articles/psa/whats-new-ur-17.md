---
title: Novidades ou alterações na Versão da Atualização 17 do Project Service Automation, V3
description: Este tópico lista as funcionalidades e correções disponíveis no Project Service Automation V3, Versão da Atualização 17, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: bb93208217972639f91b39b7b6705d9897373ef7
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126815"
---
# <a name="project-service-automation-update-release-17-v3"></a>Versão da Atualização 17 do Project Service Automation, V3

Temos o prazer de anunciar a mais recente atualização à aplicação Project Service Automation para Dynamics 365. Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização.  Esta versão é compatível com o Dynamics 365 9.x. Para atualizar esta versão, visite o Centro de Administração para o Dynamics 365 online e aceda à página de soluções para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Este tópico lista as funcionalidades e correções novas ou alteradas para o PSA V3, Versão da Atualização 17. Esta versão tem um número de compilação de V3.10.6.34 e está geralmente disponível através de uma auto-atualização em março de 2020.


## <a name="update-release-17"></a>Versão da Atualização 17

### <a name="bug-fixes"></a>Correções de erros

**Gerais**

- Corrigido: o Project Service Automation foi automatizado para impor licenças de Team Member (o Hub de Recursos do Projeto incluirá os metadados do plano Team Member Service 3.x)
 
**Tempo e Despesa**

- Corrigido: não é possível alterar uma estimativa de despesa de preço não zero para zero (0). A alteração é ignorada.

**Gestão de Projetos**

- Corrigido: foi adicionada uma verificação de valores nulos ao nome da posição de um membro de equipa.
- Corrigido: o campo **msdyn_userresourceid** na entidade **msdyn_resourceassignment** foi preterido.
- Corrigido: a atualização de 2.x para 3.x agora trata dos contornos de esforço vazio nas atribuições de tarefa.

**Sales**

- Corrigido: **Invoice.PreValidateInvoiceUpdate** agora trata corretamente do cenário de reatribuição de proprietários dos registos.
- Corrigido: quando a classe de transação é **Hora**, **UnitGroup** é não editável para todas as entidades, incluindo, **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** e **ContractLineDetails**. No entanto, **Unidade** é não editável apenas para **JournalLine** e **InvoiceLineDetails**.


