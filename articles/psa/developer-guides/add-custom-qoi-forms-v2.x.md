---
title: Adicionar novos formulários de entidade personalizada (Project Service Automation 2.x)
description: Este tópico fornece informações sobre como adicionar formulários de entidade personalizada para oportunidades, propostas, encomendas ou faturas no Dynamics 365 Project Service Automation 2.x.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: e59e343887ef59ee28bee13346a0c9bf3ad7df27346e2a4f3f02a1e5c08c060f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995235"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a>Adicionar novos formulários de entidade personalizada (Project Service Automation 2.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a>Campo Tipo 

O Dynamics 365 Project Service Automation baseia-se no campo **Tipo** (**msdyn\_ordertype**) das entidades Oportunidade, Proposta, Encomenda e Fatura para distinguir as versões **baseadas em trabalho** destas entidades das versões **baseadas em item** e **baseadas em serviços**. As versões baseadas em trabalho destas entidades são processadas pelo PSA. Muitas das lógicas de negócio do lado do cliente e do lado do servidor da solução dependem do campo **Tipo**. Consequentemente, é importante que o campo seja inicializado com um valor correto quando as entidades são criadas. Um valor incorreto pode provocar comportamentos incorretos e alguma lógica de negócio poderá não ser executada corretamente.

## <a name="automatic-form-switching"></a>Mudança automática de formulários

Para evitar a possível corrupção de dados e comportamentos inesperados causados pela inicialização e edição incorretas dos registos de entidade de vendas, o PSA agora inclui lógica para a mudança automática de formulários em formulários fornecidos com o programa. Esta lógica direciona os utilizadores para o formulário correto para trabalharem com a versão baseada em trabalho ou qualquer outro tipo de entidade Oportunidade, Proposta, Encomenda ou Fatura. Quando um utilizador abre a versão baseada em trabalho de uma entidade Oportunidade, Proposta, Encomenda ou Fatura, o formulário é mudado para **Informações do Projeto**.

A lógica de mudança automática do formulário depende do mapeamento entre o valor **formId** e o campo **msdyn\_ordertype**. Todos os formulários fornecidos com o programa foram adicionados a esse mapeamento. No entanto, os formulários personalizados têm de ser adicionados manualmente para indicar qual versão da entidade pretendem processar. É baseado no campo **msdyn\_ordertype**. Se a mudança de formulários estiver a faltar no mapeamento, a lógica será mudada para o formulário fornecido com o programa, com base no valor guardado no campo **msdyn\_ordertype** da entidade.

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a>Adicionar formulários personalizados e ativar a lógica de mudança de formulários

O exemplo que se segue mostra como adicionar um formulário personalizado, **Informações do Meu Projeto**, para que o mesmo funcione com oportunidades baseadas em trabalho. O mesmo processo é utilizado para adicionar formulários personalizados para que funcionem com propostas, encomendas e faturas.

Siga estes passos para criar uma versão personalizada do formulário **Informações do Projeto**.

1. Na entidade Oportunidade, abra o formulário **Informações do Projeto** e guarde uma cópia sob o nome **Informações do Meu Projeto**.
2. Abra o novo formulário e, nas propriedades, certifique-se de que os scripts de inicialização de formulários do formulário **Informações do Projeto** estão presentes. 

    > [!IMPORTANT]
    > Não remova os scripts. Caso contrário, poderão ser inicializados incorretamente alguns dados.

3. Verifique se o campo **Tipo** (**msdyn\_ordertype**) está presente no formulário. 

    > [!IMPORTANT]
    > Não remova este campo. Caso contrário, os scripts de inicialização falharão.

4. Localize o valor **formId** do novo formulário. Pode concluir este passo de duas maneiras:

    - Exporte o formulário **Informações do Meu Projeto** como parte de uma solução não gerida e procure o valor **formId** no ficheiro customization.xml da solução exportada.
    - Abra o formulário **Informações do Meu Projeto** no editor de formulários e, em seguida, procure o identificador exclusivo global (GUID) junto do parâmetro **fromId** no URL, como mostrado na ilustração seguinte.

    ![O valor formId do novo formulário no URL.](media/how-to-add-custom-forms-in-v2.0.png)

5. Crie um mapeamento **msdyn\_ordertype** para o valor **formId** editando o recurso Web msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js. Remova o código do recurso e substitua-o pelo seguinte código.

    ```javascript
    define(["require", "exports"], function (require, exports) {
        "use strict";
        var SalesDocumentCustomFormIds = (function () {
            function SalesDocumentCustomFormIds() {
            }
            SalesDocumentCustomFormIds.overwriteFormIds = function (mappedFormIds) {
                /*
                ---- Notes ----
                mappedFormIds[SalesEntity][OrderType] => The array of forms IDs that support particular entity and order type
                Add or overwrite customized formId for the particular entity and order type by calling:
                    mappedFormIds[<EntityType>][<msdyn_ordertype>].push("<formId>");
                Allowed msdyn_ordertype values for reference:
                    ServiceBased: 690970002 (Field Service version of the entity)
                    WorkBased: 192350001 (PSA version of the entity)
                    ItemBased: 192350000 (Regular out of the box entity)
                Uncomment and update one of the following lines to register custom PSA form for required entity:
                */      
                //mappedFormIds[1][192350001].push("<formId>"); //Quote
                //mappedFormIds[5][192350001].push("<formId>"); //Quote Line
                //mappedFormIds[2][192350001].push("<formId>"); //Sales Order
                //mappedFormIds[6][192350001].push("<formId>"); //Sales Order Line
                // In this example we have added new form for Opportunity
                mappedFormIds[0][192350001].push("192EE537-DCC4-45D3-B7AF-EA694B9113D2"); //Opportunity
                //mappedFormIds[4][192350001].push("<formId>"); //Opportunity Line
            };
            return SalesDocumentCustomFormIds;
        }());
        exports.default = SalesDocumentCustomFormIds;
    });
    ```

6. Guarde e publique as personalizações.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]