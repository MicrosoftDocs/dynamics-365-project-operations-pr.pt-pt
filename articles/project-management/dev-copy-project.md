---
title: Desenvolver modelos de projeto com Copiar Projeto
description: Este artigo fornece informações sobre como criar modelos de projetos utilizando a ação personalizada Copiar Projeto.
author: stsporen
ms.date: 03/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 47c1023bbc4c21e3571bffbf3670bf0f7854f81d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923846"
---
# <a name="develop-project-templates-with-copy-project"></a>Desenvolver modelos de projeto com Copiar Projeto

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

O Dynamics 365 Project Operations suporta a capacidade de copiar um projeto e reverter quaisquer atribuições de volta aos recursos genéricos que representam a função. Os clientes podem usar esta funcionalidade para criar modelos básicos de projeto.

Quando selecionar **Copiar Projeto**, o estado do projeto-alvo é atualizado. Utilize **Razão do Estado** para determinar quando a ação da cópia está concluída. Selecionar **Copiar Projeto** também atualiza a data de início do projeto para a data de início atual se não for detetada nenhuma data-alvo na entidade-alvo do projeto.

## <a name="copy-project-custom-action"></a>Ação personalizada Copiar Projeto

### <a name="name"></a>Name 

msdyn\_CopyProjectV3

### <a name="input-parameters"></a>Parâmetros de entrada

Existem três parâmetros de entrada:

- **ReplaceNamedResources** ou **ClearTeamsAndAssignments** – Defina apenas uma das opções. Não defina ambas.

    - **\{"ReplaceNamedResources":true\}** – O comportamento predefinido do Project Operations. Quaisquer recursos nomeados são substituídos por recursos genéricos.
    - **\{"ClearTeamsAndAssignments":true\}** – O comportamento predefinido para o Project for the Web. Todas as atribuições e membros de equipa são removidos.

- **SourceProject** – A referência da entidade do projeto de origem a copiar. Este parâmetro não pode ser nulo.
- **Target** – A referência da entidade do projeto de destino para onde copiar. Este parâmetro não pode ser nulo.

A tabela seguinte apresenta um resumo dos três parâmetros.

| Parâmetro                | Type             | valor                 |
|--------------------------|------------------|-----------------------|
| ReplaceNamedResources    | Boolean          | **Verdadeiro** ou **Falso** |
| ClearTeamsAndAssignments | Boolean          | **Verdadeiro** ou **Falso** |
| SourceProject            | Referência de Entidade | O projeto de origem    |
| Target                   | Referência de Entidade | O projeto de destino    |

Para mais predefinições sobre ações, consulte [Utilizar ações API Web](/powerapps/developer/common-data-service/webapi/use-web-api-actions).

### <a name="validations"></a>Validações

As seguintes validações estão concluídas.

1. Null verifica e devolve os projetos de origem e de destino para confirmar a existência de ambos os projetos na organização.
2. O sistema valida se o projeto de destino é válido para copiar verificando as seguintes condições:

    - Não existe nenhuma atividade anterior no projeto (incluindo a seleção do separador **Tarefas**) e o projeto foi criado recentemente.
    - Não existe nenhuma cópia anterior, não foi pedida nenhuma importação neste projeto e o projeto não tem um estado **Com falhas**.

3. A operação não é chamada utilizando HTTP.

## <a name="specify-fields-to-copy"></a>Especificar campos a copiar

Quando a ação for convocada, **Copiar Projeto** irá analisar **Copiar Colunas do Projeto** da vista do projeto para determinar quais os campos a copiar quando o projeto é copiado.

### <a name="example"></a>Exemplo

O exemplo que se segue mostra como chamar a ação personalizada **CopyProjectV3** com o parâmetro **removeNamedResources** definido.

```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    public class CopyProjectSample
    {
        private IOrganizationService organizationService;

        public CopyProjectSample(IOrganizationService organizationService)
        {
            this.organizationService = organizationService;
        }

        public void SampleRun()
        {
            // Example source project GUID
            Guid sourceProjectId = new Guid("11111111-1111-1111-1111-111111111111");
            var sourceProject = new Entity("msdyn_project", sourceProjectId);

            Entity targetProject = new Entity("msdyn_project");
            targetProject["msdyn_subject"] = "Example Project - Copy";
            targetProject.Id = organizationService.Create(targetProject);

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption, true, false);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, bool replaceNamedResources = true, bool clearTeamsAndAssignments = false)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV3");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;

            if (replaceNamedResources)
            {
                req["ReplaceNamedResources"] = true;
            }
            else
            {
                req["ClearTeamsAndAssignments"] = true;
            }

            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```

[!INCLUDE[footer-include](../includes/footer-banner.md)]
