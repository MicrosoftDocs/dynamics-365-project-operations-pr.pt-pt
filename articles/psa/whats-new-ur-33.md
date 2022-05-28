---
title: Novidades ou alterações na Versão da Atualização 33 do Project Service Automation, V3
description: Este tópico lista as funcionalidades e correções disponíveis no Project Service Automation V3, Versão da Atualização 33, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 063290526c25e7073137fc88408be6a61d2d20ac
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601492"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a>Novidades ou alterações na Versão da Atualização 33 do Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente para a aplicação Microsoft Dynamics 365 Project Service Automation. Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização. É compatível com o Dynamics 365, versão 9.x. Para atualizar para esta versão, visite a página de soluções online do Centro de Administração do Dynamics 365 e instale a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este tópico lista as funcionalidades e correções novas ou alteradas para o Project Service Automation V3, Versão da Atualização 33. Esta versão tem o número de compilação V3.10.54.98 e está em disponibilidade geral através de uma auto-atualização em julho de 2021.

## <a name="update-release-33"></a>Versão da Atualização 33

### <a name="bug-fixes"></a>Correções de erros

**Tempo e Despesa**

Foram corrigidos os seguintes problemas:

- Dois campos bloqueados, **msdyn_description** e **msdyn_externaldescription**, são editáveis após a submissão.
- Uma mensagem de erro ocorre se for criada uma despesa que não esteja relacionada com um projeto.
- Quando uma entrada de hora é criada, a função de recurso assume por omissão uma função inativa.
- As linhas do diário associadas a uma despesa recuperada e eliminada não são eliminadas.
- No **Formulário de Criação Rápida de Entrada de Hora**, atualize a vista **Lista de Tarefas do Projeto** para alterar a data apresentada por predefinição para a data de início da tarefa.
- Quando cria uma entrada de hora a partir do separador **Relacionada** do recurso reservável, a entrada de hora é criada incorretamente para o utilizador com sessão iniciada em vez do recurso reservável principal.
- São adicionados novos campos à caixa de diálogo **MDD de aprovação em massa**.

**Planeamento de projeto**

Foram corrigidos os seguintes problemas:
- Desempenho lento de criação de projetos quando são aplicados modelos de horas de trabalho do projeto com calendários complexos.
- Quando a data de início é posterior à data de fim, é apresentado um erro no modelo do projeto de texto devido a diferenças no componente de tempo de cada campo.

**Gestão de recursos**

Foram corrigidos os seguintes problemas:
- Um parâmetro incorreto é utilizado na consulta de utilização do recursos e o XML leva a resultados incorretos do filtro na grelha **Utilização do Recurso**.
- A confirmação **Expandir reservas** apresenta uma data de fim incorreta para as reservas.

**Vendas**

Foram corrigidos os seguintes problemas:
- É apresentada uma mensagem de erro se um preço de categoria for criado com valores em falta.
- É apresentada uma mensagem de erro se um marco do item de contrato for criado sem uma linha de encomenda.
