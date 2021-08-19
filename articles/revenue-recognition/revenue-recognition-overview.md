---
title: Descrição geral do reconhecimento de receitas
description: Este tópico fornece informações sobre o reconhecimento de receitas no Project Operations.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: 3d2fcf434a5086595e40f50afc2366eb806168085ae9212b5d25e3e9bd02e2c6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988665"
---
# <a name="revenue-recognition-overview"></a>Descrição geral do reconhecimento de receitas

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

No Dynamics 365 Project Operations, os princípios de reconhecimento de receitas variam em função do método de faturação selecionado para um projeto ou parte do projeto. Este tópico fornece informações sobre o reconhecimento de receitas no Project Operations.

## <a name="transactions-accounted-using-time-and-material-billing-method"></a>Transações contabilizadas utilizando o método de faturação de tempo e material

- O reconhecimento de custo e receitas estão ligados. O custo de transação e as vendas não faturadas são publicados através do [diário de Integração do Project Operations](../project-accounting/project-operations-integration-journal.md).
- O perfil de custos e receitas do projeto determinam se as transações de vendas não faturadas são publicadas no livro razão geral. Se a **Receita de acréscimo** for selecionada, o sistema utiliza o **Valor de vendas WIP** e as contas **Valor de vendas de receita de acréscimo** durante a publicação. O seguinte é um exemplo deste método.  

  | Tipo de transação | Débito/Crédito | Montante |
  | --- | --- | --- |
  | Valor de Vendas WIP | Débito | 100 |
  | Valor das vendas de receitas acumuladas | Crédito | 100 |

- A receita é reconhecida durante a faturação. O sistema utiliza a conta de **Receitas faturadas** durante a publicação. O seguinte é um exemplo deste método.  

  | Tipo de transação | Débito/Crédito | Montante |
  | --- | --- | --- |
  | Saldo do cliente | Débito | 120 |
  | Valor de imposto pagável | Crédito | 20 |
  | Receitas Faturadas | Crédito | 100 |

- Se as receitas forem acumuladas quando as vendas não faturadas forem publicadas, o sistema reverterá as receitas acumuladas na faturação.

  | Tipo de transação | Débito/Crédito | Montante |
  | --- | --- | --- |
  | Valor de Vendas WIP | Crédito | 100 |
  | Valor das vendas de receitas acumuladas | Débito | 100 |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a>Transações contabilizadas utilizando o método de faturação de preço fixo

- O reconhecimento de custo e receitas estão separados. O custo de transação é publicado através do [diário de Integração do Project Operations](../project-accounting/project-operations-integration-journal.md). As transações de vendas não faturadas não são criadas.
- As receitas podem ser reconhecidas durante a faturação se o perfil de custo e receita do projeto tiver o **Princípio utilizado para os cálculos de conclusão do projeto** definidos como **Sem WIP**. Utilize apenas este método para projetos simples e de curto prazo.
- As receitas podem ser reconhecidas usando estimativas de receitas de preço fixo, com o método **Contrato concluído** ou **Reconhecimento de receitas de conclusão de percentagem**.

## <a name="additional-resources"></a>Recursos adicionais
[Artigo Configurar gestão contabilística para projetos faturáveis](../project-accounting/configure-accounting-billable-projects.md)

[Projetos de estimativa de receitas de preço fixo](rev-rec-percentage-completion-method.md)

[Gerir estimativas de receitas](rev-rec-completed-contract-method.md)

[Métodos de custo para conclusão](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]