---
title: Recursos do item de subcontrato
description: Este tópico explica como especificar os recursos dedicados do fornecedor para um item de subcontrato específico de tempo.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 48440f82170bde7f0a0a45f8f9849d688b232949
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323385"
---
# <a name="subcontract-line-resources"></a>Recursos do item de subcontrato

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

No Dynamics 365 Project Operations, um fornecedor pode especificar os recursos que serão utilizados para fornecer a capacidade de recursos que está a ser comprada no item de subcontrato de tempo.

## <a name="create-subcontract-line-resources"></a>Criar recursos do item de subcontrato

Para criar recursos do item de subcontrato, execute os seguintes passos.

1. No painel de navegação, selecione **Subcontratos** e abra o subcontrato com o qual pretende trabalhar.
2. Abra o item de subcontrato de tempo em que pretende especificar os recursos do fornecedor.
3. No separador **Recursos do Item de Subcontrato**, na subgrelha, selecione **+ Novo Recurso do Item de Subcontrato**.
4. Na página **Novo Marco do Item de Subcontrato**, introduza as informações necessárias e selecione **Guardar e Fechar**.

A tabela seguinte explica os campos no recurso do item de subcontrato.

| Campo |  Descrição |
| ----- | ------------ |
| Recurso Reservável | Selecione um recurso reservável do tipo "Trabalhador contratado" que pretenda utilizar como recurso no item de subcontrato. Se ainda não criou um recurso reservável para o trabalhador contratado, deixe este campo vazio. Um recurso reservável é criado quando guarda o registo.  |
| Contacto | Se o campo **Recurso Reservável** estiver vazio, pode criar o seu recurso do item de subcontrato a partir de um contacto existente. Utilize a pesquisa para ver a lista de contactos ativos no sistema. Selecione um contacto para o fornecedor deste subcontrato. O contacto que selecionar é validado quando guardar o registo. Se o contacto selecionado não for um contacto válido, o registo não será guardado. Se não existir um recurso reservável para o contacto selecionado, o sistema cria um recurso reservável para o contacto selecionado antes de criar o recurso do item de subcontrato. |
| Utilizador | Se o campo **Recurso Reservável** estiver vazio, pode criar um recurso do item de subcontrato selecionando um utilizador ativo. Utilize a pesquisa para ver a lista de utilizadores ativos no sistema. Se não existir um recurso reservável para o utilizador selecionado, o sistema cria um recurso reservável para o utilizador selecionado antes da criação do recurso do item de subcontrato. |
| Data de Início | A data em que a atribuição do trabalhador subcontratado começará. Se este recurso for reservado para um período anterior a este intervalo de datas, ocorrerá um aviso. |
| Data de Fim | A data em que a atribuição do trabalhador subcontratado terminará. Se este recurso for reservado para um período posterior a este intervalo de datas, ocorrerá um aviso. |
| Esforço | O número total de horas de esforço que o trabalhador subcontratado dedicará a este item de subcontrato. Se este recurso for reservado para além do esforço a que está atribuído neste subcontrato, ocorrerá um aviso. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
