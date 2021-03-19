---
title: Novidades ou alterações na Versão da Atualização 26 do Project Service Automation, V3
description: Este tópico lista as funcionalidades e correções disponíveis no Project Service Automation V3, Versão da Atualização 26, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 135f017533705e165230ac994d217ad7c58bab10
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280412"
---
# <a name="project-service-automation-update-release-26-v3"></a>Versão da Atualização 26 do Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a mais recente atualização à aplicação Project Service Automation para Dynamics 365. Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização. Esta versão é compatível com o Dynamics 365 9.x. Para atualizar esta versão, visite o Centro de Administração para o Dynamics 365 online e aceda à página de soluções para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Este tópico lista as funcionalidades e correções novas ou alteradas para o Project Service Automation V3, Versão da Atualização 26, V3. Esta versão tem um número de compilação V3.10.44.59 e está geralmente disponível através de uma atualização automática em dezembro de 2020.

## <a name="update-release-26"></a>Versão da Atualização 26

### <a name="bug-fixes"></a>Correções de erros

**Tempo e Despesa**

Foram corrigidos os seguintes problemas:

- Os utilizadores podem alterar a tarefa numa entrada de hora que tenha sido aprovada/submetida.
- Erro de "Referência de Objeto Não Definida" ao guardar a entrada de hora.
- A importação de entrada de hora a partir de atribuições de recursos cria entradas de hora com os valores DateTime incorretos.
- Quando o Project Service Automation e a aplicação Field Service estão ambos instalados, o botão **Novo** é exibido duas vezes na barra de comando para entradas de hora na aplicação Field Service.
- Permitir atualizações de células de **Unidade** e de **Grupo de unidades** agora funciona na grelha **Estimativas de Despesas**.
- O formulário **Atualizar Edição de entrada de hora** inclui **Linha cronológica**.
- A aprovação do tempo para entradas de hora de não projeto bloqueia o sistema ao procurar uma função de aprovação do projeto.

**Gestão de Recursos**

Foram corrigidos os seguintes problemas:

- Validação adicionada no plug-in **PostProjectCreate** para verificar se há um requisito principal antes de criar um.
- O formulário de criação rápida **Membro da Equipa do Projeto** lança uma exceção de referência nula se os campos forem removidos do formulário.
- Gerar requisitos para 12 horas em 1 ano falhará.
- Exceção de referência nula de mensagem de erro melhorada durante a criação de requisitos de recursos.

**Gestão de Projetos**

Foram corrigidos os seguintes problemas:

- Validação melhorada para abordar a exceção de referência nula gerada no plug-in **PreProjectUpdate**.
- Os projetos publicados pelo suplemento de ambiente de trabalho do Microsoft Project eliminam atribuições não atribuídas.
- Adicionou nova validação quando a referência do projeto de uma tarefa é inválida devido a uma exceção de referência nula no plug-in **PreValidateProjectTaskUpdate**.
- A grelha de Membro da Equipa não mostra atribuições distintas no registo do membro da equipa.
- Adicionadas novas mensagens de validação e de erro devido à exceção de referência nula no plug-in **PreProjectTaskDelete**.

**Sales**

Foram corrigidos os seguintes problemas:

- Ao selecionar uma linha baseada em projeto em proposta ou contrato, o botão **Sugestão** só deve ser visível ao selecionar uma linha baseada no produto associada a um produto existente.
- Divida o privilégio **Create_Product** do privilégio **Create_ProjectContract**.
- A eliminação de uma linha de fatura causa falha de referência nula em **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]