---
title: Novidades ou alterações na Versão da Atualização 16 do Project Service Automation, V3
description: Este artigo lista as funcionalidades e correções disponíveis na Versão 16 da Atualização do Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: e4429ace3d8206369b91917cf87f6968fbb12277
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926514"
---
# <a name="project-service-automation-update-release-16-v3"></a>Versão da Atualização 16 do Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a mais recente atualização à aplicação Project Service Automation para Dynamics 365. Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização.  Esta versão é compatível com o Dynamics 365 9.x. Para atualizar esta versão, visite o Centro de Administração para o Dynamics 365 online e aceda à página de soluções para instalar a atualização. Para obter mais informações, consulte [Instalar, Atualizar uma Solução Preferencial](/dynamics365/project-service/upgrade-psa-home-page).
Este artigo lista as funcionalidades e correções novas ou alteradas para a Versão 16 da Atualização do PSA V3. Esta versão tem um número de compilação de V3.10.6.34 e está geralmente disponível através de uma Atualização automática em janeiro de 2020.


## <a name="update-release-16"></a>Versão da Atualização 16

### <a name="bug-fixes"></a>Correções de erros

-   Tempo e Despesa

    -   Corrigido: os utilizadores que tentam submeter entradas de tempo e de gastos eliminadas para aprovação receberão agora mensagens de erro relevantes.

-   Gestão de Projetos

    -   Corrigido: as unidades de atribuição de recursos definidas para os membros da equipa nos modelos são respeitadas e os modelos são aplicados a um novo projeto.

    -   Corrigido: foi melhorado o tratamento da reatribuição da propriedade dos registos.

    -   Corrigido: os projetos em processo de cópia não terão permissão para serem copiados enquanto não forem concluídas todas as operações de cópia.

-   Gestão de Recursos

    -   Corrigido: agora, as reservas alargadas tratam corretamente as curtas durações e já não criam zero horas para as reservas alargadas.

    -   Corrigido: agora, a vista de reconciliação é composta quando o fuso horário do projeto é +5:30 GMT e a hora do utilizador por si só é diferente.

-   Sales

    -   Corrigido: quando um projeto mapeado para um item de contrato é removido e é mapeado um novo projeto, os registos reais no novo projeto não eram reavaliados com base nas regras de faturação e definição de preços definidas no item de contrato. Este problema foi corrigido nesta versão. A definição de preços e os registos reais no projeto mapeado recentemente serão revertidos e recriados corretamente com base nas regras de definição de preços e faturação do item de contrato. Os registos reais do projeto não mapeado também serão reavaliados e recriados como consequência.

    -   Corrigido: foi adicionada validação adicional ao campo **Montante** da linha da estimativa para assegurar que os valores nulos não são mantidos.

    -   Corrigido: depois de atualizados os valores reais num projeto, foi adicionado um botão de atualização ao formulário principal do projeto para permitir que os utilizadores repitam a sincronização dos valores reais.

    -   Corrigido: quando os utilizadores fazem a atualização da versão 2.X para 3.X, serão permitidos projetos com um valor NULL para um nome de projeto.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
