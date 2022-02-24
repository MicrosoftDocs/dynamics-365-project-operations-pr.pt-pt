---
title: Novidades ou alterações na Versão da Atualização 31 do Project Service Automation, V3
description: Este tópico lista as funcionalidades e correções disponíveis no Project Service Automation V3, Versão da Atualização 31, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: a595c0a129ac35d3416984e57908e73e1eaef2fd
ms.sourcegitcommit: 6e1498502461e86cff722ccaf8795ff11c7c47ad
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5945549"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a>Novidades ou alterações na Versão da Atualização 31 do Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a mais recente atualização à aplicação Project Service Automation para Dynamics 365. Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização. Esta versão é compatível com o Dynamics 365 9.x. Para atualizar esta versão, visite o Centro de Administração para o Dynamics 365 online e aceda à página de soluções para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este tópico lista as funcionalidades e correções novas ou alteradas para o Project Service Automation V3, Versão da Atualização 31. Esta versão tem o número de compilação V3.10.52.77 e está geralmente disponível através de uma atualização automática em maio de 2021.

## <a name="update-release-31"></a>Versão da Atualização 31

### <a name="bug-fixes"></a>Correções de erros

**Tempo e Despesa**

Foram corrigidos os seguintes problemas:

- Os botões de comando de controlo de entrada de tempo na página de **Recursos reservados** eram confusos.
- Uma exceção de referência nula foi gerada em **Project.SetTrackingFields** ao aprovar uma entrada de tempo.

**Gestão de Recursos**

Foram corrigidos os seguintes problemas:

- **Criar membro de equipa** não exibe corretamente a definição de metadados de configuração de reserva para **Estado comprometido de reserva predefinida**.
- Ao atualizar de PSA 1.X para 3.X, o processo de atualização falha em **UpgradeResourceRequirements**.


**Vendas**

Foram corrigidos os seguintes problemas:

- As receitas de valores reais convertem os montantes para a moeda do projeto na grelha de deteção de movimento.
- A predefinição de moeda não é clara ao criar linhas de diário, linhas de cotação e linhas de contrato em cenários em que a moeda base de uma organização difere da moeda do projeto.
- A consulta de **Validação do diário de correção pendente** não filtra por projeto.
- As vendas remanescentes são calculadas incorretamente num projeto.
- As cotações baseadas num falha de contacto quando são criadas sem uma tabela de preços.
- Não é mostrado nenhum girador de processamento quando seleciona **Confirmar fatura**.
- Não é mostrado nenhum girador de processamento quando seleciona **Criar fatura**.
- Fechar uma proposta como perdida não cancela as reservas.







