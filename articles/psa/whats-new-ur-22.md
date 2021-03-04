---
title: Novidades ou alterações na Versão da Atualização 22 do Project Service Automation, V3
description: Este tópico lista as funcionalidades e correções disponíveis no Project Service Automation V3, Versão da Atualização 22, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: db4cbb9f9daadcb1911325f8bee987d5e480e1cf
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150997"
---
# <a name="project-service-automation-update-release-22-v3"></a>Versão da Atualização 22 do Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a mais recente atualização à aplicação Project Service Automation para Dynamics 365. Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização. Esta versão é compatível com o Dynamics 365 9.x. Para atualizar esta versão, visite o Centro de Administração para o Dynamics 365 online e aceda à página de soluções para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Este tópico lista as funcionalidades e correções novas ou alteradas para o Project Service Automation V3, Versão da Atualização 22. Esta versão tem o número de compilação V 3.10.33.48 e está geralmente disponível através de uma atualização automática em junho de 2020.

## <a name="update-release-22"></a>Versão da Atualização 22

### <a name="bug-fixes"></a>Correções de erros



**Tempo e Despesa**

Foram corrigidos os seguintes problemas:

- As **Entradas de tempo** não são automaticamente adicionadas à afe de de entradas de Tempo após a importação.
- O seletor de datas de grelha **Entrada de tempo** não reconhece as definições regionais de um utilizador.

**Gestão de Recursos**

Foram corrigidos os seguintes problemas:

- No modo manual, as alterações aos contornos de **Atribuição de Recursos** não são reconhecidas ao gerar **Requisitos de Recursos**.
- Os **Pedidos de Recursos** não suportam os estados de pedidos personalizados.

**Gestão de Projetos**

Foram corrigidos os seguintes problemas:

- A utilização de um duplo clique em EstimateGridControl não analisará corretamente os números de formato neerlandês.
- As horas atribuídas não atualizam corretamente quando as atribuições são alteradas utilizando o suplemento do cliente de ambiente de trabalho do Microsoft Project.
- As grelhas Estimativas e Rastreio de Projeto apresentam um código de moeda de venda incorreto quando a moeda do contrato é diferente da moeda do cliente e a organização é configurada para exibir códigos de moeda em vez de símbolos de moeda.
- A data de conclusão de um membro da Equipa acrescentará um dia se o horário de trabalho for de 24 horas por dia.
- Na Agenda do Projeto, adicionar uma Categoria de Transação a uma tarefa não aciona o guardar automático.
- O seguinte erro é apresentado ao adicionar um membro da equipa ao Modelo de Projeto: "Os requisitos de recursos não podem ser associados a modelos de projeto". 
- O script da regra do friso "msdyn.Approval.CanApproveOrReject" apresenta um erro de tempo limite.

**Sales**

Foram corrigidos os seguintes problemas:

- A mensagem de erro de validação não apresentada quando uma Lista de Preços de Custo é selecionada na procura da Lista de Preços no formulário/entidade "Nova Lista de Preços de Projeto de Proposta".
- Fechar a proposta como ganha não navega para o contrato criado se um BPF anexado à proposta estiver na fase final.
- Reverter **Vendas não fatutradas** está associado ao custo original quando uma entrada de tempo é recuperada.
- Depois de selecionar o botão **Confirmar**, o estado da fatura não muda para **Confirmado** a menos que a fatura seja atualizada.
