---
title: Subsídios diários
description: Este tópico fornece informações sobre as regras de subsídio diário por dia que são utilizadas na gestão de Despesas.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: e537d6c6112eb4baf38229e3e40897eacdf21983
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578308"
---
# <a name="per-diems"></a>Subsídios diários

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_


Um subsídio diário é um subsídio que é pago a um trabalhador que viaja em trabalho. Na Gestão de despesas, pode criar regras de subsídio diário para várias situações de viagem. As tarifas de subsídio diário podem basear-se na época do ano, na localização da viagem ou em ambas. Ao criar uma regra de subsídio diário, pode especificar que uma percentagem da tarifa do subsídio diário será retida se um trabalhador receber refeições ou serviços gratuitos. Também pode definir um número mínimo e máximo de horas para as quais a tarifa do subsídio por dia pode aplicar-se à viagem de um trabalhador.

## <a name="configuration"></a>Configuração 

1. Para adicionar localizações do subsídio por dia, vá para **Configurar** > **Cálculos e códigos** > **Localizações do subsídio diário**.
2. Para cada uma das localizações acima adicionadas, selecione uma tarifa e moeda do subsídio por dia que sejam válidas entre uma data de início e fim específicas para despesas de hotel e refeições, entre outras. As tarifas e a moeda do subsídio por dia são configuradas em **Configurar** > **Cálculos e códigos** > **Subsídios por dia**.
3. Na página **Localizações do subsídio por dia**, configure os níveis de tarifas de subsídio diário. Os níveis de tarifas do subsídio diário permitem definir a divisão percentual de um subsídio diário para despesas de hotel e refeições, entre outras. 
4. Para especificar a redução percentual de refeição para pequeno-almoço, almoço ou jantar, atualize os campos na página **Parâmetros de gestão de despesas** no separador **Subsídio diário**. 
    
## <a name="submit-expenses-using-per-diem"></a>Submeter despesas através do subsídio diário
Para submeter despesas através do subsídio diário, utilize a categoria de despesa **Subsídio diário** quando criar um relatório de despesas. Introduza a **Data de início do subsídio diário**, **Data de fim do subsídio diário** e a **Localização do subsídio diário**. O montante será calculado com base nas tarifas do subsídio diário para a localização selecionada. A redução de refeições será calculada com base nos níveis de tarifas do subsídio diário.


[!INCLUDE[footer-include](../includes/footer-banner.md)]