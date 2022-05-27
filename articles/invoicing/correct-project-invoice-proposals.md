---
title: Corrigir a gestão contabilística nas propostas de fatura do projeto de rascunho
description: Este tópico explica como ajustar as informações relacionadas com a gestão contabilística numa proposta de fatura de rascunho.
author: sigitac
ms.date: 01/05/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: bf0a3d6b97880920b133cb3b30389adf0c83111c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575088"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Corrigir a gestão contabilística nas propostas de fatura do projeto de rascunho

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Os *detalhes operacionais* das faturas do projeto são mantidos pelo gestor de projeto numa fatura pro forma. Estes detalhes incluem a decisão sobre as horas, as despesas, os materiais ou os marcos que têm de ser faturados, as tarifas, e a aplicação de montantes de adiantamento e de sinal. Depois de confirmar a fatura pro forma original, pode ajustar os detalhes operacionais ao criar e confirmar uma [fatura pro forma de correção](../proforma-invoicing/corrective-invoices.md).

Os *detalhes contabilísticos* para as faturas do projeto são mantidos num documento de fatura orientado para o cliente. Estes detalhes incluem o cálculo do imposto sobre vendas e as dimensões financeiras que são aplicadas à fatura. Esta tópico fornece detalhes sobre como estes detalhes contabilísticos podem ser ajustados numa proposta de fatura do projeto de rascunho.

## <a name="adjust-sales-tax"></a>Ajustar imposto sobre vendas

Os grupos de impostos sobre vendas de artigos e os grupos de impostos sobre vendas de faturação predefinidos podem ser ajustados diretamente no documento da proposta de fatura. Para ajustar estes grupos, selecione **Editar** e, em seguida, em cada linha da proposta de fatura do projeto, introduza um novo valor no campo **Grupo de impostos sobre vendas** ou **Grupo de impostos sobre vendas de artigos**.

## <a name="adjust-financial-dimensions"></a>Ajustar dimensões financeiras

### <a name="header-dimensions"></a>Dimensões do cabeçalho

Por predefinição, as dimensões financeiras da fatura derivam dos registos de transações do projeto não faturados que estão a ser faturados. No entanto, as definições de sistema permitem-lhe utilizar dimensões financeiras no cabeçalho de propostas de fatura do projeto para publicar saldos dos clientes. Para ativar esta funcionalidade, selecione **Permitir atualizações às dimensões do projeto para contas a receber** no separador **Finanças** da página **Parâmetros de gestão de Projeto e contabilidade**.

As dimensões financeiras nos cabeçalhos de fatura podem ser editadas antes de uma fatura ser publicada. Na página **Proposta de fatura do projeto**, mude para a vista **Cabeçalho** e, em seguida, edite os valores no separador **Dimensões financeiras**.

A vista **Cabeçalho** só está disponível depois de o administrador do sistema ativar a funcionalidade **Usar proposta de fatura do Projeto e formulários de diário de fatura com a vista de cabeçalho e linhas** na área de trabalho **Gestão de funcionalidades**. Esta funcionalidade necessita da atualização Finanças 10.0.25 ou posterior.

### <a name="line-dimensions"></a>Dimensões de linha

Não é possível editar as dimensões financeiras diretamente numa linha da proposta de fatura do projeto. Em vez disso, siga estes passos para ajustar as dimensões financeiras numa proposta de fatura do projeto.

1. Na proposta de fatura do projeto, selecione **Eliminar tudo** para remover as linhas da proposta de fatura do projeto.

    O botão **Eliminar tudo** só está disponível depois de o administrador de sistema ativar a funcionalidade **Eliminar linhas da proposta de fatura ao utilizar o Project Operations para cenários baseados em recursos/não em stock** na área de trabalho **Gestão de funcionalidades**.

2. Ajustar as dimensões financeiras:

    - **Transações na conta (marcos de faturação):** vá para **Todos os projetos** \> **Gerir** \> **Transações na conta** e selecione o marco que necessita de ajuste. Em seguida, no separador **Dimensões financeiras**, atualize os valores conforme seja necessário.
    - **Transações de tempo, despesas e materiais:** na página **Transações de projeto publicadas**, selecione **Ajustar a contabilidade** para atualizar as dimensões financeiras.

3. Depois de terminar o ajuste dos valores de dimensão financeira, vá para **Gestão de projetos e contabilística** \> **Periódica** \> **Integração do Project Operations** e selecione **Importar a partir da tabela de transição** para executar o processo periódico. Este processo utiliza os valores atualizados da dimensão financeira para recriar as linhas da proposta de fatura do projeto. Em seguida, os valores atualizados são utilizados no razão auxiliar do projeto e o razão geral quando a fatura do projeto é lançada.
