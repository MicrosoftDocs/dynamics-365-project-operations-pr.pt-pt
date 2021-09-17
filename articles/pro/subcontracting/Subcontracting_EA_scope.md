---
title: Subcontratação na versão de Acesso Antecipado de outubro de 2021
description: Este tópico fornece uma descrição geral das capacidades de subcontratação no Project Operations que fazem parte da versão de acesso antecipado de outubro de 2021.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 21ec8355487b5e69fc5b68b11dca029e6dc04f3c
ms.sourcegitcommit: c7f891adb5c81654c01d00c6b39beed403058eb1
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/14/2021
ms.locfileid: "7383709"
---
# <a name="subcontracting-in-october-2021-early-access-release"></a>Subcontratação na versão de Acesso Antecipado de outubro de 2021

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

Este tópico fornece uma descrição geral das capacidades de subcontratação no Dynamics 365 Project Operations que fazem parte da versão de acesso antecipado de outubro de 2021. Este conjunto de funcionalidades não está preparado para ambientes de produção ou ativos, pelo que estas funcionalidades permanecerão na versão de acesso antecipado até que o conjunto completo de funcionalidades seja disponibilizado. Recomendamos vivamente que não utilize o conjunto de funcionalidades de subcontratação para cenários de produção ativos até a faixa de pré-visualização ser removida. 

A seguinte lista apresenta uma perspetiva geral do que está disponível atualmente na versão de Acesso Antecipado de outubro de 2021:

1. O gestor de projeto cria um subcontrato com um fornecedor. Por predefinição, as listas de preços anexadas ao registo do fornecedor são utilizadas para o subcontrato. A conta do fornecedor tem um tipo de relação de **Fornecedor** ou **Prestador**.

2. O gestor de projeto pode discriminar todas as compras como itens de linha no subcontrato. Os itens de subcontrato podem ser para tempo, despesas ou produtos. A classe de transação do item de subcontrato determina a finalidade do item.

3. O gestor de conta do fornecedor e o gestor de projeto podem iterar sobre o subcontrato. Os preços podem ser ajustados nas listas de preços das compras que estão anexadas ao subcontrato.

4. Neste momento, ou mais tarde no processo, se o item do subcontrato for para tempo, o gestor de conta do fornecedor associa os contactos do fornecedor a cada item de subcontrato. Esta associação fornece informações ao gestor do projeto que está a trabalhar no subcontrato. Quando um contacto do fornecedor é associado a um item de subcontrato, o sistema cria automaticamente um recurso reservável a partir do contacto, se ainda não existir um recurso reservável.

5. O método de faturação em cada item de subcontrato pode ser **Preço Fixo** ou **Tempo e Material**. Para itens de subcontrato de preço fixo, é configurada uma agenda de faturação baseada em marcos.

Os passos restantes no fluxo do processo de negócio para a subcontratação indicados na Descrição Geral não estão disponíveis atualmente. Este tópico será atualizado à medida que são adicionadas novas funcionalidades. 

A seguinte ilustração representa a versão de Acesso Antecipado de Subcontratação em contraste com o processo de negócio ponto a ponto.

![Fluxo de processo de subcontratação](../media/SubcontractingEAFlow.png)  


## <a name="quantity-based-and-work-based-subcontract-lines-early-access-release"></a>Versão de acesso antecipado de itens de subcontrato baseados em quantidade e itens de subcontrato baseados em trabalho
Na versão de Acesso Antecipado de outubro de 2021, só são suportados os itens de subcontrato baseados em quantidade. Isto significa que um item de subcontrato pode ser utilizado para comprar tempo, despesas ou materiais de um fornecedor, mas não todo um corpo de trabalho. Isto também significa que a quantidade que está a ser comprada (unidades de tempo, despesas ou quantidade de materiais) num item de subcontrato pode ser utilizada em qualquer projeto no sistema.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
