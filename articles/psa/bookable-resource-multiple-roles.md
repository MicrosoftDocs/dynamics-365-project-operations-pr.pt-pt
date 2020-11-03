---
title: Calcular vendas e custos do projeto quando um recurso reservável preenche várias funções num projeto
description: Este tópico fornece informações sobre como as dimensões de preços podem ser usadas para suportar preços e custos de um recurso que preenche várias funções num projeto.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 8ddc827a4170c5576c0a4350b51e6a119094ac50
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082456"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-mulitple-roles-on-a-project"></a>Calcular vendas e custos do projeto quando um recurso reservável preenche várias funções num projeto 

As empresas baseadas em projetos têm muitas vezes a necessidade de que um recurso desempenhe várias funções num projeto. Cada uma destas funções poderia ser avaliada e ter custos diferentes, o que significa que o tempo do mesmo recurso no projeto poderia obter uma estimativa financeira diferente, dependendo da fatura e das taxas de custo para cada uma das funções. O Project Service Automation permite a configuração dos valores no registo do membro da equipa para o recurso nomeado e permite diferentes substituições em cada uma das tarefas a que o membro da equipa está atribuído.

O exemplo seguinte explica como a simples sobreposição deste valor permite que um recurso tenha múltiplas funções num projeto com diferentes taxas de custo e faturação.

## <a name="create-tasks"></a>Criar tarefas
Criar duas tarefas de projeto durante 40 horas cada, Tarefa A e Tarefa B. Selecione a Tarefa A como antecessora da Tarefa B.

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a>Configurar Função e Unidade da Organização para um membro da equipa de projeto genérico

1. Na página **Agendar** , selecione a linha **Tarefa** para a Tarefa A. 
2. No campo **Recursos** , selecione **Criar** na lista de pendente.
3. Na página **Criação Rápida do Membro da Equipa** , especifique os atributos do membro da equipa genérico que pode executar esta tarefa.
4. Selecione a função e a unidade organizacional apropriadas e, em seguida, selecione **Guardar e Fechar**. Um membro da equipa genérico é criado e atribuído a esta tarefa. 

Repita estes passos para a Tarefa B e certifique-se de que a função e a unidade organizacional no membro da equipa genérico criado para a Tarefa B é diferente da Tarefa A. 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a>Configurar função e unidade da organização para uma tarefa de projeto

1. Depois de criar a Tarefa A, selecione a tarefa e, em seguida, selecione **Editar tarefa**.
2. Na página **Detalhes da Tarefa** , encontre os campos **Função** e **Unidade Organizacional** , adicione os valores necessários para que um recurso que executaria esta tarefa. 

  > [!NOTE]
  > Se estiver a completar estes cenários utilizando dados de demonstração do Project Service Automation, selecione **Líder de Consultoria** como função e **Fabrikam US** como unidade organizacional.

3. Selecione Tarefa B e, em seguida, selecione **Editar tarefa**.
4. Na página **Detalhes da Tarefa** , encontre os campos **Função** e **Unidade Organizacional** , adicione os valores necessários para que um recurso que executaria esta tarefa. Certifique-se de que os valores nos campos **Função** e **Unidade Organizacional** são diferentes para a Tarefa B dos da Tarefa A. 

  > [!NOTE]
  > Se estiver a completar estes cenários utilizando dados de demonstração do Project Service Automation, selecione **Técnico de Rede** como função e **Fabrikam US** como unidade organizacional.

5. Guarde e feche a página **Detalhes da Tarefa**. 

## <a name="team-member-and-estimates-behaviour"></a>Membro da equipa e comportamento estimado 

1. Na página **Dados da Tarefa** , em **Membro da Equipa** , selecione os dois membros da equipa genéricos e, em seguida, selecione **Gerar Requisitos**. Esta ação irá gerar requisitos de recursos. 
2. Selecione a linha de membro da equipa de **Líder de Consultoria** e, em seguida, selecione **Reservar**. O quadro da agenda é aberto e reserva um recurso para esse requisito.
3. Selecione a linha de membro da equipa de **Técnico de Rede** e, em seguida, selecione **Reservar**. O quadro da agenda é aberto e reserva o mesmo recurso nesse requisito.

### <a name="team-member-grid"></a>Grelha Membro da Equipa 
Na grelha **Membro da Equipa** , note que os dois registos de membros da equipa genéricos são eliminados e foram substituídos por um recurso. Há um conjunto de valores para esse recurso que mostra um conjunto padrão de valores para **Função** e **Unidade Organizacional**.
Quando expandir a linha desse registo de Membro da Equipa, pode ver atribuições distintas no registo do membro da equipa para ambas as tarefas. Cada linha de atribuição tem valores específicos de tarefa para **Função** e **Unidade Organizacional**. 

### <a name="estimates-grid"></a>Grelha Estimativas 
Ao navegar para a grelha **Estimativas** , notará que ambas as atribuições para o mesmo recurso têm um preço diferente.
A atribuição do recurso na Tarefa A tem o preço utilizando o valor de atributo **Função** de **Líder de Consultoria**. A atribuição do mesmo recurso na Tarefa B tem o preço utilizando o valor de atributo **Função** de **Técnico de Rede**.





