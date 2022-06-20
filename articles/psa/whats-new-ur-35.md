---
title: Novidades ou alterações na Versão da Atualização 35 do Project Service Automation, V3
description: Este artigo lista as funcionalidades e correções disponíveis na Versão 35 da Atualização do Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/03/2021
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 28b4a5ccbfff83c9b1a18cb0b4062af9cdaf8f6e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912852"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-35-v3"></a>Novidades ou alterações na Versão da Atualização 35 do Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente para a aplicação Microsoft Dynamics 365 Project Service Automation. Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização. É compatível com o Dynamics 365, versão 9.x. Para atualizar para esta versão, visite a página de soluções online do Centro de Administração do Dynamics 365 e instale a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este artigo lista as funcionalidades e correções novas ou alteradas para a Versão 35 da Atualização do Project Service Automation, V3. Esta versão tem o número de compilação V3.10.56.110 e será disponibilizada de uma forma geral através de uma atualização automática em setembro de 2021.

## <a name="update-release-35"></a>Versão da Atualização 35

### <a name="bug-fixes"></a>Correções de erros

Foram corrigidos os seguintes problemas.

**Tempo e Despesa**

- O aprovador do projeto recebe um erro de privilégio de leitura quando aprova as entradas de despesas com uma função de **Aprovador do Projeto**.
- O aprovador do projeto recebe um erro de privilégio de escrita em **msdyn_projectapproval** quando cancela uma entrada de hora aprovada com uma função de **Aprovador do Projeto**.
- Quando seleciona **Copiar semana** numa entrada de hora no Dynamics 365 para telemóvel - Módulo da aplicação do Hub de Recursos do Projeto, ocorre o seguinte erro: "...\OfficeProductivity_RibbonRules.js.map: HTTP error: status code 404, net::ERR_HTTP_RESPONSE_CODE_FAILURE."
- A política **Repetir** aprova automaticamente as entradas que foram anteriormente rejeitadas.
- A subgrelha **Conjuntos de Aprovações** mostra ações de friso não aplicáveis.
- Faltam ícones em **Tarefa do Projeto** e **Função do Recurso** na entidade **Entrada de Hora**.
- Quando importa atribuições de recursos, as entradas de hora importadas não têm a duração correta para as atribuições que foram criadas através de tarefas no modo manual.
- **Eliminar** está em falta na página **Pesquisa Avançada de registos de Entrada de Hora**.
- **Guardar** está em falta na página **Informações da entrada de hora**. Este problema impede que as alterações sejam guardadas quando a página é fechada.

**Planeamento de projeto**

- As grelhas **Atribuição de Recurso** e **Reconciliação de Recursos** não ordenam os atributos agrupados por ordem alfabética.
- As tarefas não podem ser criadas se o comportamento de data estiver personalizado como **Apenas Data**.

**Gestão de recursos**

- Se tiver o Dynamics 365 Field Service e o Project Service Automation instalados, ocorrerão problemas de sobreposição quando **Vista Associada de Requisito de Recurso** estiver associada a uma página principal.
- Se fizer duplo clique em **Guardar**, na caixa de diálogo **Criação Rápida de Membro da Equipa**, impede que o requisito de recurso seja criado.

**Vendas**

- Uma exceção é gerada se eliminar uma tarefa que está associada a uma cotação com um estado **Ganha**.
