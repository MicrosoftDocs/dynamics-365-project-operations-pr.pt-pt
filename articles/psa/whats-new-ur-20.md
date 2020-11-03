---
title: Novidades ou alterações na Versão da Atualização 20 do Project Service Automation, V3
description: Este tópico lista as funcionalidades e correções disponíveis na Versão da Atualização 20 do Project Service Automation, V3
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: 12edae76dbc6de63d3e2d36058c4092f80ede77d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082353"
---
# <a name="project-service-automation-update-release-20-v3"></a>Versão da Atualização 20 do Project Service Automation, V3

Temos o prazer de anunciar a mais recente atualização à aplicação Project Service Automation para Dynamics 365. Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização. Esta versão é compatível com o Dynamics 365 9.x. Para atualizar esta versão, visite o Centro de Administração para o Dynamics 365 online e aceda à página de soluções para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Este tópico lista as funcionalidades e correções novas ou alteradas para o Project Service Automation V3, Versão da Atualização 20. Esta versão tem o número de compilação V 3.10.31.37 e está geralmente disponível através de uma atualização automática em junho de 2020.

## <a name="update-release-20"></a>Versão da Atualização 20

### <a name="bug-fixes"></a>Correções de erros

**Gestão de Projetos**

Foram corrigidos os seguintes problemas:

- Importar membros da equipa do projeto com um método de alocação que requer horas resulta numa mensagem de erro pouco clara quando as horas especificadas são zero.
- Os utilizadores recebem um erro incorreto quando o número máximo de carateres foi introduzido no campo **Descrição** para uma tarefa de projeto.
- A página de **Transferência do suplemento do Microsoft Dynamics 365 Project Service Automation** redireciona para a página de transferência em inglês quando as definições de idioma do utilizador estão definidas para o japonês.
- Quando ocorre um erro do servidor, a etiqueta de sincronização no separador **Agendar** do formulário **Projetos** por vezes permanece.
- Atualizações de tarefas redundantes são enviadas para o servidor quando uma tarefa é modificada.

**Sales**

Foram corrigidos os seguintes problemas:

- No formulário **Contrato** , clicar duas vezes com o botão direito do rato em **Criar Fatura** cria duas faturas para um único registo real.
- No Internet Explorer 11, os utilizadores são incapazes de criar entradas de despesas.
- A reversão do Custo e a reversão de Valores Reais de Vendas Não Faturáveis não estão ligados.
- O botão **Atualizar Valores Reais** no formulário **Projeto** não atualiza as **Horas Reais da Tarefa**.
- O plug-in **PreValidateProjectTeamMemberCreate** pode criar recursos agendáveis genéricos duplicados quando o atributo **msdyn_isgenericresourceprojectscoped** é definido como **False**.
- **Recalcular** elimina os custos faturáveis dos detalhes de item de proposta baseada e detalhes de item de contrato baseados em produtos.
- Em cenários específicos, o plug-in **PostEstimateLineUpdate** apresenta um erro de exceção de referência nulo.
- A duração da fase de tempo no **Gráfico de Análise de Rentabilidade** não corresponde à duração dos custos no detalhe do item de proposta de preço fixo da proposta.
- Os valores de unidade e de grupo de unidades não são predefinidos corretamente para as categorias de despesas nos formulários **Detalhes do Item de Contrato** e **Detalhes do Item de Proposta**.
- As listas de **Preço de Custo da Unidade Organizacional** permitem sobreposições na efetividade da data.
- Os utilizadores não estão autorizados a alterar **OrgUnit** quando o tipo de encomenda não é baseado no trabalho, pois irá conduzir a um erro de exceção de referência nulo.
- Ao tentar navegar a partir do formulário **Detalhes do Item de Proposta** , regresse ao separador **Proposta** , o formulário atualiza e apresenta o separador **Resumo**.
