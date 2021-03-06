---
title: Cabeçalho/resumo da oportunidade
description: Este tópico fornece informações sobre os negócios baseados em projetos e as linhas de oportunidade baseadas em projetos.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c4e91c1a869347ac1182db2de1ab9244309eb856
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908467"
---
# <a name="opportunity-headersummary"></a>Cabeçalho/resumo da oportunidade

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_


O cabeçalho ou o resumo da Oportunidade capta as informações gerais sobre um negócio baseado em projetos que se aplica a todas as linhas numa oportunidade baseada em projetos.

As oportunidades baseadas em projetos no Dynamics 365 Project Operations são extensões de oportunidades no Dynamics 365 Sales. Estas extensões fornecem funcionalidades adicionais específicas e necessárias para as oportunidades baseadas em projetos. Estas extensões podem incluir novos campos e ações do friso disponíveis em oportunidades baseadas em projetos. Pode concluir que alguns dos campos, funcionalidades e lógica de predefinição que estão disponíveis em Vendas não estão disponíveis no Project Operations.

A tabela seguinte inclui os campos numa oportunidade baseada em projetos que são exclusivos do Project Operations ou têm algumas alterações importantes no comportamento das Oportunidades em Vendas.

| **Campo** | **Localização** | **Relevância, finalidade e orientação** | **Impacto a jusante** |
| --- | --- | --- | --- |
| Tipo | Separador Geral (oculto) | Este campo do conjunto de opções tem as seguintes opções:</br>- Baseado em trabalho (disponível apenas com o Project Operations)</br>- Baseado em item (disponível apenas quando o Project Operations e o Sales estão instalados)</br>- Baseado em manutenção do serviço (disponível quando o Field Service estiver instalado) | Quando utiliza o Project Operations, este valor de campo é definido automaticamente como **Baseado em trabalho**, que classifica a Oportunidade como baseada em projetos. Uma oportunidade deve ser baseada em projetos para ativar todas as funcionalidades e extensões específicas do projeto no processo de vendas a jusante para este negócio. |
| Empresa Proprietária | Separador Geral | Esta é a empresa ou entidade legal que entregará o projeto ao cliente. | Estas informações do campo serão copiadas para o campo correspondente na proposta do Projeto que é criada a partir desta Oportunidade. |
| Contacto | Separador Geral | Referência ao contacto principal do cliente para este negócio. | |
| Conta | Separador Geral | Referência ao registo da conta ou empresa do cliente. | |
| Gestor de Contas | Separador Geral | O nome do Gestor de conta para esta oportunidade baseada em projetos. | O Gestor de conta é responsável pela gestão da relação com o cliente até à conclusão deste projeto. Baseado no registo de recurso reservável associado ao Gestor de conta, a unidade de contratação é assumida por predefinição. |
| Unidade de Contratação | Separador Geral | A Unidade organizacional que é responsável pela entrega do projeto ou projetos associados a este negócio. | A unidade de contratação é a divisão da empresa que executará os projetos após o fecho do negócio. Todas as unidades de contratação têm uma moeda, e esta moeda é utilizada para reportar os custos estimados e reais incorridos durante o projeto. |

Para todos os outros campos e secções no separador **Resumo** da oportunidade, consulte [Criar ou editar oportunidades (Sales e Hub de Vendas)](https://docs.microsoft.com/dynamics365/sales-enterprise/create-edit-opportunity-sales).
