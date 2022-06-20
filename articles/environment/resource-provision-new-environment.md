---
title: Aprovisionar um novo ambiente
description: Este artigo fornece informações sobre como aprovisionar um novo ambiente do Project Operations.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9cc3dafd6a2b6f92b585643c5d43ab52a3faf59e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931620"
---
# <a name="provision-a-new-environment"></a>Aprovisionar um novo ambiente

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_



Este artigo fornece informações sobre como aprovisionar um novo ambiente do Dynamics 365 Project Operations para cenários baseados em recursos/não abastecidos.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>Ativar o aprovisionamento automatizado do Project Operations num projeto LCS

Utilize os seguintes passos para ativar o fluxo de aprovisionamento automatizado do Project Operations para o seu projeto LCS.

1. Vá para [LCS](https://lcs.dynamics.com/v2) e selecione o mosaico **Gestão de funcionalidades de pré-visualização**.
2. Na lista **Funcionalidade de pré-visualização**, selecione **Funcionalidade Project Operations** e, em seguida, selecione **Funcionalidade de pré-visualização ativada** para ativar o Project Operations.

   > [!NOTE]
   > Este passo é executado apenas uma vez por projeto LCS.

## <a name="provision-a-project-operations-environment"></a>Aprovisionar um ambiente do Project Operations

1. Abra uma nova implementação em [ambiente de demonstração](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) no Dynamics 365 Finance ou [sandbox/ambiente de produção](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure). 
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

     ![Definições de Implementação.](./media/1DeploymentSettings.png)

    > [!IMPORTANT]
    > Selecione **Aceitar** para confirmar os temos de serviço e, em seguida, selecione **Concluído** para regressar às definições de implementação.
    >
    >![Consentimento de Implementação.](./media/2DeploymentConsent.png)

7. Opcional - Aplicar dados de demonstração ao ambiente. Vá a **definições avançadas**, selecione **Personalizar a configuração da base de dados SQL** e defina **Especificar um conjunto de dados para a base de dados de aplicações** para **demonstração**.
8. Preencha os campos obrigatórios restantes no assistente e confirme a implementação. O tempo de provisão do ambiente varia com base no tipo de ambiente. O aprovisionamento pode demorar até seis horas.

   Depois de a implementação ser concluída com êxito, o ambiente será mostrado como **Implementado**.

9. Para confirmar que o ambiente foi implementado com sucesso, selecione **Iniciar sessão** e inicie sessão no ambiente para confirmar.

    ![Detalhes do Ambiente.](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a>Aplicar atualizações ao ambiente do Finance

O Project Operations requer um ambiente do Finance com versão de aplicação **10.0.13 (10.0.569.20009)** ou superior.

Poderá precisar de aplicar atualizações de qualidade ao seu ambiente do Finance para receber esta versão.

1. No LCS, na página **Detalhes do ambiente**, na secção **Atualizações Disponíveis**, selecione **Ver Atualização**.

    ![Ver Atualizações.](./media/5ViewUpdates.png)

2. Na página **Atualizações binárias**, selecione **Guardar pacote**.

    ![Guardar pacote.](./media/6SavePackage.png)

3. Clique em **Selecionar tudo** e, em seguida, selecione **Guardar pacote**.

    ![Rever e guardar atualizações.](./media/7ReviewAndSaveUpdates.png)

4. Introduza um nome e uma descrição do pacote e, em seguida, selecione **Guardar**. Consoante a ligação à Internet, este processo poderá demorar algum tempo.

    ![Carregar pacote para a Biblioteca de Recursos.](./media/8UploadPackageToAssetsLibrary.png)

5. Depois de guardar o pacote, selecione **Concluído** e guarde este pacote na Biblioteca de Recursos no seu projeto LCS.

   Guardar e validar o pacote pode demorar ~15 minutos.

6. Para aplicar a atualização, navegue para a página **Detalhes do ambiente** no LCS e selecione **Manter** > **Aplicar atualizações**.

    ![Manter Ambientes.](./media/9MaintainEnvironment.png)

7. Na lista de atualizações, selecione o pacote que criou e selecione **Aplicar**.

    ![Aplicar Atualizações.](./media/10ApplyUpdates.png)

   A manutenção do ambiente vai demorar algum tempo. Depois de concluída, o ambiente voltará ao estado implementado.

    ![Ambiente Implementado.](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>Estabelecer uma ligação de Escrita Dupla 

1. No seu projeto LCS, vá para a página **Detalhes do ambiente**.
2. Em **Informações do ambiente do Common Data Service**, selecione **Ligação ao CDS for Apps**.
3. Depois de concluída a ligação, selecione novamente **Ligação ao CDS for Apps**. Será redirecionado para a Escrita Dupla no Finance.

    ![Associar ao CDS.](./media/12LinktoCDS.png)

4. Selecione **Aplicar Solução** para aceder às entidades que serão mapeadas na integração.

    ![Aplicar Soluções.](./media/13ApplySolutions.png)

5. Selecione ambas as soluções, **Dynamics 365 Finance e Mapa de entidade de escrita dupla de operações** e **Mapas de entidade de escrita dupla do Dynamics 365 Project Operations** e, em seguida, selecione **Aplicar**.

    ![Confirmar Soluções.](./media/14ConfirmSolutions.png)

    Depois de aplicadas as soluções, as entidades de Escrita Dupla são aplicadas ao ambiente.

    ![Aplicar Soluções.](./media/15ApplyingSolutions.png)

    Depois de aplicadas as entidades, todos os mapeamentos disponíveis são listados no ambiente.

    ![Mapas de Escrita Dupla.](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>Atualizar as entidades de dados após a atualização

1. No Finance, vá para a área de trabalho **Gestão de dados**.

    ![Área de trabalho de gestão de dados.](./media/16DataManagement.png)

2. Selecione o mosaico **Parâmetros do marco**.

    ![Parâmetros do Quadro.](./media/17FrameworkParameters.png)

3. Na página **Definições da entidade**, selecione **Atualizar lista de entidades**.

    ![Atualizar Lista de Entidades.](./media/18RefreshEntityList.png)

A atualização vai demorar aproximadamente 20 minutos. Receberá um alerta quando estiver concluída.

  ![Atualizar Confirmar.](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a>Atualizar as definições de segurança no Project Operations em Dataverse

1. Ir a Project Operations no seu ambiente Dataverse. 
2. Aceda a **Definições** > **Segurança** > **Funções de Acesso**. 
3. Na página de **Funções de segurança**, na lista de funções, selecione **utilizador de aplicações de dupla escrita** e selecione o separador **Entidades Personalizadas**.  
4. Verifique se a função tem permissões de **Leitura** e **Acrescentar a** para as seguintes entidades:
      
      - **Tipo de taxa de cambio de moeda**
      - **Tabela de contas**
      - **Calendário Fiscal**
      - **Livro-razão**
      - **Empresa**
      - **Despesa**

5. Após o direito de acesso ser atualizado, vá a **Definições** > **Segurança** > **Equipas** e selecione a equipa predefinida na vista da equipa do **Proprietário de Negócios Local**.
6. Selecione **Gerir Funções** e verifique se o privilégio de segurança do **utilizador de aplicações de dupla escrita** é aplicado a esta equipa.

## <a name="run-project-operations-dual-write-maps"></a>Executar mapas de Escrita Dupla do Project Operations

1. No seu projeto LCS, vá para a página **Detalhes do ambiente**.
2. Em **Informações do ambiente do Common Data Service**, selecione **Ligação ao CDS for Apps**. Depois de selecionar a ligação, será redirecionado para a lista de entidades nos mapeamentos.
3. Inicie os mapas. Para obter mais informações, consulte [Versões do mapa de escrita dupla do Project Operations](resource-dual-write-maps.md#project-operations-dual-write-maps)
4. Valide que todos os mapas relacionados com o projeto estão no estado de execução.

    ![Todos os Mapas em Execução.](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a>Aplicar dados de configuração no CDS para Project Operations (opcional)

Se tiver aplicado dados de demonstração ao ambiente do Finance, consulte [Configurar e aplicar dados de configuração no Common Data Service para o Project Operations](resource-apply-pro-setup-config-data.md) para aplicar dados de demonstração no ambiente CDS.


O seu ambiente do Project Operations está agora aprovisionado e configurado. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
