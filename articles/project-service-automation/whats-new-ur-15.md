---
title: Novidades na Versão da Atualização 15 do Project Service Automation, V3
description: Esta tópico fornece informações sobre o que há de novo na Versão da Atualização 15 do Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: 75117934-8042-448b-91dc-b43f1f677e4f
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 68e0faa4c1afdb0d1520388253671330f9b7d334
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754533"
---
# <a name="project-service-automation-v3-update-release-15"></a>Versão da Atualização do Project Service Automation V3, Versão da Atualização 15

Temos o prazer de anunciar a atualização mais recente para a aplicação Dynamics 365 Project Service Automation (PSA). Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização. Esta versão é compatível com o Dynamics 365 9.x. Para atualizar esta versão, visite o Centro de Administração para o Dynamics 365 online e aceda à página de soluções para instalar a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Este tópico lista as funcionalidades e correções novas ou alteradas para o PSA V3, Versão da Atualização 15. Esta versão tem um número de compilação de V3.10.5.28 e está geralmente disponível através de uma Atualização automática em janeiro de 2020.

## <a name="update-release-15"></a>Versão da Atualização 15 

### <a name="enhancements"></a>Melhorias

- Gestão de Projetos

### <a name="bug-fixes"></a>Correções de erros

- Tempo e Despesa

  - Corrigido: Adicione a manipulação de erros no carregamento na vista de reconciliação.
  - Corrigido: Hub de Recursos de Projeto: renomeiar **Quantidade** para reduzir a ambiguidade.
  - Corrigido: ajuste a vista **Copiar Colunas de Entrada de Hora** para incluir o tipo.
  - Corrigido: a edição da duração da entrada de tempo na vista de grelha utilizando números decimais resulta em erro desconhecido para alguns números.

- Gestão de Projetos

  - Corrigido: o menu pendente para **Utilização na Vista de Monitorização** expande-se agora com base na largura das opções.
  - Corrigido: quando gerir projetos no fuso horário de +13, os cálculos das tarefas podem apresentar resultados imprecisos.
  - Corrigido: a **Hora de fim do membro da equipa** foi corrigida ao utilizar um calendário de 24 horas.
  - Corrigido: reativado o **BPF** no formulário principal **msdyn_project**.
  - Corrigido: o cálculo de atribuições deixa de ignorar um dia.
  - Corrigido: foi adicionada uma nova faixa de notificação ao formulário do projeto quando o fuso horário é diferente entre o utilizador e o projeto.

- Sales

  - Corrigido: a pesquisa de categorias de estimativa de despesas pode ser utilizada para filtrar duplicados.
  - Corrigido: código em **PluginDomain.ExecuteInTryCatchBlock(..)** já não oculta a origem da exceção.
  - Corrigido: já não obtém uma mensagem de erro na **Pesquisa de projeto** no formulário **Linha da Proposta** quando existem mais de 1000 projetos.
  - Corrigido: a grelha **Estimativas** para estimativas de mão-de-obra e estimativas de despesas apresenta agora o símbolo de moeda correto.
  - Corrigido: depois de uma organização atualizar o PSA da Versão da Atualização 14 para a Versão da Atualização 15, o separador **Agenda** deixa de aparecer como em branco no formulário **Projeto**.
