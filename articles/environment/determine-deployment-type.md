---
title: Determinar o tipo de implementação
description: Este tópico fornece informações que o vão ajudar a determinar o tipo de implementação correto do Project Operations para a sua empresa.
author: stsporen
ms.date: 03/15/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 4be8e69c5b6ff1ed65e9484a9b427bb428f7ff3e6dc597c615d5586da52867ef
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994650"
---
# <a name="determine-your-deployment-type"></a>Determinar o tipo de implementação

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

> [!IMPORTANT]
> Depois de adquirir a licença, comece aqui para determinar o melhor modelo de implantação do Dynamics 365 Project Operations utilizando o [fluxo de instalação guiado](https://aka.ms/provisionprojectoperations).
> Depois de concluir o Fluxo de instalação guiado, será direcionado para o portal de gestão correto para concluir a sua instalação. Consulte os detalhes da implementação para concluir a instalação.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Clientes existentes do Dynamics que utilizam o Dynamics 365 Project Service Automation
O Project Operations inclui as capacidades que foram enviadas com o Project Service Automation. Será lançada um percurso de atualização de versão para estes clientes na vaga 1 da versão de 2021.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Clientes existentes do Dynamics 365 Finance que utilizam a Gestão de projetos e contabilística 

Os clientes existentes d Finance que utilizam a funcionalidade de Gestão e contabilidade de projetos podem continuar a usá-lo como está. Consulte [Project Operations para cenários de encomenda em stock/de produção](#pma).


## <a name="deployment-regions"></a>Regiões de Implementação
Para determinar quais as regiões que apoiam a implementação de Project Operations, consulte a [disponibilidade geográfica para o Dynamics 365 e relatório Power Platform](https://dynamics.microsoft.com/en-us/geographic-availability/). Selecione **Ver relatório** e expanda **Dynamics 365 > Operations Apps > Dynamics 365 Project Operations** para ver as regiões apoiadas.

## <a name="deployment-types"></a>Tipo de implementação
O Project Operations suporta várias opções de implementação à medida dos seus requisitos. Quer seja um cliente novo ou existente do Dynamics 365, o Project Operations suporta as suas necessidades.

O nosso [Questionário de implementação](https://aka.ms/provisionprojectoperations) ajudará a determinar a implementação certa. Os resultados vão guiá-lo para um dos seguintes tipos de implementação:

- [Implementação leve - oportunidade potencial para fatura pró-forma](#lite)
- [Project Operations para cenários baseados em recursos/não em stock](#integrated)
- [Project Operations para cenários de encomenda em stock/de produção](#pma)

O Project Operations suporta cenários de encomenda em stock/de produção e cenários não armazenados/baseados em recursos no mesmo ambiente através de configurações a nível da entidade jurídica. Por exemplo, Contoso pode utilizar as capacidades armazenadas/de produção de encomenda nas suas instalações de fabrico dos EUA (Entidade Legal = Contoso Fabricação nos Estados Unidos). Contoso pode utilizar as capacidades não abastecidas/baseadas em recursos nas suas instalações Contoso de assistência robótica no Reino Unido (entidade legal = Contoso Robótica no Reino Unido).

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>Implementação leve - oportunidade potencial para fatura pró-forma

A implementação leve inclui as seguintes capacidades:

- Processo de vendas para projetos que alarga experiências de aplicação do Dynamics 365 Sales
- Planeamento de projetos com o Microsoft Project para a Web
- Preços multidimensionais
- Gestão de recursos unificados
- Monitorização do tempo
- Despesas básicas
- Faturação pró-forma para revisão e edições do gestor de projetos 

#### <a name="deployment-steps"></a>Passos de implementação
Determine o melhor modelo de implementação do Project Operations através do [Questionário de implementação](https://aka.ms/provisionprojectoperations).

Para esta implementação, consulte [Inscrever-se em subscrições de pré-visualização](lite-preview-subscription-sign-up.md) e [Aprovisionar novo ambiente](lite-deployment.md). 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a>Project Operations para cenários baseados em recursos/não em stock
O Project Operations para cenários baseados em recursos/não em stock incluem as seguintes capacidades:
 
- Processo de vendas para projetos que alarga a aplicação do Dynamics 365 Sales
- Planeamento de projetos com o Microsoft Project para a Web
- Preços multidimensionais
- Gestão de recursos unificados
- Monitorização do tempo
- Despesas básicas
- Despesa total
- OCR de recibos
- Faturação pró-forma e virada para o cliente 
- Reconhecimento de receitas para projetos

#### <a name="deployment-steps"></a>Passos de implementação
Determine o melhor modelo de implementação do Project Operations através do [Questionário de implementação](https://aka.ms/provisionprojectoperations).

Para esta implementação, consulte [Inscrever-se em subscrições de pré-visualização](resource-sign-up-preview-subscription.md) e [Aprovisionar novo ambiente](resource-provision-new-environment.md). 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Project Operations para cenários de encomenda em stock/de produção

- Planeamento de projetos com WBS
- Gestão de recursos
- Monitorização do tempo
- Despesa total
- OCR de recibos
- Faturação completa
- Reconhecimento de receitas
- Encomendas de produção
- Suporte de materiais armazenados com inventário

#### <a name="deployment-steps"></a>Passos de implementação
Determine o melhor modelo de implementação do Project Operations através do [Questionário de implementação](https://aka.ms/provisionprojectoperations).

Para esta implementação, consulte [Inscrever-se em subscrições de pré-visualização](/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=%2fdynamics365%2ffinance%2ftoc.json) e [Aprovisionar novo ambiente](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=%2fdynamics365%2ffinance%2ftoc.json). 



[!INCLUDE[footer-include](../includes/footer-banner.md)]