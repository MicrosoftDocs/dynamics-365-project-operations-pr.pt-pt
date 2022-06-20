---
title: Novidades de novembro de 2021 - Implementação do Project Operations Lite
description: Este artigo fornece informações sobre as atualizações de qualidade que estão disponíveis na versão de novembro de 2021 da implementação do Project Operations Lite.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 947e7f6183ddeef3ab9a88d140331956bbcf23bd
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913818"
---
# <a name="whats-new-november-2021---project-operations-lite-deployment"></a>Novidades de novembro de 2021 - Implementação do Project Operations Lite

_Aplica-se a: Implementação lite – negócio para faturação pró-forma_

Este artigo aplica-se aos seguintes componentes e versões do Microsoft Dynamics 365 Project Operations:

- Project Operations num ambiente Dataverse, versão 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155
  
## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versão

Estão incluídas nesta versão as seguintes funcionalidades:

- As interfaces de programação de aplicações (APIs) do Agendamento de Projetos suportam agora a capacidade de criar e eliminar buckets do Projeto

## <a name="quality-updates"></a>Atualizações de qualidade

### <a name="project-operations-in-dataverse"></a>Project Operations no Dataverse

| Área de funcionalidades | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Faturação e Preços | 2358236 | A correção de faturas tem de permitir correções que tenham linhas de preço zero. |
| Gestão de Recursos | 2410072 | Permita a configuração de um recurso que está atribuído à tarefa como gestor de projetos. |
| Faturação e Preços | 2430234 | Corrija um problema de cálculo de desempenho de custo. |
| Tempo e Despesa | 2436978 | Permite que a hora ser introduzida no formato hh:mm. |
| Faturação e Preços | 2448623 | Permita que as listas de preços sejam atualizadas depois de associadas a uma unidade organizacional. |
| Tempo e Despesa | 2460396 | Deixe que uma entrada de tempo seja eliminada limpando a célula. |
| Faturação e Preços | 2467386 | Permita que um projeto que tenha uma tarefa seja eliminado, mesmo quando a tarefa está associada a uma cotação ganha. |
| Tempo e Despesa | 2461744 | A vista **A minha aprovação com falhas** contém apenas as aprovações de projetos na fase **Submetido**. |
| Tempo e Despesa | 2464082 | Remova a ligação das aprovações do projeto para o conjunto de aprovações quando o estado de destino for correspondido. |
| Tempo e Despesa | 2468108 | O trabalho de Agendamento não deve definir um estado de **Processamento** para o conjunto de aprovações. |
| Tempo e Despesa | 2471503 | Elimine os conjuntos de aprovações com sete dias de idade. |
| Faturação e Preços | 2480687 | A referência da linha de cotação não deve ser removida quando um marco da linha de cotação é criado. |
