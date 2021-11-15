---
title: Desempenho da API da Agenda do Projeto
description: Esta tópico fornece informações sobre os benchmarks de desempenho das APIs de Agenda do Projeto e identifica as melhores práticas para uma utilização otimizada.
author: ruhercul
ms.date: 11/03/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a1abadbae044ccbd40077c6937262f0f17387bad
ms.sourcegitcommit: 5c536cf05e2cbfc1d15982e4695d726064a074da
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 11/04/2021
ms.locfileid: "7750616"
---
# <a name="project-schedule-api-performance"></a>Desempenho da API da Agenda do Projeto

_**Aplicável a:** Project Operations para cenários baseados em recursos/itens não existentes em stock, implementação Lite - da transação à fatura pró-forma, Project for the Web_

Esta tópico fornece informações sobre os benchmarks de desempenho das interfaces de programação de aplicações (APIs) de Agenda do Projeto e identifica as melhores práticas para otimizar a utilização.

## <a name="project-scheduling-service"></a>Serviço de Agendamento de Projetos
O Serviço de Agendamento de Projetos é um serviço com vários inquilinos executado no Microsoft Azure. Foi concebido para melhorar a interação ao proporcionar uma experiência rápida e fluida quando os utilizadores trabalham nos projetos. Esta melhoria é conseguida ao aceitar os pedidos de alteração, processá-los e devolver imediatamente o resultado. O serviço persiste de forma assíncrona para o Dataverse e não impede os utilizadores de executarem outras operações.

As APIs de Agenda do Projeto recorrem ao Serviço de Agendamento de Projetos para executarem pedidos que são descritos em maior detalhe nas secções posteriores deste tópico.

As APIs de Agenda do Projeto foram concebidas para trabalhar com as seguintes entidades da estrutura hierárquica do trabalho (WBS):

  - Project
  - Tarefa de Projeto
  - Dependência de Tarefa de Projeto
  - Membro da Equipa do Projeto
  - Atribuição de Recurso
  
São suportados campos de configuração inicial e campos personalizados. Salvo indicação em contrário, são suportadas todas as operações comuns, tais como criar, atualizar e eliminar. Para mais informações, consulte [Utilizar APIs de Agenda do Projeto para executar operações e agendar entidades](schedule-api-preview.md).

Como parte das APIs de Agenda do Projeto, foi adicionado um padrão de unidade de trabalho. Este padrão é conhecido como OperationSet e pode ser utilizado quando é necessário processar vários pedidos numa única transação.

A seguinte ilustração mostra o fluxo que um parceiro irá experimentar quando esta funcionalidade é utilizada.

![O Dataverse e o fluxo do serviço de agendamento de projetos.](./media/dataverse-project-scheduling-service-flow.png)

**Passo 1**: um cliente faz uma chamada à API para um ponto final de Open Data Protocol (OData) no Dataverse para criar um OperationSet.

**Passo 2**: após a criação do novo OperationSet, é devolvido um valor **OperationSetId**.

**Passo 3**: o cliente utiliza o valor **OperationSetId** para fazer outro pedido de API de Agenda do Projeto. O resultado é criar, atualizar ou eliminar o pedido numa entidade de agendamento. Quando este pedido é feito, é feita a validação dos metadados. Se a validação falhar, o pedido é terminado e é devolvido um erro.

**Passos 4a–4c**: estes passos representam a fase ACEITAR. O cliente chama a API **ExecuteOperationSetV1**, que envia todas as alterações para o Serviço de Agendamento de Projetos num lote. O Serviço de Agendamento de Projetos executa as próprias validações nos pedidos no lote. Quaisquer falhas de validação anulam o lote e devolvem uma exceção ao chamador. Se o lote for aceite com êxito pelo Serviço de Agendamento de Projetos, o estado de OperationSet é atualizado para refletir o facto de o OperationSet estar a ser processado pelo Serviço de Agendamento de Projetos.

**Passo 5**: este passo representa a fase PERSISTIR. O Serviço de Agendamento de Projetos escreve de forma assíncrona o lote no Dataverse numa transação. Se a operação de escrita for concluída com êxito, o OperationSet é marcado como **Concluído**. Quaisquer erros revertem a transação e o lote, e o OperationSet é marcado como **Com Falhas**.

## <a name="performance-methodology"></a>Metodologia de desempenho
O tempo de execução é definido como o tempo desde a chamada para a API **ExecuteOperationSetV1** até o Serviço de Agendamento de Projetos concluir a escrita no Dataverse. Todas as operações são executadas de forma combinada 2200 vezes e são comunicadas as medições do tempo de execução P99. São medidas as operações de registo único e em massa.

Para uma operação de registo único, o OperationSet contém um pedido. Para as operações a massa, contém 20, 50 ou 100 pedidos. Cada tamanho em massa é comunicado em separado.

Estas operações são executadas numa implementação Project Operations Lite de UR 15 na América do Norte.

## <a name="results"></a>Resultados
### <a name="create-operations"></a>Criar operações
#### <a name="single-record-create-operations"></a>Operações de criação de registo único
A tabela seguinte mostra os tempos de execução para a criação de um registo único. Os tempos são apresentados em segundos.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Tipo de&nbsp;&nbsp;&nbsp;registo</th>
    <th class="tg-0lax" colspan="2">Tempo</th>
  </tr>
  <tr>
    <th class="tg-0lax">Campos necessários</th>
    <th class="tg-0lax">Todos os campos suportados</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">2.5</td>
    <td class="tg-0lax">3.78</td>
  </tr>
  <tr>
    <td class="tg-0lax">Tarefa</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Atribuição</td>
    <td class="tg-0lax">9.19</td>
    <td class="tg-0lax">9.19</td>
  </tr>
  <tr>
    <td class="tg-0lax">Membro da equipa</td>
    <td class="tg-0lax">0.84</td>
    <td class="tg-0lax">4.2</td>
  </tr>
  <tr>
    <td class="tg-0lax">Dependência</td>
    <td class="tg-0lax">8.84</td>
    <td class="tg-0lax">8.84</td>
  </tr>
</tbody>
</table>

#### <a name="bulk-create-operations"></a>Operações de criação em massa
A tabela seguinte mostra os tempos de execução para a criação de vários registos. Especificamente, a Microsoft mediu os tempos de execução para a criação de 20, 50 e 100 registos num único OperationSet. Os tempos são apresentados em segundos.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Tipo de&nbsp;&nbsp;&nbsp;registo</th>
    <th class="tg-0lax" colspan="6">Tempo</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 registos</th>
    <th class="tg-0lax" colspan="2">50 registos</th>
    <th class="tg-0lax" colspan="2">100 registos</th>
  </tr>
  <tr>
    <th class="tg-0lax">Campos necessários</th>
    <th class="tg-0lax">Todos os campos suportados</th>
    <th class="tg-0lax">Campos necessários</th>
    <th class="tg-0lax">Todos os campos suportados</th>
    <th class="tg-0lax">Campos necessários</th>
    <th class="tg-0lax">Todos os campos suportados</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Tarefa</td>
    <td class="tg-0lax">19.92</td>
    <td class="tg-0lax">38.35</td>
    <td class="tg-0lax">36.67</td>
    <td class="tg-0lax">99.13</td>
    <td class="tg-0lax">116.77</td>
    <td class="tg-0lax">174.06</td>
  </tr>
  <tr>
    <td class="tg-0lax">Atribuição</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">69.38</td>
    <td class="tg-0lax">69.38</td>
  </tr>
  <tr>
    <td class="tg-0lax">Dependência</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">176.89</td>
    <td class="tg-0lax">176.89</td>
  </tr>
</tbody>
</table>

> [!NOTE] 
> As operações de criação em massa nas entidades **Projeto** e **Membro da Equipa** não estão incluídas nesta tabela, porque o runtime para essas operações é semelhante ao runtime quando a API para criar um registo único é chamado várias vezes. Estas APIs são executadas imediatamente no Dataverse.

A ilustração seguinte mostra um gráfico dos tempos de execução para as entidades **Tarefa**, **Atribuição** e **Dependência** quando são criados 20, 50 e 100 registos, e são utilizados todos os campos suportados.

![Crie o grafo de tempo de execução de registos.](./media/create-record-execution-time.png)

### <a name="update-operations"></a>Operações de atualização
#### <a name="single-record-update-operations"></a>Operações de atualização de registo único
A tabela seguinte mostra os tempos de execução para as atualizações de um registo único. Os tempos são apresentados em segundos.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Tipo de&nbsp;&nbsp;&nbsp;registo</th>
    <th class="tg-0lax" colspan="2">Tempo</th>
  </tr>
  <tr>
    <th class="tg-0lax">Campos necessários </th>
    <th class="tg-0lax">Todos os campos suportados</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">9.53</td>
    <td class="tg-0lax">13.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Tarefa</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Membro da equipa</td>
    <td class="tg-0lax">9</td>
    <td class="tg-0lax">8.96</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> As operações de atualização nas entidades **Atribuições de Recursos** e **Dependência de Tarefa de Projeto** não são atualizadas.

#### <a name="bulk-update-operations"></a>Operações de atualização em massa
A tabela seguinte mostra os tempos de execução para as atualizações de vários registos. Especificamente, a Microsoft mediu os tempos de execução para as atualizações de 20, 50 e 100 registos num único OperationSet. Os tempos são apresentados em segundos.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Tipo de&nbsp;&nbsp;&nbsp;registo</th>
    <th class="tg-0lax" colspan="6">Tempo</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 registos</th>
    <th class="tg-0lax" colspan="2">50 registos</th>
    <th class="tg-0lax" colspan="2">100 registos</th>
  </tr>
  <tr>
    <th class="tg-0lax">Campos necessários</th>
    <th class="tg-0lax">Todos os campos suportados</th>
    <th class="tg-0lax">Campos necessários</th>
    <th class="tg-0lax">Todos os campos suportados</th>
    <th class="tg-0lax">Campos necessários</th>
    <th class="tg-0lax">Todos os campos suportados</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Tarefa</td>
    <td class="tg-0lax">8.91</td>
    <td class="tg-0lax">38.71</td>
    <td class="tg-0lax">20.92</td>
    <td class="tg-0lax">87.13</td>
    <td class="tg-0lax">36.68</td>
    <td class="tg-0lax">190.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Membro da equipa</td>
    <td class="tg-0lax">20.52</td>
    <td class="tg-0lax">26.06</td>
    <td class="tg-0lax">41.93</td>
    <td class="tg-0lax">44.51</td>
    <td class="tg-0lax">38.63</td>
    <td class="tg-0lax">66.53</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> As operações de atualização nas entidades **Atribuições de Recursos** e **Dependência de Tarefa de Projeto** não são atualizadas.

A ilustração seguinte mostra um gráfico dos tempos de execução para as entidades Tarefa e Membro da Equipa quando são atualizados 20, 50 e 100 registos, e são utilizados todos os campos suportados.

![Atualize o grafo de tempo de execução de registos.](./media/update-record-execution-time.png)

### <a name="delete-operations"></a>Operações de eliminação
#### <a name="single-record-delete-operations"></a>Operações de eliminação de registo único
A tabela seguinte mostra os tempos de execução para a eliminação de um registo único. Os tempos são apresentados em segundos.

| Tipo de registo | Tempo  |
|-------------|-------|
| Tarefa        | 20.12 |
| Atribuição  | 10.86 |
| Membro da equipa | 12.52 |
| Dependência  | 20.89 |

> [!NOTE]
> As operações de eliminação na entidade **Projeto** não são suportadas.

#### <a name="bulk-delete-operations"></a>Operações de eliminação em massa
A tabela seguinte mostra os tempos de execução para a eliminação de vários registos. Especificamente, a Microsoft mediu os tempos de execução para a eliminação de 20, 50 e 100 registos num único OperationSet. Os tempos são apresentados em segundos.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Tipo de&nbsp;&nbsp;&nbsp;registo</th>
    <th class="tg-0lax" colspan="3">Tempo</th>
  </tr>
  <tr>
    <th class="tg-0lax">20 registos</th>
    <th class="tg-0lax">50 registos</th>
    <th class="tg-0lax">100 registos</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Tarefa</td>
    <td class="tg-0lax">20.91</td>
    <td class="tg-0lax">67.43</td>
    <td class="tg-0lax">71.96</td>
  </tr>
  <tr>
    <td class="tg-0lax">Atribuição</td>
    <td class="tg-0lax">11.75</td>
    <td class="tg-0lax">25.79</td>
    <td class="tg-0lax">47.66</td>
  </tr>
  <tr>
    <td class="tg-0lax">Membro da equipa</td>
    <td class="tg-0lax">9.78</td>
    <td class="tg-0lax">39.73</td>
    <td class="tg-0lax">24.33</td>
  </tr>
  <tr>
    <td class="tg-0lax">Dependência</td>
    <td class="tg-0lax">24.61</td>
    <td class="tg-0lax">54.9</td>
    <td class="tg-0lax">109.16</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> As operações de eliminação na entidade **Projeto** não são suportadas.

A ilustração seguinte mostra um gráfico dos tempos de execução para as entidades **Tarefa**, **Atribuição**, **Membro da Equipa** e **Dependência** quando são eliminados 20, 50 e 100 registos.

![Elimine o grafo de tempo de execução de registos.](./media/delete-record-execution-time.png)

## <a name="observations"></a>Observações
Para cada operação de registo, a API **ExecuteOperationSet** demora cerca de 800 milissegundos a enviar um pedido para o Serviço de Agendamento de Projetos. Em seguida, o Serviço de Agendamento de Projetos demora cerca de cinco segundos a processar o payload e a chamar o Dataverse. O restante tempo de execução é dedicado a executar a lógica de negócio e a escrever os dados na base de dados no Dataverse.

Quando são criados, atualizados ou eliminados 100 registos, a API **ExecuteOperationSet** demora cerca de três segundos para enviar o pedido para o Serviço de Agendamento de Projetos. Em seguida, o Serviço de Agendamento de Projetos demora cerca de cinco segundos a processar os pedidos e a chamar o Dataverse. As operações em massa têm de pagar um **imposto de Serviço de Agendamento de Projetos** uma vez para todos os registos no OperationSet. Consequentemente, as operações em massa têm um tempo médio de execução significativamente mais baixo do que as operações de registo único.

## <a name="scenarios"></a>Cenários
A tabela seguinte mostra os tempos de execução quando as APIs de Agenda do Projeto são utilizadas para executar cenários específicos. Os tempos são apresentados em segundos.

| Cenário                                                                   | Tempo  |
|----------------------------------------------------------------------------|-------|
| Crie um projeto com 40 tarefas.                                      | 36.01 |
| Crie um projeto com 40 tarefas e 20 dependências.                  | 38.11 |
| Crie um projeto com 40 tarefas e 30 atribuições.                   | 60.17 |
| Crie um projeto com 40 tarefas, 20 dependências e 30 atribuições. | 60.27 |

## <a name="best-practices"></a>Melhores práticas
Baseado nos resultados do cenário anterior, as APIs têm um melhor desempenho nas seguintes condições:

  - Agrupe o maior número de operações possível. O runtime médio das operações em massa é melhor do que o runtime médio para as operações de registo único. Quanto menor for o número de OperaçãoSets em uso, mais rápido será o tempo médio de execução.
  - Defina apenas os atributos mínimos necessários para concretizar o seu cenário. Seja seletivo sobre os tipos de campos não obrigatórios incluídos num pedido OperationSet. Os campos que contêm chaves externas ou campos de rollup afetarão negativamente o desempenho.
