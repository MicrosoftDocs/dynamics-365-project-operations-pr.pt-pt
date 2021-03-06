---
title: Aprovisionar um novo ambiente
description: Este tópico fornece informações sobre como aprovisionar um novo ambiente do Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 45700371c50e3b5a840df45fc24fa8a5b4584b61
ms.sourcegitcommit: 87b7a8d793c19c50f3765b8d788cde24a6a0ca24
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949376"
---
# <a name="provision-a-new-environment"></a>Aprovisionar um novo ambiente

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Este tópico fornece informações sobre como aprovisionar um novo ambiente do Dynamics 365 Project Operations para cenários baseados em recursos/não armazenados.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>Ativar o aprovisionamento automatizado do Project Operations num projeto LCS

Utilize os seguintes passos para ativar o fluxo de aprovisionamento automatizado do Project Operations para o seu projeto LCS.

1. Vá para [LCS](https://lcs.dynamics.com/v2) e selecione o mosaico **Gestão de funcionalidades de pré-visualização**.
2. Na lista **Funcionalidade de pré-visualização**, selecione **Project Operations** e selecione **Funcionalidade de pré-visualização ativada** para ativar o Project Operations.

> [!NOTE]
> Este passo é executado apenas uma vez por projeto LCS.

## <a name="provision-a-project-operations-environment"></a>Aprovisionar um ambiente do Project Operations

1. Abra um novo [ambiente de demonstração](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) do Dynamics 365 Finance ou implementação do [ambiente de sandbox/ produção](https://docs.microsoft.com/edynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure). 
2. Percorra o assistente de **Aprovisionamento do ambiente**. 

> [!IMPORTANT]
> Certifique-se de que a versão de aplicação selecionada é a 10.0.13 ou superior.

3. Para aprovisionar o Project Operations, em **Definições avançadas**, selecione **Common Data Service**. 
4. Ative a **Definição do Common Data Service** ao selecionar **Sim** e, em seguida, introduza as informações nos campos obrigatórios:

  - Nome
  - Região
  - Linguagem
  - Moeda
 
5. No campo **Modelo do Common Data Service**, selecione **Project Operations** 

6. Selecione o tipo de ambiente para a sua implementação. Uma avaliação baseada em subscrições permitir-lhe-á implementar um ambiente do CDS durante 30 dias. 

![Definições de Implementação](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> Selecione **Aceitar** para confirmar os temos de serviço e, em seguida, selecione **Concluído** para regressar às definições de implementação.

![Consentimento de Implementação](./media/2DeploymentConsent.png)

7. Preencha os campos obrigatórios restantes no assistente e confirme a implementação. O tempo de aprovisionamento do ambiente varia com base no tipo de ambiente. O aprovisionamento pode demorar até seis horas.

  Depois de a implementação ser concluída com êxito, o ambiente será mostrado como **Implementado**.

8. Para confirmar que o ambiente foi implementado com êxito, selecione **Iniciar sessão** e inicie sessão no ambiente para confirmar.

![Detalhes do ambiente ](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a>Aplicar dados de demonstração do Project Operations Finance (passo opcional)

Aplique os dados de demonstração do Project Operations Finance à versão de serviço 10.0.13 do Cloud Hosted Environment, tal como descrito [neste artigo](resource-apply-finance-demo-data.md).

## <a name="apply-updates-to-the-finance-environment"></a>Aplicar atualizações ao ambiente do Finance

O Project Operations requer um ambiente do Finance com versão de aplicação **10.0.13 (10.0.569.20009)** ou superior.

Poderá precisar de aplicar atualizações de qualidade ao seu ambiente do Finance para receber esta versão.

1. No LCS, na página **Detalhes do ambiente**, na secção **Atualizações Disponíveis**, selecione **Ver Atualização**.

![Ver Atualizações](./media/5ViewUpdates.png)

2. Na página **Atualizações binárias**, selecione **Guardar pacote**.

![Guardar pacote](./media/6SavePackage.png)

3. Clique em **Selecionar tudo** e, em seguida, selecione **Guardar pacote**.

![Rever e guardar atualizações](./media/7ReviewAndSaveUpdates.png)

4. Introduza um nome e uma descrição do pacote e, em seguida, selecione **Guardar**. Consoante a ligação à Internet, este processo poderá demorar algum tempo.

![Carregar pacote para a Biblioteca de Recursos](./media/8UploadPackageToAssetsLibrary.png)

5. Depois de guardar o pacote, selecione **Concluído** e guarde este pacote na Biblioteca de Recursos no seu projeto LCS.

Guardar e validar o pacote pode demorar ~15 minutos.

6. Para aplicar a atualização, navegue para a página **Detalhes do ambiente** no LCS e selecione **Manter** > **Aplicar atualizações**.

![Manter Ambientes](./media/9MaintainEnvironment.png)

7. Na lista de atualizações, selecione o pacote que criou e selecione **Aplicar**.

![Aplicar Atualizações](./media/10ApplyUpdates.png)

A manutenção do ambiente vai demorar algum tempo. Depois de concluída, o ambiente voltará ao estado implementado.

![Ambiente Implementado](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>Estabelecer uma ligação de Escrita Dupla 

1. No seu projeto LCS, vá para a página **Detalhes do ambiente**.
2. Em **Informações do ambiente do Common Data Service**, selecione **Ligação ao CDS for Apps**.
3. Depois de concluída a ligação, selecione novamente **Ligação ao CDS for Apps**. Será redirecionado para a Escrita Dupla no Finance.

![Associar ao CDS](./media/12LinktoCDS.png)

4. Selecione **Aplicar Solução** para aceder às entidades que serão mapeadas na integração.

![Aplicar Soluções](./media/13ApplySolutions.png)

5. Selecione as duas soluções, **Mapa de Entidades de Escrita Dupla do Dynamics 365 Finance and Operations** e **Mapas de Entidades de Escrita Dupla do Dynamics 365 Project Operations**, e selecione **Aplicar**.

![Confirmar Soluções](./media/14ConfirmSolutions.png)

Depois de aplicadas as soluções, as entidades de Escrita Dupla são aplicadas ao ambiente.

![Aplicar Soluções](./media/15ApplyingSolutions.png)

Depois de aplicadas as entidades, todos os mapeamentos disponíveis são listados no ambiente.

![Mapas de Escrita Dupla](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>Atualizar as entidades de dados após a atualização

1. No Finance, vá para a área de trabalho **Gestão de dados**.

![Área de trabalho de gestão de dados](./media/16DataManagement.png)

2. Selecione o mosaico **Parâmetros do marco**.

![Parâmetros do Quadro](./media/17FrameworkParameters.png)

3. Na página **Definições da entidade**, selecione **Atualizar lista de entidades**.

![Atualizar lista de entidades](./media/18RefreshEntityList.png)

A atualização vai demorar aproximadamente 20 minutos. Receberá um alerta quando estiver concluída.

![Atualizar Confirmar](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a>Executar mapas de Escrita Dupla do Project Operations

1. No seu projeto LCS, vá para a página **Detalhes do ambiente**.
2. Em **Informações do ambiente do Common Data Service**, selecione **Ligação ao CDS for Apps**. Depois de selecionar a ligação, será redirecionado para a lista de entidades nos mapeamentos.
3. Inicie os mapas,, conforme descrito na tabela seguinte. Certifique-se de segue a sequência conforme listado.

| **Mapa da Entidade** | **Atualizar entidade** | **Sincronização inicial** | **Mestre para sincronização inicial** | **Executar pré-requisitos** | **Sincronização inicial dos pré-requisitos** |
| --- | --- | --- | --- | --- | --- |
| **Funções de Recursos de Projeto para Todas as Empresas (bookableresourcecategories)** | No | Sim | Common Data Service | No | N/A |
| **Entidades legais (cdm\_empresas)** | No | Sim | Aplicações do Finance and Operations | No | N/A |
| **Valores reais de integração com o Project Operations (msdyn\_valores reais)** | No | No | N/A | Sim | No |
| **Itens de contrato do projeto (salesorderdetails)** | No | No | N/A | No | No |
| **Entidade de integração para as relações de transações do projeto (msdyn\_transactionconnections)** | No | No | N/A | No | N/A |
| **Marcos do item de contrato de integração com o Project Operations (msdyn\_contractlinesscheduleofvalues)** | No | No | N/A | No | N/A |
| **Entidade de integração com o Project Operations para estimativas de despesa (msdyn\_estimateslines)** | No | No | N/A | No | N/A |
| **Entidade de integração com o Project Operations para estimativas de horas (msdyn\_resourceassignments)** | No | No | N/A | No | N/A |
| **Entidade de exportação de despesas do projeto de integração com o Project Operations (msdyn\_despesas)** | Sim | No | N/A | No | N/A |
| **Entidade de integração com o Project Operations para estimativas de horas (msdyn\_resourceassignments)** | Sim | No | N/A | No | N/A |

4. Para atualizar a entidade, selecione o nome do mapa e, em seguida, selecione **Atualizar entidades**. 
5. Prossiga com a execução do mapa após a atualização estar concluída.

![Atualizar Mapa](./media/20RefreshMapping.png)

Antes de ativar o mapa seguinte, verifique se o mapa da tabela está no estado **Em execução**. A execução de mapas com um maior número de pré-requisitos poderá demorar algum tempo.

Para executar um mapa com pré-requisitos, ative o seletor **Mostrar mapas de entidade relacionados**. Se a tabela indicar que **Sincronização inicial dos pré-requisitos** é **Não**, verifique se o sinalizador **Sincronização inicial** está **Desativada** em todos os mapas de pré-requisitos antes de executá-lo.

![Executar Mapa](./media/21RunMap.png)

6. Valide que todos os mapas relacionados com o projeto estão no estado de execução.

![Todos os mapas em execução](./media/22AllMapsRunning.png)

O seu ambiente do Project Operations está agora aprovisionado e configurado.
