---
title: Descrição geral dos modos de gestão de recursos
description: Este tópico fornece informações sobre a funcionalidade de gestão de recursos no Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 872f4f2878f474e16674932f23fe192c6a8de6eb
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279467"
---
# <a name="resource-management-modes-overview"></a>Descrição geral dos modos de gestão de recursos

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_


O Dynamics 365 Project Operations suporta dois modos para executar o fluxo de reserva global. O modo de gestão é definido como um parâmetro de projeto e pode ser modificado se o seu negócio precisar de alteração.    

## <a name="central-mode"></a>Modo central
Para as organizações que centralizam a alocação de recursos para projetos, o modo Central oferece uma forma de assegurar que os Gestores de projeto podem definir os requisitos de recursos a nível do projeto. A conclusão dos requisitos do recurso é delegada num Gestor de recursos. Os gestores de projetos podem aceitar ou rejeitar recursos que são propostos pelo Gestor de recursos.

![Modo Central](./media/resource-management-central.png)

Para gerir recursos com o modo Central, consulte:

- [Atribuir recursos reserváveis genéricos a uma tarefa e gerar requisitos de recursos](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Reservar recursos nomeados a partir de requisitos de recursos](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [Submeter um pedido de recurso](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [Concluir um pedido de recurso](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [Aceitar ou rejeitar um recurso de projeto proposto a partir de um pedido de recurso](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Modo híbrido
Para as organizações que necessitam de flexibilidade na alocação de recursos, o modo híbrido conferem aos Gestores de projeto e aos Gestores de recursos a capacidade de reservar recursos.

![Modo Híbrido](./media/resource-management-hybrid.png)

Além do processo do modo Central suportado, consulte os seguintes tópicos para gerir todos os outros fluxos de reservas suportados no modo Híbrido:

Reservar um recurso diretamente para um projeto:
- [Reservar recursos reserváveis nomeados para uma equipa do projeto e atribuir tarefas](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

Reservar um recurso a partir de um requisito de recurso:
- [Atribuir recursos reserváveis genéricos a uma tarefa e gerar requisitos de recursos](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Reservar recursos nomeados a partir de requisitos de recursos](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]