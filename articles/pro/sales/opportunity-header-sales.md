---
title: Definições de oportunidade – lite
description: Este artigo fornece informações sobre negócios baseados em projetos e linhas de oportunidade baseadas em projetos.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e2a95c57bff326237fb97a6cf432096833369eb8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934426"
---
# <a name="header-details-for-project-opportunities"></a>Detalhes do cabeçalho para oportunidades de projetos

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

O cabeçalho da Oportunidade capta as informações gerais sobre um negócio baseado em projetos que se aplica a todas as linhas na oportunidade baseada em projetos.

As oportunidades baseadas no Dynamics 365 Project Operations são extensões de oportunidades no Dynamics 365 Sales. Estas extensões fornecem funcionalidades adicionais específicas e necessárias para as oportunidades baseadas em projetos. Estas extensões podem incluir novos campos e ações do friso disponíveis em oportunidades baseadas em projetos. Pode concluir que alguns dos campos, funcionalidades e lógica de predefinição que estão disponíveis em Vendas não estão disponíveis no Project Operations.

A tabela seguinte inclui os campos numa oportunidade baseada em projetos que são exclusivos do Project Operations ou têm algumas alterações importantes no comportamento das Oportunidades em Vendas.

| **Campo** | **Localização** | **Descrição** | **Impacto a jusante** |
| --- | --- | --- | --- |
| Tipo | Separador Geral (oculto) | Este campo do conjunto de opções tem as seguintes opções:</br>- Baseado em trabalho (disponível apenas com o Project Operations)</br>- Baseado em item (disponível apenas quando o Project Operations e o Sales estão instalados)</br>- Baseado em manutenção do serviço (disponível quando o Field Service estiver instalado) | Quando utiliza o Project Operations, este valor de campo é definido automaticamente como **Baseado em trabalho**, que classifica a Oportunidade como baseada em projetos. Uma oportunidade deve ser baseada em projetos para ativar todas as funcionalidades e extensões específicas do projeto no processo de vendas a jusante para este negócio. |
| Contacto | Separador Geral | Referência ao contacto principal do cliente para este negócio. | |
| Conta | Separador Geral | Referência ao registo da conta ou empresa do cliente. | |
| Gestor de Contas | Separador Geral | O nome do Gestor de conta para esta oportunidade baseada em projetos. | O Gestor de conta é responsável pela gestão da relação com o cliente até à conclusão deste projeto. Baseado no registo de recurso reservável associado ao Gestor de conta, a unidade de contratação é assumida por predefinição. |
| Unidade de Contratação | Separador Geral | A Unidade organizacional que é responsável pela entrega do projeto ou projetos associados a este negócio. | A unidade de contratação é a divisão da empresa que executará os projetos após o fecho do negócio. Todas as unidades de contratação têm uma moeda, e esta moeda é utilizada para reportar os custos estimados e reais incorridos durante o projeto. |

Para todos os outros campos e secções no separador **Resumo** da oportunidade, consulte [Criar ou editar oportunidades (Sales e Hub de Vendas)](/dynamics365/sales-enterprise/create-edit-opportunity-sales)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
