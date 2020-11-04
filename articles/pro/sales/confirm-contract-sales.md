---
title: Confirmar um contrato de projeto
description: Este tópico fornece informação sobre como confirmar um contrato no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: babce9c64098a9c87072786d914d2340251a8986
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082524"
---
# <a name="confirm-a-project-contract"></a>Confirmar um contrato de projeto

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Um contrato de projeto no Dynamics 365 Project Operations pode estar ativo com uma razão de **Confirmado** ou fechado com uma razão de **Perdido**. Quando confirma um contrato de projeto, o estado atualiza-se de **Rascunho** para **Ativo** e a razão do estado é **Confirmado**. Um contrato ativo ou fechado não pode ser editado ou reaberto. 

### <a name="financial-impact-of-confirming-a-project-contract"></a>Impacto financeiro da confirmação de um contrato de projeto

Depois de um contrato de projeto ser confirmado, a aplicação recalcula os custos ao inverter os valores reais do custo mais antigos e criar novos custos reais. Os novos valores reais de custos são processados com base no método de faturação do item de contrato do projeto associado. Se os valores reais de custo fizerem referência um item de contrato de Tempo e Material, a aplicação recria automaticamente os valores reais de vendas não faturados correspondentes. Se os valores reais de custo fizerem referência a um item de contrato de Preço Fixo, a aplicação para de reprocessar os valores reais do custo.

Os limites A Não Exceder, a configuração de capacidade da faturação e os preços e custos sobre de valores reais é avaliado e, em seguida, atualizado como parte do processo de confirmação.

## <a name="close-a-project-contract-as-lost"></a>Fechar um contrato de projeto como perdido

Quando fecha um contrato de projeto como perdido, o estado do contrato é atualizado para **Fechado** e a razão do estado é **Perdido**. O contrato do projeto torna-se apenas de leitura. Um diálogo de confirmação é fornecido antes das alterações estarem completas porque não é possível reabrir um contrato de projeto fechado.

Se o contrato de projeto que está fechado como referências perdidas um projeto nas suas linhas, esse projeto também é marcado como fechado. Quaisquer reservas de recursos a partir desse dia são canceladas. Quaisquer valores reais de vendas não faturados no contrato do projeto que ainda não estejam numa fatura, serão invertidos.

> [!NOTE]
> No Dynamics 365 Project Operations, fechar um contrato de projeto como perdido não terá impacto nesse estado da oportunidade associada. A oportunidade permanecerá aberta e deve ser fechada manualmente.