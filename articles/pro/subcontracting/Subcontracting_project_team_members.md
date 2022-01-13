---
title: Subcontratar membros da equipa do projeto
description: Este tópico explica como subcontratar membros da equipa do projeto no Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 846de9afab5bf9ebc13670abd6ce735801796f0e
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902922"
---
# <a name="subcontracting-project-team-members"></a>Subcontratar membros da equipa do projeto

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

No Microsoft Dynamics 365 Project Operations, pode optar por subcontratar membros da equipa do projeto com ou sem contrato.

- Os membros da equipa do projeto sem contrato têm um recurso genérico atribuído.
- Os membros da equipa contratados têm um recurso nomeado.

Quando liga um membro da equipa do projeto a um item de subcontrato, quaisquer atribuições às tarefas que o membro da equipa tem voltarão a ser custeadas com base na lista de preços de compra anexada ao subcontrato.  No separador **Estimativas** na página **Detalhes do Projeto**, selecione o botão **Atualizar preços** para ver os preços e/ou custos atualizados resultantes da decisão de subcontratar. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Subcontratar um membro da equipa do projeto não contratado
A página **Detalhes do Membro da Equipa** tem campos de subcontrato e de item de subcontrato que permitem a um gestor de projeto expressar como gostaria de retirar a capacidade necessária de um subcontrato. Para subcontratar um membro da equipa do projeto como recurso genérico, siga estes passos:

1.  Escolha um subcontrato na página **Detalhe do membro da equipa**.

2.  Só pode selecionar subcontratos com o estado **Rascunho** ou **Confirmado**. Os subcontratos **Fechados** ou **Cancelados** não podem ser selecionados. 

3.  O campo **Item de subcontrato** torna-se visível depois de selecionar um subcontrato.

4.  No campo **Item de subcontrato**, só é possível selecionar itens de subcontrato que sejam de tempo. Não é possível selecionar itens de subcontrato para despesas ou material.

5.  A função para o registo de membro da equipa do projeto tem de corresponder à função no item de subcontrato. Isto garante que o tempo para a função que está a ser estimado no projeto é a mesma função que é comprada no item de subcontrato. 

Quando um membro genérico da equipa estiver associado a um subcontrato e item de subcontrato, o campo **Tipo de trabalhador** na linha de membro genérica da equipa será atualizado para **Trabalhador Contratado** e a **Validade do Subcontrato** será definido como **Válida**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Subcontratar um membro da equipa do projeto contratado
Tal como os membros da equipa genéricos ou sem contrato, a capacidade do membro da equipa contratado requerido num projeto também pode ser associada a um subcontrato. Para subcontratar um membro da equipa do projeto nomeado, siga estes passos:

1.  Certifique-se de que o recurso nomeado é configurado como um tipo de trabalhador contratado de recurso reservável. Além disso, certifique-se de que o campo **Fornecedor** no recurso reservável corresponde ao fornecedor no subcontrato que está a selecionar. 

2.  Só pode selecionar subcontratos no estado **Rascunho** ou **Confirmado**. Os subcontratos **Fechados** ou **Cancelados** não podem ser selecionados. 

3.  O campo **Item de subcontrato** torna-se visível depois de selecionar um subcontrato.

4.  No campo **Item de subcontrato**, só é possível selecionar itens de subcontrato que sejam de tempo. Não é possível selecionar itens de subcontrato para despesas ou material.

5.  A função para o registo de membro da equipa do projeto tem de corresponder à função no item de subcontrato. Isto garante que o tempo para a função que está a ser estimado no projeto é a mesma função que é comprada no item de subcontrato. 

Os membros da equipa do projeto nomeados que forem criados como um tipo de trabalhador contratado de **Recurso reservável** serão apresentados com um estado de validade de subcontrato de **Não válido** se não estiverem ligados a um subcontrato. Quando um membro da equipa do projeto nomeado estiver associado a um subcontrato e item de subcontrato, o campo **Tipo de trabalhador** na linha de membro da equipa irá atualizar para **Trabalhador Contratado** e a **Validade do Subcontrato** será definido como **Válida**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]