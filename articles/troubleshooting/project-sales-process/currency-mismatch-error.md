---
title: Erro de correspondência de moeda
description: Este artigo fornece informações sobre um erro de correspondência de moeda que ocorre quando guarda tipos de registo específicos.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5b0973a340dec8e68f326803d75bea9803e19791
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914738"
---
# <a name="currency-mismatch-error"></a>Erro de correspondência de moeda 

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Quando guarda um projeto, contrato, proposta ou recurso reservável, poderá receber o erro **A moeda da empresa proprietária do contrato não corresponde à moeda da unidade de contratação. Escolha uma empresa proprietária ou unidade de contratação diferente para continuar**. Isto porque existe um erro de correspondência de moeda entre a moeda da unidade de contratação para o registo e a moeda da empresa proprietária.


## <a name="resolution"></a>Resolução

Para contornar este problema, faça o seguinte:
- Verifique a moeda da unidade de contratação para este registo. Pode ver a moeda abrindo o registo da unidade organizacional e verificando o valor no separador **Geral** no campo **Moeda**.
- Verifique a moeda da empresa proprietária. Pode ver a moeda indo a **Relacionados** > **Livros Razão** no registo da empresa. Clique duas vezes no registo do livro razão que está associado à empresa e verifique o valor no separador **Geral** no campo da **Moeda contabilística**.

Se a moeda definida na unidade de contratação e o registo do livro razão não corresponder, ajuste a configuração ou selecione valores diferentes quando guardar o registo. O sistema requer que estes registos correspondam para garantir fluxos de faturação interempresa corretos. Para obter mais informações sobre as configurações interempresa, consulte [Criar transações interempresa](../../project-accounting/create-intercompany-transactions.md).

Se o registo da empresa não tiver registo de livro razão associado, isto indica que há uma configuração em falta ao configurar o ambiente. A configuração tem de ser corrigida pelo administrador do sistema. O administrador do sistema tem de ir a **Configurações de escrita dupla** e parar e reiniciar o **Mapa de escrita dupla dos livros razão** com a sincronização inicial deste mapa e os seus pré-requisitos. Para mais informações, consulte [Versões do mapa de escrita dupla do Project Operations](../../environment/resource-dual-write-maps.md).
