---
title: Inscreva-se nas subscrições de pré-visualização do Project Operations para os cenários de recursos/não armazenados
description: Este tópico fornece informações sobre como subscrever e implementar o Project Operations para cenários baseados em recursos/não armazenados.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f47d5a29c0e40a49aed7b3e52c5d52a9c27b8dbc
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323430"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Inscreva-se nas subscrições de pré-visualização do Project Operations para os cenários de recursos/não armazenados

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Este tópico explica como subscrever a oferta de avaliação e implementar o ambiente do Project Operations para os cenários baseados em recursos/não armazenados.

## <a name="prerequisites"></a>Pré-requisitos
- O utilizador que implementar a pré-visualização tem de ter direitos de administrator global do inquilino do Azure. Poderá criar um inquilino durante o primeiro resgate da oferta. 
- A implementação de um ambiente do Finance requer uma subscrição válida do Azure que será faturada por ambiente. Poderá utilizar subscrição existente das suas organizações ou utilizar uma [Avaliação do Azure](https://azure.microsoft.com/free/) para começar. O ambiente do CDS será disponibilizado gratuitamente durante um período limitado de 30 dias.

> [!IMPORTANT]
> Só uma pessoa, o administrador inquilino, numa organização precisa de executar esta tarefa. Se não for subscritor desta versão, aguarde até a sua organização estar inscrita e receber as suas credenciais de utilizador.
> 
> As avaliações são de utilização única no inquilino. Só é possível executar uma avaliação uma vez. Recomendamos que crie um novo inquilino para os fins da avaliação.


### <a name="dynamics-365-project-operations-ce---preview-trial"></a>Dynamics 365 Project Operations (CE) - Avaliação de Pré-visualização 

Antes de começar, certifique-se de que está a iniciar sessão num browser com a conta de profissional de utilizador no inquilino onde pretende a pré-visualização do Project Operations.

1. Resgate o primeiro código de oferta do **Dynamics 365 Project Operations** aqui [Avaliação do Project Operations](https://aka.ms/try-po).
2. Confirme a encomenda.

  Verá que a oferta de confirmação foi resgatada com sucesso.

### <a name="dynamics-365-finance-preview-trial"></a>Avaliação da pré-visualização do Dynamics 365 Finance

Vá para [Avaliação da Pré-visualização do Dynamics 365 for Finance](https://aka.ms/trypoche) e repita os passos da secção anterior com a oferta, Inscrição no Ambiente Alojado na Cloud.  

## <a name="assign-licenses"></a>Atribuir licenças

> [!IMPORTANT]
> Necessitará de acesso administrativo ao Portal Microsoft 365 da sua organização do para concluir os seguintes passos.

1. Vá para o [Centro de administração do Microsoft 365](https://portal.office.com/) para atribuir as licenças aos seus utilizadores.

2. Na página **Utilizadores ativos**, selecione os utilizadores aos quais pretende atribuir uma licença.

3. Verifique se a licença do **Dynamics 365 Project Operations** foi selecionada e selecione **Guardar alterações**.

> [!NOTE]
> A oferta de avaliação do Finance não precisa de ser atribuída a um utilizador.

## <a name="start-a-new-project-in-lcs"></a>Iniciar um novo projeto no LCS

Criar um novo projeto LCS conforme descrito no tópico [Iniciar um novo projeto no LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Adicionar uma subscrição do Azure a um projeto LCS

Para concluir esta tarefa, siga os passos na tópico, [Adicionar uma subscrição do Azure ao projeto LCS](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Implementar o ambiente de demonstração do Finance com o Project Operations para cenários de recursos/non armazenados

Siga as orientações no tópico [Aprovisionar um novo ambiente](resource-provision-new-environment.md) para concluir a implementação. Utilize o tipo de implementação do [ambiente de demonstração](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) para pré-visualização. 

## <a name="install-cds-setup-and-configuration-data"></a>Instalar dados de configuração do CDS

Instale os dados de configuração do CDS descritos no tópico [Configurar e aplicar dados de configuração no Common Data Service](resource-apply-pro-setup-config-data.md).
Conclua este passo apenas após a implementação do ambiente de demonstração do Finance e de os dados de demonstração estarem prontos.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
