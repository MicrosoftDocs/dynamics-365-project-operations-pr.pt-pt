---
title: Dotar um projeto com trabalhadores contratados e capacidade subcontratada
description: Este tópico explica como os requisitos do projeto podem ser dotados de colaboradores utilizando trabalhadores contratados ou capacidade subcontratada no Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 7e9a0ca08f472999138589f31ca820b733b6303e
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903513"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Dotar um projeto com trabalhadores contratados e capacidade subcontratada

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

Os membros da equipa do projeto genéricos podem ser dotados de colaboradores ou trabalhadores contratados. Ao dotar um projeto com trabalhadores contratados, pode limitar as suas opções de colaboradores a trabalhadores contratados específicos que sejam atribuídos a um item de subcontrato. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Pesquisar por requisitos de recursos de pessoal com trabalhadores contratados que pertençam a um item de subcontratação específico

Para pesquisar por requisitos de recursos de pessoal com trabalhadores contratados que pertençam a um item de subcontratação específico, siga estes passos:

1. Crie um membro da equipa do projeto genérico que referencia um subcontrato e item de subcontrato.
2. Gere um requisito de recursos para este membro da equipa do projeto genérico utilizando o botão **Gerar requisito** na subgrelha de membros da equipa do projeto.
3. Selecione a linha de membro da equipa e, em seguida, selecione o botão **Reservar** na subgrelha. 
4. Isto abre o Quadro da Agenda com o contexto do requisito. Juntamente com outros atributos, tais como campos de datas, função e de unidade organizacional, os filtros do Quadro da Agenda também são automaticamente preenchidos com os campos de fornecedor, subcontrato e item de subcontrato a partir do requisito de recursos.
5. O sistema pesquisa por recursos que satisfaçam os critérios do filtro e lista-os. 
6. Selecione um dos recursos filtrados e reserve o recurso do requisito. 
7. Um membro da equipa do projeto é criado e atualizado com referências de subcontrato e item de subcontrato. Vá a **Estimativas do Projeto** e selecione **Atualizar preços** para ver o custo atualizado da atribuição de recursos. 

> [!NOTE]
> A atualização do membro da equipa do projeto com uma referência de item de subcontrato e subcontrato pode nem sempre ser possível durante a reserva se o recurso for atribuído a vários itens de subcontrato. Se o sistema não conseguir atualizar o membro da equipa do projeto com um item de subcontrato e subcontrato, abra o registo do membro da equipa do projeto e atualize manualmente estes campos de modo a que a estimativa de custos financeiros reflita com precisão o custo do subcontratante.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Pesquisa por e dota de requisitos de recursos com qualquer trabalhador contratado

Para pesquisar por e dotar de requisitos de recursos com qualquer trabalhador contratado, siga estes passos:

1. Crie um membro da equipa do projeto genérico.
2. Gere um requisito de recursos para este membro da equipa do projeto genérico utilizando o botão **Gerar requisito** na subgrelha de membros da equipa do projeto.
3. Selecione a linha de membro da equipa e, em seguida, selecione o botão **Reservar** na subgrelha. 
4. Isto abre o Quadro da Agenda com o contexto do requisito. Juntamente com outros atributos, tais como campos de datas, função e de unidade organizacional, os filtros do Quadro da Agenda também são automaticamente preenchidos com os campos de fornecedor, subcontrato e item de subcontrato a partir do requisito de recursos. Como o requisito não tinha valores de subcontrato ou de item de subcontrato preenchidos, estes atributos ficarão vazios no painel de filtros.
5. O sistema pesquisa por recursos que satisfaçam os critérios do filtro e lista-os.
6. Atualize o campo **Tipo de trabalhador** no painel de filtros para **Trabalhador Contratado** para limitar a procura aos trabalhadores contratados. Atualize **Fornecedor** no painel de filtros para selecionar um fornecedor para limitar a pesquisa para mostrar apenas trabalhadores contratados que pertencem a uma empresa fornecedora específica.
7. Selecione um trabalhador contratado da lista e reserve o recurso para o requisito.
8. Um membro da equipa do projeto é criado. No entanto, o membro da equipa do projeto não é atualizado com qualquer subcontrato ou item de subcontrato, pelo que a atribuição de recursos não será custeada através do preço do subcontrato. Atualize manualmente o membro da equipa do projeto com um item de subcontrato e vá a **Estimativas do Projeto** e selecione **Atualizar preços** para ver o custo atualizado da atribuição de recursos.

> [!NOTE]
> Os membros da equipa do projeto que têm o **Tipo de trabalhador** como **Trabalhador contratado**, mas que não têm um subcontrato são sinalizados como **Inválidos** na grelha **Membros da equipa do projeto**. Se existirem quaisquer membros da equipa do projeto com este estado, abra o registo do membro da equipa do projeto e atualize manualmente os campos de item de subcontrato e subcontrato, de modo a que a estimativa de custos no separador **Estimativas**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
