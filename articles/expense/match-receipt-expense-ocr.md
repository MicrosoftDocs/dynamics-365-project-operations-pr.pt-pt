---
title: Corresponder um recibo à uma despesa com OCR
description: Este tópico fornece informações sobre o processamento de reconhecimento de caracteres óticos (OCR) para obter recibos.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 02c1bafbe907a657689b610ae792f88085320903
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897015"
---
# <a name="match-a-receipt-to-an-expense-using-ocr"></a>Corresponder um recibo à uma despesa com OCR

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

A entrada de despesas foi reforçada através da introdução do processamento de reconhecimento de caracteres óticos (OCR) para obter receitas. Esta funcionalidade destina-se a melhorar a experiência do utilizador ao criar relatórios de despesas.

## <a name="key-features"></a>Funcionalidades principais

- O sistema extrai o nome do comerciante, a data e o valor total dos recibos.
- O sistema tentará combinar recibos não ligados a transações de despesas não associadas.
- Pode criar transações de despesas inseridas manualmente a partir de recibos.

## <a name="attach-receipts-to-an-expense-report"></a>Anexar recibos a um relatório de despesas

Para anexar automaticamente recibos que incluam transações de cartões de crédito quando um relatório de despesas é criado, siga os passos seguintes.

  1. Abra área de trabalho da **gestão de despesas**.
  2. No separador **Recibos**, verifique se existem recibos não anexados. Também pode carregar recibos no separador **Recibos**.
  3. No separador **Despesas**, verifique se existem despesas não anexadas. Normalmente, o Administrador de despesas importa estas despesas do cartão de crédito do prestador.
  4. Selecione **novo relatório de despesas**. Note que agora também pode incluir despesas e recibos quando criar um relatório de despesas. Se adicionar despesas e recibos, é desencadeada uma correspondência automática dos recibos com as despesas.

## <a name="create-or-match-receipts-to-an-expense-report"></a>Criar ou fazer corresponder recibos a um relatório de despesas
Para criar uma despesa, ou fazer corresponder a uma despesa de um recibo, complete os seguintes passos.

  1. Num relatório de despesas, no separador **Recibos**, anexe um recibo selecionando **Adicionar recibos**.
  2. Por baixo da imagem carregada do recibo, observe as opções **Criar** e **Corresponder**.

      - Selecione **Criar** para criar uma transação de despesas inserida manualmente e preencher os valores extraídos do recibo.
      - Se selecionar **Corresponder**, o sistema tenta corresponder uma despesa existente ao recibo.

## <a name="installation"></a>Instalação

Para utilizar estas capacidades de despesas avançadas, instale o suplemento do Serviço de Gestão de Despesas para o Microsoft Dynamics 365 Finance, e ligue as funcionalidades na sua instância. Pode aceder ao suplemento do seu projeto em Microsoft Dynamics Lifecycle Services (LCS).

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

## <a name="frequently-asked-questions"></a>Perguntas mais frequentes

**A Microsoft usa os meus dados para os seus modelos?**

Não, a Microsoft construiu um modelo de aprendizagem automática geral para o seu serviço de processamento de recibos. Este modelo não se baseia nos recibos que envia.

**Onde é que esta funcionalidade está disponível e processada?**

Atualmente, os Estados Unidos são compatíveis.

**Para onde vão os meus recibos?**

A contabilidade entrará em contacto com os Serviços Cognitivos para extrair os dados de campo. Os Serviços Cognitivos conservarão uma cópia do seu recibo durante 24 horas enquanto ocorre o processamento. Após o processamento estar concluído, os Serviços Cognitivos removerão o recibo. Os recibos ainda estão guardados na Contabilidade.

Para obter mais informações, consulte [Ativar o compreensão do recibo com a nova capacidade do Reconhecedor de Formato](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).
