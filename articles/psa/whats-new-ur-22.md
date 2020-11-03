---
title: Novidades ou alterações na Versão da Atualização 22 do Project Service Automation, V3
description: Este tópico lista as funcionalidades e correções disponíveis no Project Service Automation V3, Versão da Atualização 22, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: badd87a276d68d9959e9cca4220daf61ed570638
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082352"
---
# <a name="project-service-automation-update-release-22-v3"></a>Versão da Atualização 22 do Project Service Automation, V3

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
- Depois de selecionar o botão **Confirmar** , o estado da fatura não muda para **Confirmado** a menos que a fatura seja atualizada.
