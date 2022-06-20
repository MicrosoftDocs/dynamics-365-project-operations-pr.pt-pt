---
title: Configurar recursos do projeto
description: Este artigo fornece informações sobre a configuração ou o pedido de recursos de projeto.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a4e6fe829d6b39aed9eb6aaea42f245fc997593
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933782"
---
# <a name="set-up-project-resources"></a>Configurar recursos do projeto

[!include [banner](../includes/banner.md)]

Tem de configurar um calendário e associá-lo a um empregado ou a um trabalhador. O calendário é utilizado para agendar o projeto e o tempo de trabalho dos recursos que estão reservados para o projeto. Durante a configuração do calendário, os gestores de projetos podem nivelar os recursos como parte da otimização dos recursos. Baseado na agenda do calendário, podem ser colocadas restrições nos recursos. Pode configurar um calendário na página **Calendários**.

Quando configura um trabalhador como um recurso do projeto, pode selecionar entre os trabalhadores que trabalham na empresa para a qual está a configurar recursos. Em alternativa, poderá selecionar trabalhadores de outras empresas na sua organização. Estes trabalhadores são conhecidos como recursos entre empresas.

Os seguintes procedimentos explicam como configurar um trabalhador como recurso de projeto na sua empresa e como configurar um recurso de projeto entre empresas.

## <a name="set-up-a-worker-as-a-project-resource"></a>Configurar um trabalhador como recurso do projeto

1. Na página **Trabalhadores**, na lista **Trabalhadores**, selecione o trabalhador que está a adicionar como recurso do projeto e abra o registo do trabalhador.
2. No Painel de Ação, selecione **Projeto** &gt; **Configurar** &gt; **Configuração do projeto**.
3. Selecione um calendário e, em seguida, feche a página.

Também pode especificar projetos predefinidos para um recurso como um tipo de pré-atribuição. As pré-atribuições podem ser utilizadas quando o gestor de recursos ou o gestor de projetos sabe antecipadamente em que projetos o recurso irá trabalhar. As pré-atribuições também podem basear-se no pedido de um patrocinador ou cliente do projeto. Para pré-atribuir um projeto, na página **Atribuir projetos**, no separador **Projetos**, na lista **Projetos restantes**, selecione o projeto adequado.

## <a name="set-up-an-intercompany-resource"></a>Configurar um recurso entre empresas

Quando configura um trabalhador como um recurso entre empresas, tem de concluir a configuração tanto na empresa prestadora como na empresa tomadora.

### <a name="in-the-lending-company"></a>Na empresa prestadora

1. No Finance, verifique se a empresa prestadora está selecionada e, em seguida, conclua o procedimento na secção anterior: "Configurar um trabalhador como recurso do projeto".
2. Na página **Gestão contabilística entre empresas**, selecione **Novo**.
3. No campo **ID da entidade jurídica**, selecione a empresa prestadora. Preencha os campos restantes conforme adequado e, em seguida, selecione **Guardar**.
4. Na página **Preço de transferência**, selecione **Novo**.
5. No campo **Entidade jurídica tomadora**, selecione a empresa adequada.
6. Para emprestar à empresa tomadora apenas o recurso que criou no início desta secção, no campo **Recurso**, selecione o nome do recurso que criou. Para disponibilizar todos os recursos na empresa prestadora à empresa tomadora, deixe o campo **Recursos** em branco.
7. Na página **Parâmetros da gestão de projetos e contabilística**, no separador **Entre empresas**, defina a opção **Ativar as folhas de horas e o agendamento de recursos entre empresas** para **Sim**.

### <a name="in-the-borrowing-company"></a>Na empresa tomadora

- Na página **Lista de recursos**, no filtro de pesquisa, insira o nome do recurso que criou para a empresa prestadora para verificar se o nome está incluído na lista de recursos da empresa tomadora.

## <a name="request-project-resources"></a>Pedir recursos de projeto
A funcionalidade para o agendamento de recursos do projeto só permite que os gestores de recursos distribuam recursos com pessoal em compromissos ou projetos. Para ativar esta funcionalidade, execute as seguintes tarefas ou verifique se foram concluídas:

- Configurar sequências de números.
- Configurar os fluxos de trabalho de gestão de projetos e contabilística.
- Ativar os fluxos de trabalho de pedido de recursos.

Após a conclusão das tarefas anteriores, pode concluir as seguintes tarefas, conforme necessário:

- Criar um pedido de recurso a partir de um recurso com pessoal com reserva flexível.
- Monitorizar pedidos de recursos.
- Executar pedidos de recursos.
- Pedir um recurso com pessoal de uma WBS.
- ReservAr recursos para um projeto sem ter um pedido de recurso com pessoal.


[!INCLUDE[footer-include](../includes/footer-banner.md)]