---
title: Navegar na interface de utilizador
description: Este tópico fornece informações sobre a Gestão de projetos no Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: deedfe0c6601fd09e09460034c9a0db936b6566e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127532"
---
# <a name="navigating-the-user-interface"></a>Navegar na interface de utilizador

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

## <a name="overview"></a>Descrição geral

O formulário do projeto principal é separado em vários separadores. Cada separador representa um nível de detalhe diferente no projeto.

- **Resumo**: fornece uma descrição do projeto e agrega tanto o desempenho do projeto planeado e real.

    ![Separador e campos de Resumo](media/navigation7.png)

- **Tarefas**: fornece os detalhes relativos à estrutura hierárquica do trabalho representada por uma vista de grelha, vista de quadro e um gráfico gantt.

    ![Separador e campos de Tarefa](media/navigation8.png)

- **Equipa**: fornece detalhes sobre os participantes do projeto. O esforço atribuído de cada membro da equipa também é resumido nesta vista.

    ![Separador e campos de Equipa](media/navigation9.png)

- **Atribuições de recursos**: fornece uma vista faseada no tempo do esforço de cada recurso num projeto.

    ![Separador e campos de Atribuições de recursos](media/navigation10.png)

- **Reconciliação de recursos**: fornece uma vista faseada no tempo das diferenças entre as atribuições de cada recurso nomeado e as suas reservas.

    ![Separador e campos de Reconciliação de recursos](media/navigation11.png)

- **Estimativas**: fornece uma vista faseada no tempo das estimativas de vendas e de custo de um projeto.

    ![Separador e campos de Estimativas](media/navigation12.png)

- **Monitorização**: fornece uma vista que mostra o progresso das tarefas na estrutura hierárquica do trabalho em termos de esforço, custo e vendas.

    ![Separador e campos de Monitorização](media/navigation13.png)

- **Vendas**: fornece ligações avançadas às propostas e contratos associados ao projeto.

- **Estimativas de Despesas**: fornece uma grelha que define as despesas do projeto baseadas nas categorias de despesas organizacionais.

    ![Separador e campos de Estimativas de despesas](media/navigation14.png)

## <a name="grid-controls"></a>Controlos da grelha

Segue-se uma breve descrição geral dos controlos típicos encontrados nos vários separadores de planeamento de projetos.

### <a name="refresh"></a>Actualizar

**Atualizar**: obtém os dados mais recentes do servidor se tiverem ocorrido alterações após o carregamento da grelha.

![Botão Atualizar](media/navigation7.png)

### <a name="group-by"></a>Agrupar por

**Agrupar por**: atualiza o agrupamento das linhas na grelha para refletir os recursos, as funções ou as categorias com base nas necessidades do utilizador.

![Botão Agrupar por](media/navigation6.png)

### <a name="previousnext"></a>Anterior/Seguinte

**Anterior**/**Seguinte**: atualize os períodos visíveis nas grelhas faseadas no tempo.

![Botões Anterior e Seguinte](media/navigation2.png)

### <a name="timescale"></a>Horário

**Horário**: alterar a agregação dos dados faseados no tempo entre dias, semanas, meses e anos.

![Botão Horário](media/navigation3.png)

### <a name="expand"></a>Expandir

**Expandir**: tornar a grelha visível em ecrã inteiro para fornecer mais capacidade para ver funções adicionais.

![botão Expandir](media/navigation4.png)

### <a name="time-phase-by"></a>Faseamento no tempo por

**Faseamento no tempo por**: atualizar o agrupamento de linhas na grelha para refletir as estimativas de custos para as estimativas de vendas. Este controlo também se aplica ao script de estimativa e à grelha de monitorização.

![Botão Faseamento no tempo por](media/navigation0.png)

### <a name="add-column"></a>Adicionar coluna

**Adicionar coluna**: permite ao utilizador definir as colunas visíveis na grelha. Só as colunas de configuração inicial podem ser adicionadas às grelhas no formulário **Planeamento de projeto**.

![Botão Adicionar coluna](media/navigation5.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]