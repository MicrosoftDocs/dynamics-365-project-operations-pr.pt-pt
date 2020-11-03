---
title: Definir calendários de projetos
description: Este tópico fornece informações sobre a utilização de um calendário de projeto para monitorizar o cronograma do projeto.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 774399f2c02d8434c9c042c3a9f995792893bfce
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082578"
---
# <a name="define-project-calendars"></a>Definir calendários de projetos

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Para criar uma agenda de projeto, cria um modelo de calendário do projeto que define o número de horas de trabalho por dia e todos os encerramentos de companhia. Para criar um modelo de calendário do projeto, associe um modelo de trabalho ao campo **Modelo de calendário** do projeto. Siga estes passos para criar um modelo de trabalho.

1. No painel de navegação esquerdo, selecione **Recursos**. 
2. Na página da lista de **Recursos** , abra o registo de utilizador e selecione **Mostrar Horas de Trabalho**.

  > [!NOTE]
  > Certifique-se de que permite pop-ups na página do browser. Isto permite-lhe ver as horas de trabalho definidas para o recurso.
  
3. No separador **Vista Mensal** , selecione **Configurar**. É apresentada uma lista de três opções: 

  - Nova Agenda Semanal
  - Agenda de Trabalho Para Um Dia
  - Licença

4. Selecione **Nova Agenda Semanal** e, em seguida, defina as opções para esta agenda de recursos. É possível definir uma agenda semanal periódica, os parâmetros de hora diária, os encerramentos de companhia e muito mais.
5. Defina o intervalo de datas, selecione **Guardar** e selecione **Fechar**. 
6. Volte à página da lista de **Recursos** e selecione o recurso para o qual define as horas de trabalho. 
7. Selecione **Definir Calendário Como** para definir o modelo de trabalho. 
8. Na caixa de diálogo **Modelo de Trabalho** , introduza um nome para o modelo de trabalho e selecione **Aplicar**. 

Agora, pode associar o modelo de trabalho a um modelo de calendário do projeto.
