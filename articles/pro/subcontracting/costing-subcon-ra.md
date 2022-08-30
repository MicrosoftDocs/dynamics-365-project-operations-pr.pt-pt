---
title: Estimativa de custos de atribuições de recursos subcontratados
description: Este artigo explica como o Microsoft Dynamics 365 Project Operations calcula a estimativa de custos das atribuições de recursos subcontratados.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5a4d0707f8373b5083272eacb7dc1318e82a23ac
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262074"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Estimativa de custos de atribuições de recursos subcontratados

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

As atribuições de tarefas de membros da equipa do projeto subcontratados são custeadas utilizando a lista de preços **Compra** anexada ao subcontrato no registo de membros da equipa relacionada. Isto é diferente de como as atribuições de recursos dos colaboradores são custeados quando as atribuições de tarefas dos recursos dos colaboradores são custeados usando a lista de preços **Custo** que está anexada à unidade de contratação do projeto. 

Para membros da equipa do projeto genéricos subcontratados, as atribuições são custeadas utilizando a configuração de preços baseada em funções na lista de preços anexada ao subcontrato. Os preços de Compra também podem ser configurados especificamente para cada recurso. Estes preços específicos de recursos terão prioridade quando custear atribuições de tarefas de membros da equipa do projeto nomeados forem trabalhadores contratados. 

A prioridade da utilização de preços de compra específicos de funções por oposição a específicos de recursos é impulsionada pela configuração da prioridade da dimensão de preços em **Parâmetros > Dimensões de preços baseadas em montantes**.

Esta funcionalidade de derivar preços dinamicamente com base na configuração da dimensão para os preços de compra dos subcontratantes é semelhante à forma como os custos e as taxas de faturamento são derivados para os colaboradores a tempo inteiro. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Criar tarefas para obter estimativas de custos de recursos subcontratados

As atribuições de tarefas para subcontratantes podem ser criadas de duas formas: 
- Utilizando o separador **Tarefas**.
- Utilizando o separador **Equipa**.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Criar atribuições de recursos utilizando o separador Tarefas
Utilizando a lista **Recursos** no separador **Tarefas** para uma tarefa específica, pode criar uma atribuição de tarefas para um recurso nomeado ou um recurso genérico. Se selecionar um recurso nomeado a partir da lista pendente **Recursos Atribuídos** na tarefa e este recurso for um trabalhador contratado, o recurso nomeado é atribuído à tarefa e um registo de membro da equipa do projeto correspondente é criado com o tipo de trabalhador definido como **Trabalhador Contratado** e **Validade** definida como **Inválida**. Como próximo passo, terá de abrir o registo do membro da equipa do projeto e selecionar um subcontrato e item de subcontrato. Isto atualizará a atribuição de tarefas para ter uma referência ao subcontrato e item de subcontrato e também atualizará o estado do membro da equipa para **Válido**.

Se optar por criar um membro da equipa genérico a partir da lista pendente **Recursos Atribuídos** na tarefa, o diálogo **Criação de membro da equipa genérico** irá permitir-lhe selecionar um subcontrato e item de subcontrato. Quando o recurso genérico for atribuído à tarefa e o registo correspondente do membro da equipa do projeto for criado, irá notar que o registo do membro da equipa do projeto é criado com o tipo de trabalhador definido como **Trabalhador Contratado** e a **Validade** definida como **Válida**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Criar membros da equipa do projeto utilizando o separador Equipa
Utilizando o separador Equipa no projeto, pode criar um membro da equipa genérico ou nomeado. Ao criar o membro da equipa, pode selecionar o subcontrato e o item de subcontrato. Após a criação do membro da equipa, terá de atribuir o membro da equipa a uma tarefa utilizando a lista pendente **Recursos Atribuídos** na tarefa. 

## <a name="updating-estimates"></a>Atualizar estimativas
Depois de ter atribuído membros da equipa do projeto a tarefas, terá de navegar para o separador **Estimativas** no projeto e selecionar **Atualizar preços** para garantir que as taxas de custos das atribuições de recursos de subcontratante sejam atualizadas com base na lista de preços de compra anexada ao subcontrato. As estimativas não são geradas para tarefas não atribuídas no Microsoft Dynamics 365 Project Operations. Como resultado, terá de criar atribuições de tarefas para atribuir preços e custear várias tarefas no seu projeto. 

> [NOTA!] Os membros da equipa do projeto que têm o **Tipo de trabalhador** como **Trabalhador contratado**, mas que não têm um subcontrato são sinalizados como **Inválidos** na grelha **Membros da equipa do projeto**. Se existirem quaisquer membros da equipa do projeto com este estado, abra o registo do membro da equipa do projeto e atualize manualmente os campos de item de subcontrato e subcontrato, de modo a que a estimativa de custos no separador **Estimativas**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
