---
title: Aplicar dados de configuração da demonstração – lite
description: Este artigo fornece informações sobre como aplicar dados de preparação e configuração de demonstração para o Project Operations.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9a3a99c326b7ebbdfa859c3298b35e910af0eb2a
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410048"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Aplicar dados de configuração de demonstração para Project Operations – lite 

_**Implementação leve - oportunidade potencial para fatura pró-forma_



## <a name="prerequisites"></a>Pré-requisitos

Antes de iniciar a configuração, tem de ter um ambiente Dataverse aprovisionado para o Dynamics 365 Project Operations.


## <a name="instructions"></a>Instruções

1. Transferir o [Pacote de Dados Mestres](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip). 
2. Navegue para a pasta *ProjOpsSampleSetupData - CE apenas CMT* e execute o ficheiro executável, *DataMigrationUtility*.
3. Na página 1 do Assistente de Migração da Configuração do Common Data Service (CMT), selecione **Importar Dados** e, em seguida, selecione **Continuar**.

    ![Migração da Configuração.](./media/1ConfigurationMigration.png)

4. Na página 2 do Assistente do CMT, selecione **Microsoft 365** como **Tipo de Implementação**.
5. Selecione as caixas de verificação **Apresentar lista de organizações disponíveis** e **Mostrar Avançadas**.
6. Selecione a região do seu inquilino, introduza as suas credenciais e, em seguida, selecione **Iniciar Sessão**.

   ![Início de Sessão da Configuração.](./media/2ConfigurationSignin.png)

7. Na página 3, a partir da lista de Organizações no Inquilino, selecione a organização para a qual pretende importar os dados de demonstração e, em seguida, selecione **Iniciar Sessão**.
8. Na página 4, selecione o ficheiro zip, *SampleSetupAndConfigData* da pasta desempacotada, *ProjOpsSampleSetupData - CE apenas CMT*.

   ![Ficheiro Zip.](./media/3ZipFile.png)

   ![Selecionar um ficheiro.](./media/4SelectAFile.png)

9. Depois de selecionado o ficheiro zip, selecione **Importar Dados**.

   ![Importar dados.](./media/5ImportData.png)

10. A importação será executada durante aproximadamente 2 a 10 minutos, consoante a velocidade da sua rede. Depois de concluída, saia do Assistente de CMT. 
11. Contacte a sua organização para obter dados nas seguintes 18 entidades:

    -   Moeda
    -   Conta
    -   Unidade Organizacional
    -   Contacto
    -   Unidade
    -   Grupo de Unidades
    -   Lista de Preços
    -   Lista de Preços do Parâmetro do Projeto 
    -   Frequência da Fatura
    -   Categoria de Recurso Reservável
    -   Categoria de Transação
    -   Categoria de Despesa
    -   Preço da Função
    -   Preço de Categoria de Transação
    -   Característica
    -   Recurso Reservável
    -   Associação de categorias de recurso reservável
    -   Característica de Recurso Reservável

    ![Concluir Importação.](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
