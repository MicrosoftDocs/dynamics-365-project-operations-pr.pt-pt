---
title: Configurar os subcontratantes como recursos reserváveis
description: Este artigo explica como configurar e manter recursos de subcontratante que são criados a partir de utilizadores e contactos no sistema, para que possam ser associados a subcontratos no Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 727508c41c190c3703e9cd1420066fa0e551f147
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522716"
---
# <a name="set-up-subcontractors-as-bookable-resources"></a>Configurar os subcontratantes como recursos reserváveis

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Siga estes passos para configurar os subcontratantes como recursos reserváveis no Microsoft Dynamics 365 Project Operations.

1. Aceda a **Projeto** \>**Recursos** e selecione **Novo**.
2. Na página **Novo Recurso Reservável**, no campo **Tipo de Recurso**, selecione uma das seguintes opções:

    - **Utilizador** – Selecione este tipo de recurso se o subcontratado tiver de aceder ao Project Operations para introduzir tempo ou despesas. Se selecionar **Utilizador**, o subcontratado necessita de uma licença válida para aceder ao sistema.
    - **Contacto** ou **Conta** – Selecione um destes tipos de recursos se o subcontratado não necessitar de aceder ao Project Operations, mas deve estar disponível para atribuições de tarefas ou reservas em projetos. Nenhum destes tipos de recursos fornece acesso ao sistema. Selecione **Conta** para representar a empresa do fornecedor como recurso reservável. Selecione **Contacto** para representar os colaboradores individuais do fornecedor.

3. Dependendo do tipo de recurso selecionado, é-lhe solicitado que selecione o registo de utilizador, conta ou contacto correspondente.
4. No campo **Tipo de Trabalhador**, selecione o "Trabalhador contratado" para configurar o subcontratante como recurso reservável.

    > [!NOTE]
    > Se deixar o campo **Tipo de Trabalhador** em branco, o recurso reservável será considerado como colaborador.

5. Se tiver selecionado o **Trabalhador contratado** como o tipo de trabalhador, selecione o fornecedor para o qual o recurso trabalha.
6. Selecione o fuso horário do recurso e, em seguida, selecione **Guardar**. Para atribuir um modelo de horas de trabalho ao recurso reservável, pode selecionar **Definir calendário** na página da lista de **Recursos Reserváveis**.

Para ser associado a um item de subcontrato, um recurso reservável tem de satisfazer estas condições:

- O recurso reservável deve ser um trabalhador contratado.
- Um recurso reservável do tipo de recurso **Contacto** deve ser associado à conta do fornecedor como contacto. Um recurso reservável do tipo de recurso **Utilizador** não tem de ser associado à conta do fornecedor como contacto.
- O valor do campo **Fornecedor** para o recurso reservável deve corresponder ao valor do campo **Fornecedor** para o subcontrato.

## <a name="update-the-type-of-worker-and-vendor-mapping-for-bookable-resources"></a>Atualizar o tipo de mapeamento de trabalhador e fornecedor para recursos reserváveis

O campo **Tipo de trabalhador** para um recurso reservável determina se o recurso reservável é um trabalhador contratado ou um colaborador. O campo **Fornecedor** define a conta do fornecedor a que o recurso reservável está associado. Ao associar um recurso reservável a um fornecedor como contacto, indica que o contacto é um colaborador da empresa fornecedora.

Se os campos **Tipo de Trabalhador** e **Fornecedor** para um recurso reservável forem alterados, as alterações afetam quaisquer validações futuras em novos registos que o recurso reservável cria, como entradas de tempo. No entanto, as alterações não invalidam os registos existentes.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]