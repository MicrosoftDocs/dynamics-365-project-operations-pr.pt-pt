---
title: Requisitos de itens para contratos de projeto com várias origens de fundos
description: Este artigo fornece informações sobre como configurar e utilizar requisitos de itens com várias origens de financiamento.
author: sigitac
ms.date: 05/04/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: a54ca1ec5e78d9d0af7b67914f6a63154c7347d3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931206"
---
# <a name="item-requirements-for-project-contracts-with-multiple-funding-sources"></a>Requisitos de itens para contratos de projeto com várias origens de fundos

_**Aplica-se a:** Project Operations para cenários baseados em Stock/Produção_

Alguns contratos para entregas baseadas em projetos podem exigir várias origens de fundos. Este artigo explica como selecionar e configurar as origens de fundos pretendidas quando são necessárias várias origens para um projeto ou contrato de projeto.

## <a name="terminology"></a>Terminologia

- **Origem de fundos** – A entidade que financia o trabalho do contrato do projeto. Esta entidade pode ser uma organização interna ou uma conta de faturação externa (cliente ou concessão).
- **Cliente do projeto** – A entidade a quem o trabalho do projeto é entregue.
- **Conta da fatura** – A entidade externa que paga pelo trabalho do projeto.

## <a name="example"></a>Exemplo

A Contoso venceu um contrato de renovação de equipamento com dois dos seus clientes: Adatum US e Adatum Corporate. O contrato inclui serviços de hardware e instalação que serão entregues à Adatum US (o cliente do projeto). O hardware será financiado pela Adatum Corporate (conta de faturação 1) e o trabalho de instalação será financiado pela Adatum US (conta de faturação 2).

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Configurar regras predefinidas da conta de faturação para os requisitos de item

### <a name="prerequisites"></a>Pré-requisitos

- É necessário o Microsoft Dynamics 365 Finance and Operations **versão 10.0.27 ou posterior** para a utilização dos requisitos de item que tenham várias contas de fatura.
- O seu administrador de sistema deve ativar a característica **Permitir requisitos de itens com várias origens de fundos para cenários com stock/baseados na produção no Project Operations** na área de trabalho **Gestão de funcionalidades**.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>Configurar as regras predefinidas da conta de faturação

Para configurar as regras predefinidas para a conta de faturação, siga estes passos.

1. Vá para **Gestão de projetos e contabilística** \> **Configurar** \> **Parâmetros da Gestão de projetos e contabilística**.
1. No separador **Geral**, na secção **Requisitos de ordens de venda e itens**, defina a opção **Permitir projetos com várias origens de fundos** como **Sim**.
1. No campo **Cliente predefinido**, especifique de onde vem o cliente de entrega do projeto no requisito de item por predefinição:

    - **A partir da origem de fundos** – O cliente de entrega de projeto predefinido é a origem de fundos. Se estiverem associadas várias origens de fundos ao contrato do projeto, será utilizada a primeira origem de fundos na lista.
    - **A partir do projeto** – O cliente de entrega de projeto predefinido vem do cliente que está selecionado no campo **Conta de registo do projeto**.

1. Opcional: definir ou alterar a conta de faturação predefinido nos dados do projeto:

    1. Aceda a **Gestão de projetos e contabilidade** \> **Projetos** \> **Todos os projetos** e abra os detalhes do registo do projeto.
    2. No separador **Geral**, defina ou atualize o campo **Conta de faturação predefinida**. A conta que especificar será utilizada como conta de faturação predefinida para os novos requisitos de item criados para o projeto. Se deixar o campo em branco, será utilizada a conta de faturação da primeira origem de fundos do contrato do projeto como predefinida. No entanto, os utilizadores poderão alterar a conta quando guardarem o registo.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Selecionar a conta de faturação a utilizar quando cria um requisito de item

Para selecionar a conta de faturação a utilizar quando cria um requisito de item, siga estes passos.

1. Aceda a **Gestão de projetos e contabilidade** \> **Projetos** \> **Todos os projetos** e selecione o registo do projeto.
1. No separador **Plano**, selecione **Requisitos de itens**.
1. Crie um novo registo de requisito de item.

    - Por predefinição, o campo **Conta de faturação** no registo é definido como a conta de faturação definida para o projeto. Pode alterar o valor do campo **Conta de faturação** e, em seguida, guardar o registo. Depois de o registo ser guardado, já não pode atualizar o valor da **Conta de faturação**. Se tiver de atualizar o valor **Conta de faturação** para o requisito de item, elimine o requisito de item existente e, em seguida, crie um novo que tenha o valor pretendido.
    - Por predefinição, o campo **Cliente** para o requisito de item é definido com base no valor **Cliente predefinido** que está definido na página **Parâmetros de gestão de projetos e contabilidade**.

    Quando o registo de requisito de item é guardado, o sistema associa-o ao registo do cabeçalho **Ordem de vendas do requisito de item**. Se nenhum cabeçalho da ordem de vendas aberto tiver a conta de faturação selecionada, o sistema vai criar uma e associar a linha de requisito de item à mesma.

> [!NOTE]
> Os requisitos de item são sempre totalmente faturados na conta de faturação que está definida no registo. Atualmente, o sistema não suporta regras de alocação de fundos que tenham requisitos de itens e não vai dividir a publicação com base na configuração de regras de alocação de fundos.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Criar um requisito de item a partir de um registo de previsão de itens

Para criar um requisito de item a partir de um registo de previsão de itens, siga estes passos.

1. Aceda a **Gestão de projetos e contabilidade** \> **Projetos** \> **Todos os projetos** e selecione o registo do projeto.
1. No separador **Plano**, selecione **Previsão de itens**.
1. Crie um novo registo de previsão de item.
1. Opcional: no separador **Projeto**, no campo **Origem de fundos**, selecione a conta de faturação pretendida.
1. Selecione **Criar requisito de item** e confirme a mensagem que recebe.

    > [!NOTE]
    > O sistema copia o valor da **Origem de fundos** do registo de previsão de itens para o registo de requisito de item criado recentemente.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Conta de faturação predefinida quando o sistema cria automaticamente um requisito de item a partir de uma linha de encomenda de compra

Se a opção **Criar requisito de item** estiver definida como **Sim** na página **Parâmetros de gestão de projetos e contabilidade**, o sistema cria automaticamente o requisito de item quando uma nova linha de encomenda de compra do projeto é guardada. Por predefinição, os campos **Conta de faturação** e **Requisito de item** são definidos para o valor do campo **Conta de faturação predefinida** no registo do projeto. Atualmente, o sistema não suporta a atualização nem a alteração da conta de faturação para os dados deste tipo.
