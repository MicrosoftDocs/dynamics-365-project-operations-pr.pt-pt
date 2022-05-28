---
title: Novidades ou alterações na Versão da Atualização 38 do Project Service Automation, V3
description: Este tópico lista as funcionalidades e correções que estão disponíveis na Versão de Atualização 38 do Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 12/06/2021
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
ms.openlocfilehash: 16994535d57dc1d7fefbe6e892c154f52638c7c0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598732"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Novidades ou alterações na Versão da Atualização 38 do Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente para a aplicação Microsoft Dynamics 365 Project Service Automation. Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização. É compatível com o Dynamics 365, versão 9.x. Para atualizar para esta versão, visite a página de soluções online do Centro de Administração do Dynamics 365 e instale a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este tópico lista as funcionalidades e correções novas ou alteradas para o Project Service Automation V3, Versão da Atualização 38, V3. Esta versão tem um número de compilação V3.10.59.117 e está geralmente disponível através de uma atualização automática em dezembro de 2021.

## <a name="update-release-38"></a>Versão da Atualização 38

### <a name="bug-fixes"></a>Correções de erros

Foram corrigidos os seguintes problemas.

**Tempo e Despesa**

- Uma exceção ocorre quando o comprimento dos registos de registos de conjuntos de aprovação excede 100.000 registos.
- Os utilizadores não podem aceder à grelha **Entrada de Tempo** a partir da página principal **Entrada de Tempo**.
- A caixa de diálogo **Importação da Entrada de Tempo** não mostra qualquer texto quando nenhum item é elegível para importação.
- Os utilizadores podem criar conjuntos de aprovação onde o campo **Estado de Destino** está definido como **Desconhecido**.

**Gestão de Projetos**

- Os contornos não são mostrados corretamente nas atribuições de recursos para UTC (+09:30) e UTC (+10:00) quando a hora de verão começa.
- O campo **Coluna Adicional** para estruturas hierárquicas de trabalho está ocultado em algumas regiões.
- O seletor de datas para o controlo do calendário na grelha **Tarefa do Projeto** não está corretamente localizado para chinês.

**Vendas**

- Os valores de **Desempenho do Contrato** e do **Custo Real do Projeto** não correspondem quando os recursos reserváveis que têm diferentes unidades de contratação e moedas apresentam entradas de tempo.
- Um fluxo de trabalho personalizado para confirmar automaticamente as faturas falha quando as faturas são importadas como um solução gerida. A seguinte mensagem é mostrada: "Mensagem Microsoft.Xrm.Sdk.InvalidPluginExecutionException: Estado inválido da fatura."
- Quando **Raiz** é selecionada como a opção de resumo, e o projeto tem estimativas de uma mistura de classes de transações (por exemplo, uma combinação de estimativas de tempo, despesas e materiais), o sistema resume entre classes de transações como uma linha de taxa única.
- Em cenários em que uma linha de despesas é adicionada antes de um item de contrato ser associada a um projeto, o preço correto não é introduzido como um valor predefinido no campo **Atualizar Preço**.
- Os montantes de vendas negativos não são permitidos nas entidades **Projeto** e **Tarefa**.
