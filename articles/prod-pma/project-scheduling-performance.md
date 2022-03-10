---
title: Desempenho do agendamento de recursos do projeto
description: Este tópico fornece informações sobre como melhorar o desempenho do agendamento de recursos para um grande número de projetos.
author: Yowelle
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 9dc638a7b2d8e0db45b5acfa5cc9512f356f8b2635028748a1e2c3230605c154
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007295"
---
# <a name="project-resource-scheduling-performance"></a>Desempenho do agendamento de recursos do projeto

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


Os problemas de desempenho relacionadas com o agendamento de recursos podem ocorrer quando o número de projetos chega aos milhares. Para melhorar o desempenho do agendamento de recursos, existe uma funcionalidade que permite aos utilizadores reduzir o tempo que demora a iniciar o formulário de disponibilidade de recursos. Especificamente, isto remove o processo de sincronização de roll-up de capacidade de recursos e utiliza a tabela **ResProjectResource** para acelerar a procura de recursos. Note que a tabela **ResRollup** deixará de ser utilizada.

> [!IMPORTANT]
> Se houver uma dependência do processo de sincronização da capacidade de recursos ou da tabela **ResProjectResource**, não utilize esta funcionalidade.

## <a name="enable-resource-scheduling-performance-enhancement"></a>Ativar a melhoria do desempenho do agendamento de recursos
Para ativar o melhoramento do desempenho do agendamento de recursos, complete os seguintes passos.

1. Vá a **Gestão de funcionalidades** > **Todas** e, na lista de funcionalidades, localize **Ativar a funcionalidade de melhoria do desempenho de agendamento de recursos do projeto**.
2. Selecione **Ativar agora**.

> [!NOTE]
> Se não conseguir encontrar a funcionalidade na lista, selecione **Verificar se há atualizações** para atualizar a lista.

3. Atualize o seu browser e, em seguida, vá para **Gestão de projetos e contabilística** > **Periódico** > **Recursos do projeto** > **Sincronizar a capacidade dos calendários de recursos em todas as empresas**.
4. Defina **Remover registos de capacidade existentes** como **Sim** para remover dados anteriores. Se pretender gerar dados incrementais, defina-o para **Não**.
5. No campo **Código de período**, selecione o período em que os dados devem ser gerados. Se selecionar um código de período, não é necessário definir uma data de início e de fim.
6. Se deixar o campo **Código de período** em branco, selecione datas específicas de início e de fim para gerar dados.
7. Selecione **OK**.

 > [!NOTE]
 > Isto irá distribuir dados gerais para a tabela **ResCalendarCapacity** em todas as empresas do seu ambiente, pelo que a tarefa de lote só precisa de ser executado numa entidade legal. Os dados nesta tarefa de lote são necessários para calcular a capacidade de recursos através do calendário associado.

8. Vá à **Gestão de projetos e contabilística** > **Periódico** > **Recursos do projeto** > **Preencher recursos do projeto em todas as empresas** e, em seguida, selecione **OK**. Este é o script de atualização de versão dos dados para dados gerais nas tabelas **ResProjectResource**, **ResCalendarDateTimeRange** e **ResEffectiveDateTimeRange**. Os valores para o campo **PSAPRojSchedRole.RootActivity** também são atualizados. Se isto não for executado, receberá um aviso quando tentar executar operações de agendamento de recursos.
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a>Desativar a melhoria do desempenho do agendamento de recursos

1. Vá a **Gestão de funcionalidades** > **Todas** e procure por **Ativar a funcionalidade de melhoria do desempenho de agendamento de recursos do projeto**.
2. Selecione a funcionalidade e, em seguida, selecione o botão **Desativar**.
3. Atualize o seu browser.
4. Aceda a **Gestão de projetos e contabilística** > **Periódico** > **Sincronização da capacidade** > **Sincronizar roll-ups de capacidade dos recursos**.
5. Na página **Sincronização de roll-up de capacidade**, defina **Remover registos de capacidade existentes** como **Sim** para remover dados anteriores. Se pretender gerar dados incrementais, defina-o para **Não**.
6. No campo **Código de período**, selecione o período em que os dados devem ser gerados. Se selecionar um código de período, não é necessário definir uma data de início e de fim.
7. Se deixar o campo **Código de período** em branco, selecione datas específicas de início e de fim para gerar dados.
8. Selecione **OK**.

> [!NOTE]
> Isto irá distribuir dados gerais para a tabela **ResRollup** em todas as empresas do seu ambiente, pelo que a tarefa de lote só precisa de ser executado numa entidade legal. Esta tarefa de lote é necessária para todas as vistas **Disponibilidade de Recursos**. Se esta tarefa de lote não for executada, os dados **ResRollup** serão gerados no momento, o que pode levar tempo.


[!INCLUDE[footer-include](../includes/footer-banner.md)]