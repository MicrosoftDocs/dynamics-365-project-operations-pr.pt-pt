---
title: Recuperação de IVA
description: Este tópico explica como recuperar reembolsos em transações elegíveis com imposto sobre o valor acrescentado (IVA).
author: saraschi2
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76706fd8ced58063b05bc8ebe4b25c1dddbf0890e72e9c7194d17ff2937dc8ca
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986055"
---
# <a name="vat-recovery"></a>Recuperação de IVA 

Para receber reembolsos em transações elegíveis de imposto sobre o valor acrescentado (IVA), uma empresa ou organização tem de identificar, recolher, verificar e submeter informações precisas. Este processo inclui várias tarefas e, consoante o tamanho da sua empresa, pode incluir vários colaboradores ou funções.

Para recuperar o IVA utilizando a Gestão de despesas, têm de ser preenchidos os seguintes pré-requisitos:

- Têm de ser criados códigos fiscais para os países/regiões afetados às categorias de despesas.
- Tem de ser criado um grupo fiscal para cada código fiscal.
- Tem de ser criado um código do imposto sobre as vendas do artigo para cada grupo de impostos sobre vendas.

Após a conclusão dos pré-requisitos, os funcionários têm de seguir estes passos para solicitar reembolsos por transações de IVA.

1. Num relatório de despesas, introduza as informações fiscais sobre as transações com cartões de crédito para identificar os reembolsos de IVA elegíveis.
2. Certifique-se de que toda a informação fiscal está completa e, em seguida, lance o relatório de despesas.
3. Processar despesas elegíveis para recuperação do IVA internacional.
4. Envie os dados de recuperação do IVA para o fornecedor de terceiros para apresentar declarações de recuperação internacionais.
5. Processar despesas para a recuperação do VAT nacional.

As secções seguintes fornecem exemplos que mostram como os colaboradores da Contoso completam cada passo.

## <a name="on-an-expense-report-enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>Num relatório de despesas, introduza as informações fiscais sobre as transações com cartões de crédito para identificar os reembolsos de IVA elegíveis

Bárbara, uma representante de vendas da Contoso que está sediada nos EUA, regressou recentemente de uma viagem de vendas ao Reino Unido. Durante a sua viagem, ela incorreu em algumas despesas pessoais com cartão de crédito para as refeições. Agora, a Bárbara tem de criar um relatório de despesas para reconciliar as suas despesas.

Quando Bárbara introduz informações no seu relatório de despesas, ela seleciona **Reino Unido** no campo **País/região** na página **Editar relatório de despesas**. Em seguida, a lista de grupos de impostos sobre as vendas é filtrada para mostrar apenas os grupos aplicáveis ao Reino Unido. Nancy seleciona o grupo de impostos sobre vendas **Reino Unido 001** e, em seguida, seleciona o grupo de impostos sobre vendas de artigos **Refeições**. Em seguida, ela adiciona uma nova transação para o seu alojamento. Como só existe um grupo de impostos sobre as vendas e grupo de impostos sobre as vendas de artigos para alojamento no Reino Unido, esta informação é preenchida automaticamente no relatório de despesas da Bárbara.

De acordo com a política da Contoso, todas as despesas devem ter um recibo correspondente. Assim, quando a Bárbara guarda o seu relatório de despesas, recebe uma mensagem que indica que tem de anexar um recibo por cada transação que listou no seu relatório de despesas. Nancy verifica se anexou uma imagem digital de cada recibo de transação ao seu relatório de despesas e, em seguida, submete o seu relatório para aprovação. Em seguida, envia os recibos em papel para a equipa de processamento de back-office. Esta equipa enviará os dados de recuperação do IVA ao fornecedor externo que arquiva as devoluções internacionais de recuperação do IVA para a Contoso.

## <a name="make-sure-that-all-tax-information-is-complete-and-then-post-the-expense-report"></a>Certifique-se de que toda a informação fiscal está completa e, em seguida, lance o relatório de despesas

April, a coordenadora das contas a pagar da Contoso deve introduzir qualquer informação fiscal que esteja em falta de um relatório de despesas antes que este possa ser publicado. Ela abre a página **Detalhes do relatório de despesas** e vê o relatório de despesas aprovado pela Nancy. Em seguida, April abre o relatório de despesas para ver os detalhes das transações. Ela vê que a Nancy não introduziu um grupo de impostos sobre vendas de artigos para uma das transações. Como esta informação não é fornecida, a April não pode lançar o relatório de despesas. Assim, a April consulta a página **Configurações de impostos** na Gestão de despesas e encontra o grupo de impostos sobre as vendas de artigos adequado para o país/região e o tipo de transação. April pode agora lançar o relatório de despesas no Razão Geral.

Quando April lança o relatório de despesas, é criado um item de trabalho recuperável do IVA. Este item de trabalho é atribuído a um membro da equipa de processamento em back-office. April recebe uma mensagem que confirma que o lançamento foi concluído com êxito. Esta mensagem também lista o número de transações de IVA que foram identificadas para recuperação.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Processar despesas elegíveis para recuperação do IVA internacional

Arnie, membro da equipa de processamento de back-office da Contoso, é responsável por confirmar se todas as informações necessárias para a recuperação do IVA estão incluídas nos relatórios de despesas. Ele abre a página **Recuperação de impostos de despesas** e seleciona o relatório de despesas que a Nancy submeteu. Arnie verifica se todos os recibos necessários estão anexados, e se foram introduzidos o grupo de impostos sobre vendas e os códigos de imposto sobre as vendas de produtos corretos.

Quando Arnie recebe os recibos em papel da Bárbara, verifica os recibos de papel em relação aos recibos digitais e altera o estado do relatório de despesas para **Pronto para recuperação**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor-to-file-international-recovery-returns"></a>Envie os dados de recuperação do IVA para o fornecedor de terceiros para apresentar declarações de recuperação internacionais

Quando Arnie estiver pronto para enviar os dados do relatório de despesas para o fornecedor terceiros que apresentará as declarações de recuperação do IVA, abre a página **Recuperação de impostos de despesas**. Filtra a página para mostrar apenas os relatórios de despesas marcados como **Pronto para recuperação**. Em seguida, Arnie seleciona **Arquivar** &gt; **Exportar para Excel**. A informação sobre o IVA dos relatórios de despesas é exportada para uma folha de cálculo do Microsoft Excel. Arnie submete esta folha de cálculo para o fornecedor externo e inclui uma mensagem que indica que os recibos em papel foram enviados por correio.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Processar despesas para a recuperação do VAT nacional

Arnie tem de verificar se as transações de relatórios de despesas são elegíveis para recuperação do IVA e se os recibos digitais são anexados aos relatórios. Para começar a processar as despesas elegíveis para recuperação interna, Arnie abre a página **Recuperação de impostos de despesas** e seleciona o relatório de despesas que necessita de verificação. Ele verifica se os recibos estão em nome da empresa, em vez do empregado. Para a recuperação do IVA, os recibos devem estar em nome da empresa. Arnie confirma então que foram aplicados os códigos de imposto sobre as vendas corretos e os códigos fiscais de venda de produtos.

Quando Arnie recebe os recibos em papel, altera o estado do relatório de despesas para **Pronto para recuperação**. Em seguida, pode apresentar a declaração junto da autoridade tributária competente. Neste caso, a autoridade tributária competente nos EUA é a direção geral de impostos (IRS).


[!INCLUDE[footer-include](../includes/footer-banner.md)]