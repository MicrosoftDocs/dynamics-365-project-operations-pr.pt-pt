---
title: Novidades ou alterações na Versão da Atualização 34 do Project Service Automation, V3
description: Este artigo lista as funcionalidades e correções disponíveis na Versão 34 da Atualização do Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/05/2021
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
ms.reviewer: johnmichalak
ms.openlocfilehash: e47a5442f285952c165a2d30e337a362a6b065dd
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928676"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-34-v3"></a>Novidades ou alterações na Versão da Atualização 34 do Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente para a aplicação Microsoft Dynamics 365 Project Service Automation. Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização. É compatível com o Dynamics 365, versão 9.x. Para atualizar para esta versão, visite a página de soluções online do Centro de Administração do Dynamics 365 e instale a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este artigo lista as funcionalidades e correções novas ou alteradas para a Versão 34 da Atualização do Project Service Automation V3. Esta versão tem o número de compilação V3.10.55.38 e está em disponibilidade geral através de uma auto-atualização em julho de 2021.

## <a name="update-release-34"></a>Versão da Atualização 34

### <a name="bug-fixes"></a>Correções de erros
Foram corrigidos os seguintes problemas.

**Geral**

- As atualizações orientadas pelo fabricante não ativam o novo fluxo de trabalho de aprovação moderno.
- Faltam os atributos **Estado de Destino** e **Tipo de Ação** na página principal do **Conjunto de Aprovação**.

**Tempo e Despesa**

- Não é possível aprovar um pedido de recuperação utilizando o fluxo de aprovação moderno.
- Copiar uma semana de entradas de tempo não funciona ao copiar entradas que não estejam relacionadas com o utilizador com sessão iniciada.

**Planeamento de projeto**

- Os contornos de atribuição de recursos são corrompidos quando são importados do suplemento de ambiente de trabalho do Microsoft Project.

**Gestão de recursos**

- Quando publica um projeto a partir do suplemento de cliente de ambiente de trabalho do Microsoft Project, a data de fim dos requisitos existentes é alterada.
- A precisão decimal excede duas casas decimais na caixa de diálogo de confirmação de reservas de extensão.

**Vendas**

- Quando adiciona uma linha baseada no produto com um produto existente a um contrato de projeto, é apresentada uma exceção de **chave não encontrada no dicionário**.
- As oportunidades potenciais não podem ser qualificadas quando um tipo de encomenda é mapeado de uma oportunidade potencial para uma oportunidade.
