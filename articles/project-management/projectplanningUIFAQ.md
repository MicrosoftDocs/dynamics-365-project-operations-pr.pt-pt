---
title: Resolução de problemas a trabalhar na grelha de tarefas
description: Esta tópico fornece informações necessárias para a resolução de problemas quando trabalham na grelha de tarefas.
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: dedd989cc7c959d9ea97a0abfb13f8f1b2150a56
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286577"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Resolução de problemas a trabalhar na grelha de tarefas 

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Este tópico descreve como corrigir problemas que pode encontrar enquanto trabalha com a gestão de custos.

## <a name="enable-cookies"></a>Ativar cookies

O Project Operations requer que os cookies de terceiros sejam ativados de forma a compor a estrutura hierárquica do trabalho. Quando os cookies de terceiros não estiverem ativados, em vez de ver tarefas, verá uma página em branco quando selecionar o separador **Tarefas** na página **Projeto**.

![Separador em branco quando os cookies de terceiros não estão ativados](media/blankschedule.png)


### <a name="workaround"></a>Solução
Para Microsoft Edge ou para os navegadores Google Chrome, os seguintes procedimentos descrevem como atualizar a configuração do seu navegador para ativar cookies de terceiros.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Abra o browser Microsoft Edge.
2. No canto superior direito, selecione **elipse** (...) e, em seguida, **Definições**.
3. Sob **Cookies e permissões do site**, selecione **Cookies e dados do site**.
4. Desligue os **cookies de terceiros do bloco**.

#### <a name="google-chrome"></a>Google Chrome

1. Abra o browser Chrome.
2. No canto superior direito, selecione os três pontos verticais e, em seguida, selecione **Definições**.
3. Sob **Privacidade e segurança**, selecione **Cookies e outros dados do site**.
4. Selecione **Permitir todas as cookies**.

> [!IMPORTANT]
> Se bloquear cookies de terceiros, todos os cookies e dados do site de outros sites serão bloqueados, mesmo que o site seja permitido na sua lista de exceções.

## <a name="pex-endpoint"></a>Ponto final de PEX

O Project Operations requer que um parâmetro de projeto refira o ponto final PEX. Este ponto final é necessário para comunicar com o serviço utilizado para compor a estrutura hierárquica do trabalho. Se o parâmetro não estiver ativado, receberá o erro: "O parâmetro do projeto não é válido". 

### <a name="workaround"></a>Solução
 ![Campo PEX ponto final no parâmetro do projeto](media/projectparameter.png)

1. Adicione o campo **ponto final PEX** à página **Parâmetros do Projeto**.
2. Atualize o campo com o seguinte valor: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`
3. Retire o campo da página **Parâmetros do Projeto**.

## <a name="privileges-for-project-for-the-web"></a>Privilégios para Projeto para a Web

O Project Operations conta com um serviço de agendamento externo. O serviço requer que um utilizador tenha várias funções atribuídas para ler e escrever a entidades relacionadas com a estrutura hierárquica do trabalho. Estas entidades incluem tarefas de projeto, atribuições de recursos e dependências de tarefas. Se um utilizador não consegue tornar a estrutura hierárquica do trabalho quando vai para o separador **Tarefas**, é provavelmente porque o Project for Project Operations não foi ativado. Um utilizador pode receber um erro de direito de acesso ou um erro relacionado com uma negação de acesso.


## <a name="workaround"></a>Solução

1. Ir para **Definição > Segurança > Utilizadores > Utilizadores de Aplicações**.  

   ![Leitor de aplicação](media/applicationuser.jpg)
   
2. Clique duas vezes no registo do utilizador da aplicação para verificar o seguinte:

 - O utilizador tem acesso ao projeto. Esta verificação é normalmente feita garantindo que o utilizador tem direito de acesso ao **Gestor de projeto**.
 - O utilizador da aplicação Microsoft Project existe e está configurado corretamente.
 
3. Seeste utilizador não existir, pode criar um novo registo de utilizador. Selecionar **Novos utilizadores**. Altere o formulário de inscrição para **Utilizador de Aplicações** e adicione o **ID da aplicação**.

   ![Detalhes da candidatura do utilizador](media/applicationuserdetails.jpg)

4. Verifique se o utilizador foi atribuído a licença correta e se o serviço está ativado nos detalhes dos planos de serviço da licença.
5. Verifique se o utilizador pode abrir project.microsoft.com.
6. Verifique através dos parâmetros do projeto que o sistema está apontando para o projeto correto ponto final.
7. Verifique se a candidatura de projeto do utilizador foi criada
8. Aplicar as seguintes funções de segurança ao utilizador:

  - Utilizador do Dataverse
  - Sistema do Project Operations
  - Sistema do projeto

## <a name="error-when-updating-the-work-breakdown-structure"></a>Erro ao atualizar a estrutura hierárquica do trabalho

Quando uma ou mais atualizações são feitas para a estrutura hierárquica do trabalho, as alterações acabam por falhar e não são salvas. Ocorre um erro na grelha de agenda, notando que "Não foi possível salvar a mudança recente que fez."

### <a name="workaround"></a>Solução

1. Verifique se o utilizador foi atribuído a licença correta e se o serviço está ativado nos detalhes dos planos de serviço da licença.
2. Verifique se o utilizador pode abrir project.microsoft.com.
3. Verifique que o sistema está a apontar para o projeto correto ponto final.
4. Verifique se a Candidatura de projeto do utilizador tenha sido criada.
5. Aplicar as seguintes funções de segurança ao utilizador:
  
  - Utilizador ou Utilizador base Dataverse
  - Sistema do Project Operations
  - Sistema do projeto
  - Sistema de Escrita Dupla do Project Operations (Esta função é necessária se estiver a implementar o cenário baseado em recursos/não armazenados do Project Operations.)


[!INCLUDE[footer-include](../includes/footer-banner.md)]