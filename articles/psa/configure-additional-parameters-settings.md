---
title: Configurar definições de parâmetros adicionais
description: Como configurar definições de parâmetros adicionais no Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 24a4fe83471da916fb91cfe20e739279c08d8e5e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082404"
---
# <a name="configure-additional-parameter-settings-project-service"></a>Configurar definições de parâmetros adicionais (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Depois de configurar os itens nos tópicos anteriores, terá de definir parâmetros do projeto adicionais para utilizar nos seus projetos. Quando o [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] foi instalado pela primeira vez, criou uma definição de parâmetros para criar todos os registos necessários para o [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] funcionar. Agora é o momento de voltar atrás e configurar os campos adicionais para estas definições.  
  
 Terá de ter configurado as seguintes definições:  
  
-   Unidade organizacional  
  
-   Frequência da Fatura  
  
-   Modelo de horas de trabalho  
  
-   Lista de preços  
 
Neste passo, indique também o tipo de alocação de recursos pretende:  
  
- **Central**. Só os gestores de recursos podem alocar recursos a projetos.  
  
- **Híbrido**. Os gestores de recursos, os gestores de projetos e os gestores de contas podem alocar recursos a projetos.  
  
 
Para definir os parâmetros do projeto:  
  
1. Vá para **Project Service > Parâmetros**.  
  
2. Clique na definição de parâmetros que pretende configurar (a que criou quando instalou o [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] pela primeira vez) ou clique em **Novo** para criar um novo.  
  
3. Na área **Geral** , defina todas as opções para os parâmetros do projeto.  
  
4. Na área **Lista de Preços** , clique em **+** para adicionar uma lista de preços, selecione uma lista de preços na lista pendente **Lista de Preços do Parâmetro do Projeto** e clique em **Guardar**.  
  
5. Clique no botão **Guardar** no canto inferior direito do ecrã.  

> [!NOTE]
> O registo de parâmetro do projeto tem de ser mantido para que o Project Service funcione corretamente. Este registo não deve ser eliminado.

### <a name="see-also"></a>Consulte Também  
 [Configurar recursos](../psa/set-up-resources.md)