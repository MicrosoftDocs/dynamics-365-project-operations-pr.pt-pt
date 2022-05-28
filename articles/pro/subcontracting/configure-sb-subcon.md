---
title: Configurar o Quadro da Agenda para mostrar trabalhadores contratados e capacidade subcontratada
description: Este tópico descreve como configurar o Quadro da Agenda no Microsoft Dynamics 365 Project Operations para mostrar capacidade de recursos subcontratados ao dotar requisitos de recursos do projeto.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 6e382b33fafe91c8b96a91d033fe12b998114bdc
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587860"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Configurar o Quadro da Agenda para mostrar trabalhadores contratados e capacidade subcontratada 

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

O Quadro da Agenda no Microsoft Dynamics 365 Project Operations pode ser utilizado para pesquisar recursos de duas formas:

- Pesquisa geral de recursos sem o contexto de qualquer requisito específico de recursos baseados em projetos.
- Pesquisa de recursos específicos de requisito onde o requisito do projeto fornecerá o contexto para os recursos sugeridos.

Para notificar o quadro da agenda de capacidade de recurso subcontratado e dos trabalhadores contratados, é necessário fazer atualizações às definições do Quadro da Agenda. Estas atualizações incluem: 
- Atualizar as definições do Quadro da Agenda para pesquisa geral de recursos.
- Atualizar as definições do Quadro da Agenda para pesquisa de recursos baseada em requisitos.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Atualizar as definições do Quadro da Agenda para pesquisa geral de recursos
### <a name="update-filters-for-general-resource-search"></a>Atualizar filtros para pesquisa geral de recursos
Ao pesquisar um recurso, os filtros disponíveis no quadro da agenda devem ser atualizados para que também possa pesquisar recursos externos especificando qualquer ou todos os seguintes:
  - Tipo de trabalhador, se os recursos apresentados devem ser trabalhadores contratados ou colaboradores.
  - Empresa do fornecedor ao qual um recurso deve pertencer.
  - Recursos pertencentes a subcontrato ou item de subcontrato específicos.
    
### <a name="update-retrieve-resource-query"></a>Atualizar a consulta de obtenção de recursos
A consulta utilizada para pesquisar também deve ser atualizada para utilizar estes atributos de filtro adicionais. Utilize os seguintes passos para atualizar a configuração do Quadro da Agenda para pesquisa geral de recursos:  
1. Abra as **Definições do Quadro da Agenda** para um Quadro da Agenda específico.
2. Abra o separador **Definições gerais** e desloque-se para **Outras definições**.
3. Na lista de definições nesta secção, atualize o **Esquema de Filtros** para **Esquemas de Filtros Predefinidos para o Project Operations Lite**.
4. Atualize **Consulta de Obtenção de Recursos** para **Consulta de Obtenção de Recursos Predefinida para o Project Operations Lite**.

![Atualizar as definições do Quadro da Agenda para pesquisa geral de recursos](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Atualizar as definições do Quadro da Agenda para pesquisa de recursos baseada em requisitos
### <a name="update-filters-for-requirement-specific-resource-search"></a>Atualizar filtros para pesquisa de recursos específica de requisitos 
Ao pesquisar um recurso, os filtros disponíveis no quadro da agenda devem ser atualizados para que também possa pesquisar recursos externos especificando qualquer ou todos os seguintes:
 - Tipo de trabalhador, se os recursos apresentados devem ser trabalhadores contratados ou colaboradores.
 - Empresa do fornecedor ao qual um recurso deve pertencer.
 - Recursos pertencentes a subcontrato ou item de subcontrato específicos.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Atualizar a consulta de obtenção de recursos para pesquisa de recursos específica de requisitos 
A consulta utilizada para pesquisar também deve ser atualizada para utilizar estes atributos de filtro adicionais. Utilize os seguintes passos para atualizar a configuração do Quadro da Agenda para pesquisa de recursos baseada em requisitos:

1. Abra as **Definições do Quadro da Agenda** para um Quadro da Agenda específico e, em seguida, selecione **Abrir definições predefinidas** para abrir as definições para pesquisa específica de requisitos.
2. Abra o separador **Definições gerais** e desloque-se para **Outras definições**.
3. Na lista de definições nesta secção, atualize o **Esquema de Filtros** para **Esquemas de Filtros Predefinidos para o Project Operations Lite**.
4. Atualize **Consulta de Obtenção de Recursos** para **Consulta de Obtenção de Recursos Predefinida para o Project Operations Lite**.
5. Abra o separador **Tipos de Agenda** e vá a **Projeto**.
6. Sob as definições de **Projeto**, atualize **Consulta de Obtenção de Recursos do Assistente da Agenda** para **Consulta de Obtenção de Recursos Predefinida para o Project Operations Lite** e atualize **Consulta de Obtenção de Restrições do Assistente da Agenda** para **Consulta de Obtenção de Restrições para o Project Operations Lite**.

![Atualizar as definições do Quadro da Agenda para pesquisa de recursos baseada em requisitos](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
