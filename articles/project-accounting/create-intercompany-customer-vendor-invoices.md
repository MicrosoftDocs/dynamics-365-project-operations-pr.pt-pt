---
title: Criar faturas de clientes e fornecedores interempresa
description: Este tópico fornece informações sobre como criar faturas de clientes e fornecedores interempresa.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f1560469d2bdbb8e81dc26c16b272c44446ab20a
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595532"
---
# <a name="create-intercompany-customer-and-vendor-invoices"></a>Criar faturas de clientes e fornecedores interempresa

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Um contabilista do projeto numa entidade legal de concessão cria uma fatura de cliente interempresa para os custos do projeto que estão a ser transferidos para a entidade de contração. Após a aprovação e publicação da fatura do cliente interempresa, a entidade legal de concessão envia a fatura interempresa à entidade legal de contração.

O contabilista do projeto para a entidade legal de concessão pode criar um processo de lote para gerar faturas interempresa numa base recorrente. O contabilista do projeto especifica os critérios, tais como projetos específicos, para a criação de faturas interempresa num lote.

## <a name="manually-create-an-intercompany-customer-invoice-for-project-transactions"></a>Criar manualmente uma fatura de cliente interempresa para transações de projetos 

Utilize este procedimento para criar uma fatura de cliente interempresa para transações de projetos. Pesquise por horas que foram publicadas por trabalhadores em projetos nas entidades legais de contração e para despesas que foram incorridas pela sua entidade legal em nome de entidades legais de contração. Pode pesquisar por nome de entidade legal, número de contrato de projeto, número de projeto, intervalo de data ou qualquer combinação destas opções. Nos resultados da pesquisa, selecione as transações a adicionar a uma fatura interempresa.

1. No Dynamics 365 Finance, vá a **Gestão de projetos e contabilística** > **Faturas de projeto** > **Faturas de cliente interempresa**. Na página de lista **Faturas de cliente interempresa**, no Painel de Ação, selecione **Novo.**
2. Na página **Criar fatura interempresa**, no campo **entidade legal**, selecione uma entidade legal de contração.
3. Opcional: Introduza um contrato de projeto específico e número de projeto.
4. Reduza a pesquisa selecionando um intervalo de datas. Introduza datas específicas nos campos **Data de início** e **Data de fim**. Apenas as transações interempresa que são publicadas dentro deste intervalo de datas são apresentadas nos resultados da pesquisa.
5. Defina **Parâmetro de linha do diário avançada do projeto** como **Sim** e selecione **Pesquisar**.
6. Nos resultados da pesquisa, selecione as transações a incluir na proposta de fatura interempresa e, em seguida, selecione **OK**.
7. Na página **Fatura de cliente interempresa**, são apresentadas as transações de projetos interempresa que selecionou a partir dos resultados da pesquisa. Para modificar as transações antes de enviar a fatura à entidade legal de contração, faça o seguinte:
  
    1. Abra a página **Criar proposta de fatura**. Selecione transações interempresa adicionais para a fatura atual e, em seguida, selecione **Adicionar linha**.
    2. Para remover uma linha, selecione-a e, em seguida, selecione **Remover**.
    3. Ver comentários, razões, dimensões financeiras e outras informações sobre uma linha selecionada no Separador Rápido **Linhas de fatura**.
    
8. Para publicar a fatura de cliente interempresa, no Painel de Ação, selecione **Publicar**.

> [!NOTE]
> Se a sua organização exigir que as faturas interempresa sejam revistas antes de serem publicadas, um administrador de sistema pode configurar um fluxo de trabalho para faturas interempresa. Se não for criado um fluxo de trabalho para faturas interempresa, pode publicar a fatura interempresa.

## <a name="create-a-batch-job-for-intercompany-invoices"></a>Criar uma tarefa em lote para faturas interempresa

Pode criar várias faturas interempresa ao mesmo tempo para todas as entidades legais de contração. Utilizando a funcionalidade de pesquisa, pode, por exemplo, pesquisar todas as transações que são publicadas por trabalhadores emprestados e relacionadas com projetos que são geridos por outras entidades legais. Em seguida, para cada entidade legal de contração, pode criar uma fatura interempresa para as transações fornecidas nos resultados da pesquisa.

1. Vá a **Gestão de projetos e contabilística** > **Periódicas** > **Faturas de projeto** > **Criar faturas de cliente interempresa**.
2. Na página **Criar faturas de cliente interempresa**, no campo **Empresa**, selecione uma entidade legal a faturar. Se não selecionar uma empresa, todas as transações que satisfaçam os critérios de pesquisa são apresentadas para todas as entidades legais de contração.
3. Em **Criar uma fatura por**, selecione se cria uma fatura para transações interempresa com base num projeto ou baseada numa entidade legal de contração.
4. Opcional: Para selecionar um projeto específico e um contrato de projeto para criar faturas interempresa, clique em **Selecionar**. Na página **Inquérito**, no campo **Critérios**, selecione o contrato do projeto, número do projeto ou ambos e, em seguida, selecione **OK**.
5. No separador **Lote**, crie um processo de lote para criar faturas interempresa numa base recorrente. Para obter mais informações, consulte [Submeter uma tarefa de processamento de lote a partir de um formulário](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/submit-a-batch-processing-job-from-a-form).
6. Para publicar faturas interempresa, no Painel de Ação, selecione **Publicar**.

> [!NOTE]
> Se a sua organização exigir que as faturas interempresa sejam revistas antes de serem publicadas, um administrador de sistema pode configurar um fluxo de trabalho para faturas interempresa. Se não for criado um fluxo de trabalho para faturas interempresa, pode publicar faturas interempresa.

## <a name="post-the-intercompany-vendor-invoice"></a>Publicar a fatura de fornecedor interempresa

Um contabilista de projeto na entidade legal de contração pode rever faturas de fornecedor interempresa pendentes quando a fatura do cliente interempresa correspondente for publicada. No Finance, na entidade legal de contração, vá a **Contas a pagar** > **Faturas** > **Fatura de fornecedor pendentes**. O número da fatura pendente corresponderá ao número da fatura do cliente interempresa. Verifique se a fatura está correta e, em seguida, publique a fatura. A fatura do fornecedor interempresa cria um sub-livro razão do projeto e uma transação de livro razão geral que reflete os custos de transação na entidade legal de contração.


[!INCLUDE[footer-include](../includes/footer-banner.md)]