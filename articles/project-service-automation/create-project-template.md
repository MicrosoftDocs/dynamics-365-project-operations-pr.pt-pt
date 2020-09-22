---
title: Criar um modelo de projeto
description: Como criar um modelo do projeto no Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: ba15d6d5-a43b-456a-9488-db6e92023fa1
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 50e12d65d5ed957565485413490b8d9f0e2f47ab
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754495"
---
# <a name="create-a-project-template-project-service"></a>Criar um modelo de projeto (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Os modelos de projeto poupam tempo se a sua empresa apresenta propostas em tipos semelhantes de projetos. Fornecem um conjunto de funções padrão e as horas estimadas para um tipo de projeto. Os gestores de contas e os gestores de projetos podem criar projetos com num modelo de design ou copiar o modelo e assumir um.  
  
## <a name="components-of-project-template"></a>Componentes do modelo de projeto
 Um modelo de projeto é composto por três componentes:  
  
- **Estrutura hierárquica do trabalho**: Uma estrutura hierárquica do trabalho num modelo de projeto tem o mesmo conjunto de elementos que no projeto. Pode criar uma hierarquia de tarefas, associar funções à tarefa, definir atributos da agenda, definir dependências e ver todos os dados no gráfico Gantt. A estrutura hierárquica do trabalho nos modelos de projeto também suportam modos de tarefa para cada tarefa. Não existem diferença entre um modelo de projeto e um projeto ao criar a agenda de trabalho.  
  
- **Estimativas do projeto**: As estimativas do projeto em funcionam da mesma forma que nos projetos, à exceção das listas de preços, que para assumir por predefinição o custo e os preços de vendas, são sempre as listas de preços de venda e o custo definidos nos parâmetros do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. A restante funcionalidade é igual à de um projeto.  
  
- **Formação da equipa do projeto**: Ao formar uma equipa do projeto para um modelo de projeto, não é possível reservar um recurso nomeado num modelo. Pode utilizar **Gerar Equipa do Projeto** estrutura hierárquica do trabalho para gerar um conjunto de recursos genéricos. Também pode especificar as competências e as proficiências necessárias para os recursos genéricos. Não pode substituir um recurso genérico por um recurso reservável nos modelos do projeto.  
  
## <a name="create-a-project-from-a-template"></a>Criar um projeto a partir de um modelo  
 Pode criar um projeto a partir de um modelo das seguintes formas:  
  
-   Ao criar um projeto a partir da cotação, pode escolher um modelo de projeto no formulário de criação rápida de projeto.  
  
-   Ao criar um projeto clicando em **Novo Projeto**, o formulário do projeto é apresentado antes de guardar o registo. A partir daqui, poderá clicar no campo **Selecionar um modelo** para escolher na lista de modelos de projeto predefinidos na sua organização.  
  
-   Clique em **Criar projeto a partir de um modelo** na página **Modelo de Projeto** para criar um projeto a partir do modelo.  
  
## <a name="copying-components-of-a-template-to-a-project"></a>Copiar componentes de um modelo para um projeto  
 Quando copia os componentes de um modelo para um projeto, há alguns aspetos que deve conhecer.  
  
 **Copiar uma estrutura hierárquica do trabalho**: Quando copia a estrutura hierárquica do trabalho a partir de um modelo de projeto, se o projeto tiver um calendário do projeto diferente do modelo, as horas de trabalho do calendário do projeto serão aplicadas à agenda das tarefas. Isto ajusta a agenda ao calendário do projeto de reserva. Da mesma forma, a primeira tarefa na estrutura hierárquica do trabalho assume a data de início do projeto, pelo que a restante agenda da hierarquia de tarefas é atualizada com base na duração e nas dependências especificadas na estrutura hierárquica do trabalho  
  
 **Copiar estimativas do projeto**: Quando copia entre linhas de estimativa do projeto, as listas de preços são atualizadas com base na unidade proprietária do projeto para a lista de preços de custo e o cliente para a lista de preços de venda. O custo unitário e os preços de venda são determinadas com base nestas listas de preços nos projetos associados a uma entidade de vendas.  
  
 **Copiar uma equipa do projeto**: Quando copia a equipa do projeto do modelo para um projeto, os recursos genéricos são copiados com as competências e as proficiências definidas no modelo. As atribuições de recursos genéricos também são mantidas como no modelo do projeto.  
  
### <a name="see-also"></a>Consulte Também  
 [Guia do Gestor de Projeto](../project-service/project-manager-guide.md)
