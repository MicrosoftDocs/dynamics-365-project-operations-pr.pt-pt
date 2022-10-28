---
title: Atualizar a versão do Project Service Automation para Project Operations
description: Este artigo fornece uma descrição geral do processo para atualizar a versão do Microsoft Dynamics 365 Project Service Automation para o Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/11/2022
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
ms.openlocfilehash: 2d7b372cac391fab7a81ac6ac5d2ea6d12977b5c
ms.sourcegitcommit: 9de444ae0460c8d15c77d225d0c0ad7f8445d5fc
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/18/2022
ms.locfileid: "9686990"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Atualizar a versão do Project Service Automation para Project Operations

Estamos entusiasmados por anunciar a segunda de três fases para a atualizar a versão do Microsoft Dynamics 365 Project Service Automation para o Microsoft Dynamics 365 Project Operations. Este artigo fornece uma descrição geral para os clientes que estão a embarcar nesta viagem emocionante. 

O programa de entrega da atualização de versão será dividido em três fases.

| Entrega da atualização de versão | Fase 1 (janeiro de 2022) | Fase 2 (novembro de 2022) | Fase 3 (Vaga de abril de 2023)  |
|------------------|------------------------|---------------------------|---------------------------|
| Não há dependência na estrutura hierárquica do trabalho (WBS) para projetos | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Um WBS dentro dos limites atualmente suportados do Project Operations | | :heavy_check_mark: | :heavy_check_mark: |
| Um WBS fora dos limites atualmente suportados do Project Operations, incluindo o suporte para o Project Desktop Client | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Atualizar a versão das funcionalidades do processo 

Como parte do processo de atualização de versão, adicionámos registos de atualização de versão ao mapa do site para permitir que os administradores diagnostiquem falhas mais facilmente. Além da nova interface, serão adicionadas novas regras de validação para garantir a integridade dos dados após uma atualização de versão. As validações que se seguem serão adicionadas ao processo de atualização de versão.

| Validações | Fase 1 (janeiro de 2022) | Fase 2 (novembro de 2022) | Fase 3  |
|-------------|------------------------|---------------------------|---------------------------|
| O WBS será validado contra violações comuns de integridade dos dados (por exemplo, atribuições de recursos que estão associadas à mesma tarefa principal, mas que têm diferentes projetos principais). | | :heavy_check_mark: | :heavy_check_mark: |
| O WBS será validado contra os [limites conhecidos do Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| O WBS será validado contra os limites conhecidos do Project Desktop Client. | |  | :heavy_check_mark: |
| Os recursos reserváveis e os calendários de projetos serão avaliados contra exceções de regras de calendário incompatíveis comuns. | | :heavy_check_mark: | :heavy_check_mark: |

Na fase 2, os clientes que atualizaram a versão para o Project Operations terão os seus projetos existentes atualizados para uma experiência só de leitura para planeamento de projetos. Nesta experiência só de leitura, o WBS completo será visível na grelha de monitorização. Para editar o WBS, os gestores de projetos podem selecionar [**Converter**](/PSA-Upgrade-Project-Conversion.md) na página principal do projeto. Um processo de fundo atualiza o projeto para que suporte a nova experiência de agendamento de projetos do Project for the Web. Esta fase é adequada para clientes que tenham projetos que se enquadram dentro dos [limites conhecidos do Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries).

Na fase 3, será adicionado suporte para o Project Desktop Client, em benefício dos clientes que pretendam continuar a editar os seus projetos a partir dessa aplicação. No entanto, se os projetos existentes forem convertidos para a nova experiência do Project for the Web, o acesso ao suplemente será desativado para cada projeto convertido.

## <a name="prerequisites"></a>Pré-requisitos

Para ser elegível para a atualização da versão da Fase 1, tem de cumprir os seguintes critérios:

- O ambiente de destino não pode conter quaisquer registos na entidade **msdyn_projecttask**.
- Têm de ser atribuídas licenças válidas do Project Operations a todos os utilizadores ativos. 
- Tem de validar o processo de atualização de versão em, pelo menos, um ambiente de não produção que contenha um conjunto de dados representativo que esteja alinhado com o seu ambiente de produção.
- O ambiente de destino tem de ser atualizado para a Atualização do Project Service Automation, Versão 37 (V3.10.58.120) ou posterior.

Para ser elegível para a atualização da versão da Fase 2, tem de cumprir os seguintes critérios:

- Têm de ser atribuídas licenças válidas do Project Operations a todos os utilizadores ativos. 
- Tem de validar o processo de atualização de versão em, pelo menos, um ambiente de não produção que contenha um conjunto de dados representativo que esteja alinhado com o seu ambiente de produção.
- O ambiente de destino tem de ser atualizado para a Atualização do Project Service Automation, Versão 37 (V3.10.58.120) ou posterior.
- Os ambientes que contenham tarefas (msdyn_projecttask) só são suportados se o número total de tarefas por projeto for 500 ou menos.

Os pré-requisitos para a Fase 3 serão atualizados à medida que a data de disponibilidade geral se aproxima.

## <a name="licensing"></a>Licenciamento

Se tiver licenças ativas para o Project Service Automation, pode instalar e utilizar o Project Operations, que inclui todas as capacidades do Project Service Automation e muito mais. Pode então testar as capacidades do Project Operations num ambiente separado enquanto continua a utilizar o Project Service Automation em produção. Após a expiração das licenças do Project Service Automation, terá de mudar para o Project Operations. Ao planear esta transição, tem de ter em conta o facto de que a licença do Project Operations não inclui uma licença do Project Service Automation.

## <a name="testing-and-refactoring-customizations"></a>Testar e refatorizar personalizações

Como ponto de partida, importa todas as personalizações para um ambiente limpo do Project Operations (Lite) para confirmar que a importação foi bem sucedida e que as operações comerciais se comportam como esperado.

Eis algumas coisas a ter em conta:

- A importação pode falhar por causa de dependências em falta. Por outras palavras, os campos de referência de personalizações ou outros componentes que foram removidos no Project Operations. Neste caso, remova estas dependências do ambiente de desenvolvimento.
- Se as suas soluções não geridas e geridas incluírem componentes que não são personalizados, remova esses componentes da solução. Por exemplo, quando personalizar a entidade **Projeto**, adicione apenas o cabeçalho de entidade à sua solução. Não adicione todos os campos. Se já adicionou todos os subcomponentes, poderá ter de criar manualmente uma nova solução e adicionar-lhe componentes relevantes.
- Os formulários e as vistas podem não aparecer como esperado. Em algumas circunstâncias, se personalizou qualquer um dos formulários ou vistas de origem, as personalizações podem impedir que novas atualizações no Project Operations entrem em vigor. Para identificar estes problemas, recomendamos que faça uma revisão lado a lado de uma instalação limpa do Project Operations e uma instalação do Project Operations que inclua as suas personalizações. Compare os formulários mais utilizados no seu negócio para confirmar que a sua versão do formulário ainda faz sentido e que não está a perder nada da versão limpa do formulário. Faça o mesmo tipo de revisão lado a lado para quaisquer vistas que tenha personalizado.
- A lógica de negócio pode falhar em runtime. Como as referências aos campos nos seus plug-ins não são validadas no momento da importação, a lógica de negócio pode falhar devido a referências a campos que já não existem, e pode receber uma mensagem de erro que se assemelha ao seguinte exemplo: "A entidade "Projeto" não contém atributo com Name = 'msdyn_plannedhours' and NameMapping = 'Logical'." Neste caso, modifique as suas personalizações para que utilizem os novos campos. Se utilizar classes de proxy e referências de tipo forte geradas automaticamente na sua lógica de plug-in, considere regenerar esses proxies a partir de uma instalação limpa. Desta forma, pode identificar facilmente todos os locais onde os seus plug-ins dependem de campos preteridos.

Depois de atualizar as suas personalizações para importar de forma limpe o Project Operations, passe para os próximos passos.

## <a name="end-to-end-testing-in-development-environments"></a>Testes de ponto a ponto em ambientes de desenvolvimento

### <a name="initiate-upgrade"></a>Iniciar atualização 

1. No centro de administração do Power Platform, encontre e selecione o seu ambiente. Em seguida, nas aplicações, encontre e selecione **Dynamics 365 Project Operations**.
2. Selecione **Instalar** para iniciar a atualização. O centro de administração do Power Platform apresentará esta instalação como uma nova instalação. No entanto, será detetada a presença de uma versão anterior do Project Service Automation e a instalação existente será atualizada.

    Após a conclusão da atualização, o ambiente deve mostrar que o Project Operations estão instaladas e que o Project Service Automation não está instalado.

    Dependendo da quantidade de dados no ambiente, a atualização de versão pode demorar várias horas. A equipa principal que está a gerir a atualização da versão deve planear em conformidade e executar a atualização da versão durante o horário não comercial. Em alguns casos, se o volume de dados for grande, a atualização da versão deve ser executada durante o fim de semana. A decisão sobre o agendamento deve basear-se nos resultados dos testes em ambientes mais baixos.

3. Atualize as soluções personalizadas, conforme apropriado. Neste ponto, implemente quaisquer alterações que tenha feito às suas personalizações na secção [Testar e refatorizar personalizações](#testing-and-refactoring-customizations) deste artigo.
4. Vá a **Definições** \> **Soluções** e selecione para desinstalar a solução **Componentes Preteridos do Project Operations**.

    Esta solução é uma solução temporária que detém o modelo de dados e componentes existentes que estão presentes durante a atualização da versão. Ao remover esta solução, remova todos os campos e componentes que já não são utilizados. Desta forma, ajuda a simplificar a interface e a facilitar a integração e a extensão.
    
### <a name="upgrade-to-project-operations-lite"></a>Atualizar a versão para o Project Operations Lite

Os seguintes passos descrevem o processo de atualização de versão e registo de erros associado:

1. **Verificação da Versão da PSA:** para instalar o Project Operations, tem de ter a V3.10.58.120 ou posterior.
1. **Pré-validação:** quando um administrador iniciar uma atualização de versão, o sistema executa uma operação de pré-validação em cada entidade que é o núcleo da solução Project Operations. Este passo verifica se todas as referências de entidade são válidas e assegura que os dados relacionados com o WBS estão dentro dos limites publicados do Project for the Web.
1. **Atualização de versão dos metadados:** após a pré-validação com êxito, o sistema inicia alterações ao esquema e cria uma solução de componentes preterida. Pode remover esta solução preterida depois de ter concluído toda a refatorização necessária das personalizações. Este passo é a parte mais comprida do processo de atualização de versão e pode demorar até quatro horas a ser concluído.
1. **Atualização de versão dos dados:** depois de concluídas todas as alterações de esquema necessárias no passo de atualização de versão dos metadados, os dados são migrados para o novo esquema e quaisquer predefinições e recálculos necessários são efetuados.
1. **Atualização do motor da agenda do projeto:** após a atualização de versão com êxito dos dados, o separador **Agenda** na página principal é etiquetado como **Tarefas**. Quando um utilizador seleciona este separador depois da atualização de versão, é direcionado para navegar para a grelha de monitorização para uma vista só de leitura da WBS. Para editar a WBS, têm de iniciar o [processo de conversão](/PSA-Upgrade-Project-Conversion.md) da agenda. Todos os projetos sem uma WBS pré-existente podem utilizar a nova experiência de agendamento diretamente, sem conversão.
 
### <a name="validate-common-scenarios"></a>Validar cenários comuns

Quando valida as personalizações específicas, recomendamos que reveja também os processos de negócio suportados em todas as aplicações. Estes processos de negócio incluem, mas não se limitam à criação de entidades de vendas, tais como propostas e contratos, e a criação de projetos que incluem WBS e aprovação de valores reais.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Principais alterações entre o Project Service Automation e o Project Operations

Esta secção fornece um resumo das principais alterações que pode esperar entre o Project Service Automation e o Project Operations.

### <a name="project-planning"></a>Planeamento de projeto

As capacidades de planeamento no projeto Project Operations já não dependem de uma lógica combinada do lado do cliente e da lógica do lado do servidor. Em vez disso, o Project Operations utiliza o Project for the Web como o seu motor de agendamento. Esta alteração nas capacidades de agendamento permite várias novas funcionalidades, como vistas do Quadro e de Gantt, planeamento condicionado por recurso, [itens de lista de verificação de tarefas](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) e modos de agendamento de projetos. As novas capacidades de agendamento também são suportadas por um conjunto de novas [interfaces de programação de aplicações (APIs)](../project-management/schedule-api-preview.md). Estas APIs destinam-se a ajudar a garantir que nenhuma operação programática para criar, atualizar ou eliminar uma entidade no WBS corrompe os campos calculados na agenda.

### <a name="billing-and-pricing"></a>Faturação e preços

Como parte de investimentos contínuos no Project Operations, várias novas capacidades estão disponíveis em Faturação e preços. Seguem-se alguns exemplos:

- [Registar a utilização do material em projetos e tarefas de projeto](../material/material-usage-log.md)
- [Gestão de subcontratos](../pro/subcontracting/managing-subcontracts-overview.md)
- [Adiantamentos e contratos baseados em sinais](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Estado a não exceder e validações do contrato](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Faturação baseada em tarefas

### <a name="resource-management"></a>Gestão de recursos

O Project Operations fornece suporte opcional para o quadro do Universal Resource Scheduling (URS) e assistente de agendamento. Esta nova experiência será obrigatória na vaga de abril de 2023.

## <a name="frequently-asked-questions"></a>Perguntas mais frequentes

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Que tipos de implementação são atualmente suportados para a atualização de versão?

| Source                                                 | Target                                                    | Status                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Implementação do Project Operations Lite                        | Suportado               |
| Gestão de projetos e contabilidade do Dynamics 365 Finance | Implementação do Project Operations Lite                        | Não é suportado atualmente |
| Gestão de Projetos e Contabilística de Finanças              | Project Operations para cenários baseados em recursos/não em stock     | Não é suportado atualmente |
| Project Service Automation 3.x                         | Project Operations para cenários baseados em recursos/não em stock     | Não é suportado atualmente |
| Project for the Web (ambiente dedicado)            | Implementação do Project Operations Lite                        | Não é suportado atualmente |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Como posso instalar o Project Operations antes da ferramenta de atualização de versão estar disponível?

Existem duas opções para instalar o Project Operations antes das ferramentas de atualização da versão:

- Aprovisionar um novo ambiente.
- Implemente Project Operations separadamente em qualquer organização de vendas onde o Project Service Automation não está presente.

Se o Project Service Automation estiver instalado numa organização, mas não foi utilizado, pode ser desinstalado. Depois de remover completamente o Project Service Automation, o Project Operations podem ser instaladas na mesma organização.