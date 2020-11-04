---
title: Gerir oportunidades baseadas em projetos
description: Este tópico fornece informações sobre como trabalhar com oportunidades relacionadas com projetos.
author: rumant
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 39ce52d5da4c7027ee2f2fa44579c0d4bf74925e
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088055"
---
# <a name="manage-project-based-opportunities"></a>Gerir oportunidades baseadas em projetos

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

As empresas baseadas em projetos normalmente têm as suas operações de entrega espalhadas por vários países e geografias. O custo da execução e entrega do projeto pode variar em função do qual a geografia ou divisão gere a entrega. Por sua vez, isto pode ter impacto nas margens do negócio. A prestação de serviços baseados em projetos envolve normalmente grandes quantidades de tempo de recursos humanos, despesas consideráveis para viagens, custos materiais e outras despesas.

As oportunidades baseadas em projetos no Dynamics 365 Project Operations são concebidas com extensões para o Dynamics 365 Sales. O tópico fornece detalhes sobre as diferentes áreas e lógica de negócio incluída na funcionalidade adicional que é exigida pelas empresas baseadas em projetos para gerir oportunidades baseadas em projetos.

## <a name="view-all-project-based-opportunities"></a>Ver todas as oportunidades baseadas em projetos

Uma lista de todas as oportunidades baseadas em projetos pode ser vista na página da lista **Oportunidade**. 

1. Aceda a **Vendas** > **Oportunidades**.
2. Utilize **Ver comutador** para selecionar outras vistas filtradas das oportunidades. Pode criar as suas próprias vistas com critérios de filtro personalizados para configurar estas vistas e opções de navegação.

As Oportunidades de Projeto podem ser criadas ou eliminadas a partir desta página de lista ou da página de detalhes.

## <a name="business-process-flow-for-project-based-deals"></a>Fluxo do processo de negócio para as oportunidades potenciais baseadas em projetos

Os seguintes fluxos do processo de negócio são suportados para as oportunidades potenciais baseadas no projeto no Project Operations:

- Processo de negócio da Oportunidade Potencial à Oportunidade
- Processo de vendas da Oportunidade

### <a name="lead-to-opportunity-business-process"></a>Processo de negócio de Oportunidade Potencial a Oportunidade 
O processo de negócio da oportunidade potencial à oportunidade suporta as seguintes fases:

| Fase | Entidade mapeada | Funcionalidade |
| --- | --- | --- |
| Qualificar | Oportunidade Potencial | Qualifique a oportunidade potencial para criar uma conta, um contacto e uma oportunidade. |
| Desenvolver | Oportunidade | Desenvolva a oportunidade para adicionar mais informações sobre o trabalho envolvido, os principais intervenientes e a concorrência. |
| Propor | Oportunidade | Desenvolva a proposta e obtenha a aprovação da equipa de revisão interna. |
| Fechar | Oportunidade | Ganhe a oportunidade de fechar o negócio. |

### <a name="opportunity-sales-process"></a>Processo de vendas da Oportunidade
O processo de vendas de Oportunidades no Project Operations é uma extensão ao fluxo de negócio do processo de vendas de Oportunidades na aplicação Sales. Este processo de negócio foi concebido pronto a utilizar para suportar as seguintes fases numa oportunidade baseada em projetos.

| Fase | Entidade mapeada | Funcionalidade |
| --- | --- | --- |
| Qualificar | Oportunidade | Qualifique a oportunidade potencial para criar uma conta, um contacto e uma oportunidade. |
| Propor | Proposta | Desenvolva a proposta utilizando propostas de projeto e obtenha a aprovação da equipa de revisão interna. |
| Contrato | Contrato do Projeto | Ganhe a proposta para criar o contrato e inicie a execução e entrega do projeto. |
| Fechar | Contrato do Projeto | Termine o trabalho com sucesso e feche o contrato do projeto. |

> [!NOTE]
> Se o seu negócio baseado em projetos começou com uma Oportunidade Potencial, o processo de negócio de Oportunidade Potencial a Oportunidade tem precedência.
>
> Se o seu negócio baseado em projetos começou com uma Oportunidade, o processo de vendas de Oportunidades tem precedência.

Pode editar o fluxo de processo empresarial de produto ou criar os seus próprios fluxos de processo empresarial para monitorizar o seu processo de vendas, conforme necessário. Para mais informações sobre o fluxos do processo empresarial, consulte [Descrição geral de fluxos do processo empresarial](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).