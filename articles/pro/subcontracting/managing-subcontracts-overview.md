---
title: Gestão de subcontratos no Project Operations
description: Este tópico fornece uma descrição geral do processo de gestão de subcontratos ponto a ponto, normalmente em organizações baseadas em projetos.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 993edfd064279a970d7c42d5fcefd794e949a931
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323610"
---
# <a name="subcontract-management-in-project-operations"></a>Gestão de subcontratos no Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

Este tópico fornece uma descrição geral do processo de gestão de subcontratos ponto a ponto em organizações baseadas em projetos. A subcontratação de serviços normalmente segue o fluxo do processo de negócio que é apresentado no seguinte diagrama.

![Fluxo de processo de subcontratação](../media/SubcontractingProcessFlow.png)

A lista seguinte fornece uma descrição passo a passo do processo de subcontratação.

1. O gestor de projeto cria um subcontrato com um fornecedor. Por predefinição, as listas de preços anexadas ao registo do fornecedor são utilizadas para o subcontrato. A conta do fornecedor tem um tipo de relação de **Fornecedor** ou **Prestador**.
2. O gestor de projeto pode discriminar todas as compras como itens de linha no subcontrato. Os itens de subcontrato podem ser para tempo, despesas ou produtos. A classe de transação do item de subcontrato determina a finalidade do item.
3. O gestor de conta do fornecedor e o gestor de projeto podem iterar sobre o subcontrato. Os preços podem ser ajustados nas listas de preços das compras que estão anexadas ao subcontrato.
4. Neste momento, ou mais tarde no processo, se o item do subcontrato for para tempo, o gestor de conta do fornecedor associa os contactos do fornecedor a cada item de subcontrato. Esta associação fornece informações ao gestor do projeto que está a trabalhar no subcontrato. Quando um contacto do fornecedor é associado a um item de subcontrato, o sistema cria automaticamente um recurso reservável a partir do contacto, se ainda não existir um recurso reservável.
5. O método de faturação em cada item de subcontrato pode ser **Preço Fixo** ou **Tempo e Material**. Para itens de subcontrato de preço fixo, é configurada uma agenda de faturação baseada em marcos.
6.  Após a configuração do subcontrato e a conclusão da negociação, está confirmado. Os subcontratos confirmados não podem ser editados, mas se ocorrerem alterações, um subcontrato pode ser "reaberto para edições", o que muda o estado de **Confirmado** novamente para **Rascunho** e a negociação pode ser reaberta. 
7.  Ao criar um membro da equipa genérico num projeto, o membro da equipa pode ser associado a um item de subcontrato. Isto indica que um membro da equipa genérico deve ter a capacidade de subcontratante.
8.  Os membros da equipa nomeados podem ser criados diretamente num projeto ou através de reserva, utilizando as experiências de agendamento de recursos. Se um membro da equipa do projeto nomeado for um trabalhador contratado, é possível associá-lo a um item de subcontrato. Isto reduzirá a capacidade disponível num item de subcontrato.
9.  Os recursos de subcontratantes podem registar o tempo, as despesas e a utilização de materiais em projetos e tarefas de projetos, e submetê-los para aprovação. O procedimento é semelhante para os empregados. Ao registar o tempo, um trabalhador contratado pode selecionar um subcontrato e um item de subcontrato específicos.
10. Após a aprovação, o tempo aprovado pelos subcontratos registará o custo real do projeto com base no preço de compra associado ao trabalhador contratado ou na função que este desempenhou no projeto.
11. As faturas do fornecedor e os itens da linha de fatura do fornecedor podem ser registados no sistema como trabalho realizado pelos recursos do fornecedor ou produtos entregues pelo fornecedor. As linhas de fatura do fornecedor têm de ser específicas de um projeto e de uma classe de transação de tempo, despesa, produto/material, marco ou taxa. Em alternativa, as linhas de fatura do fornecedor podem referenciar um item de subcontrato.
12. O sistema associará automaticamente todos os custos reais que correspondam ao item de subcontrato e ao projeto à fatura do fornecedor. Isto facilitará um processo de verificação e correspondência de 3 vias.
13. O gestor do projeto pode então rever os valores reais do projeto de correspondência automática, remover ou adicionar outros custos reais do projeto e concluir o processo de verificação.
14. A conclusão do processo de verificação em todas as linhas marcará a fatura do fornecedor como **Pronta para Pagamento**. Nesta fase, as linhas e a fatura do fornecedor podem ser transferidas para um sistema de Gestão Contabilística ou Pagamentos para processar o pagamento ao fornecedor. Os custos do projeto registados previamente serão revertidos e os custos reais da linha de fatura do fornecedor serão registados no projeto.

## <a name="quantity-based-subcontract-lines-and-work-based-subcontract-lines"></a>Itens de subcontrato baseados em quantidade e itens de subcontrato baseados em trabalho

Um item de subcontrato pode ser baseado na quantidade ou no trabalho. 

Quando um item de subcontrato é **baseado na quantidade**, a quantidade que está a ser comprada no item de subcontrato de tempo, despesa ou material pode ser utilizada em qualquer projeto.

Quando um item de subcontrato é **baseado no trabalho**, o item de subcontrato é mapeado para um corpo de trabalho representado por um nó no plano do projeto. O valor do item de subcontrato corresponde à soma de todos os componentes necessários para entregar esse corpo de trabalho. Estes são modelados como detalhes do item de subcontrato e podem ser uma coleção de tempo, despesa ou materiais. No caso de um item de subcontrato baseado no trabalho, o item de subcontrato também é dedicado a um único projeto.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

