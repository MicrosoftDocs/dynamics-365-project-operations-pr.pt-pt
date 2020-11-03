---
title: Reservar para um projeto
description: Este tópico fornece informações sobre como reservar um recurso para um projeto.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 19128264ed3db7efeeba948155f0ddbdc806c2a0
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082256"
---
# <a name="book-to-a-project"></a>Reservar para um projeto

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Por vezes, um Gestor de Projetos ou Gestor de Recursos terá de alocar um recurso para a um projeto sem que seja definido um requisito específico a partir de um membro da equipa genérico. Isto pode ser conseguido de uma de três formas.

- Reservar a partir da grelha de membro de equipa
- Reservar a partir do quadro da agenda
- Reservar a partir do formulário **Projeto**

## <a name="book-from-the-team-member-grid"></a>Reservar a partir da grelha de membro de equipa

Se a sua organização estiver a operar no modo híbrido Alocação de recursos, o Gestor de Projetos pode reservar um recurso diretamente para o projeto ao concluir os seguintes passos.

1. A partir do projeto, vá para a grelha de membro de equipa e selecione **Novo**.
2. Defina o nome da posição e a função do recurso.
3. Selecione o recurso reservável a partir da pesquisa disponível.
4. Depois de selecionar o recurso, defina as seguintes informações do campo para reservar o recurso:

    - Data de início
    - Data de conclusão
    - Método de alocação
    - Horas, se aplicável
    - Aprovador do projeto

6. Selecione **Guardar e Fechar**

## <a name="book-from-the-schedule-board"></a>Reservar a partir do quadro da agenda

Quando um Gestor de Recursos precisa de reservar um recurso diretamente para um projeto, pode utilizar o quadro da agenda e os requisitos do projeto. O requisito do projeto é um requisito de recursos que está sempre disponível para ser reservado novamente. Para reservar diretamente para um formulário de projeto a partir do quadro da agenda, execute os seguintes passos.

1. Navegue para o quadro da agenda e, na página esquerda, filtre pelos recursos que está a considerar para o requisito.
2. No painel inferior, selecione o separador **Projeto** para ver uma lista dos requisitos do projeto.
3. Arraste o requisito para um recurso e defina as seguintes informações:

    - Data de início
    - Data de conclusão
    - Estado de reserva
    - Método de reserva
    - Duração

## <a name="book-from-the-project-form"></a>Reservar a partir do formulário Projeto

Como Gestor de projetos, pode precisar de reservar um recurso para um projeto, mas conhecer apenas os critérios, em vez do nome do recurso. Conclua os seguintes passos para utilizar o assistente da agenda para localizar um recurso baseado em quaisquer atributos disponíveis do recurso. 

1. Navegue para o projeto e selecione **Reservar** para abrir o Assistente da Agenda.
2. Utilize os filtros no lado esquerdo do Assistente da Agenda para reduzir os critérios e selecione **Procurar**.
3. Baseado nos recursos devolvidos nos resultados, pode reservar um recurso.

> [!NOTE]
> Este método não cria quaisquer reservas para o recurso. Em vez disso, adiciona o recurso à equipa. Depois de o membro da equipa ser adicionado ao projeto, o gestor de projetos pode utilizar a opção para manter as reservas ou prolongar as reservas para adicionar as reservas necessárias ao recurso.
