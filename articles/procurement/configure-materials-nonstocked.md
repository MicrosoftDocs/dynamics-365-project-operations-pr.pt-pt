---
title: Configure materiais não armazenados e faturas pendentes do fornecedor
description: Esta tópico explica como permitir materiais não armazenados e faturas pendentes do fornecedor.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9b55d959228062fc3577cf7f12d8926f51e9791f98c73fdc4b78251312a8a77a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003245"
---
# <a name="configure-non-stocked-materials-and-pending-vendor-invoices"></a>Configure materiais não armazenados e faturas pendentes do fornecedor

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

## <a name="minimum-version-requirement"></a>Requisito de versão mínima

A utilização de materiais não armazenados e faturas pendentes de fornecedores para Dynamics 365 Project Operations cenários baseados em não armazenados/recursos requer as seguintes versões:

Soluções Dynamics 365 Dataverse:

- Project Operations – 4.9.0.221 ou superior
- Solução de orquestração de aplicação de dupla escrita - 2.2.2.23 ou superior

Dynamics 365 Finance:
- 10.0.18 (10.0.793.52) ou superior. Certifique-se de que o seu ambiente de Finanças está atualizado e todas as atualizações de qualidade são aplicadas para satisfazer os requisitos mínimos de versão.

## <a name="run-dual-write-maps-for-non-stocked-materials-and-vendor-invoice-integration"></a>Executar mapas de escrita dupla para materiais não armazenados e integração de faturas de fornecedor

Esta secção fornece informações sobre os mapas específicos necessários para materiais não armazenados e faturas do fornecedor. Verifique se os mapas de pré-requisitos listados no tópico [Aprovisionar um novo ambiente](../environment/resource-provision-new-environment.md#run-project-operations-dual-write-maps) estão em execução no seu ambiente.

1. Vá aos Lifecycle Services (LCS), navegue para o seu projeto LCS e vá à página de **Detalhes do Ambiente**.
2. Na secção de **Common Data Service Informação de ambiente**, selecione **Ligar a CDS for Apps**. Depois de selecionar a ligação, será redirecionado para a lista de entidades nos mapeamentos.
3. Certifique-se de que os seguintes mapas estão a funcionar. Se não estiverem a funcionar, inicie-os e certifique-se de incluir todos os mapas de tabela relacionados.

    - CDS lançou produtos distintos (produtos)
    - Fornecedores v2 (msdyn_vendors)
    - Tabela do Project Operations para estimativas de materiais (msdyn_estimatelines)
    - Entidade de exportação de faturas de projeto de integração de projetos do Project Operations (msdyn_projectvendorinvoices)
    - Entidade de exportação de linhas de faturas de projeto de integração de projetos do Project Operations (msdyn_projectvendorinvoicelines)
    - Valores reais de integração com o Project Operations (msdyn_actuals). Certifique-se de que está a executar a versão do mapa 1.0.0.14 ou superior. Pode ver a versão ativa do mapa na coluna **Versão** na página **Escrita dupla**. Pode ativar uma nova versão do mapa selecionando a **versão do mapa de tabela** e, em seguida, guardar a versão selecionada.

Se estiver a utilizar dados de demonstração padrão, poderá também ter de parar e reiniciar os seguintes mapas de entidades com sincronização inicial:
  - Dias de pagamento CDS V2 (msdyn_paymentdays)
  - Horário de pagamento (msdyn_paymentschedules)
  - Condições de pagamento (msdyn_paymentterms)
  - Grupos de fornecedores (msdyn_vendorgroups)
  - Unidades (uom)

> [!NOTE]
> A sincronização inicial para grupos e unidades de fornecedores pode falhar nalguns registos na demo conjunto de dados existente. Pode ignorar as falhas, uma vez que não o impedirão de usar dados de demonstração com o Project Operations.

## <a name="configure-prerequisites-in-dataverse"></a>Configurar pré-requisitos em Dataverse

### <a name="activate-workflow-to-create-accounts-based-on-vendor-entity"></a>Ativar fluxo de trabalho para criar contas com base na entidade fornecedora

A solução Orquestração Escrita Dupla proporciona [Integração mestra aos Fornecedores](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-mapping). Como pré-requisito para esta funcionalidade, os dados do fornecedor devem ser criados na entidade **Contas**. Ative um processo de fluxo de trabalho do modelo para criar fornecedores na tabela **Contas**, tal como descrito em [Alternar entre os desenhos do fornecedor](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-switch).

### <a name="set-products-to-be-created-as-active"></a>Definir produtos a serem criados como ativos

Os materiais não armazenados devem ser configurados como **Produtos libertados** em Finanças. A solução Orquestração em Escrita dupla proporciona uma [integração de produtos out-of-the-box para o catálogo de produtos Dataverse](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/product-mapping). Por defeito, os produtos das Finanças são sincronizados para Dataverse num projeto de rascunho. Para sincronizar o produto para um estado ativo para que possa ser diretamente utilizado em documentos de utilização de materiais ou faturas pendentes do fornecedor, vá para **Sistema** > **Administração** > **Administração de sistema** > **Definições de sistema** e, no separador **Vendas**, defina **Criar produtos em estado ativo** para **Sim**.

## <a name="configure-prerequisites-in-finance"></a>Configurar pré-requisitos em Finanças

### <a name="enable-the-feature-key-for-pending-vendor-invoices"></a>Ativar a chave de funcionalidades para faturas pendentes do fornecedor

Complete os seguintes passos para permitir que a funcionalidade adicione detalhes do projeto em linhas de fatura pendentes do fornecedor.

1. Em Finanças, vá à área de trabalho **Gestão de funcionalidades**.
2. Na lista de funcionalidades, encontre a funcionalidade **Ativar as faturas pendentes do fornecedor no Project Operations para cenários baseados em recursos/não armazenados** e selecione **Ativar**.

### <a name="define-category-groups-and-project-categories-for-items"></a>Definir grupos de categorias e categorias de projetos para itens

Configure pelo menos um grupo de categoria para o tipo de transação **Item** e, pelo menos, uma categoria de projeto usando este grupo. Para obter mais informações, consulte [Configurar categorias de projetos](../project-accounting/configure-project-categories.md#category-groups).

Verifique os perfis de custos e receitas do projeto e configure a definição da publicação de livro-razão para transações de artigos. Para mais informações, consulte [Configurar Gestão contabilística para projetos faturáveis](../project-accounting/configure-accounting-billable-projects.md).

### <a name="set-up-a-write-in-product"></a>Configurar um produto de escrita

No Project Operations é possível registar estimativas e utilização de materiais para produtos de catálogo configurados no catálogo de produtos lançados e para produtos de escrita. A utilização de produtos de escrita requer um único produto lançado que esteja configurado em Finanças para este fim. Complete os seguintes passos para configurar um produto de inscrição. Repita estes passos em cada entidade jurídica que está a utilizar o Project Operations para cenários de recursos/não armazenados.

1. Em Finanças, vá a **Gestão de informação de produto** > **Produtos** > **Produtos lançados** e selecione **Novo**.
2. No campo **Tipo de produto**, selecione **Item** e no campo **Subtipo de Produto**, selecione **Produto**.
3. Introduza o número do produto (WRITEIN) e o nome do produto (Produto de escrita).
4. Selecione o grupo de modelos de artigos. Certifique-se de que o grupo de modelos de artigos selecionados tem o campo de **produtos armazenados da política de inventário** definido como **Falso**.
5. Selecione valores nos campos **Grupo de artigos**, **Grupo de dimensão de armazenamento** e **Deteção de movimentos de dimensão de grupo**. Utilize a **Dimensão de armazenamento** apenas para **Local** e, no campo **Dimensões de seguimento**, selecione **Nenhum**.
6. Selecione valores nos campos **Unidade de Inventário**, **Unidade de compra** e **Unidade de vendas** e, em seguida, guarde as suas alterações.
7. No separador **Plano**, defina as definições de ordem predefinidos e no separador **Inventário**, defina o local e o armazém predefinidos.
8. Vá à **gestão de projetos e gestão contabilística** > **Configuração** > **Gestão de projetos e parâmetros de gestão contabilística** e abra **Project Operations no Dynamics 365 Dataverse**. 
9. No separador **Materiais**, no campo do **produto de escrita**, selecione o produto que criou.
10. No seu ambiente Dataverse, no mapa do site, abra a entidade **Produtos** e encontre o registo do produto de inscrição. 
11. Abra os detalhes do recorde e configure o estado do produto para **Retirado**. Este estado do produto impede qualquer pessoa de utilizar acidentalmente este registo diretamente em estimativas de materiais e documentos de utilização.

### <a name="set-up-a-procurement-integration-account"></a>Criar uma conta de integração de aquisições

A conta de integração de aquisições é utilizada como uma conta de compensação ao publicar uma fatura pendente do fornecedor com linhas atribuídas a um projeto.

Quando o sistema regista uma fatura pendente do fornecedor, esta conta é utilizada para o valor do custo do projeto. Os detalhes da fatura do fornecedor são processados no Dataverse e é criado um projeto correspondente de valores reais. A informação dos valores reais do projeto é adicionada ao diário Integração do Project Operations. Ao publicar o diário de integração, o valor é apurado da conta de integração de aquisições e registado ao custo do projeto.

1. Para configurar a conta de integração de aquisições, vá a **Gestão de projetos e gestão contabilística** > **Configuração** > **Gestão de projetos e parâmetros de gestão contabilística** e abra **Project Operations no Dynamics 365 Dataverse**. 
2. Selecione o separador **Materiais** e selecione um valor no campo **Conta de integração de Aquisições**.

#### <a name="set-up-project-category-defaults-for-an-item"></a>Configurar as predefinições da categoria de projeto para um artigo

1. Em Finanças, vá à **gestão de projetos e gestão contabilística** > **Configuração** > **Gestão de projetos e parâmetros de gestão contabilística** e abra **Project Operations no Dynamics 365 Dataverse**. 
2. No separador **Predefinições da categoria de projeto**, no campo **Artigo**, selecione um valor. Esta categoria de projeto é utilizada para transações materiais se a categoria do projeto não tiver sido definida no registo de valores reais do projeto.
