---
title: Subsídios diários
description: Este tópico fornece informações sobre as regras de subsídio diário por dia que são utilizadas na gestão de Despesas.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 8d723b49e9556401c364b323cf58eaaf44906275
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128522"
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