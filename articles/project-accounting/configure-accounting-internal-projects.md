---
title: Configurar gestão contabilística para projetos internos
description: Este tópico fornece informações sobre como configurar práticas contabilísticas para projetos internos no Project Operations.
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9da72d8dbf720e380a49a1010caca472ee024783
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597858"
---
# <a name="configure-accounting-for-internal-projects"></a>Configurar gestão contabilística para projetos internos

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Os projetos internos permitem que as empresas monitorizem os custos relacionados com atividades que não estão a ser faturadas a um cliente. Exemplos de projetos internos incluem:

- Desenvolver um produto, como uma aplicação móvel, e monitorizar o custo associado ao desenvolvimento.
- Gerir o tempo e as despesas de pré-venda. Este projeto interno de pré-venda pode ser convertido mais tarde para um projeto faturável se a proposta for ganha.

Qualquer projeto não associado a um contrato em Dynamics 365 Project Operations é tratado como interno. Os perfis de custos e receitas do projeto não são utilizados para determinar regras contabilísticas para o projeto. O custo interno do projeto é sempre publicado utilizando princípios de lucros e perdas. As contas de livro razão para publicações são definidas na página **Configuração de publicação do livro razão**.

- As transações de tempo são publicadas debitando a conta **Custo** e creditando a conta **Alocação de folha de pagamentos**.
- As transações de despesas são publicadas debitando a conta **Custo** e creditando a conta **Conta de desfasamento para despesas**.
- As transações de item são publicadas debitando a conta **Custo** e creditando a conta **Custo - Item**.

Após as transações serem publicadas no projeto, se o projeto estiver associado a um contrato de projeto, o sistema reverte todas as transações acumuladas e cria novas transações faturáveis. As transações faturáveis seguem as regras contabilísticas definidas no respetivo perfil de receita e custo do Projeto.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
