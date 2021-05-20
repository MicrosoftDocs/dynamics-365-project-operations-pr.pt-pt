---
title: Modelo de segurança
description: Este tópico fornece informações sobre o modelo de segurança no Dynamics 365 Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 8acaa86dec8ebca8f9850877d345e30be3e3a919
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951223"
---
# <a name="security-model"></a>Modelo de Segurança

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

O Microsoft Dynamics 365 Project Operations contém um modelo de segurança exclusivo que permite um modelo de segurança empresarial baseado em funções que colabora com Grupos do Microsoft Office. 


## <a name="security-roles"></a>Funções de segurança
As capacidades front-end do Project Operations incluem as seguintes funções:

| Função                          | Descrição                                                                                                                                                                 | Scope |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| Gestor de práticas              | Suporta relatórios entre projetos.                                                                                                            | Unidade de negócio              |
| Aprovador do projeto              | Aprova tempo e despesas para um projeto (Project Service)                                                                                                                              | Unidade de negócio |
| Administrador de faturação do projeto | Cria a proposta de fatura.                                                                                                                                                 | Unidade de negócio |
| Gestor de projeto               | Cria o plano de projeto e solicita recursos.                                                                                                                              | Unidade de negócio |
| Recurso de Projeto              | Membros da equipa que podem ser reservados e reportar o tempo.                                                                                                          | Unidade de negócio|
| Gestor de recursos              | Todas as funções de gestão de recursos, como satisfazer os pedidos de recursos e reservas, são separadas para suportar uma configuração híbrida de Gestor de projeto + Gestor de recursos e uma única e centralizada função de Gestor de recursos. | Unidade de negócio |


O Microsoft Project for the Web inclui as seguintes funções:

| Função           | Descrição                                                                                                        | Scope  |
|----------------|--------------------------------------------------------------------------------------------------------------------|--------|
| Utilizador do projeto   | Utilizador colaborativo do Projeto que é capaz de criar os seus próprios projetos e ver quaisquer projetos partilhados com ele. | Utilizador   |
| Sistema de projetos | Função usada para o contexto da aplicação. Os clientes não devem utilizar esta função do sistema.                                    | Global |

## <a name="security-enforcement"></a>Aplicação da segurança
As ações que são executadas a nível do projeto são executadas no contexto do utilizador com sessão iniciada. Isto significa que, para criar, abrir ou eliminar um projeto, o utilizador tem de ter acesso disponível no CDS. O acesso no CDS pode ser concedido através de qualquer um dos mecanismos possíveis incluídos na plataforma. Por exemplo, um utilizador com um âmbito mais alargado pode aceder ao projeto ou se tiver sido executada uma ação de partilha de projeto explícita que conceda acesso ao utilizador.

É importante ter isto em consideração ao criar projetos no Project Operations.

## <a name="modern-group-collaboration-with-project-operations"></a>Colaboração em grupo moderna com Project Operations
O Project para a Web e o Project Operations suportam grupos modernos para a colaboração. Os utilizadores adicionados ao projeto através de um grupo são capazes de editar o plano do projeto.

O Project para a Web adiciona utilizadores ao grupo automaticamente após a atribuição.

Os grupos permitem trabalhar de forma colaborativa nas permissões do projeto e nos artefactos de colaboração de suporte. O diagrama seguinte representa os eventos e alterações de estado que ocorrem durante o processo de atribuição de grupo.

O Project Operations não cria um grupo através de uma ação implícita e só o faz através da ação explícita de premir nos grupos.

A pesquisa de membros do grupo na caixa de diálogo **Gestão de grupos** está limitada àqueles que estão definidos como parte do grupo de segurança do ambiente. Para mais informações, consulte [Controlar o acesso de utilizadores a ambientes: grupos de segurança e licenças](/power-platform/admin/control-user-access)

![Modo de grupo](./media/groupsmode.png)

1. O Projeto é criado e é propriedade do Utilizador que o cria.
2. O proprietário do Projeto é atualizado para a equipa.
3. A Equipa proprietária é mapeada para o Grupo do Office especificado ou criado.
4. O proprietário original do Projeto é adicionado ao Grupo do Office.

## <a name="deployment-recommendation"></a>Recomendações de implementação
À medida que o modelo de colaboração do grupo do Office evolui, a funcionalidade será adicionada para proporcionar um controlo mais detalhado ao longo do tempo. Os clientes que implementam atualmente o Project Operations são encorajados a concentrarem-se num modelo de segurança tradicional do Microsoft Dynamics 365.

Para mais informações, consulte [Segurança no Common Data Service](/power-platform/admin/wp-security).

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a>Segurança do Microsoft Dynamics 365 Finance e Project Operations
O Project Operations inclui as seguintes funções:

- Gestor de projeto
- Gestão contabilística do projeto

Para mais informações sobre segurança no Finance, consulte [Acesso baseado na segurança](/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).




[!INCLUDE[footer-include](../includes/footer-banner.md)]