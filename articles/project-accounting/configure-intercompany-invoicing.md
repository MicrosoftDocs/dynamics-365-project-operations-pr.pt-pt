---
title: Configurar faturação interempresa
description: Este tópico fornece informações e exemplos sobre a configuração da faturação interempresa para projetos.
author: sigitac
manager: tfehr
ms.date: 11/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: bdb6122d8aba84d2b449f9f17a4093388b585614
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595534"
---
# <a name="configure-intercompany-invoicing"></a>Configurar faturação interempresa

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Complete os seguintes passos para configurar a faturação interempresa para projetos no Dynamics 365 Project Operations. As transações interempresa são transações de tempo e despesas de um contrato de projeto que pertencem a uma empresa ou unidade organizacional, enquanto os recursos no contrato de projeto fazem parte de uma empresa ou unidade organizacional diferente.

## <a name="example-configure-intercompany-invoicing"></a>Exemplo: configurar faturação interempresa

No exemplo seguinte, a Contoso Robotics USA (USPM) é a entidade legal de contração e a Contoso Robotics UK (GBPM) é a entidade legal de concessão. 

1. **Configure a contabilidade interempresa entre entidades legais**. Cada par de entidades legais de contração e de concessão deve ser configurado na página de livro razão Geral da [Contabilidade interempresa](https://docs.microsoft.com/dynamics365/finance/general-ledger/intercompany-accounting-setup).
    
    1. No Dynamics 365 Finance, aceda a **Livro Razão Geral** > **Configuração da publicação** > **Contabilidade interempresa**. Crie um registo com as seguintes informações:

        - **Empresa de origem** = **GBPM**
        - **Empresa de destino** = **USPM**

2. **Configure a relação comercial entre entidades legais**. O registo do cliente que representa a entidade legal de contração deve ser criada na entidade legal de concessão. O registo do fornecedor que representa a entidade legal de concessão deve ser criada na entidade legal de contração.

     1. No Finance, selecione a entidade legal **GBPM**.
     2. Vá a **Contas a receber** > **Cliente** > **Todos os clientes**. Crie um novo registo para a entidade legal **USPM**.
     3. Expanda **Nome**, filtre os registos por **Tipo** e selecione **Entidades legais**. 
     4. Encontre e selecione o registo do cliente para **Contoso Robotics USA (USPM)**.
     5. Selecione **Utilizar correspondência**. 
     6. Selecione o grupo de clientes e, em seguida, guarde o registo.
     7. Selecione a entidade legal **USPM**.
     8. Vá a **Contas a pagar** > **Fornecedores** > **Todos os fornecedores**. Crie um novo registo para a entidade legal **GBPM**.
     9. Expanda **Nome**, filtre os registos por **Tipo** e selecione **Entidades legais**. 
     10. Encontre e selecione o registo do cliente para **Contoso Robotics USA UK (GBPM)**.
     11. Selecione **Utilizar correspondência**, selecione o grupo de fornecedores e, em seguida, guarde o registo.
     12. No registo do fornecedor, selecione **Geral** > **Configurar** > **Interempresa**.
     13. No separador **Relação comercial**, defina **Ativa** como **Sim**.
     14. Selecione a empresa fornecedora **GBPM** e, em **Registo da minha conta**, selecione o registo de cliente que criou anteriormente no procedimento.

3. **Configurar definições interempresa nos parâmetros de Gestão de projetos e contabilística**. 

    1. Selecione a entidade legal **USPM** e vá a **Gestão de projetos e contabilística** > **Configurar** > **Parâmetros de gestão de projetos e contabilística**.
    2. No separador **Interempresa**, selecione a categoria de aprovisionamento para corresponder às faturas do fornecedor que são geradas automaticamente.
    3. Na **Categoria predefinida**, selecione **Recursos interempresa**.
    4. Selecione a entidade legal **GBPM** e vá a **Gestão de projetos e contabilística** > **Configurar** > **Parâmetros de gestão de projetos e contabilística**.
    5. No separador **Interempresa**, selecione uma categoria de projeto predefinida para cada tipo de transação. As categorias de projeto são utilizadas para a configuração fiscal quando a categoria faturada nas transações entre empresas existe apenas na entidade jurídica tomadora. Pode optar por acumular as receitas para as transações entre empresas. A imputação acontece quando as transações são publicadas através do diário de Integração do Project Operations na entidade legal de concessão. O diário é revertido quando a fatura interempresa é publicada.
    6. No grupo **Quando recursos de concessão**, selecione **...** > **Novo**. 
    7. Na grelha, selecione as seguintes informações:

          - **entidade legal de contração** = **GBPM**
          - **Imputar receita** = **Sim**
          - **Categoria de folha de horas predefinida** = **Predefinição – Hora**
          - **Categoria de despesas predefinida** = **Predefinição – despesas**

4. **Definir contas de custos e receitas interempresa na configuração de publicação do Livro Razão**. A conta de receitas interempresa é creditada quando a fatura do cliente interempresa é publicada na entidade legal de concessão. A conta de custos interempresa é debitada quando a fatura do fornecedor pendente correspondente é publicada na entidade legal de contração. Estas contas são configuradas nas entidades legais correspondentes. 
      
     1. No Finance, selecione a entidade legal de contração **USPM**. 
     2. Aceda a **Gestão de projetos e contabilística** > **Configurar** > **Publicar** > **Configuração de publicação do Livro Razão**. 
     3. No separador **Contas de custos**, em **Tipo de conta de livro razão**, selecione **Custo interempresa**. Crie um novo registo com as seguintes informações:
      
        - **entidade legal de concessão** = **GBPM**
        - **Conta principal** = Selecione a conta principal para o custo interempresa
        
     4. Selecionar a entidade legal de concessão **GBPM**. 
     5. Aceda a **Gestão de projetos e contabilística** > **Configurar** > **Publicar** > **Configuração de publicação do Livro Razão**. 
     6. No separador **Contas de receitas**, em **Tipo de conta de livro razão**, selecione **Receita interempresa**. Crie um novo registo com as seguintes informações:

        - **entidade legal de contração** = **USPM**
        - **Conta principal** = Selecione a conta principal para a receita interempresa 

5. **Configurar preços de transferência para o trabalho**. Os preços de transferência interempresa são configurados no Project Operations no Dataverse. Configurar as [taxas de custo do trabalho](../pricing-costing/set-up-labor-cost-rate.md#transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity) e as [taxas de faturação do trabalho](../pricing-costing/set-up-labor-bill-rate.md#transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions) para a faturação interempresa. Os preços de transferência não são suportados para transações de despesas interempresa. O preço de vendas de unidade interorganização será sempre definido para o mesmo valor que o preço de custo de unidade de atribuição de recursos.

      O custo de recursos do programador na Contoso Robotics UK é de 88 GBP por hora. A Contoso Robotics UK vai faturar à Contoso Robotics USA 120 USD por cada hora que este recurso trabalhou em projetos dos EUA. A Contoso Robotics USA vai cobrar ao cliente Adventure Works 200 USD pelo trabalho feito pelo recurso de programação da Contoso Robotics UK.

      1. No Project Operations no Dataverse, vá a **Venda** > **Listas de preços**. Crie uma nova lista de preços de custos chamada **Taxas de custo da Contoso Robotics UK.** 
      2. Na lista de preços de custo, crie um registo com as seguintes informações:
         - **Função** = **Programador**
         - **Custo** = **88 GBP**
      3. Vá a **Definições** > **Unidades organizacionais** e anexe esta lista de preços de custos à unidade organizacional **Contoso Robotics UK**.
      4. Vá à **Vendas** > **Listas de preços**. Crie uma lista de preços de custos chamada **Taxas de custo da Contoso Robotics USA**. 
      5. Na lista de preços de custo, crie um registo com as seguintes informações:
          - **Função** = **Programador**
          - **Empresa de atribuição de recursos** = **Contoso Robotics UK**
          - **Custo** = **120 USD**
      6. Vá a **Definições** > **Unidades organizacionais** e anexe a lista de preços de custos **Taxas de custo da Contoso Robotics USA** à unidade organizacional **Contoso Robotics USA**.
      7. Vá à **Vendas** > **Listas de preços**. Crie uma lista de preços de venda chamada **Taxas de faturação da Adventure Works**. 
      8. Na lista de preços de vendas, crie um registo com as seguintes informações:
          - **Função** = **Programador**
          - **Empresa de atribuição de recursos** = **Contoso Robotics UK**
          - **Taxa de faturação** = **200 USD**
      9. Vá a **Vendas** > **Contratos do projeto** e anexe a lista de preços **Taxas de faturação da Adventure Works** à lista de preços do projeto Adventure Works do contrato do projeto.
