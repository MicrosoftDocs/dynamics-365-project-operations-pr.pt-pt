---
title: Novidades ou alterações na Versão da Atualização 21 do Project Service Automation, V3
description: Este tópico lista as funcionalidades e correções disponíveis no Project Service Automation V3, Versão da Atualização 21, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: 799be481c365e82e8ffb59ba242e30378644008b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126722"
---
# <a name="project-service-automation-update-release-21-v3"></a>Versão da Atualização 21 do Project Service Automation, V3

Temos o prazer de anunciar a mais recente atualização à aplicação Project Service Automation para Dynamics 365. Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização. Esta versão é compatível com o Dynamics 365 9.x. Para atualizar esta versão, visite o Centro de Administração para o Dynamics 365 online e aceda à página de soluções para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Este tópico lista as funcionalidades e correções novas ou alteradas para o Project Service Automation V3, Versão da Atualização 21. Esta versão tem o número de compilação V 3.10.32.50 e está geralmente disponível através de uma atualização automática em junho de 2020.

## <a name="update-release-21"></a>Versão da Atualização 21

### <a name="bug-fixes"></a>Correções de erros

**Tempo e Despesa**

Foram corrigidos os seguintes problemas:

- Ao hospedar o **Controlo da Grelha de Entrada de Tempo** nos Dashboards, a grelha não utiliza toda a largura do recipiente da grelha do dashboard.
- Para fusos horários específicos, o controlo da grelha de **Entrada de Tempo** não apresenta registos.
- As entradas de tempo que são depois das 9:00 PM aparecem no dia errado.
- Os utilizadores não podem apresentar despesas se a categoria de despesas, **Recibo de despesas exigido** não tiver qualquer valor.

**Gestão de Recursos**

Foram corrigidos os seguintes problemas:

- As reservas inativas são apresentadas na vista **Reconciliação**.
- Faltava a validação genérica do recurso para garantir a existência de um estado de reserva válido.

**Gestão de Projetos**

Foram corrigidos os seguintes problemas:

- As grelhas de formulário do **Projeto** (**Atribuição de Recursos**, **Tarefa**, vista **Reconciliação**, **Estimativas de Despesas**) continuam a ser editáveis mesmo quando um projeto não está ativo.
- Os clientes duplicados não podem ser unidos a clientes que estejam ligados a contratos de projeto confirmados.
- Quando um recurso que não tenha um calendário válido é adicionado, o sistema não devolve uma mensagem de erro amigável ao utilizador.
- O botão **Adicionar Tarefa** na grelha de tarefas está ativado quando o projeto está ligado ao **Suplemento do Microsoft Project**.
- O esforço cresce incontrolavelmente quando uma tarefa com uma categoria é atribuída a um recurso com uma função para a qual existe um preço de custo definido.

**Sales**

Foram feitos os seguintes melhoramentos:

- A **Frequência de Fatura** e o **Início da Faturação** foram transferidos para o separador **Agenda de Faturas**.

Foram corrigidos os seguintes problemas:

- O **Preço Total de Venda** é zero (0) para **Categoria**, embora a **Função** tenha um preço de venda total que não é zero.
- Os clientes não podem alterar o valor do campo de **Estado da Fatura** para **Pronto para Faturação** quando outro processo personalizado está a atualizar um campo adicional.
- O botão **Atualizar Linhas de Fatura** pode criar várias linhas duplicadas se for repetidamente selecionado.
- O botão **Atualizar Preços** não funciona na subgrelha **Preços de Função** no formulário **Vista Rápida**.
- A lógica de **Resolução da Lista de Preços de Venda** processa incorretamente fusos horários, resultando na seleção incorreta das listas de preços.
- O **Custo Total Real** de um projeto pode estar incorreto por um valor fracional após a aprovação de uma única entrada.
- A lógica de **Resolução de Preços** não fornece uma mensagem de erro amigável se **RolePrice Recuperado** não tiver valores nos campos **Unidade Principal** e **Preço na Unidade Principal**.
