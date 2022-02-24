---
title: Estimar vendas e custos do projeto quando um recurso reservável preenche várias funções num projeto
description: Este tópico fornece informação sobre como podem ser usadas as dimensões dos preços para suportar as estimativas de preços e custos para um recurso que preenche várias funções num projeto.
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
ms.openlocfilehash: 67e24156e960b9b09cf92f7f0cd77f6c74a982b8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145057"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-for-a-project"></a>Estimar vendas e custos do projeto quando um recurso reservável preenche várias funções num projeto 

[!include [banner](../includes/psa-now-project-operations.md)]

As empresas baseadas em projetos têm muitas vezes a necessidade que um recurso realize várias funções num projeto. Cada uma destas funções poderia ser avaliada e ter custos diferentes, o que significa que o tempo do mesmo recurso no projeto poderia obter uma estimativa financeira diferente, dependendo da fatura e das taxas de custo para cada uma das funções. O Project Service Automation permite a configuração dos valores no registo do membro da equipa para o recurso nomeado e permite diferentes substituições em cada uma das tarefas a que o membro da equipa está atribuído.

O exemplo seguinte explica como a simples sobreposição deste valor permite que um recurso tenha múltiplas funções num projeto com diferentes taxas de custo e faturação.

## <a name="create-tasks"></a>Criar tarefas
Criar duas tarefas de projeto durante 40 horas cada, Tarefa A e Tarefa B. Selecione a Tarefa A como antecessora da Tarefa B.

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a>Configurar Função e Unidade da Organização para um membro da equipa de projeto genérico

1. Na página **Agendar**, selecione a linha **Tarefa** para a Tarefa A. 
2. No campo **Recursos**, selecione **Criar** na lista de pendente.
3. Na página **Criação Rápida do Membro da Equipa**, especifique os atributos do membro da equipa genérico que pode executar esta tarefa.
4. Selecione a função e a unidade organizacional apropriadas e, em seguida, selecione **Guardar e Fechar**. Um membro da equipa genérico é criado e atribuído a esta tarefa. 

Repita estes passos para a Tarefa B e certifique-se de que a função e a unidade organizacional no membro da equipa genérico criado para a Tarefa B é diferente da Tarefa A. 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a>Configurar função e unidade da organização para uma tarefa de projeto

1. Depois de criar a Tarefa A, selecione a tarefa e, em seguida, selecione **Editar tarefa**.
2. Na página **Detalhes da Tarefa**, encontre os campos **Função** e **Unidade Organizacional**, adicione os valores necessários para que um recurso que executaria esta tarefa. 

  > [!NOTE]
  > Se estiver a completar estes cenários utilizando dados de demonstração do Project Service Automation, selecione **Líder de Consultoria** como função e **Fabrikam US** como unidade organizacional.

3. Selecione Tarefa B e, em seguida, selecione **Editar tarefa**.
4. Na página **Detalhes da Tarefa**, encontre os campos **Função** e **Unidade Organizacional**, adicione os valores necessários para que um recurso que executaria esta tarefa. Certifique-se de que os valores nos campos **Função** e **Unidade organizacional** sejam diferentes para a Tarefa B dos valores da Tarefa A. 

  > [!NOTE]
  > Se estiver a completar estes cenários utilizando dados de demonstração do Project Service Automation, selecione **Técnico de Rede** como função e **Fabrikam US** como unidade organizacional.

5. Guarde e feche a página **Detalhes da Tarefa**. 

## <a name="team-member-and-estimates-behavior"></a>Comportamento de membro da equipa e estimativa 

1. Na página **Dados da Tarefa**, em **Membro da Equipa**, selecione os dois membros da equipa genéricos e, em seguida, selecione **Gerar Requisitos**. 
2. Selecione a linha de membro da equipa de **Líder de Consultoria** e, em seguida, selecione **Reservar**. O quadro da agenda é aberto e reserva um recurso para esse requisito.
3. Selecione a linha de membro da equipa de **Técnico de Rede** e, em seguida, selecione **Reservar**. O quadro da agenda é aberto e reserva o mesmo recurso nesse requisito.

### <a name="team-member-grid"></a>Grelha Membro da Equipa 
Na grelha **Membro da Equipa**, note que os dois registos de membros da equipa genéricos são eliminados e foram substituídos por um recurso. Há um conjunto de valores para esse recurso que mostra um conjunto padrão de valores para **Função** e **Unidade Organizacional**.
Quando expandir a linha desse registo de Membro da Equipa, pode ver atribuições distintas no registo do membro da equipa para ambas as tarefas. Cada linha de atribuição tem valores específicos de tarefa para **Função** e **Unidade Organizacional**. 

### <a name="estimates-grid"></a>Grelha Estimativas 
Ao navegar para a grelha **Estimativas**, notará que ambas as atribuições para o mesmo recurso têm um preço diferente.
A atribuição do recurso na Tarefa A tem o preço utilizando o valor de atributo **Função** de **Líder de Consultoria**. A atribuição do mesmo recurso na Tarefa B tem o preço utilizando o valor de atributo **Função** de **Técnico de Rede**.

