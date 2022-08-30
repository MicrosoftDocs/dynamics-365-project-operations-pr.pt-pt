---
title: Sincronizar Estado do Projeto para impedir entradas em projetos fechados
description: Este artigo explica como sincronizar o Estado do Projeto para impedir entradas em projetos inativos ou fechados.
author: ryansandnessMSFT
ms.date: 08/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandnessMSFT
ms.openlocfilehash: 7a306da164235f36d9ed5e69196508dce6d257de
ms.sourcegitcommit: 6b6c2bfd04e3e613ed1f38355c7cd47c3a56748d
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348039"
---
# <a name="sync-project-status-to-prevent-entry-against-closed-projects"></a>Sincronizar Estado do Projeto para impedir entradas em projetos fechados

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

## <a name="scenario"></a>Cenário

A Contoso lançou o Microsoft Dynamics 365 Project Operations para cenários de recursos/sem existências. Como parte das atividades normais do negócio, os projetos podem ser concluídos ou colocados em espera. Pode desativar o projeto para garantir que não são geradas despesas nem faturas.

## <a name="solution"></a>Solução

### <a name="prerequisites"></a>Pré-requisitos

-   Tem de ser instalado o Microsoft Dynamics 365 Finance 10.0.29 ou posterior.
-   O mapa de Escrita Dupla 1.0.0.3 para Projects V2 (msdyn\_projetos) tem de ser instalado ou configurado manualmente conforme descrito abaixo.

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>Criar uma versão atualizada do mapa de escrita dupla do Projects V2 de integração do Project Operations

Para atualizar o mapa de escrita dupla do Projects V2 do Project Operations:

1. Aceda à área de trabalho **Gestão de dados** e selecione **Escrita dupla**.
2. Selecione o mosaico **Escrita dupla**.
3. Na coluna **Mapa da tabela**, localize e selecione **Project V2 (msdyn\_projetos)** e, em seguida, selecione Parar.
4. Selecione o nome do mapa para abrir o mapa e, em seguida, selecione **[Nenhum]**.
5. Na caixa de diálogo Selecionar colunas, selecione **statecode \[Estado do Projeto\]** e, em seguida, selecione OK. Pode escrever **estado** no valor do filtro para limitar a lista.
6.  Selecione **Adicionar ou editar transformação** na coluna de **tipo de mapa** para editar a transformação.
7.  Em **Tipo de transformação**, selecione **ValueMap**.
8.  Selecione **Adicionar mapeamento de valores** e, em seguida, adicione as seguintes **Chaves** e **Valores**:

   Key       | valor 
   ----------|-------
   InProcess | 0     
   concluída | 5     

![Captura de ecrã a mostrar o Mapeamento de escrita dupla](media/projectstage-dw-mapping.png)

9. Selecione **Guardar**.
10. Na parte superior da página **Escrita dupla > Projects V2 (msdyn_projects)**, selecione **Guardar Como**.
11. Em **Adicionar tabela**, no campo **Editor**, selecione **Editor Predefinido CDS**.
12. Defina o campo **Versão** como 1.0.0.3.
13. Escreva uma **Descrição** e, em seguida, selecione **Guardar**.
14. Na parte superior da página **Escrita dupla > Projects V2 (msdyn_projects)**, selecione **Executar** para iniciar o mapa e, em seguida, selecione **Sim** se lhe for pedido para confirmar antes da execução. 

### <a name="close-a-newly-completed-project"></a>Fechar um projeto recém-concluído

O Dynamics 365 Finance utiliza o campo de **fase do projeto** para diferenciar os projetos **em processo** ou **concluídos**. Os projetos **concluídos** não podem incorrer em despesas nem podem ser faturados aos clientes.

1. Abra um projeto para desativar.
2. No friso, selecione **Desativar**.

> [!NOTE]
> Pode desativar ou fechar um projeto, pois ambos se comportam da mesma forma no contexto de Finanças.

3. Em Finanças, abra a página **Lista de todos os projetos**.
4. Confirme que o projeto desativado não aparece na lista.
5. No filtro **mostrar projetos** acima da lista, altere o valor de **Ativo** para **Todos**.
6. Verá agora o projeto desativado.

Se tentar registar tempo ou despesas com este projeto em Finanças, não deverá ver o projeto para seleção. Se introduzir manualmente o número do projeto numa despesa, verá uma mensagem como "A fase do projeto concluída não permite a gravação no projeto". A faturação e outras funções de faturação deverão estar desativadas, uma vez que estarão no contexto de um projeto fechado.

