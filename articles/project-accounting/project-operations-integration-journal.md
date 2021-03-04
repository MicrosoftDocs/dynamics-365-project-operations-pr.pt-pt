---
title: Diário de integração no Project Operations
description: Este tópico fornece informações sobre o trabalho com o diário de Integração no Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ffe3373184c8cd776bf3705fd674bedf221d9b77
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4133416"
---
# <a name="integration-journal-in-project-operations"></a>Diário de integração no Project Operations

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

As entradas de tempo e despesas criam transações de **Valor Real** que representam a vista operacional do trabalho concluído contra um projeto. O Dynamics 365 Project Operations fornece aos contabilistas uma ferramenta para rever as transações e ajustar os atributos contabilísticos, conforme necessário. Após a revisão e os ajustes estarem concluídos, as transações são publicadas no sub-livro razão do Projeto e no livro razão Geral. Um contabilista pode realizar estas atividades através do diário **Integração no Project Operations** (diário **Dynamics 365 Finance** > **Gestão de projetos e contabilística** > **Diários** > **Integração do Project Operations**.

![Fluxo do diário de integração](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Criar registos no diário de Integração do Project Operations

Os registos na diário de Integração do Project Operations são criados através de um processo periódico, **Importar da tabela de teste**. Pode executar este processo indo a **Dynamics 365 Finance** > **Gestão de projetos e contabilística** > **Periódica** > **Integração do Project Operations** > **Importar da tabela de teste**. Pode executar o processo de forma interativa ou configurar o processo para ser executado em fundo, se necessário.

Quando o processo periódico decorre, são encontrados quaisquer valores reais que ainda não foram adicionados ao diário de Integração do Project Operations. É criada uma linha do diário para cada transação real.
O sistema agrupa linhas do diário em diários separados com base no valor selecionado no campo **Unidade de período no diário de Integração do Project Operations** (**Finance** > **Gestão de projetos e contabilística** > **Configuração** > **Parâmetros de gestão de projetos e contabilística**, Project Operations no separador **Dynamics 365 Customer Engagement** _). Os valores possíveis para este campo incluem:

  - _*Dias**: Os valores reais são agrupados por data de transação. Um diário separado é criado para cada dia.
  - **Meses**: Os valores reais são agrupados por mês civil. Um diário separado é criado para cada mês.
  - **Anos**: Os valores reais são agrupados por ano civil. Um diário separado é criado para cada ano.
  - **Todas**: Todas as transações reais estão incluídas no mesmo diário de integração. Se o diário não estiver disponível quando o processo periódico for executado, por exemplo, se o diário estiver em processo de publicação de transações, é criado um novo diário.

As linhas do diário são criadas com base em valores reais de projetos. A lista que se segue inclui algumas das regras de predefinição e transformação mais notáveis:

  - Cada transação real do projeto tem uma linha no diário de Integração do Project Operations. As transações de vendas e de custos e não faturadas para o tipo de faturação de tempo e material são apresentadas em linhas separadas.
  - O campo **Data** representa a data da transação. O campo **Data de contabilidade** representa a data em que a transação é registada no livro razão. Se a data contabilística estiver num [período financeiro fechado](https://docs.microsoft.com/dynamics365/finance/general-ledger/close-general-ledger-at-period-end), e o parâmetro **Definir automaticamente a data contabilística para o período do livro razão aberto** é definido no separador **Financeiro** da página **Parâmetros de gestão de projetos e contabilística**, o sistema ajustará a data contabilística da transação para a primeira data no próximo período de livro razão aberto.
  - O campo **Cupão** mostra o número do cupão para cada transação real. A sequência de números do cupão é definida no separador **Sequências de Número**, na página **Parâmetros de gestão de projetos e contabilística**. Cada linha é atribuída a um novo número. Após o cupão ser publicado, pode ver como o custo e a transação de vendas não faturadas estão relacionados selecionando **Cupões relacionados** na página **Transação do Cupão**.
  - O campo **Categoria** representa uma transação de projeto e assume a predefinição com base na categoria de transação para o valor real do projeto relacionado.
    - Se **Categoria de transações** for definida no valor real do Projeto e existir uma **Categoria de projeto** relacionada numa determinada entidade jurídica, a categoria assume a predefinição desta categoria de projeto.
    - Se **Categoria de transações** não estiver definida no valor real do Projeto, o sistema utiliza o valor no campo **Predefinições da categoria de projeto** no separador **Project Operations no Dynamics 365 Customer Engagement** na página **Parâmetros de gestão de projetos e contabilística**.
  - O campo **Recurso** representa o recurso do projeto relacionado com esta transação. O recurso é utilizado como referência nas propostas de fatura do Projeto para os clientes.
  - O campo **Taxa de câmbio** assume a predefinição da **Taxa de câmbio da moeda** definida no Dynamics 365 Finance. Se faltar a configuração da taxa de câmbio, o processo periódico **Importar do teste** adicionará o registo a um diário e uma mensagem de erro será adicionada ao registo de execução da tarefa.
  - O campo **Propriedade da linha** representa o tipo de faturação nos valores reais do projeto. O mapeamento da propriedade da linha e de tipo de faturação são definidos no separador **Project Operations no Dynamics 365 Customer Engagement** na página **Parâmetros de gestão de projetos e contabilística**.

Apenas os seguintes atributos contabilísticos podem ser atualizados nas linhas do diário de integração do Project Operations:

- **Grupo de impostos sobre vendas de faturação** e **Grupo de impostos de venda de artigos de faturação**
- **Dimensões financeiras** (utilizando a ação **Distribuir montantes**)

As linhas do diário de integração podem ser eliminadas, no entanto, quaisquer linhas não publicadas serão novamente inseridas no diário depois de voltar a executar o processo periódico **Importar de teste**.

Ao publicar o diário de Integração, são criadas transações de sublivro razão de projeto e de livro razão geral. Estes são utilizados na faturação dos clientes a jusante, no reconhecimento de receitas e nos relatórios financeiros.


[!INCLUDE[footer-include](../includes/footer-banner.md)]