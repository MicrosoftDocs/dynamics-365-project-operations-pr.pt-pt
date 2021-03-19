---
title: Configurar gestão contabilística para projetos internos
description: Este tópico fornece informações sobre como configurar práticas contabilísticas para projetos internos no Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9f1cc75b12fec81d726e46f8d970dcfe030f6b29
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287612"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="48f01-103">Configurar gestão contabilística para projetos internos</span><span class="sxs-lookup"><span data-stu-id="48f01-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="48f01-104">_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_</span><span class="sxs-lookup"><span data-stu-id="48f01-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="48f01-105">Os projetos internos permitem que as empresas monitorizem os custos relacionados com atividades que não estão a ser faturadas a um cliente.</span><span class="sxs-lookup"><span data-stu-id="48f01-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="48f01-106">Exemplos de projetos internos incluem:</span><span class="sxs-lookup"><span data-stu-id="48f01-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="48f01-107">Desenvolver um produto, como uma aplicação móvel, e monitorizar o custo associado ao desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="48f01-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="48f01-108">Gerir o tempo e as despesas de pré-venda.</span><span class="sxs-lookup"><span data-stu-id="48f01-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="48f01-109">Este projeto interno de pré-venda pode ser convertido mais tarde para um projeto faturável se a proposta for ganha.</span><span class="sxs-lookup"><span data-stu-id="48f01-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="48f01-110">Qualquer projeto não associado a um contrato em Dynamics 365 Project Operations é tratado como interno.</span><span class="sxs-lookup"><span data-stu-id="48f01-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="48f01-111">Os perfis de custos e receitas do projeto não são utilizados para determinar regras contabilísticas para o projeto.</span><span class="sxs-lookup"><span data-stu-id="48f01-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="48f01-112">O custo interno do projeto é sempre publicado utilizando princípios de lucros e perdas.</span><span class="sxs-lookup"><span data-stu-id="48f01-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="48f01-113">As contas de livro razão para publicações são definidas na página **Configuração de publicação do livro razão**.</span><span class="sxs-lookup"><span data-stu-id="48f01-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="48f01-114">As transações de tempo são publicadas debitando a conta **Custo** e creditando a conta **Alocação de folha de pagamentos**.</span><span class="sxs-lookup"><span data-stu-id="48f01-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="48f01-115">As transações de despesas são publicadas debitando a conta **Custo** e creditando a conta **Conta de desfasamento para despesas**.</span><span class="sxs-lookup"><span data-stu-id="48f01-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>

<span data-ttu-id="48f01-116">Após as transações serem publicadas no projeto, se o projeto estiver associado a um contrato de projeto, o sistema reverte todas as transações acumuladas e cria novas transações faturáveis.</span><span class="sxs-lookup"><span data-stu-id="48f01-116">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="48f01-117">As transações faturáveis seguem as regras contabilísticas definidas no respetivo perfil de receita e custo do Projeto.</span><span class="sxs-lookup"><span data-stu-id="48f01-117">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]