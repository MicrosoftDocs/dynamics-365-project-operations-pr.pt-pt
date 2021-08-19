---
title: Configurar e aplicar dados de configuração no Common Data Service
description: Este tópico fornece informações sobre como configurar e aplicar dados de configuração no Project Operations.
author: sigitac
ms.date: 05/10/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 26f49ad3b9fb08824071699128f8b907ec98bb54505c6fea3c97288cbaf31633
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986640"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a>Configurar e aplicar dados de configuração no Common Data Service 

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a>Pré-requisitos

Antes de começar a configurar os dados no Common Data Service (CDS), os seguintes pré-requisitos devem ser cumpridos:

1.  Aprovisionar um ambiente CDS e um ambiente Dynamics 365 Finance para o Project Operations.
2.  As informações da entidade jurídica do Dynamics 365 Finance são partilhadas com o ambiente CDS. Isto significa que a entidade **Empresa** tem os seguintes registos da empresa:
  - THPM
  - USPM
  - GBPM

## <a name="install-setup-and-configuration-data"></a>Instalar dados de configuração

1. Transfira, desbloqueie e descompacte o [Pacote de Dados de Configuração](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).
2. Navegue para a pasta descompactada e execute o ficheiro executável *DataMigrationUtility*.
3. Na página 1 do Assistente de Migração da Configuração do Common Data Service (CMT), selecione **Importar Dados** e, em seguida, selecione **Continuar**.

![Migração da Configuração.](./media/1ConfigurationMigration.png)

4. Na Página 2 do Assistente do CMT, selecione **Microsoft 365** como **Tipo de Implementação**.
5. Selecione as caixas de verificação **Apresentar lista de organizações disponíveis** e **Mostrar Avançadas**.
6. Selecione a região do seu inquilino, introduza as suas credenciais e selecione **Iniciar Sessão**.

![Início de Sessão da Configuração.](./media/2ConfigurationSignin.png)

7. Na página 3, a partir da lista de organizações no inquilino, selecione a organização para a qual pretende importar os dados de demonstração e selecione **Iniciar Sessão**.
8. Na página 4, selecione o ficheiro zip *SampleSetupAndConfigData* a partir da pasta descompactada.

![Seleção de ficheiros Zip.](./media/3ZipFile.png)

![Selecionar um ficheiro.](./media/4SelectAFile.png)

9. Depois de selecionado o ficheiro zip, selecione **Importar Dados**.

![Importar Dados.](./media/5ImportData.png)

10. A importação será executada durante aproximadamente 2 a 10 minutos, consoante a velocidade da sua rede. Depois de concluída a importação, saia do Assistente de CMT. 
11. Contacte a sua organização para obter dados nas seguintes 26 entidades:

  - Moeda
  - Tabela de Contas
  - Calendário Fiscal
  - Tipos de Câmbio de Moeda
  - Dia de Pagamento
  - Agenda de Pagamento
  - Prazo de Pagamento
  - Unidade Organizacional
  - Contacto
  - Grupo de Impostos
  - Grupo de Clientes
  - Grupo de Fornecedores
  - Unidade
  - Grupo de Unidades
  - Lista de Preços
  - Lista de Preços do Parâmetro do Projeto
  - Frequência da Fatura
  - Categoria de Recurso Reservável
  - Categoria de Transação
  - Categoria de Despesa
  - Preço da Função
  - Preço de Categoria de Transação
  - Característica
  - Recurso Reservável
  - Associação de categorias de recurso reservável
  - Característica de Recurso Reservável

![Concluir Importação.](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a>Atualizar configurações do Project Operations

1. Navegye para o ambiente CE. Pode encontrá-lo ao abrir o [Centro de Administração do Power Platform](https://admin.powerplatform.microsoft.com/environments), selecionar o ambiente e, em seguida, selecionar **Abrir Ambiente**. 

![Abrir Ambiente.](./media/7OpenEnvironment.png)

2. Vá para **Projetos** > **Recursos** e, em seguida, selecione **Novo** para criar um recurso reservável para o seu utilizador.

![Recursos Reserváveis.](./media/8BookableResources.png)

3. No separador **Geral**, selecione o seu utilizador administrador. Verifique se o fuso horário corresponde àquele em que está. 

![Novo Recurso Reservável.](./media/9NewBookableResource.png)

4. No separador **Agendamento**, no campo **Empresa**, escolha a empresa **USPM** e, em seguida, selecione **Guardar**. 

![Separador Agendamento.](./media/10SchedulingTab.png)

5. Selecione o separador **Horas de trabalho**.  

![Horas de Trabalho.](./media/11WorkHours.png)

6. Faça duplo clique em qualquer valor no calendário e selecione **Editar** > **Todos os eventos na série**. 

![Calendário de Trabalho.](./media/12WorkCalendar.png)

7. Altere as horas de trabalho para um dia de trabalho de oito (8) horas, marque os fins de semana como dias de descanso e certifique-se de que o fuso horário corresponde ao seu. 
8. Selecione **Guardar e fechar**.

![Atualizar Calendário.](./media/13UpdateCalendar.png)

9. Vá para **Definições** > **Modelos de calendário** e selecione **Novo**.
 
 ![Modelos de Calendário.](./media/14CalendarTemplates.png)
 
 10. Introduza um nome, selecione o recurso de modelo que criou e, em seguida, selecione **Guardar**. 
 
 ![Guardar Modelo de Calendário.](./media/15SaveCalendarTemplate.png)
 
 11. Vá para **Parâmetros** e faça duplo clique no registo. 
 
 ![Parâmetros do Projeto.](./media/16ProjectParameters.png)
 
12. Atualize os seguintes campos:

 - **Empresa predefinida**: USPM
 - **Unidade Organizacional Predefinida**: Contoso Robotics Global
 - **Frequência da Fatura**: Sétimo e Último dia
 - **Modelo de horas de trabalho**: altere para o modelo que criou.

13. Selecione **Guardar**. 

![Parâmetros do Projeto Atualizados.](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
