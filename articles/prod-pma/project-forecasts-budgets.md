---
title: Previsões e orçamentos de projetos
description: O Microsoft Dynamics 365 Finance fornece previsões de projetos e orçamentos de projeto para gerir e controlar os seus projetos.
author: Yowelle
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c1c1cde984334af8cc30e7899e3cf0b38467666f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999640"
---
# <a name="project-forecasts-and-budgets"></a>Previsões e orçamentos de projetos

[!include [banner](../includes/banner.md)]

Existem duas formas de gerir e controlar os seus projetos: previsões de projetos e orçamentos de projetos. 

Utilize a previsão se a sua organização tiver uma perspetiva operacional, e se concentrar nas receitas e nos custos provenientes de transações específicas. Utilize a orçamentação de projetos se a sua organização se concentrar mais nos montantes financeiros. 

Tanto as previsões de projetos como os orçamentos de projetos utilizam modelos de previsão para manter os montantes de transação projetados. 

Cada método tem as suas vantagens. Deve considerar os seguintes pontos antes de selecionar um método para a sua organização.

|   Método de alocação       |           Previsão do projeto            |        Orçamentação do projeto                           |
|---------------------------|------------------------------------------|----------------------------------------------------|
| **Alocação de períodos**     | Não pode alocar transações explicitamente durante um período fiscal. Em vez disso, a previsão, e o controlo da previsão baseiam-se na vida útil do projeto. Como as previsões se baseiam numa data específica, tem de inferir o período a partir da data. | Pode alocar transações durante todo o projeto ou um período fiscal. Se alocar durante um período, pode transportar montantes não utilizados para o próximo período fiscal. |
| **Ver transações**  | Pode ver as transações nos formulários de previsão, onde verá as previsões para toda a empresa e para todos os projetos, independentemente da hierarquia. Para se concentrar num projeto específico, é necessário filtrar os dados.                                       | Pode ver transações orçamentadas para uma única hierarquia de projeto. Assim, poderá ver os detalhes da transação para um projeto principal ou os seus subprojetos.                 |
| **Variáveis da transação** | Quando introduz transações de previsão, pode utilizar cada atributo existente para uma transação real. Isto permite um maior detalhe na previsão. Por exemplo, pode introduzir detalhes para as quantidades, os trabalhadores, os itens ou as propriedades da linha.         | Quando introduz os detalhes orçamentais, só pode utilizar montantes, categorias e atividades.                    |
| **Segurança**              | A previsão baseia-se em transações que introduz nos formulários de previsão e não envolve nenhum mecanismo de controlo de processos. Qualquer trabalhador que tenha permissões para um formulário de previsão pode rever as informações sem aprovação.                                        | A orçamentação utiliza o sistema de fluxo de trabalho, que permite a gestão de alterações e permite manter um histórico das revisões.         |
| **Tipo de entrada**           | As entradas de transações de previsão baseiam-se no número de unidades, e nos preços unitários de custo e venda.  | Os detalhes orçamentais baseiam-se em montantes, que são divididos entre custos e receitas.                                          |
| **Modelos de previsão**       | Como cada previsão tem de ser associada a um modelo, pode criar vários modelos de previsão e também configurar submodelos.           | A orçamentação de projetos limita os modelos de previsão que são utilizados para a orçamentação. Menos modelos de previsão podem ajudar a aumentar a consistência nas projeções.                           |
| **Derrapagens de custos**         | Só pode permitir ou não permitir a entrada de transações que causem uma derrapagem de custos.   | A orçamentação de projetos fornece opções de controlo adicionais para os utilizadores. Pode permitir avisos e derrapagens.                    |
| **Controlo**               | O controlo de previsões é efetuado através da redução da previsão. Os montantes reais são subtraídos dos saldos de transações previstos sem qualquer registo de auditoria. Isto pode dificultar o rastreio de onde as transações reais ocorreram.                   | No controlo do orçamento do projeto, os montantes reais são subtraídos dos montantes do orçamento restante. Isto permite um registo de auditoria mais claro.                                   |

## <a name="project-forecasts"></a>Previsões do projeto
Quando utiliza a previsão de projetos, pode introduzir transações de previsão em formulários de previsão para cada tipo de transação. Todos os atributos que estão disponíveis para uma transação real podem ser utilizados para uma transação de previsão, por exemplo, rentabilidade da linha, atributos da linha, trabalhadores ou descrições. Também pode projetar quanto tempo depois de incorrer num custo irá faturar um cliente. 

As transações de previsão de projetos baseiam-se em unidades e montantes. 

Tem de associar cada previsão de projeto a um modelo de previsão. Quando introduz uma transação de previsão, é sugerido automaticamente um modelo de previsão. O modelo de previsão funciona como um contentor para as transações de previsão. 

Pode designar modelos de previsão como submodelos para um modelo. Isto permite fazer previsões por região, período ou departamento. Pode copiar as transações de previsão num modelo para criar um novo modelo e também pode transferir as transações para o razão geral. Como existe uma relação de um-para-um entre uma previsão e um modelo, cada modelo de previsão compõe um orçamento separado para um projeto. 

Os modelos de previsão podem utilizar a redução da previsão como mecanismo de controlo para projetos. Na redução da previsão, as transações reais reduzem os saldos das transações de previsão. No entanto, como a redução da previsão é aplicada ao projeto mais elevado na hierarquia, proporciona uma visão limitada das alterações na previsão. Por exemplo, se um trabalhador estiver associado a um subprojecto, as transações reais para o trabalhador são lançadas no projeto principal. Isto pode dificultar a monitorização das alterações, porque não é possível determinar facilmente qual a transação em que o subprojecto causou uma redução no montante previsto. Assim, é uma boa ideia criar uma cópia de um modelo de previsão para a redução de previsão a utilizar. Em seguida, pode utilizar os relatórios para ver qual era a previsão original. 

Pode rever, copiar, eliminar ou transferir as previsões do projeto para um orçamento do razão geral. No entanto, não existe qualquer controlo de processo. Qualquer trabalhador que tenha permissão para um formulário de previsão pode fazer revisões sem revisão.

-   **Rever** – Pode rever uma transação de previsão nos mesmos formulários em que as entradas originais foram feitas.
-   **Copiar ou eliminar** – quando copia as transações de previsão, está a copiar as linhas de transação de um modelo de previsão para outro modelo de previsão. Quando elimina uma previsão, está a eliminar as transações de previsão a partir de um modelo de previsão. Para limitar as transações de previsão que são copiadas ou eliminadas, selecione tipos e datas de transações específicas. Isto permite-lhe copiar ou eliminar apenas partes específicas de uma previsão.
-   **Transferência** – Ao transferir uma previsão de projeto para um orçamento do razão geral, está a transferir as transações de previsão de um modelo de previsão para um orçamento do razão geral. Pode substituir quaisquer transações transferidas previamente no orçamento do razão geral para o qual transfere a sua previsão do projeto.

## <a name="project-budgets"></a>Orçamentos de projetos
A orçamentação de projetos é um método mais simples do que a previsão, apesar de se integrar com os modelos de previsão. Utiliza um formulário de entrada única para os detalhes e as revisões orçamentais originais, e permite projeções baseadas apenas no montante, categoria ou atividade. 

Na orçamentação de projetos, todos os orçamentos e revisões originais têm de ser enviados para um fluxo de trabalho do projeto para aprovação. Os fluxos de trabalho dão-lhe um maior controlo sobre o processo e criam um registo do histórico de alterações. 

A orçamentação de projetos assemelha-se à orçamento do razão geral, mas é mais rápida e fácil de configurar. Muitas das opções na orçamentação do razão geral, tais como as sequências numéricas ou a moeda, não têm de ser configuradas em separado para os projetos.

Os orçamentos de projetos são associados automaticamente a dois modelos de previsão, um para o orçamento original e outro para o orçamento restante. Assim, os relatórios baseados em modelos de previsão podem utilizar os dados orçamentais. Quando um orçamento do projeto é consolidado, o sistema cria transações de previsão com base nos modelos associados, que são utilizados para fins de geração de relatórios e controlo.

## <a name="forecast-models"></a>Modelos de previsão
Os modelos de previsão têm uma hierarquia de camada única. Isto significa que uma previsão de projeto tem de ser associada a um modelo de previsão.

Se utilizar a previsão de projetos, pode identificar modelos como submodelos. E, seguida, pode criar previsões por departamento, período ou região. Por exemplo, pode criar um modelo de previsão para um ano e, depois, criar submodelos para as previsões regionais de Nordeste, Sudeste, Noroeste e Sudoeste que os responsáveis regionais enviam. Ao selecionar diferentes opções nos relatórios disponíveis, pode ver as informações por previsão total ou por submodel.





[!INCLUDE[footer-include](../includes/footer-banner.md)]