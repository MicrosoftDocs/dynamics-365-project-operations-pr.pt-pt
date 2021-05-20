---
title: Novidades ou alterações na Versão da Atualização 19 do Project Service Automation, V3
description: Este tópico lista as funcionalidades e correções disponíveis no Project Service Automation V3, Versão da Atualização 19, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 0137d0241238ff96de406884dd05a5d7f023c318
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949153"
---
# <a name="project-service-automation-update-release-19-v3"></a>Versão da Atualização 19 do Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a mais recente atualização à aplicação Project Service Automation para Dynamics 365. Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização. Esta versão é compatível com o Dynamics 365 9.x. Para atualizar esta versão, visite o Centro de Administração para o Dynamics 365 online e aceda à página de soluções para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este tópico lista as funcionalidades e correções novas ou alteradas para o PSA V3, Versão da Atualização 19. Esta versão tem o número de compilação V3.10.30.41 e está geralmente disponível através de uma atualização automática em maio de 2020.

## <a name="update-release-19"></a>Versão da Atualização 19

### <a name="bug-fixes"></a>Correções de erros

**Tempo e Despesa**

Foram corrigidos os seguintes problemas: 

- Os erros derivados das importações de entrada de tempo não surgem corretamente.
- A Grelha de Entrada de Tempo não suporta o comportamento do campo **Apenas Data**.
- Os Recursos do Projeto são incapazes de criar uma despesa com um projeto.

**Gestão de Projetos**

Foram corrigidos os seguintes problemas: 

-  A tarefa secundária causa uma estimativa de esforço incorreta durante o Cálculo de Conclusão (EAC).

**Sales**

Foram corrigidos os seguintes problemas: 

- A ação **Recalcular** não funciona com detalhes de item de contrato de despesas ou detalhes de item de proposta.
- **Atualizar preços** está em falta das estimativas de despesas.
-  Os clientes não conseguem selecionar razões do estado do contrato personalizadas a partir da página **Contrato do Projeto**.
- Os clientes experimentam um desempenho degradado ao criar uma lista de preços personalizada a partir de uma proposta.
- Os clientes experimentam inconsistência com predefinições de **unidade** nas páginas **Detalhes de Item de Proposta** e **Detalhes de Item de Contrato**.
- A adição de itens de categoria de transação não faturável a um item de contrato faturável não respeitará o tipo de faturação **Não faturável** da categoria de transação.
- Os clientes não podem utilizar as funções e categorias recém-adicionadas em contratos previamente criados.
- Clientes experimentam desempenho degradado de recuperação desnecessária em PreValidateProjectTeamMemberUpdate.cs
- As funções configuradas como não faturáveis na lista **Categorias de Recursos** devem ser adicionadas ao separador **Funções Faturáveis** como **Não Faturáveis** no item de contrato de um projeto.
- Os clientes podem experimentar um desempenho degradado ao criar um projeto porque **GetBookableResourceIdFromUser** recupera todas as colunas de recursos reservados em vez de apenas o ID primário.
- A entidade **TransactionType** que não tem o plug-in de atualização de pré-validação para impedir que os utilizadores entrem em **Unidades** e **GruposUnitários** que não são válidos para tipos de transação.
- O passo **Remover** não funciona para a importação de entrada de tempo.


[!INCLUDE[footer-include](../includes/footer-banner.md)]