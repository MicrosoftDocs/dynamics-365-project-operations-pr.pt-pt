---
title: Novidades ou alterações na Versão da Atualização 27 do Project Service Automation, V3
description: Este tópico lista as funcionalidades e correções disponíveis no Project Service Automation V3, Versão da Atualização 27, V3.
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
ms.openlocfilehash: 8879229b50ef113d6d6cb8622b707f0c12182a57
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280322"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-27-v3"></a>Novidades ou alterações na Versão da Atualização 27 do Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a mais recente atualização à aplicação Project Service Automation para Dynamics 365. Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização. Esta versão é compatível com o Dynamics 365 9.x. Para atualizar esta versão, visite o Centro de Administração para o Dynamics 365 online e aceda à página de soluções para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Este tópico lista as funcionalidades e correções novas ou alteradas para o Project Service Automation V3, Versão da Atualização 27. Esta versão tem um número de compilação de V3.10.45.98 e está geralmente disponível através de uma Atualização automática em janeiro de 2021.

## <a name="update-release-27"></a>Versão da Atualização 27

### <a name="bug-fixes"></a>Correções de erros

**Gerais**

Foram corrigidos os seguintes problemas:

- Os registos gerados por plug-ins no Project Service Automation não foram definidos para apagar automaticamente.
- A atualização automática falha porque a solução do Project Service Automation contém um legado nulo NavBarArea e elemento de título.

**Tempo e Despesa**

Foram corrigidos os seguintes problemas:

- A grelha de **Entrada de tempo** apresenta dados incorretos para o comportamento da data **Zona horária independente**.
- A grelha de **Entrada de tempo** cria dados hora incorreta para comportamento de data de **Zona horária independente**.
- A procura de tarefas não se limita ao projeto selecionado na página de **Editar entrada de tempo**.
- A aprovação do tempo para entradas de tempo de não projeto bloqueia porque o sistema está à procura de aprovador do projeto.
- As entradas corretas em Valores Reais exibem uma mensagem de erro incorreta.
- Quando uma tarefa contém um valor nulo para o custo real e os totais do projeto são atualizados, ocorre o seguinte erro: "Chave dada não presente no dicionário".
- Em casos específicos, os filtros **Agrupar por** no separador **Estimativa do projeto** não apresentam estimativas de despesas.
- O intervalo de **horário de verão** não está correto para as entradas de tempo.

**Gestão de Projetos**

Foram corrigidos os seguintes problemas:

- Melhorias de colocação em cache, o que melhora o desempenho relacionado com o carregamento da página do **Projeto**.
- Regra de negócio obsoleta que impede que as tarefas do projeto sejam concluídas.
- Os contornos de suplemento do Microsoft Project não estão a respeitar o calendário do suplemento, resultando em requisitos de recursos incorretos.
- A criação de projetos a partir de modelos define incorretamente as datas de atribuição e impede a capacidade de gerar requisitos de recursos.
- O utilizador não pode aceder a opções de **Categoria**, **Descrição**, **Estado** utilizando o teclado.
- Os valores reais de venda do projeto não incluem valores de venda de taxas e materiais.
- Agregação das vendas efetivas e do custo real ocorre incorretamente com taxas de câmbio diferentes.
- A descrição no **modelo de hora de trabalho padrão** é enganosa.
- Avançar uma tarefa não remove a **categoria** na interface do utilizador até que seja atualizada.
- Validação em falta para garantir que mover um projeto para além da data final não é permitido.

**Sales**

Foram corrigidos os seguintes problemas:

- Uma exceção de referência nula é gerada numa linha de cotação do projeto porque a **Importar de estimativa de projeto** é visível quando um projeto não foi selecionado.
- O seguinte erro, "Referência de objeto não definida para uma instância de um objeto" ocorre ao fechar uma citação como **Venceu**.
- O estado de ajustamento não está definido durante uma reversão real, ao mesmo tempo que desassocia um projeto de um item de contrato.
- Quando Dynamics 365 Field Service e o Project Service Automation estão ambos instalados, as opções **Bloquear preços** e **Usar preços atuais** não são apresentadas ao mesmo tempo na página **Fatura**.
- Para a língua japonesa, há uma tradução inconsistente com outras páginas baseadas em calendários.
- **Ativar** e **Desativar** foram removidas das entidades da **Associação de Listas de Preços** no Project Service Automation.


[!INCLUDE[footer-include](../includes/footer-banner.md)]