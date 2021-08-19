---
title: Implementar manualmente a aplicação Project Operations Dataverse com suporte de escrita dupla
description: Este tópico explica como implementar manualmente a aplicação Project Operations Dataverse para suportar a escrita dupla.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 06325a9a9f9084d1f506f2493c32565fe7b7c52ae6fe22c81339b9c1d632e688
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986460"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a>Implementar manualmente a aplicação Project Operations Dataverse com suporte de escrita dupla

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Este tópico explica como implementar manualmente o Microsoft Dynamics 365 Project Operations no Microsoft Dataverse para suportar a escrita dupla. O Project Operations deteta a configuração do ambiente e inclui suporte adicional para escrita dupla se os requisitos forem satisfeitos.

Durante a implementação através do Microsoft Dynamics Lifecycle Services (LCS), se seguiu as instruções neste tópico, pode ignorar a implementação da integração do Microsoft Power Platform (anteriormente conhecido como ambiente Common Data Service).

O processo de implementação do Project Operations no Dataverse para suportar escrita dupla tem quatro passos principais:

1. [Criar um novo ambiente no Dataverse que suporta escrita dupla](#create).
2. [Adicionar pré-requisitos de escrita dupla ao ambiente](#prerequisites).
3. [Adicionar a aplicação Project Operations Dataverse](#dataverse).
4. [Associar os seus ambientes](#link).

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a>Criar um novo ambiente no Dataverse que suporta escrita dupla

Para concluir este procedimento, tem de iniciar sessão como administrador.

1. Abra o [centro de administração do Power Platform](https://admin.powerplatform.com) e inicie sessão como administrador.
2. Crie um novo ambiente e atribua-lhe um nome.
3. Selecione o tipo de ambiente. Se se inscreveu na oferta de avaliação, selecione **Avaliação (baseada em subscrições)**.
4. Confirme a região de implementação.
5. Ative a opção **Criar uma base de dados para este ambiente**. 
6. Confirme o idioma e, em seguida, confirme que a moeda corresponde à moeda das suas aplicações do Finance and Operations.
7. Ative a opção **Aplicações do Dynamics 365** e confirme que o campo **Implementar automaticamente estas aplicações** está definido como **Nenhum**.
8. Adicione um grupo de segurança, se for necessário um grupo de segurança.
9. Selecione **Guardar** para criar o ambiente.
10. Aguarde até a implementação estar concluída e o ambiente atingir o estado **Pronta**.

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a>Adicionar pré-requisitos de escrita dupla ao ambiente

O suporte de escrita dupla inclui campos adicionais que são adicionados a entidades chave, como a entidade **Empresa**. Se estiver a adicionar suporte de escrita dupla a um ambiente existente, poderá ter de atualizar os dados para ativar o suporte. Para obter informações sobre como inicializar o programa de arranque do sistema dos dados, consulte [Inicializar os dados da empresa](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data). Para mais informações sobre a escrita dupla, consulte [Requisitos de sistema de escrita dupla](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).

Conclua este procedimento para adicionar os pré-requisitos de escrita dupla ao seu ambiente.

1. Abra o ambiente que acabou de criar e, em seguida, vá para **Recurso** \> **Aplicações do Dynamics 365**.
2. Selecione **Solução central de escrita dupla** na lista de aplicações e instale-a.
3. Aguarde até a instalação ser concluída. Em seguida, selecione **Solução de orquestração de aplicações de escrita dupla** na lista de aplicações e instale-a.

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a>Adicionar a aplicação Project Operations Dataverse

Só pode concluir este procedimento se tiver concluído os procedimentos anteriores antes de instalar o Project Operations. Durante a instalação, o sistema analisa a configuração do ambiente e adiciona suporte para escrita dupla, se for necessário.

1. Abra o ambiente que criou anteriormente e, em seguida, vá para **Recurso** \> **Aplicações do Dynamics 365**.
2. Selecione **Microsoft Dynamics 365 Project Operations** na lista de aplicações e instale-o.

## <a name="link-your-environments"></a><a name="link"></a>Associar os seus ambientes

Após a implementação do ambiente Dataverse, pode configurar a associação nas suas aplicações do Finance and Operations. Siga os passos em [Utilizar o assistente de escrita dupla para associar os seus ambientes](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).