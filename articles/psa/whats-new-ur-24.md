---
title: Novidades ou alterações na Versão da Atualização 24 do Project Service Automation, V3
description: Este tópico lista as funcionalidades e correções disponíveis no Project Service Automation V3, Versão da Atualização 24, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6c8348e65307f63a251f97bf1ea17578e7026da8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082356"
---
# <a name="project-service-automation-update-release-24-v3"></a>Versão da Atualização 24 do Project Service Automation, V3

Temos o prazer de anunciar a mais recente atualização à aplicação Project Service Automation para Dynamics 365. Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização. Esta versão é compatível com o Dynamics 365 9.x. Para atualizar esta versão, visite o Centro de Administração para o Dynamics 365 online e aceda à página de soluções para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Este tópico lista as funcionalidades e correções novas ou alteradas para o Project Service Automation V3, Versão da Atualização 24. Esta versão tem um número de compilação de V 3.10.42.43 e está geralmente disponível através de uma Atualização automática em outubro de 2020.

## <a name="update-release-24"></a>Versão da Atualização 24

### <a name="bug-fixes"></a>Correções de erros

**Sales**

Foram corrigidos os seguintes problemas:

- Problema ao definir a lista de preços predefinidos dos produtos.
- O desempenho da vitória de Proposta é lento devido à lista de preços incorporados e à cópia dos registos de preços de função.
- **Contrato do Projet/Hub de Vendas** > **Quantidade de Linha de Item/Encomenda de Linha de Produtos** é automaticamente arredondado para o número inteiro mais próximo.
- Elevar para privilégios do sistema ao ler listas de preços.
- Copie os campos de endereço do cliente **address1_freighttermscode** e **address1_shippingmethodcode** para Proposta/Encomenda. 


**Tempo e Despesa**

Foram corrigidos os seguintes problemas:

- A **Grelha de Entrada de Tempo** não suporta o comportamento de tempo **Apenas Data**.
- **Entrada de Tempo** não atualizar automaticamente. É necessária uma atualização manual.
- Não é possível importar as entradas de tempo de uma atribuição quando há uma pausa (0 horas) nas atribuições de um recurso.
- Ao criar uma entrada de tempo, defina o início para o mesmo **msdyn_date**.
- Reativar a edição em massa para entrada de tempo.

**Gestão de Recursos**

Foram corrigidos os seguintes problemas:

- Tentar atualizar o estado de uma reserva inter-diária sem um requisito irá lançar uma exceção null-ref.
- Erro ao carregar a **Vista de Reconciliação**.


**Gestão de Projetos**

Foram corrigidos os seguintes problemas:

- Na **Agenda do Projeto** , ao mudar de **Manual** para **Automático** , a atualização automática não é concluída.
- Os custos de despesas não contam para a variância na **Grelha de Monitorização do Projeto**.
- Comportamento inconsistente para colunas de **Etiqueta de estimativas** durante o carregamento vs. alterar o tipo **Fase de Tempo**.
- O custo real de um projeto pode não refletir os totais de **Atuais**.
- **Data de Conclusão Estimada** no separador **Resumo** não corresponde à **Agenda WBS**.
- **Atualizar Horas Atuais** no avanço não funciona corretamente.
- Um Gestor de projetos fora da raiz **BU** não pode criar um projeto.
- As alterações à tarefa ou à categoria em **Estimativas de Despesas** não persistem.
- **Cópia do contrato** copia os horários da fatura e o estado da execução.
- O botão **Atualizar Atuais** calcula incorretamente as tarefas resumidas.
- Microsoft Project Add-in: Corrigir um erro de referência nulo se algum membro da equipa tiver uma unidade de recursos vazia.
