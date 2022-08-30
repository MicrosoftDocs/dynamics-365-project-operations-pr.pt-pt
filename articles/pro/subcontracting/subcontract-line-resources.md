---
title: Recursos do item de subcontrato
description: Este artigo explica como especificar os recursos dedicados fornecidos pelo fornecedor para uma item de subcontrato específico para tempo.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d440201fde26e835b407db0b8ee1de8d663311a0
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261479"
---
# <a name="subcontract-line-resources"></a>Recursos do item de subcontrato

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

No Dynamics 365 Project Operations, um fornecedor pode especificar os recursos que serão utilizados para fornecer a capacidade de recursos que está a ser comprada no item de subcontrato de tempo.

## <a name="create-subcontract-line-resources"></a>Criar recursos do item de subcontrato

Para criar recursos do item de subcontrato, execute os seguintes passos.

1. No painel de navegação, selecione **Subcontratos** e abra o subcontrato com o qual pretende trabalhar.
2. Abra o item de subcontrato de tempo em que pretende especificar os recursos do fornecedor.
3. No separador **Recursos do Item de Subcontrato**, na subgrelha, selecione **+ Novo Recurso do Item de Subcontrato**.
4. Na página **Novo Recurso de Item de Subcontrato**, introduza as informações necessárias e, em seguida, selecione **Guardar e Fechar**.

A tabela seguinte explica os campos no recurso do item de subcontrato.

| Campo | Descrição | Impacto funcional |
| ----- | ----------- | ----------------- |
| Recurso Reservável | Selecione um recurso reservável do tipo **Trabalhador contratado** que pretenda utilizar como recurso no item de subcontrato.| Se não criou um recurso reservável para o trabalhador contratado, deixe este campo vazio. Será criado um recurso reservável quando guardar o registo.  |
| Contacto | Pode criar o recurso de item de subcontrato a partir de um contacto existente. Utilize a pesquisa para ver a lista de contactos ativos no sistema. Selecione um contacto para o fornecedor deste subcontrato. Se o contacto selecionado não for um contacto válido para o fornecedor no subcontrato, o registo do recurso de item de subcontrato não será guardado.| Se não existir um recurso reservável para o contacto selecionado, o sistema cria um recurso reservável para o contacto selecionado antes de criar o recurso do item de subcontrato. |
| Utilizador | Pode criar um recurso de item de subcontrato selecionando um utilizador ativo. Utilize a pesquisa para ver a lista de utilizadores ativos no sistema.| Se não existir um recurso reservável para o utilizador selecionado, o sistema cria um recurso reservável para o utilizador selecionado antes da criação do recurso do item de subcontrato. |
| Data de Início | A data em que a atribuição do trabalhador subcontratado começará.| Se este recurso for reservado para um período anterior a este intervalo de datas, ocorrerá um aviso. |
| Data de Fim | A data em que a atribuição do trabalhador subcontratado terminará.| Se este recurso for reservado para um período posterior a este intervalo de datas, ocorrerá um aviso. |
| Esforço | O número total de horas de esforço que o trabalhador contratado gastará neste item de subcontrato.| Se este recurso for reservado para além do esforço atribuído neste subcontrato, ocorrerá um aviso. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
