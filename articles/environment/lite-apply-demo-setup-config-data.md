---
title: Aplicar dados de configuração da demonstração
description: Este tópico fornece informações sobre como aplicar dados de configuração da demonstração para o Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42e02f393e89d20b2a462645f519a3792bee8f2f
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949017"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a>Aplicar os dados de configuração da demonstração para a a implementação do Project Operations lite - oportunidade potencial para fatura pró-forma

_**Implementação leve - oportunidade potencial para fatura pró-forma_

1. Transferir o [Pacote de Dados Mestres](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip). 
2. Navegue para a pasta *ProjOpsDemoDataSetupAndMaster - Integrated CMT* e execute o ficheiro executável *DataMigrationUtility*.
3. Na página 1 do Assistente de Migração da Configuração do Common Data Service (CMT), selecione **Importar Dados** e, em seguida, selecione **Continuar**.

![Migração da Configuração](./media/1ConfigurationMigration.png)

4. Na página 2 do Assistente do CMT, selecione **Office 365** como **Tipo de Implementação**.
5. Selecione as caixas de verificação **Apresentar lista de organizações disponíveis** e **Mostrar Avançadas**.
6. Selecione a região do seu inquilino, introduza as suas credenciais e, em seguida, selecione **Iniciar Sessão**.

![Início de Sessão da Configuração](./media/2ConfigurationSignin.png)

7. Na página 3, a partir da lista de Organizações no Inquilino, selecione a organização para a qual pretende importar os dados de demonstração e, em seguida, selecione **Iniciar Sessão**.
8. Na página 4, selecione o ficheiro zip, *MasterAndSetupData* a partir da pasta descompactada *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.

![Ficheiro Zip](./media/3ZipFile.png)

![Selecionar um ficheiro](./media/4SelectAFile.png)

9. Depois de selecionado o ficheiro zip, selecione **Importar Dados**.

![Importar Dados](./media/5ImportData.png)

10. A importação será executada durante aproximadamente 2 a 10 minutos, consoante a velocidade da sua rede. Depois de concluída, saia do Assistente de CMT. 
11. Contacte a sua organização para obter dados nas seguintes 20 entidades:

- Moeda
- Unidade Organizacional
- Contacto
- Grupo de Impostos
- Grupo de Clientes
- Unidade
- Grupo de Unidades
- Lista de Preços
- Lista de Preços do Parâmetro do Projeto
- Frequência da Fatura
- Detalhe de Frequência de Fatura
- Categoria de Recurso Reservável
- Categoria de Transação
- Categoria de Despesa
- Preço da Função
- Preço de Categoria de Transação
- Característica
- Recurso Reservável
- Associação de categorias de recurso reservável
- Característica de Recurso Reservável

![Concluir Importação](./media/6CompleteImport.png)
