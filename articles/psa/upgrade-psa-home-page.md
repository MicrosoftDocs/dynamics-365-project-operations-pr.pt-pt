---
title: Home page de atualização
description: Este tópico mostra onde encontrar informações importantes sobre os recursos novos e alterados no Dynamics 365 Project Service Automation e o processo de atualização para a versão mais recente.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
author: rumant
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 29e7b519b61e8709c025e9906d04aed0156f65eb
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082485"
---
# <a name="upgrade-home-page"></a>Home page de atualização

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a>Atualização do PSA versão 2.x ou 1.x para a versão 3.x

### <a name="new-instances"></a>Novas instâncias

Desde 17 de maio de 2019, quando o Project Service Automation é selecionado durante o aprovisionamento de uma nova instância, a versão 3.x é instalada por predefinição.

### <a name="existing-instances"></a>Instâncias existentes

Anteriormente, os clientes com uma instância do PSA versão 2.x e que precisavam de atualizar para a versão 3.x, que é a versão do PSA baseada em UCI (Interface Unificada do Cliente), tinham de contactar o Suporte da Microsoft e fornecer os detalhes da instância para que o suporte pudesse ativar a instância para atualização para a versão 3.x. A partir de 1 de março de 2020, os clientes com um instância da versão 2.x do PSA, e que precisarem de atualizar para a versão 3.x, poderão atualizar as respetivas instâncias diretamente a partir do portal Admin sem terem de contactar o Suporte da Microsoft.  

> [!NOTE]
> O PSA versão 3.x inclui alterações significativas. Ele foi baseado na arquitetura da Interface Unificada para ajudar a fornecer uma melhor experiência do utilizador. A aplicação redesenhada oferece uma interface do utilizador consistente e uniforme e segue princípios de design responsivos para uma visualização ideal em qualquer tamanho de ecrã ou dispositivo. Houve outras alterações em toda a aplicação. Algumas das áreas que foram alteradas incluem preços, reservas e atribuição de recursos, tempo, despesas e aprovações.

Antes de iniciar o processo de atualização, recomendamos que conclua as seguintes tarefas:

- Verifique se o Dynamics 365 Field Service e o Project Service Automation estão instalados na instância identificada. Se as duas soluções estiverem instaladas, planeie atualizar as duas antes de retomar a utilização regular da instância.
- Analise cuidadosamente os seguintes tópicos. A perceção e a compreensão das alterações entre as versões ajudá-lo-ão no processo de atualização. Estes tópicos fornecem informações sobre as principais alterações no PSA, juntamente com considerações e recomendações para planear a sua atualização para a versão 3.x.

    - [Novidades ou alterações no Project Service Automation versão 3](whats-new-changed-v3.md)
    - [Considerações sobre atualização - Project Service Automation versão 2.x ou 1.x para a versão 3](upgrade-v3.md)

- Atualize a sua instância de área restrita para avaliar as alterações na sua implementação antes de atualizar a sua instância de produção.

Depois de analisar os tópicos mencionados anteriormente e estar pronto para atualizar para o PSA versão 3.x ou a versão baseada em UCI, submeta um pedido para o suporte da Microsoft para disponibilizar a atualização no Centro de administração. No seu pedido, forneça os detalhes da sua instância.

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a>Versões mais antigas do PSA (PSA versão 2.x) numa instância criada recentemente

Desde 17 de maio de 2019, todas as novas instâncias têm a UCI como cliente predefinido. Para alinhamento com esta alteração, o PSA versão 3.x e e o Field Service versão 8.x serão aprovisionados por predefinição, porque estas versões foram concebidas para funcionar com o cliente de UCI.

A partir de 1 de março de 2020, os clientes do Dynamics PSA deixarão de poder criar novos ambientes com versões mais antigas do PSA, por exemplo, a versão 2.x ou anterior do PSA. Qualquer novo ambiente só obterá a versão 3.x do PSA.

> [!NOTE]
> Para obter a melhor experiência ao utilizar versões mais antigas das aplicações Field Service e PSA, aceda à página **Definições do sistema** e, no campo **Utilizar apenas a nova Interface Unificada (recomendado)** , selecione **Não** , já que estas versões não foram concebidas para serem carregadas corretamente na UCI. Depois de desativar a UCI, pode abrir e executar estas versões do Field Service e PSA utilizando o cliente Web antigo. 
