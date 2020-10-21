---
title: Descrição geral da despesa
description: Este tópico fornece informação sobre a funcionalidade Despesa no Project Operations.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 6da831fef5dba060b8019d7689645405c7ebdbed
ms.sourcegitcommit: 0874b3d89e1dc0e65a51cedb82bf8f80831ca0bb
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/06/2020
ms.locfileid: "3967380"
---
# <a name="expense-home-page"></a>Home page das despesas

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_


O Dynamics 365 Project Operations suporta a capacidade de processar despesas. O processamento de despesas ocorre com ou sem projetos através de um fluxo de trabalho personalizável de políticas, categorias de transação e aprovações.

No Project Operations, existem dois modelos de implementação suportados para Despesas: 

- **Completo**: está disponível a implementação completa para o **Project Operations para cenários baseados em recursos/não armazenados** ou **Project Operations para cenários baseados em encomenda de produção**.
- **Básico**: a implementação básica está disponível para **Project Operations para cenários baseados em recursos/não armazenados** e **Implementação leve – oportunidade potencial para fatura pró-forma**.

## <a name="full"></a>Total 
A implementação Despesa Total fornece uma aplicação completa de políticas que inclui a capacidade de criar políticas, tais como:

  - Limites da categoria de despesa
  - Viagens
  - Diária
  - Importações de cartão de crédito
  - Reconhecimento de caracteres óticos de recibos

## <a name="basic"></a>Básica 
O cenário de implementação Despesa Básica só permite registar as despesas básicas para um projeto. 

Para mais informações, consulte [Entrada de despesas (lite)](basic-expense.md)

## <a name="determine-your-expense-deployment"></a>Determinar a Implementação de despesa
Para determinar se está a executar a implementação da gestão Despesa Básica, verifique se o URL do endereço termina com **.crm.dynamics.com**. 
