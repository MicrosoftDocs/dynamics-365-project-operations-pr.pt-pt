---
title: Inscrever-se para obter uma subscrição de pré-visualização – lite
description: Este tópico fornece informações sobre como subscrever e implementar o Project Operations lite - oportunidade potencial para fatura pró-forma.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2b5a65f5e29915c349d40400ebbf3e4923b36a67
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334796"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Inscrever-se para obter uma subscrição de pré-visualização - leve 

Este tópico explica como subscrever a oferta de avaliação e proceder à implementação leve Dynamics 365 Project Operations - oportunidade potencial para fatura pro forma.

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
> Necessitará de acesso administrativo ao Portal Microsoft 365 da sua organização do para concluir os seguintes passos.


1. Vá para o [Centro de administração do Microsoft 365](https://portal.office.com/) para atribuir as licenças aos seus utilizadores.
2. Na página **Utilizadores ativos**, selecione os utilizadores aos quais pretende atribuir uma licença.
3. Verifique se a licença **Dynamics 365 Project Operations** foi selecionada. 
4. Selecione **Guardar alterações**.

## <a name="create-a-new-dataverse-environment"></a>Criar um novo ambiente do Dataverse

1. Aprovisione um novo ambiente de implementação do Project Operations Dataverse ao seguir as instruções no tópico [Modelo de implementação do Dataverse](lite-deployment.md). Ao selecionar o tipo de ambiente, certifique-se de que utiliza **Avaliação (baseado em Subscrição)**.

  ![Novo ambiente](./media/19CreateEnvironment.png)

2. Selecione a definição **Ativar aplicações do Dynamics 365** e deixe **Implementar automaticamente estas aplicações** em branco.  
3. Selecione **Guardar** para criar o ambiente.

  ![Adicionar base de dados](./media/20CreateEnvironment1.png)

4. Depois de criar o ambiente, instale a solução **Microsoft Dynamics 365 Project Operations**. 

![Instalar Solução](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Instalar uma configuração CDS e dados de demonstração da configuração

Instale a configuração CDS e configure os dados de demonstração da configuração ao seguir as instruções no tópico [Aplicar dados de configuração da demonstração](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
