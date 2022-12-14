---
title: Implementar o Project Operations Lite
description: Este artigo fornece informações sobre como instalar a implementação do Project Operations lite – negócio para faturação proforma.
author: stsporen
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 2c508f56b3018b6a86fea78bcf9ee4136e90f385
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 11/30/2022
ms.locfileid: "9810993"
---
# <a name="deploy-project-operations-lite"></a>Implementar o Project Operations Lite

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_



O Project Operations suporta vários modelos de implementação. Para determinar o melhor modelo de implementação, consulte [Tipo de implementação](determine-deployment-type.md).


> [!IMPORTANT]
> Esta implementação, Implementação leve - oportunidade potencial para fatura pró-forma, resulta numa **Implementação só do Dataverse do Project Operations**.

- [Instalar o Project Operations num novo ambiente Dataverse](#new)
- [Instalar num ambiente Dataverse existente](#existing)
- [Instalar num ambiente existente do Dataverse que tem componentes de Escrita dupla](#existingdw)



## <a name="install-project-operations-lite-to-a-new-dataverse-environment"></a><a name="new"></a>Instalar o Project Operations Lite num novo ambiente do Dataverse

1. Como [Administrador Global ou do Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) com uma licença do Project Operations, crie um novo ambiente Dataverse no [Centro de administração do PowerPlatform](https://admin.powerplatform.com). Certifique-se de que a **Criação de uma base de dados para este ambiente** e **as aplicações do Dynamics 365** estão ativadas. Para mais informações, consulte [Criar e gerir ambientes no Centro de administração do Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
1. Selecione **Microsoft Dynamics 365 Project Operations** da lista de implementação de aplicações do Dynamics 365.


## <a name="install-project-operations-lite-to-an-existing-dataverse-environment"></a><a name="existing"></a>Instalar o Project Operations Lite num ambiente do Dataverse existente 
1. Como [Administrador Global ou do Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) com uma licença do Project Operations, localize o ambiente no [Centro de administração do PowerPlatform](https://admin.powerplatform.com) onde pretende instalar o Project Operations.
1. Instale o **Microsoft Dynamics 365 Project Operations** da lista de implementação de aplicações do Dynamics 365. Para mais informações, consulte [Gerir Aplicações do Dynamics 365](/power-platform/admin/manage-apps).

## <a name="install-project-operations-lite-to-an-existing-dataverse-environment-where-dual-write-solutions-are-already-present"></a><a name="existingdw"></a>Instalar Project Operations Lite num ambiente do Dataverse existente onde as soluções de Escrita dupla já estão presentes

Se quiser continuar a executar o Project Operations no modo de Implementação Lite, deverá seguir estes passos:

1. Como [Administrador Global ou do Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) com uma licença do Project Operations, localize o ambiente no [Centro de administração do PowerPlatform](https://admin.powerplatform.com) onde pretende instalar o Project Operations.
1. Instale o **Microsoft Dynamics 365 Project Operations** da lista de implementação de aplicações do Dynamics 365. Para mais informações, consulte [Gerir Aplicações do Dynamics 365](/power-platform/admin/manage-apps).
1. Uma vez que o ambiente tem componentes de Escrita dupla que ajudam a integrar com as aplicações de finanças e operações instaladas, a instalação do Project Operations também instalará as capacidades e extensões necessárias para integrar dados relacionados com o Projeto com aplicações de finanças e operações. Uma vez que pretende executar o Project Operations na implementação Lite, estes componentes de integração devem ser removidos, pois criarão restrições e overhead para cenários de implementação Lite. Desinstale manualmente as soluções de **Escrita Dupla do Dynamics 365 Project Operations** e **Mapas de Entidade de Escrita Dupla do Dynamics 365 Project Operations** para remover estes componentes.
1. Aceda a **Project Operations -> Definições -> Parâmetros**. Abra a página de detalhes do **Parâmetro do Projeto** e defina o campo **Comportamento da Atualização de Versão da Solução** como **Só Lite**. Isto assegura que quaisquer atualizações de versão subsequentes do Project Operations não devolverão os componentes de integração para o Project Operations.  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
