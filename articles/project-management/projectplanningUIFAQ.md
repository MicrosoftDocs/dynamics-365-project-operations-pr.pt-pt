---
title: Resolução de problemas a trabalhar na grelha de tarefas
description: Este artigo fornece informações de resolução de problemas necessárias quando trabalha na grelha Tarefa.
author: ruhercul
ms.date: 04/05/2022
ms.topic: article
ms.product: ''
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: e6ab4f34fe3f6732f7bef252f298671e07a3c3ca
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911058"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Resolução de problemas a trabalhar na grelha de tarefas 


_**Aplicável a:** Project Operations para cenários baseados em recursos/itens não existentes em stock, implementação Lite - da transação à fatura pró-forma, Project for the Web_

A grelha de Tarefas utilizada pelo Dynamics 365 Project Operations é um iframe alojado no Microsoft Dataverse. Como resultado desta utilização, é necessário cumprir requisitos específicos para garantir o funcionamento correto da autenticação e autorização. Este artigo descreve os problemas comuns que podem afetar a capacidade de compor a grelha ou gerir tarefas na estrutura hierárquica do trabalho (WBS).

Os problemas comuns incluem:

- O separador **Tarefa** na grelha de Tarefas está vazio.
- O projeto não é carregado quando é aberto e a interface de utilizador (IU) fica bloqueada no ícone de progresso.
- Administração de privilégios do **Project for the Web**.
- As alterações não são guardadas quando cria, atualiza ou elimina uma tarefa.

## <a name="issue-the-task-tab-is-empty"></a>Problema: O separador Tarefa está vazio

### <a name="mitigation-1-enable-cookies"></a>Mitigação 1: Ativar cookies

O Project Operations exige que os cookies de terceiros sejam ativados para compor a estrutura hierárquica do trabalho. Quando os cookies de terceiros não estiverem ativados, em vez de ver tarefas, verá uma página em branco quando selecionar o separador **Tarefas** na página **Projeto**.

Para Microsoft Edge ou para os navegadores Google Chrome, os seguintes procedimentos descrevem como atualizar a configuração do seu navegador para ativar cookies de terceiros.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Abra o browser Microsoft Edge.
2. No canto superior direito, selecione **elipse** (...) e, em seguida, **Definições**.
3. Sob **Cookies e permissões do site**, selecione **Cookies e dados do site**.
4. Desligue os **cookies de terceiros do bloco**.
5. Atualize o seu browser. 

#### <a name="google-chrome"></a>Google Chrome

1. Abra o browser Chrome.
2. No canto superior direito, selecione os três pontos verticais e, em seguida, selecione **Definições**.
3. Sob **Privacidade e segurança**, selecione **Cookies e outros dados do site**.
4. Selecione **Permitir todas as cookies**.
5. Atualize o seu browser. 

> [!NOTE]
> Se bloquear cookies de terceiros, todos os cookies e dados do site de outros sites serão bloqueados, mesmo que o site seja permitido na sua lista de exceções.

### <a name="mitigation-2-validate-the-pex-endpoint-has-been-correctly-configured"></a>Mitigação 2: Validar se o Ponto Final PEX foi configurado corretamente

O Project Operations requer que um parâmetro de projeto refira o ponto final PEX. Este ponto final é necessário para a comunicação com o serviço utilizado para compor a estrutura hierárquica do trabalho. Se o parâmetro não estiver ativado, receberá o erro: "O parâmetro do projeto não é válido". Para atualizar o Ponto Final PEX, conclua os passos a seguir.

1. Adicione o campo **ponto final PEX** à página **Parâmetros do Projeto**.
2. Identifique o tipo de produto que está a utilizar. Este valor é utilizado quando o ponto final PEX está definido. Após a recuperação, o tipo de produto já está definido no ponto final PEX. Mantenha este valor.
3. Atualize o campo com o seguinte valor: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=<id>&type=2`. A tabela a seguir fornece o parâmetro do tipo que deve ser utilizado com base no tipo de produto.

      | **Tipo de produto**                     | **Parâmetro do tipo** |
      |--------------------------------------|--------------------|
      | Project for the Web na Organização predefinida   | tipo=0             |
      | Project for the Web na organização com o nome CDS | tipo=1             |
      | Project Operations                   | tipo=2             |

4. Retire o campo da página **Parâmetros do Projeto**.

### <a name="mitigation-3-sign-in-to-projectmicrosoftcom"></a>Mitigação 3: iniciar sessão em project.microsoft.com
No browser Microsoft Edge, abra um novo separador, aceda project.microsoft.com, inicie sessão utilizando a função de utilizador que está a utilizar para aceder ao Project Operations.

## <a name="issue-the-project-doesnt-load-and-the-ui-is-stuck-on-the-spinner"></a>Problema: O projeto não é carregado e a IU está bloqueada no ícone de progresso

Para efeitos de autenticação, os pop-ups devem ser ativados para que a grelha de Tarefas seja carregada. Se os pop-ups não forem ativados, o ecrã fica bloqueado no ícone de progresso do carregamento. O gráfico a seguir mostra o URL com uma etiqueta pop-up bloqueada na barra de endereço, o que faz com que o ícone de progresso fique bloqueado ao tentar carregar a página. 

   ![Ícone de progresso bloqueado e bloqueio de pop-ups.](media/popupsblocked.png)

### <a name="mitigation-1-enable-pop-ups"></a>Mitigação 1: Ativar os pop-ups

Quando o seu projeto estiver bloqueado no ícone de progresso, é possível que os pop-ups não estejam ativados.

#### <a name="microsoft-edge"></a>Microsoft Edge

Existem duas formas de ativar pop-ups no browser Edge.

1. No browser Edge, selecione a notificação no canto superior direito do browser.
2. Selecione **Permitir sempre popups e redirecionamentos a partir** do ambiente Dataverse específico.
 
     ![Janela de pop-ups bloqueados.](media/enablepopups.png)

Em alternativa, pode concluir os passos a seguir.

1. Abra o browser Microsoft Edge.
2. No canto superior direito, selecione as **reticências** (...) e, em seguida, selecione **Definições** > **Permissões do site** > **Pop-ups e redirecionamentos**.
3. Desative a opção **Pop-ups e redirecionamentos** para bloquear os pop-ups ou ative-a para permitir pop-ups no dispositivo.
4. Depois de ativar os pop-ups, atualize o browser. 

#### <a name="google-chrome"></a>Google Chrome
1. Abra o browser Chrome.
2. Navegue para uma página onde os pop-ups estão bloqueados.
3. Na barra de endereço, selecione **Pop-up bloqueado**.
4. Selecione a ligação para o pop-up que pretende ver.
5. Depois de ativar os pop-ups, atualize o browser. 

> [!NOTE]
> Para ver sempre pop-ups para o site, selecione **Permitir sempre pop-ups e redirecionamentos de [site]** e, em seguida, selecione **Concluído**.

## <a name="issue-3-administration-of-privileges-for-project-for-the-web"></a>Problema 3: Administração de privilégios do Project for the Web

O Project Operations conta com um serviço de agendamento externo. O serviço exige que um utilizador tenha várias funções atribuídas que lhe permita ler e escrever em entidades relacionadas com o WBS. Estas entidades incluem tarefas de projeto, atribuições de recursos e dependências de tarefas. Se um utilizador não conseguir compor o WBS quando navega para o separador **Tarefas**, provavelmente o **Projeto** do **Project Operations** não foi ativado. Um utilizador pode receber um erro de direito de acesso ou um erro relacionado com uma negação de acesso.

### <a name="mitigation-1-validate-the-application-user-and-end-user-security-roles"></a>Mitigação 1: Validar os direitos de acesso do utilizador da aplicação e do utilizador final

1. Aceda a **Definição** > **Segurança** > **Utilizadores** > **Utilizadores de Aplicações**.  

   ![Leitor de aplicação.](media/applicationuser.jpg)
   
2. Faça duplo clique no registo do utilizador da aplicação para verificar:

     - O utilizador tem acesso ao projeto. Para fazê-lo, verifique se o utilizador tem o direito de acesso de **Gestor de Projeto**.
     - O utilizador da aplicação Microsoft Project existe e está configurado corretamente.
 
3. Se este utilizador não existir, crie um novo registo de utilizador. 
4. Selecione **Novos Utilizadores**, altere o formulário de entrada de dados para **Utilizador da Aplicação** e, em seguida, adicione o **ID da Aplicação**.

   ![Detalhes da candidatura do utilizador.](media/applicationuserdetails.jpg)


## <a name="issue-4-changes-arent-saved-when-you-create-update-or-delete-a-task"></a>Problema 4: As alterações não são guardadas quando cria, atualiza ou elimina uma tarefa

Quando faz uma ou mais atualizações ao WBS, ocorreu uma falha nas alterações e estas não são guardadas. Ocorre um erro na grelha da agenda com a mensagem "Não foi possível guardar a alterações que fez recentemente".

### <a name="mitigation-1-validate-the-license-assignment"></a>Mitigação 1: Validar a atribuição da licença

1. Verifique se o utilizador foi atribuído a licença correta e se o serviço está ativado nos detalhes dos planos de serviço da licença.  
2. Verifique se o utilizador consegue abrir **project.microsoft.com**.
    
### <a name="mitigation-2-validation-configuration-of-the-project-application-user"></a>Mitigação 2: Configuração de validação do utilizador da aplicação Project
1. Verifique se o utilizador da aplicação Project foi criado.
2. Aplicar as seguintes funções de segurança ao utilizador:
  
  - Utilizador do Dataverse ou Servidor Base
  - Sistema do Project Operations
  - Sistema do projeto
  - Sistema de Escrita Dupla do Project Operations. Esta função é necessária para o cenário de implementação baseado em recursos/itens não existentes em stock do Project Operations.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
