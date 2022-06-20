---
title: Processamento de recibos de despesas
description: Este artigo fornece informações sobre o processamento do reconhecimento ótico de carateres (OCR) para recibos. Esta funcionalidade foi concebida para melhorar a experiência do utilizador quando são criados relatórios de despesas no Microsoft Dynamics 365 Finance.
author: stsporen
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 5a72802e3c52b6a9e55ac779aa36c32072dc8b8b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911426"
---
# <a name="expense-receipt-processing"></a>Processamento de recibos de despesas

A entrada de despesas foi reforçada através da introdução do processamento de reconhecimento de caracteres óticos (OCR) para obter receitas. Esta funcionalidade destina-se a melhorar a experiência do utilizador ao criar relatórios de despesas.

## <a name="key-features"></a>Funcionalidades principais

- O nome do comerciante, a data e o valor total são extraídos dos recibos.
- A funcionalidade tenta combinar recibos não ligados a transações de despesas não associadas.
- Os utilizadores podem criar transações de despesas inseridas manualmente a partir de recibos.

## <a name="usage-examples"></a>Exemplos de utilização

Para anexar automaticamente recibos que incluam transações de cartões de crédito quando um relatório de despesas é criado, faça o seguinte:

  1. Abra área de trabalho da **gestão de despesas**.
  2. No separador **Recibos**, verifique se existem recibos não anexados. Também pode carregar recibos no separador **Recibos**.
  3. No separador **Despesas**, verifique se existem despesas não anexadas. Normalmente, o Administrador de despesas importa estas despesas do cartão de crédito do prestador.
  4. Selecione **novo relatório de despesas**. Note que agora também pode incluir despesas e recibos quando criar um relatório de despesas. Se adicionar despesas e recibos, é desencadeada uma correspondência automática dos recibos com as despesas.

Para criar uma despesa, ou fazer corresponder a uma despesa de um recibo, faça o seguinte:

  1. Num relatório de despesas, no separador **Recibos**, anexe um recibo selecionando **Adicionar recibos**.
  2. Por baixo da imagem carregada do recibo, observe as opções **Criar** e **Corresponder**.

      - Selecione **Criar** para criar uma transação de despesas inserida manualmente e preencher os valores extraídos do recibo.
      - Se selecionar **Corresponder**, o sistema tenta corresponder uma despesa existente ao recibo.

## <a name="installation"></a>Instalação

Esta funcionalidade funciona em combinação com a funcionalidade **Relatórios de despesas reimaginados** para ajudar a simplificar a experiência de despesas. Esta funcionalidade está disponível apenas para ambientes Camada 2+, que são Sandbox e Produção.

Para utilizar estas capacidades de despesas avançadas, instale o suplemento Serviço de Gestão de Despesas para o Microsoft Dynamics 365 Finance e ative as funcionalidades da sua instância. Pode aceder ao suplemento do seu projeto em Microsoft Dynamics Lifecycle Services (LCS).

1. Iniciar sessão no LCS e abrir o ambiente desejado.
2. Aceda a **Todos os detalhes**.
3. Selecione **Manter** ou desloque-se para baixo para FastTab dos **Suplementos do ambiente**.
4. Selecione **Instalar um novo suplemento**.
5. Selecione **Serviço de Gestão de Despesas**.
6. Siga o guia de instalação e concorde com os termos e condições.
7. Selecione **Instalar**.

Na área de trabalho de **Gestão de recursos**, ligue as seguintes funcionalidades:

- Relatórios de despesas reinventados
- Correspondência automática e criar despesas a partir do recibo

Quando liga estas funcionalidades, ocorrem as seguintes ações:

- A área de trabalho existente de **gestão de despesas** é substituída pela nova área de trabalho.
- Um novo item de menu para visibilidade do campo de despesas é adicionado.
- Pode ainda abrir a página de **relatórios de despesas** anteriores ao aceder a **Gestão de Despesas > As minhas despesas > Relatórios de despesas**.
- Fluxos de trabalho e quaisquer aprovações ainda o levam à página de relatórios de despesas existentes.
- Os recibos serão processados através do Microsoft Azure Cognitive Services, e os metadados serão extraídos e adicionados.
- Uma opção é adicionada que lhe permite criar um relatório de despesas que inclui recibos não anexados.
- Uma opção que é adicionada aos relatórios de despesas permite criar uma linha de despesas a partir de um recibo, ou tenta combinar um recibo existente com uma linha de despesas existente.

Para obter mais informações sobre os relatórios de despesas reimaginados, consulte [Relatórios de despesas reimaginados](ExpenseWorkspaceNew.md).

## <a name="frequently-asked-questions"></a>Perguntas mais frequentes

**A Microsoft usa os meus dados para os seus modelos?**

Não, a Microsoft construiu um modelo de aprendizagem automática geral para o seu serviço de processamento de recibos. Este modelo não se baseia nos recibos que envia.

**Onde é que esta funcionalidade está disponível e processada?**

Atualmente, os Estados Unidos são compatíveis.

**Para onde vão os meus recibos?**

A contabilidade entrará em contacto com os Serviços Cognitivos para extrair os dados de campo. Os Serviços Cognitivos conservarão uma cópia do seu recibo durante 24 horas enquanto ocorre o processamento. Após o processamento estar concluído, os Serviços Cognitivos removerão o recibo. Os recibos ainda estão guardados na Contabilidade.

Para obter mais informações, consulte [Ativar o compreensão do recibo com a nova capacidade do Reconhecedor de Formato](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).


[!INCLUDE[footer-include](../includes/footer-banner.md)]