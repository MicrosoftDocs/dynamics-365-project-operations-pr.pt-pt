---
title: Opções de subcontratação para membros da equipa do projeto
description: Este artigo explica as opções de subcontratação para membros da equipa do projeto no Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5e0955d58365a4ecbe1c053882736f196758816e
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261621"
---
# <a name="subcontracting-options-for-project-team-members"></a>Opções de subcontratação para membros da equipa do projeto

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

No Microsoft Dynamics 365 Project Operations, pode avaliar as opções de subcontratação disponíveis para um ou mais membros da equipa do projeto. As opções de subcontratação disponíveis permitem-lhe:

- Crie um novo subcontrato e/ou crie novos itens num subcontrato existente para os membros da equipa do projeto selecionados. 
- Reserve para um subcontrato e um item de subcontrato já existente. 

Pode escolher entre as opções de subcontratação disponíveis para membros genéricos da equipa do projeto ou escolha entre membros da equipa do projeto que tenham sido dotados de um recurso nomeado que seja um trabalhador contratado. 

Não existem opções de subcontratação disponíveis para o seguinte:

- Membros da equipa do projeto que foram empregados. 
- Membros da equipa do projeto que já estão associados a um subcontrato e item de subcontrato. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Subcontratar um membro da equipa do projeto não contratado

Para rever e escolher entre as opções de subcontratação disponíveis para um membro da equipa do projeto genérico ou não contratado, siga estes passos:

1. Selecione um ou mais registos de membros da equipa do projeto onde o recurso é um recurso genérico.
2. Certifique-se de que nenhum dos registos selecionados do membro da equipa do projeto já está subcontratado. 
3. Selecione **Opções de subcontratação** na subgrelha de membros da equipa do projeto. É aberta a caixa de diálogo **Opções de subcontratação**. 
4. Se selecionou apenas um registo de membro da equipa do projeto no passo 1, estarão disponíveis as seguintes opções:
    - Crie novos itens de subcontrato. 
    - Reserve para um subcontrato existente, se selecionou vários registos de membros da equipa do projeto no passo 1, a única opção disponível é criar um novo item de subcontrato.
5. A opção de reserva para um item de subcontrato existente permite-lhe selecionar subcontrato e um item de subcontrato que pretende reservar. Ao selecionar um item de subcontrato à capacidade de reserva, deve certificar-se de que o item de subcontrato selecionado é de tempo e que a função requerida no membro da equipa do projeto corresponde à função adquirida no item de subcontrato.
6. Quando selecionar para criar novos itens de subcontrato para os membros da equipa do projeto, o sistema permitir-lhe-á selecionar o subcontrato em que pretende criar estas linhas. O subcontrato que seleciona para criar novos itens deve estar no estado de **Rascunho**. Com esta opção de criar novos itens de subcontrato para os membros selecionados da equipa do projeto, o sistema criará um item de subcontrato para cada membro da equipa do projeto. A função, horas e datas serão copiados do membro da equipa do projeto para cada item de subcontrato que for criado. 
7. Quando um membro genérico da equipa estiver associado a um subcontrato e item de subcontrato, o campo **Tipo de trabalhador** na linha de membro genérica da equipa será atualizado para **Trabalhador Contratado** e o valor de **Validade do Subcontrato** será definido como **Válida**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Subcontratar um membro da equipa do projeto contratado

Tal como os membros genéricos ou não contratados da equipa, também pode ver opções de subcontratação para um membro da equipa do projeto contratado, desde que o membro da equipa do pessoal seja um trabalhador contratado. Para rever e escolher entre as opções de subcontratação disponíveis para um membro da equipa do projeto contratado ou nomeado, siga estes passos:

1. Selecione um ou mais registos de membros da equipa do projeto onde o recurso é um trabalhador contratado nomeado.
2. Certifique-se de que nenhum dos registos do membro da equipa do projeto selecionados já está subcontratado. 
3. Selecione **Opções de subcontratação** na subgrelha de membros da equipa do projeto. É aberta a caixa de diálogo **Opções de subcontratação**. 
4. Se selecionou apenas um registo de membro da equipa do projeto no passo 1, estarão disponíveis as seguintes opções:
      - Crie novos itens de subcontrato.
      - Reserve para um subcontrato existente.
  Se selecionou vários registos de membros da equipa do projeto no passo 1, a única opção disponível é criar um novo item de subcontrato.
5. A opção de reserva para um item de subcontrato existente permite-lhe selecionar subcontrato e um item de subcontrato que pretende reservar. Ao selecionar um item de subcontrato para a capacidade de reserva, deve assegurar o seguinte:
      - O item de subcontrato selecionada é de tempo. 
      - A função requerida no membro da equipa do projeto corresponde à função que foi adquirida no item de subcontrato. 
      - O vendedor a que o trabalhador contratado está associado é o mesmo que o vendedor no subcontrato.
6. Quando selecionar para criar novos itens de subcontrato para os membros da equipa do projeto, o sistema permitir-lhe-á selecionar o subcontrato em que pretende criar estas linhas. Com esta opção, deve certificar-se de que o vendedor a que o trabalhador contratado pertence é o mesmo que o vendedor no subcontrato. 
7. O subcontrato que seleciona para criar novos itens deve estar no estado de **Rascunho**. Com esta opção de criar novos itens de subcontrato para os membros selecionados da equipa do projeto, o sistema criará um item de subcontrato para cada membro da equipa do projeto. A função, horas e datas serão copiados do membro da equipa do projeto para cada item de subcontrato que for criado.  
8. Quando um membro da equipa nomeado estiver associado a um subcontrato e item de subcontrato, o campo **Tipo de trabalhador** na linha de membro da equipa nomeado será atualizado para **Trabalhador Contratado** e o valor de **Validade do Subcontrato** será definido como **Válida**.

## <a name="re-costing-subcontractor-assignments"></a>Voltar a custear atribuições de subcontratantes

Quando um membro da equipa do projeto (genérico ou nomeado) estiver ligado a itens de subcontrato utilizando o diálogo **Opções de subcontratação**, qualquer atribuição a tarefas que o membro da equipa tenha voltará a ser custeada com base na lista de preços de compra anexada ao subcontrato. No separador **Estimativas** na página **Detalhes do Projeto**, selecione o botão **Atualizar preços** para ver os preços e/ou custos atualizados resultantes da decisão de subcontratar.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
