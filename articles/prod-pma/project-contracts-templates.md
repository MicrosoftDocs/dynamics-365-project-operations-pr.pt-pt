---
title: Sincronizar contratos de projetos e projetos diretamente de Project Service Automation para Finanças
description: Este artigo descreve o modelo e tarefas subjacentes que são utilizados para sincronizar contratos do projeto e projetos diretamente do Microsoft Dynamics 365 Project Service Automation para o Dynamics 365 Finance.
author: Yowelle
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 62a24f3af823d474cbb4d63f8d079c708256a75e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933874"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance"></a>Sincronizar contratos de projetos e projetos diretamente de Project Service Automation para Finanças 

[!include[banner](../includes/banner.md)]



Este artigo descreve o modelo e tarefas subjacentes que são utilizados para sincronizar contratos do projeto e projetos diretamente do Dynamics 365 Project Service Automation para o Dynamics 365 Finance.

> [!NOTE] 
> Se estiver a utilizar o Enterprise edition 7.3.0, tem de instalar o KB 4074835.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Fluxo de dados para o Project Service Automation para o Finance

> [!NOTE]
> Antes de poder utilizar a solução de integração do Project Service Automation para o Finance, dever estar familiarizado com a funcionalidade Integração de Dados do Dynamics 365.

A solução de integração do Project Service Automation para Finance utiliza a funcionalidade Integração de Dados para sincronizar os dados entre instâncias do Project Service Automation e do Finance. O modelo de integração disponível com a funcionalidade de integração de Dados permite o fluxo de dados sobre contratos de projetos, projetos, itens de contrato do projeto e marcos de itens de contrato do projeto do Project Service Automation para o Finance.

A seguinte ilustração mostra como os dados são sincronizados entre o Project Service Automation e o Finance.

[![Fluxo de dados para a integração do Project Service Automation com o Finance.](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Modelos e tarefas

Para aceder aos modelos disponíveis, no centro de administração do Microsoft Power Apps, selecione **Projetos** e, em seguida, no canto superior direito, selecione **Novo projeto** para selecionar modelos públicos.

Os modelos seguintes e as tarefas subjacentes são utilizados para sincronizar os contratos do projeto e os projetos do Project Service Automation para o Finance:

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a>Integração com Dynamics 365 Project Service Automation v2.x
- **Nome do modelo na integração de dados**: Projetos e contratos (Project Service Automation para Finanças)
- **Nome das tarefas no projeto:**

    - Contratos do projeto (Project Service Automation) para Finanças
    - Projetos (Project Service Automation) para Finanças
    - Linhas de contrato do projeto (Project Service Automation) para Finanças
    - Marcos de linhas de contrato do projeto (Project Service Automation) para Finanças
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>Integração com Dynamics 365 Project Service Automation v3.x
Existe uma alteração de esquema no Project Service Automation que afeta o modelo de marco de item de contrato do Projeto e a utilização da versão v2 do modelo é necessária para integrar a Project Service Automation v3.x com o Dynamics 365.

- **Nome do modelo na integração de dados:** Projetos e Contratos (Project Service Automation 3x para Finanças) - v2
- **Nome das tarefas no projeto:**

    - Contratos do projeto (Project Service Automation) para Finanças
    - Projetos (Project Service Automation) para Finanças
    - Linhas de contrato do projeto (Project Service Automation) para Finanças
    - Marcos de linhas de contrato do projeto (Project Service Automation) para Finanças

Antes de poder ocorrer a sincronização dos contratos de projeto e dos projetos, é necessário sincronizar as contas.

## <a name="entity-set"></a>Conjunto de entidades

| Project Service Automation       | Finanças                                                |
|----------------------------------|--------------------------------------------------------|
| Encomendas                           | Entidade de integração para o contrato de projeto                |
| Projetos                         | Entidade de integração para o projeto                         |
| Linhas de encomenda                      | Entidade de integração para o item de contrato de projeto           |
| Marcos do item de contrato do projeto | Entidade de integração para o marco do item de contrato de projeto |

## <a name="entity-flow"></a>Fluxo de entidades

Os contratos do projeto são geridos no Project Service Automation e sincronizados com o Finance como contratos de projeto. Como parte do modelo de integração, pode definir a fonte de integração no Finance para o contrato do projeto.

Os projetos de tempo e material e de preço fixo são geridos no Project Service Automation e sincronizados para Finanças como projetos. Como parte da integração do modelo, pode definir a fonte de integração para o projeto em Finanças. Atualmente, apenas são apoiados projetos de tempo e material e de preço fixo.


Os itens de contrato são geridos no Project Service Automation e sincronizados com o Finance como regras de faturação de contratos. Se o método de faturação diferir do tipo de projeto predefinido, a sincronização atualiza o tipo de projeto para o projeto da item de contrato e o grupo de projetos.

Os marcos do item de contrato são geridos no Project Service Automation e sincronizados com o Finance como marcos de regra de faturação de contrato.

## <a name="project-service-automation-to-finance-integration-solution"></a>Solução de integração do Project Service Automation para Finance

O campo **ID do contrato de projeto** está disponível na página **Contratos de projeto**. Este campo foi convertido numa chave natural e exclusiva para apoiar a integração.

Quando é criado um novo contrato de projeto, se um valor **ID de contrato de projeto** ainda não existir, é gerido automaticamente ao utilizar uma sequência numérica. O valor é composto por **ORD** seguido por uma sequência de números incrementais e, em seguida, um sufixo de seis caracteres. Segue-se um exemplo: **ORD-01022-Z4M9Q0**.

O campo **Número de projeto** está disponível na página **Projetos**. Este campo foi convertido numa chave natural e exclusiva para apoiar a integração.

Quando é criado um novo projeto, se um valor **Número de projeto** ainda não existir, é gerido automaticamente ao utilizar uma sequência numérica. O valor é composto por **PRJ** seguido por uma sequência de números incrementais e, em seguida, um sufixo de seis caracteres. Segue-se um exemplo: **PRJ-01049-CCNID0**.

Quando a solução de integração Project Service Automation para Finance é aplicada, um script de atualização define o campo **ID do contrato de projeto** para os contratos de projeto existentes e o campo **Número de Projeto** para os projetos existentes no Project Service Automation.

## <a name="prerequisites-and-mapping-setup"></a>Pré-requisitos e configuração do mapeamento

- Antes de poder ocorrer a sincronização dos contratos de projeto e dos projetos, é necessário sincronizar as contas.
- No seu conjunto de ligações, adicione um mapeamento de campos chave de integração para **msdyn\_organizationalunits** para **msdyn\_name \[Nome\]**. Primeiro, poderá ter de adicionar um projeto ao conjunto de ligações. Para mais informações, consulte [Integrar dados no Common Data Service para Aplicações](/powerapps/administrator/data-integrator).
- No seu conjunto de ligações, adicione um mapeamento de campos chave de integração para **msdyn\_projects** para **msdynce\_projectnumber \[Número de Projeto\]**. Primeiro, poderá ter de adicionar um projeto ao conjunto de ligações. Para mais informações, consulte [Integrar dados no Common Data Service para Aplicações](/powerapps/administrator/data-integrator).
- **SourceDataID** para contratos de projeto e projetos pode ser atualizado para um valor diferente ou removido do mapeamento. O valor do modelo predefinido é **Project Service Automation**.
- O mapeamento **PaymentTerms** tem de ser atualizado para refletir os termos de pagamento válidos no Finance. Também pode remover o mapeamento da tarefa do projeto. O mapa de valores predefinidos tem valores predefinidos para os dados de demonstração. A tabela seguinte mostra os valores no Project Service Automation.

    | valor | Description   |
    |-------|---------------|
    | 5     | Líq. a 30 Dias        |
    | 2     | 2% a 10 Dias, Líq. a 30 Dias |
    | 3     | Líq. a 45 Dias        |
    | 4     | Líq. a 60 Dias        |

## <a name="power-query"></a>Power Query

Utilize o Microsoft Power Query para Excel para filtrar dados se as seguintes condições for cumpridas:

- Tem ordens de venda no Dynamics 365 Sales.
- Tem várias unidades organizacionais no Project Service Automation e estas unidades organizacionais serão mapeadas para várias entidades jurídicas no Finance.

Se tiver de utilizar o Power Query, siga estas orientações:

- O modelo Projetos e contratos (PSA para Fin and Ops) tem um filtro predefinido que inclui apenas as ordens de venda do tipo **Item de trabalho (msdyn\_ordertype = 192350001)**. Este filtro ajuda a garantir que os contratos de projeto não são criados para as ordens de venda no Finance. Se criar o seu próprio modelo, terá de adicionar este filtro.
- Crie um filtro Power Query que inclua apenas as organizações de contratos que devem ser sincronizadas com a entidade legal do conjunto de ligações de integração. Por exemplo, os contratos de projeto que tem com a unidade organizacional contratual Contoso US devem ser sincronizados com a entidade jurídica USSI, mas os contratos de projeto que tem com a unidade organizacional contratual Contoso Global devem ser sincronizados com a entidade jurídica USMF. Se não adicionar este filtro ao seu mapeamento de tarefas, todos os contratos de projeto serão sincronizados com a entidade jurídica que está definida para o conjunto de ligações, independentemente da unidade organizacional contratual.

## <a name="template-mapping-in-data-integration"></a>Mapeamento de modelos na Integração de dados

> [!NOTE] 
> Os campos **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState** e **AddressZipCode** não estão incluídos no mapeamento predefinido para contratos de projeto. Pode adicionar os mapeamentos se necessitar que estes dados sejam sincronizados para contratos de projeto.
>
> Os campos **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber** e **ProjectType** não estão incluídos no mapeamento predefinido para projetos. Pode adicionar os mapeamentos se necessitar que estes dados sejam sincronizados para projetos.

As seguintes ilustrações mostram exemplos dos mapeamentos de tarefas do modelo na Integração de Dados. O mapeamento mostra as informações do campo que serão sincronizadas do Project Service Automation para Finance.

[![Mapeamento de modelo de contrato de projeto.](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Mapeamento de modelo de projeto.](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Mapeamento de modelo de itens de contrato de projeto.](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Mapeamento de modelo de marco de item de contrato de projeto.](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>Mapeamento de marcos de item de contrato de projeto no modelo Projetos e Contratos (PSA 3.x para Dynamics) - v2:

[![Mapeamento de marco de item de contrato de projeto com o a versão dois do modelo.](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]