---
title: Inscrever-se para obter uma subscrição de pré-visualização - leve
description: Este artigo fornece informações sobre como subscrever e implementar o Project Operations lite – negócio para faturação proforma.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 29bf31cd1bc9c1c5ac757de989154b4c7acc53fe
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410074"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Inscrever-se para obter uma subscrição de pré-visualização - leve 

Este artigo explica como subscrever a oferta de avaliação e implementar o Dynamics 365 Project Operations lite – negócio para faturação proforma.

> [!NOTE]
> Este processo será alterado nas próximas versões do Project Operations.

## <a name="prerequisites"></a>Pré-requisitos
- O utilizador que implementar a pré-visualização tem de ter direitos de administrator global do inquilino do Azure. Poderá criar um inquilino durante o primeiro resgate da oferta.

> [!IMPORTANT]
> Só uma pessoa, o administrador inquilino, numa organização precisa de executar esta tarefa. Se não for subscritor desta versão, aguarde até a sua organização estar inscrita e receber as suas credenciais de utilizador.
> 
> As avaliações são de utilização única no inquilino. Só é possível executar uma avaliação uma vez. Recomendamos que crie um novo inquilino para os fins da avaliação.

### <a name="dynamics-365-project-operations-trial"></a>Avaliação do Dynamics 365 Project Operations 

Antes de começar, certifique-se de que está a iniciar sessão num browser com a conta de profissional de utilizador no inquilino onde pretende a pré-visualização do Project Operations.

1. Vá para [Avaliação do Project Operations](https://aka.ms/try-po) para resgatar o primeiro código de oferta, **Dynamics 365 Project Operations**.
2. Confirme a encomenda.

  Verá que a oferta de confirmação foi resgatada com êxito.

## <a name="assign-licenses"></a>Atribuir licenças

> [!IMPORTANT]
> Necessitará de acesso administrativo ao Portal Microsoft 365 da sua organização para concluir os seguintes passos.


1. Aceda ao [Centro de administração do Microsoft 365](https://portal.office.com/) para atribuir as licenças aos seus utilizadores.
2. Na página **Utilizadores ativos**, selecione os utilizadores aos quais pretende atribuir uma licença.
3. Verifique se a licença **Dynamics 365 Project Operations** foi selecionada. 
4. Selecione **Guardar alterações**.

## <a name="create-a-new-dataverse-environment"></a>Criar um novo ambiente do Dataverse

1. Aprovisione um novo ambiente de implementação do Dataverse do Project Operations seguindo as instruções no artigo [Modelo de implementação do Dataverse](lite-deployment.md). Ao selecionar o tipo de ambiente, certifique-se de que utiliza **Avaliação (baseado em Subscrição)**.

  ![Novo ambiente.](./media/19CreateEnvironment.png)

2. Selecione a definição **Ativar aplicações do Dynamics 365** e deixe **Implementar automaticamente estas aplicações** em branco.  
3. Selecione **Guardar** para criar o ambiente.

  ![Adicionar base de dados.](./media/20CreateEnvironment1.png)

4. Depois de criar o ambiente, instale a solução **Microsoft Dynamics 365 Project Operations**. 

![Instalar Solução.](./media/21InstallSolution.png)

## <a name="set-up-demo-data"></a>Configurar dados de demonstração

Configure dados de demonstação, seguindo as instruções no artigo [Aplicar configuração de demonstração e dados de configuração](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
