---
title: Criar um novo projeto
description: Este tópico fornece informações sobre como criar um novo projeto.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5aa5e00252697f91a585eaaa83a0c8a39b315cc1b25fcbf6343fdf2ce31a824e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6985965"
---
# <a name="create-a-new-project"></a>Criar um novo projeto

[!include [banner](../includes/banner.md)]

Conclua os seguintes passos para criar um novo projeto.

1. Na página **Gestão de projetos**, selecione **Novo projeto** e introduza os seguintes valores:

    - **Tipo de projeto:** Tempo e material
    - **Nome do projeto:** Fase de Atualização 2 XYZ
    - **Grupo do projeto:** TM\_WIP
    - **ID de contrato do projeto:** 00000002

2. Selecione **Criar projeto**.

## <a name="assign-a-resource-to-a-project"></a>Atribuir um recurso a um projeto

1. Na página **Trabalhadores**, na lista **Trabalhadores**, selecione o registo para o trabalhador para o qual configurou anteriormente competências, e abra o registo do trabalhador.
2. No Painel de Ação, no separador **Projeto**, no grupo **Configurar**, selecione **Atribuir projetos**.
3. Na página **Atribuições de projetos de validação de recursos**, no separador **Projetos**, no campo **Adicionar o projeto aos projetos selecionados**, filtre pelo projeto **Fase de Atualização 2 XYZ**.
4. No painel de **Projetos restantes**, selecione um projeto e, em seguida, selecione o botão de seta para adicioná-lo ao painel **Projetos selecionados**.

Também pode atribuir categorias para um recurso, conforme necessário. O tipo de categoria é **Custo** ou **Receitas**. O tipo de categoria é determinado pela sua organização. Se não forem atribuídas categorias a um recurso, o Finance procura a categoria predefinida nos preços por hora para custos e receitas.

## <a name="set-up-project-resource-and-role-characteristics"></a>Configurar características de recursos e funções do projeto

Um gestor de projetos pode utilizar a funcionalidade de atribuição de recursos do projeto para criar as funções necessárias para o projeto. As funções podem ser utilizadas se os recursos confirmados ainda forem desconhecidos quando os recursos estão a ser reservados. As funções podem ser reservadas temporariamente como recursos planeados para poder continuar as fases de planeamento do projeto.

[![Exemplo de uma função.](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Cenário:** A Contoso foi contratada para concluir um projeto de Tempo e material que tem uma carta de projeto aprovada. O gestor de projetos junior ainda está a concluir o âmbito do projeto. O gestor de recursos está neste momento a identificar os recursos específicos que serão reservados para trabalhar no novo projeto. Dada a natureza crítica do projeto, o patrocinador do projeto solicitou o gestor de projeto sénior como uma das funções. O gestor de recursos tem de adquirir o novo recurso e definir a função no sistema no caso de o gestor de projeto júnior necessitar de informações dos recursos durante o planeamento do projeto.

Os passos seguintes mostram como o gestor de recursos pode configurar a função de gestor de projetos Sénior e associar características de recursos a ele. Mais tarde, a função pode ser utilizada para procurar recursos disponíveis que correspondam às competências de recursos necessárias.

1. Na página **Configurar funções**, selecione **Novo** e introduza os seguintes valores:

    - **ID de função:** Gestor de Projetos Sénior
    - **Descrição:** Gestor de Projetos Sénior

2. Selecione **Criar**.
3. Selecione a função **Gestor de Projetos Sénior** e, em seguida, selecione **Configurar características**.
4. No campo **Tipo de características**, selecione **Aptidão**.
5. No campo **Características disponíveis**, introduza a aptidão a procurar.
6. No campo **Tipo de característica**, selecione **Certificado**.
7. No campo **Características disponíveis**, introduza o tipo de certificado a procurar.

## <a name="assign-a-project-resource-to-a-project"></a>Atribuir um recurso de projeto a um projeto

1. Na página **Todos os projetos**, selecione o projeto **Fase de Atualização 2 XYZ**.
2. No separador **Equipa do projeto e agendamento**, selecione **Adicionar**.
3. No campo **Função**, selecione **Membro da equipa**.
4. Selecione **Reservar no calendário**.
5. Na página **Disponibilidade do recurso**, selecione **Ver definições**.
6. Na página **'Ajustar definições da vista**, introduza os seguintes valores:

    - **Formato para a vista de intervalo de datas:** Dia
    - **Apresentar descrições de disponibilidade:** Sim
    - **Apresentar capacidade restante:** Sim

7. Na lista de recursos, selecione um recurso.
8. Selecione **Reserva Fixa** e **Capacidade Total**.

## <a name="assign-a-resource-to-a-default-role"></a>Atribuir um recurso a uma função predefinida

Para ajudar os gestores de projetos ou recursos, podem desagregar mais nos recursos que podem ser reservados para um projeto. Pode associar uma função predefinida a um recurso existente ou a um recurso adquirido recentemente. Por exemplo, quando o Daniel foi contratado, tinha experiência e aptidões para preencher a função Analista de negócios. O gestor de recursos atribuiu esta função como função predefinida de Daniel. Por isso, o gestor de recursos adicionou Daniel a um conjunto de analistas de negócios que estão disponíveis para trabalhar em projetos.

Durante a reserva de recursos, os gestores de projetos podem filtrar os recursos da função que estão disponíveis para trabalhar em projetos. Podem utilizar esta informação como um critério quando executam a análise de decisões de vários critérios durante a execução dos recursos. Podem ainda adicionar outras características de recursos ao filtro para procurar recursos com aptidões, formação e experiência específicas para um determinado projeto.

**Cenário:** foi iniciado um projeto aprovado e a função de de gestor de projetos Sénior foi reservada como recurso planeado durante a fase de planeamento do projeto. O gestor de recursos adquiriu agora um recurso para executar a função Gestor de projetos sénior.

1. Na página **Lista de recursos**, selecione **Daniel Goldschmidt**.
2. Na página **Função do recurso**, selecione **Novo** e introduza os seguintes valores:

    - **Data Efetiva:** Introduza a data atual.
    - **Expiração:** introduza **Nunca**.
    - **Função:** introduza **Gestor de Projetos Sénior**.

3. Selecione **Guardar** e feche a página.
4. No separador **Competências**, adicione a aptidão **ProjectMgmt** e o certificado **PMP**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]