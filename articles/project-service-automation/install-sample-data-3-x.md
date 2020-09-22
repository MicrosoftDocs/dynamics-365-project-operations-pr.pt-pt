---
title: Instalação de dados de exemplo
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.reviewer: kfend
ms.suite: ''
ms.technology: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.assetid: 8580fc8b-868a-42a3-aa04-2afab28d6de4
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: 1c1300116fe42091620267fb128ca6c63184970e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754461"
---
# <a name="sample-data-installation-for-the-project-service-application"></a>Instalação de dados de exemplo para a aplicação Project Service

Para ajudar a criar os seus próprios ambientes de demonstração, a Microsoft fornece pacotes de dados de exemplo transferíveis para demonstrar as capacidades das suas aplicações. Existem dois tipos de pacotes de dados de exemplo:
- dados de referência/configuração
- dados de demonstração (dados de referência/configuração e transacionais, tais como ordens de intervenção e projetos)

Os pacotes de dados de exemplo **referência** podem ser transferidos em três pacotes diferentes, para que possa instalar dados apenas no Project Service ou apenas no Field Service, ou para que possa instalar dados de exemplo nas duas aplicações em simultâneo.

Os pacotes de dados de exemplo configuração/referência são:

- [**V902PSMasterData** - Project Service versão 3.x apenas](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [**V902FSMasterData** - Field Service versão 8.x apenas](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [**V902FPSMasterData** - Field Service 8.x e Project Service 3.x](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

O último pacote de dados de **demonstração** é:

 - [**FPSDemoData** - Field Service 8.x e Project Service 3.x](https://aka.ms/fpsdemodatapackage)

   As instruções de instalação diferem ligeiramente nos utilizadores para criar e configurar uma secção, mas o resto é igual como na anterior [**publicação do blogue**](https://aka.ms/fpsdemodatablog). Este pacote apresenta um conjunto de dados de demonstração reduzido e demora aproximadamente 3 horas para instalar.

Estes pacotes de dados de exemplo só estão disponíveis em inglês.

> [!IMPORTANT]
> **Não é possível desinstalar os dados de exemplo.** Só deve instalar estes pacotes nos sistemas de demonstração, avaliação, formação ou teste. Note também que instalar um pacote individual e, em seguida, instalar o outro pacote individual, não é suportado. (Ou seja, não é possível instalar **FSMasterData** e, em seguida, **PSMasterData**, ou vice versa.) Se necessitar de dados de exemplo para as duas aplicações mais tarde, deverá instalar o pacote **v902FPSMasterData**.

Quando instala qualquer um dos pacotes de dados de exemplo, o processo de instalação efetua as seguintes acções:

- Cria ou define parâmetros predefinidos para utilizar o Project Service, Field Service ou ambas as aplicações (se aplicável).

- Importa dados de exemplo para as aplicações, tais como recursos reserváveis, direitos específicos da aplicação, listas de vendas e preços de custo, unidades organizacionais, registos do processo de vendas e outras entidades para demonstrar as principais capacidades.  

Com o pacote **dados de demonstração**, obtém os dados de transações acima e adicionais, tais como ordens de intervenção e projetos.

Não sabe que capacidades pode demonstrar com os dados de exemplo? Veja o cenário fictício da Fabrikam Robotics nas [Notas técnicas](#technical-notes).

Se tiver dúvidas sobre a instalação destes pacotes de dados de exemplo, [envie-nos um e-mail para fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).

## <a name="requirements"></a>Requisitos

O protocolo de instalação assume o seguinte sobre a instância alvo (org):

- O idioma base é inglês e a moeda base é dólares norte-americanos (USD, $).

- A organização ainda não tem dados do Project Service ou Field Service ou apenas tem dados predefinidos de barebones que são fornecidos com qualquer organização nova.

- A versão correta da aplicação de negócio já está instalada:
       
    - **Para FPSDemoData ou v902FPSMasterData:** a organização tem o Field Service versão 8.x e Project Service versão 3.x instalados.

    - **Para v902PSMasterData:** a organização tem o Project Service versão 3.x instalado.

    - **Para v902FSMasterData:** a organização tem o Field Service versão 8.x instalado.

> [!NOTE]
> Se necessitar de instalar os dados de exemplo sobre uma versão de avaliação ou ambiente de demonstração existente do Project Service e Field Service que já contém dados (não recomendado), terá de suspender as pré-verificações de segurança efetuadas pelo programa de instalação. Para mais informações, consulte as notas técnicas abaixo.

## <a name="prepare-for-installation"></a>Preparar a instalação

Tem de executar o programa de instalação num computador com uma versão recente do Windows (Windows 10 preferencialmente).

Deverá planear que o computador permaneça com ligação a uma rede e que a instalação fique a executar até **1 hora** para **dados de configuração/referência**. (Normalmente a instalação demora cerca de 30 minutos para **FPSMasterData**, que inclui dados de exemplo para ambas as aplicações.) Para **FPSDemoData**, a instalação demorará cerca de **3 horas**.

O computador deverá ter a função de proteção de ecrã desativada. Caso contrário, as credenciais de sessão para a instalação podem ser perdidas quando a proteção de ecrã é acionada (a menos que mantenha a sua sessão sempre ativa).

> [!div class="mx-imgBorder"]
> ![Captura de ecrã das definições da proteção de ecrã, com a proteção de ecrã desativada](media/sample-data-1.png)

## <a name="download-and-unpack"></a>Transferir e descompactar

O programa de instalação de dados de exemplo do Project Service e Field Service é distribuído como executável de extração automática. Os nomes de ficheiro podem variar consoante o pacote de dados de exemplo, mas caso contrário, os passos são iguais seja qual for o pacote que instale.

Depois de transferir um pacote, execute o ficheiro .exe e, em seguida, aceite os termos e condições para descompactar o ficheiro comprimido zip. Depois tem de extrair o conteúdo desse ficheiro para uma pasta no computador.

Consoante as definições de segurança e do sistema operativo, poderá ter de realizar os seguintes passos após a descompactação do ficheiro zip:

1. Localize e clique com o botão direito do rato no ficheiro **FPSDemoData.dll** na pasta **v902FPSMasterData** / **PackageDeployer_FPSDemoData**.

2. Escolha **Desbloquear**.

3. Selecione **Aplicar**.

4. Selecione **OK**.


## <a name="create-or-configure-users"></a>Criar ou configurar os utilizadores

O pacote **FPSDemoData** requer seis utilizadores, enquanto que os pacotes **FPSMasterData** requerem um utilizador. Consulte o mais adequado para o seu pacote de dados de exemplo.

## <a name="create-or-configure-users---setupreference-data-packages"></a>Criar ou configurar utilizadores - pacotes de dados de configuração/referência

O pacote **FPSMasterData** foi concebido para instalar com um utilizador denominado Spencer Low com as definições descritas aqui. Para instalar o pacote corretamente, é necessário criar (ou mudar o nome temporariamente dos) utilizadores no seu ambiente para que correspondam à configuração de dados de exemplo de entrada.

Para criar ou configurar os utilizadores, vá a **Definições** > **Segurança** > **Utilizadores** e efetue o seguinte:

1. Defina UserFullname="Spencer Low" com o nome de utilizador "spencerl" (**letra minúscula**) para as funções de Gestor de projeto e Gestor de práticas.

2. Selecione o utilizador **Spencer Low** e, em seguida, selecione **Gerir Funções**. Localize e selecione a função **Administrador de sistema** e, em seguida, selecione **Ok** para conceder direitos de administração completos a Spencer Low. Este passo é necessário para assegurar que os registos de exemplo são criados com a propriedade do utilizador correta e, assim, povoar vistas corretamente.

3. Do pacote transferido, é necessário atualizar um ficheiro de mapeamento de dados com endereços de e-mail do contexto de utilizador predefinido. Para tal, abra **PkgFolder** e, em seguida, localize e abra o ficheiro **ImportUserMapFile.xml** no Bloco de Notas (ou Visual Studio ou outro editor de XML). Defina o campo **DefaultUserToMapTo=** com o endereço de e-mail do utilizador Spencer Low.

4. Se não utilizar Spencer Low com o nome de utilizador **spencerl**, necessita de atualizar um ficheiro adicional. Abra o ficheiro **DemoDataPreImportConfig.xml** e, em seguida, localize a etiqueta **userstocreateandconfigure**. Atualize a etiqueta **\<início de sessão\>** com o nome de utilizador do utilizdor Spencer Low. Para mais informações, consulte as [Notas técnicas](#technical-notes).

## <a name="create-or-configure-users---demo-data-package"></a>Criar ou configurar utilizadores - pacote de dados de demonstração

O pacote de dados de demonstração requer seis utilizadores. Para que o pacote seja instalado corretamente, efectue o seguinte:

 1. Crie ou mude o nome temporariamente dos utilizadores existentes para corresponder à configuração dos dados de exemplo recebidos, acedendo a **Definições** > **Segurança** > **Utilizadores**.
 
    Estes direitos só são necessários para demonstrações baseadas nas pessoas.  
    - Utilizador Fullname="David So" como Técnico de Field Service   
    - Utilizador Fullname = "Jaime Reding" como Expedidor de Customer Service & Field Service   
    - Utilizador Fullname = "Molly Clark" como Gestor de Contas   
    - Utilizador Fullname = "Spencer Low" como Gestor de Práticas e de Projeto  
    - Utilizador Fullname = "Veronica Quek" como Membro da Equipa   
    - Utilizador Fullname = "William Contoso"
  
2. Para fins de importação de dados de demonstração, atribua os seis utilizadores acima da função de Administrador para que os registos de exemplo sejam importados corretamente. 

3. Abra **PkgFolder** e, em seguida, localize e abra **ImportUserMapFile.xml**. Atualize os campos **Novos=** para os endereços de e-mail dos utilizadores correspondentes do seu sistema.

   > [!div class="mx-imgBorder"]
   > ![Captura de ecrã do UserMapFile](media/sample-data-7.png)

4. Se o utilizador de nome completo "Spencer Low" tiver um ID de utilizador diferente de **"spencerl"**, então, necessita de atualizar um ficheiro adicional. Abra **DemoDataPreImportConfig.xml** e localize a etiqueta **userstocreateandconfigure**. Atualize a etiqueta **\<início de sessão\>** com o loginId (sensível a maiúsculas e minúsculas). 

5. O calendário do primeiro utilizador (na etiqueta **userstocreateandconfigure**) é utilizado para povoar as horas de trabalho para todos os recursos reserváveis na importação de dados de demonstração. Navegue para **Definições** > **Segurança** > **Utilizadores**, localize o utilizador "Spencer Low" e abra a opção "Horas de trabalho". Edite as horas de trabalho existentes, selecionando a opção **Agenda semanal periódica completa do início ao fim**. Verifique se as **Horas de trabalho estão definidas das 8:00 às 17:00 (9 horas), de segunda a sexta-feira e com o fuso horário definido como Hora do Pacífico (E.U.A. e Canadá)**. Isto é necessário para assegurar que o quadro da Agenda e do Projeto mostram conforme esperado.

**Recomendação:** considere a criação de uma cópia de segurança da sua organização agora, no caso de necessitar de reverter para o ponto de partida se algo correr mal durante a instalação de dados de exemplo. Para mais informações, consulte [Fazer cópias de segurança e restaurar instâncias](https://docs.microsoft.com/dynamics365/customer-engagement/admin/backup-restore-instances).

## <a name="run-the-package-deployer"></a>Executar o Package Deployer

1. Localize e execute **PackageDeployer.exe** na pasta **v902FPSMasterData** OU **PackageDeployer_FPSDemoData**.

2. Aceite os termos e condições.

3. Na janela seguinte:

   a. Selecione o tipo de implementação **Office 365**.

   b. Utilize o utilizador e palavra-passe do utilizador de administrador de sistema configurado em "Criar ou configurar utilizadores" ("Spencer Low" com o nome de utilizador "spencerl").

   c. Certifique-se de que **Apresentar lista de organizações disponíveis** está selecionado.

      > [!div class="mx-imgBorder"]
      > ![Captura de ecrã da janela do Package Deployer com "Apresentar lista de organizações disponíveis" selecionado](media/sample-data-2.png)

4. Selecione a organização onde pretende instalar os dados de exemplo.

5. Selecione **Seguinte** até ver a caixa de diálogo **Configuração de dados de demonstração**.

   > [!div class="mx-imgBorder"]
   > ![Captura de ecrã da janela do estado do programa de instalação de dados de demonstração](media/sample-data-3.png)

6. Antes de continuar, tenha em atenção que a instalação de dados de exemplo poderá demorar até uma hora (normalmente cerca de 10 minutos). Terá de certificar-se de que o computador permanece ligado a uma rede ao longo do processo de instalação e a sessão permanece ativa.   

7. Quando estiver pronto, clique em **Seguinte** para iniciar o processo de instalação de dados de exemplo. Depois de carregar os dados de exemplo, clique em **Concluir**.

## <a name="verify-the-sample-data-installation"></a>Verificar a instalação dos dados de exemplo

Para uma verificação completa, verifique se o número de registos e tipos de entidades listados no cenário fictício Fabrikam Robotics aparecem conforme esperado.

Depois de carregar os dados de exemplo totalmente, inicie sessão como utilizador Spencer Low e confirme:

- Se a aplicação Project Service está instalada, vá a **Project Service** > **Definições** > **Listas de preços**. Confirme se as taxas de faturação e taxas de custos existem com a moeda adequada para cada país/região no conjunto de dados.

- Se a aplicação Project Service está instalada, vá para **Universal Resource Scheduling** > **Definições** > **Unidades Organizacionais**. Confirme se uma lista de preços de custos com a moeda apropriada foi associada a cada unidade organizacional (excluindo entradas de localidade). Se faltar algum, localize e associe a lista de preços de custos correta.

- Se a aplicação Field Service está instalada, vá a **Project Service** > **Definições** > **Listas de preços**. Confirme se existem taxas de custos e taxas de faturação. Aceda a **Field Service** > **Definições** > **Listas de preços** e verifique se existem taxas de faturação e taxas de custos, com a moeda adequada, para cada país/região no conjunto de dados.

  > [!div class="mx-imgBorder"]
  > ![Captura de ecrã de listas de preços ativas](media/sample-data-4.png)

  > [!div class="mx-imgBorder"]
  > ![Captura de ecrã de unidades organizacionais ativas](media/sample-data-5.png)

## <a name="technical-notes"></a>Notas técnicas

Consulte abaixo para obter mais detalhes técnicos sobre a instalação destes dados.

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a>Instalar dados de exemplo sobre os dados existentes (não recomendado)

Se necessitar de instalar dados de exemplo sobre uma versão de avaliação ou ambiente de demonstração existente do Field Service ou Project Service que já contém dados, terá de suspender as pré-verificações de segurança efetuadas pelo programa de instalação.

Para tal, vá à pasta **PkgFolder** para localizar e abrir o ficheiro **DemoDataPreImportConfig.xml** com o Bloco de Notas (ou outro editor de XML).

Localize o valor seguinte e, em seguida, altere a definição de verdadeiro para falso:

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

Esta alteração faz com que o programa de instalação ignore algumas verificações importantes de segurança, incluindo:

- Confirmar de que não existe mais do que um registo ativo **Unidade organizacional** e, em seguida, mudar o nome para **Fabrikam US**.

- Confirmar de que não existe mais do que um registo ativo **Modelo de trabalho**.

- Confirmar de que não existe mais do que um registo ativo **Parâmetro do Projeto** e, em seguida, mudar o nome dessa entrada para **Parâmetros**.

### <a name="configuration-components"></a>Componentes de configuração

Existem outros componentes de configuração neste ficheiro de configuração de pré-importação. Para utilizadores técnicos, alguns incluem:

- **\<RequiredSolutions\>** especifica as instalações de soluções pré-requisito e os números de versão.

- **\<InstallSampleData\>** controla se os dados de exemplo fornecidos com o programa para as aplicações estão instalados.

    - falso - ignora a instalação destes dados incorporadas (que são removidos)

    - verdadeiro - instala os dados incorporados em simultâneo com a instalação dos dados de exemplo FS e PSA

- **\<PreImportDataCollection\>** especifica os Mapas de Dados de ficheiro simples e registos associados para serem importados antes da instalação de dados de exemplo principal.

- **\<EntitiesToEnableScheduling\>** especifica as entidades que devem ser ativadas para Reserva no Agendamento do Microsoft Dynamics (também conhecido como Universal Resource Scheduling).

- **\<UsersToCreateAndConfigure\>** especifica os Recursos reserváveis que serão criados (se não existirem já) antes da importação de dados de exemplo ser executada. Note que os Recursos reserváveis dos dados de exemplo do sistema de origem correspondem aos registos de Recursos reserváveis do sistema de destino no FullName e início de sessão de cada recurso. Por conseguinte, NÃO é possível alterar os nomes existentes neste ficheiro de pré-configuração, a menos que importe primeiro dados de exemplo para um sistema de destino utilizando estes nomes, depois mudar o nome dos Recursos reserváveis para o nome pretendido de acordo com os registos de utilizador ativados e, em seguida, exportar os dados novamente para importar para o sistema de destino final (atualizar as entradas Antigas e Novas de **ImportUserMapFile.xml** em conformidade).

- **\<PluginsToDisable\>** especifica plug-ins itens muito discretos que devem ser desativados durante a importação de dados de exemplo e, em seguida, reativados posteriormente.

### <a name="fabrikam-robotics-fictitious-scenario"></a>Cenário fictício Fabrikam Robotics

Os pacotes de dados de referência de exemplo de Field Service e Project Service instalam a solução **Fabrikam Manufacturing Master Data (v3.0.0.0)**, juntamente com aproximadamente 4000 registos e aproximadamente 40 entidades diferentes. Os pacotes de dados de exemplo separados para Field Service ou Project Service contêm um subconjunto dos dados de exemplo **v902FPSMasterData** para essa aplicação. O pacote **Dados de demonstração** instala a **solução de dados de demonstração da Fabrikam Manufacturing (v3.0.0.7)** com aproximadamente 22.000 registos de 148 entidades.

A empresa fictícia, Fabrikam Robotics, é um fabricante de robôs de linha de montagem de dispositivos electrónicos e é conhecido pela qualidade de produtos, inovação e sólido suporte ao cliente, incluindo planeamento de instalação, implementação e serviços de manutenção contínuos. A Fabrikam tem sede nos Estados Unidos (Fabrikam US) e operações de serviços com base em projetos em França, Índia, Reino Unido e Suíça.

As operações de serviço no terreno estão centralizadas nos Estados Unidos, sobretudo, na zona de Seattle. A empresa concentra-se na utilização da conectividade da Internet das coisas (IoT) para monitorizar o desempenho ativo do cliente e fornecer serviços mais proativos no local.

Uma descrição geral de alto nível dos dados de exemplo é:

- Elementos de dados de exemplo comuns (incluídos para ambas as aplicações)

    - 1 utilizador

    - 71 contas

    - 137 contactos

    - Vários tipos e categorias de transação

    - 50 produtos com a lista de preços de 1 produto

    - 14 listas de preço/custo

    - 31 características (competências de recurso) em 2 modelos de classificação com 3 níveis (valores de classificação)

- Project Service

    - 8 unidades organizacionais

    - 6 níveis de utilização específicas da função

    - 2.8 k + especificações de preços de função

- Field Service

    - 4 territórios

    - 5 tipos de ordem de intervenção

    - 22 ativos de cliente

    - 9 tipos de incidente com uma variedade de características de recursos associadas (9), serviços (13) e tarefas de serviço (13)
   
O pacote **Dados de demonstração** instala aproximadamente 179 ordens de intervenção, 12 projetos e dados das transações associados. 

### <a name="change-the-work-hours-for-sample-resources"></a>Alterar as horas de trabalho para recursos de exemplo

Por predefinição, todos os recursos reserváveis têm um calendário de 24 horas de trabalho.

Se precisar de alterar as horas de trabalho por recursos reserváveis de exemplo, vá para **Universal Resource Scheduling** > **Agendamento** > **Recursos**.

Selecione um utilizador (por exemplo, Spencer Low) e altere as horas de trabalho do Spencer para as horas de trabalho que pretende aplicar a vários utilizadores. Aceda a **Universal Resource Scheduling** > **Definições** > **Modelos de Horas de Trabalho** e edite o registo **Modelo de Trabalho Predefinido**. No campo **Recurso do Modelo**, selecione um utilizador com horas de trabalho que pretende aplicar para outros recursos. Aceda a **Universal Resource Scheduling** > **Agendamento** > **Recursos** > **Recursos Reserváveis Ativos**. Selecione os recursos que pretende alterar e, em seguida, selecione **Definir calendário**. Na lista pendente **Modelo de trabalho**, selecione o modelo **Horas de trabalho predefinidas** ou outro modelo com o recurso correcto de modelos. Quando vai ao quadro da agenda, deverá ver que os recursos agora atualizaram as horas de trabalho.

> [!div class="mx-imgBorder"]
> ![Captura de ecrã de recursos reserváveis ativos](media/sample-data-6.png)
