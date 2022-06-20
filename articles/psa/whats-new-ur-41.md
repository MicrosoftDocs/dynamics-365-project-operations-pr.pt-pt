---
title: Novidades ou alterações na Versão da Atualização 41 do Project Service Automation, V3
description: Este artigo lista as funcionalidades e correções disponíveis na Versão 41 da Atualização do Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/07/2022
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
ms.openlocfilehash: 8625ae16e45da30614b3a3eec44193bee0c0b36f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930562"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-41-v3"></a>Novidades ou alterações na Versão da Atualização 41 do Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente para a aplicação Microsoft Dynamics 365 Project Service Automation. Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização. É compatível com o Dynamics 365, versão 9.x. Para atualizar para esta versão, visite a página de soluções online do Centro de Administração do Dynamics 365 e instale a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este artigo lista as funcionalidades e correções novas ou alteradas para a Versão 41 da Atualização do Project Service Automation, V3. Esta versão tem um número de compilação de V3.10.62.162 e está geralmente disponível através de uma auto-atualização em março de 2022.

## <a name="update-release-41"></a>Versão da Atualização 41

### <a name="bug-fixes"></a>Correções de erros

Foram corrigidos os seguintes problemas.

**Gestão de Projetos**
- Quando tenta criar um projeto a partir de um modelo baseado num projeto criado a partir do suplemento de ambiente de trabalho, o erro seguinte é apresentado, "Validação de campo de trabalho planeado da atribuição de recursos: a data de fim de setor de tempo de cada atribuição de recurso não deve ser anterior à data de início".

**Tempo e Despesa**
- Quando tenta eliminar uma entrada de tempo, é apresentada a mensagem de erro seguinte, "Ocorre um erro inesperado a partir do código ISV".

**Vendas**
- Quando cria uma fatura para um marco de preço fixo, os campos **Descrição** e **Descrição externa** não são povoados. 
