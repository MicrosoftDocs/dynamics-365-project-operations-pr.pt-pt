---
title: Atualizar o Project Operations no seu ambiente financeiro
description: Este tópico fornece informações sobre como atualizar o Project Operations no seu ambiente Dynamics 365 Finance.
author: ruhercul
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d85a180aa094a048b4422605b25151d10785f67d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011070"
---
# <a name="update-project-operations-in-your-finance-environment"></a>Atualizar o Project Operations no seu ambiente financeiro

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_


Este tópico fornece informações sobre como atualizar o Dynamics 365 Project Operations no seu ambiente Dynamics 365 Finance. Existem três procedimentos que são necessários para atualizar o Project Operations para a Atualização 5 (UR5):

- [Importe o pacote no seu projeto de pré-visualização](#import)
- [Aplicar a atualização](#apply)
- [Atualizar o seu ambiente Dataverse](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a>Importe o pacote para o seu projeto de LCS

1. Iniciar sessão nos [Lifecycle Services (LCS)](https://lcs.dynamics.com/) como Proprietário de Projeto ou Gestor de Ambiente.
2. Da lista de projetos, selecione o seu projeto LCS.
3. Na página do **Projeto**, no grupo **Ambientes**, abra o ambiente que pretende atualizar.
4. Verifique se o ambiente está a funcionar. Se não tiver iniciado, inicie o ambiente.
5. Na secção **Nova versão** em **Atualizações disponíveis**, selecione **Ver atualização** para 10.0.15.

![Ver botão de atualização](media/view-update.png)

6. Na página **Atualizações binárias**, selecione **Guardar pacote**.
7. Na página **Rever e guardar atualizações**, selecione **Guardar pacote**.
8. No painel **Guardar para a biblioteca de ativos** que se abre, introduza o nome do pacote e, em seguida, selecione **Guardar o pacote**.
9. Quando o LCS terminar de guardar o pacote, o botão **Feito** está ativado. Selecione **Concluído**. O LCS verificará o pacote. A verificação pode demorar alguns minutos ou até uma hora.


## <a name="apply-the-package-update"></a><a name="apply"></a>Aplique a atualização de pacote

1. No LCS, na página de **Detalhes do ambiente**, selecione **Manter** > **Aplicar atualizações**.
2. Na lista, selecione o pacote que guardou anteriormente e, em seguida, selecione **Aplicar**.
3. Selecione **Sim** para confirmar que deseja implementar o pacote.

![Confirme a caixa de diálogo de implementação do pacote](media/confirm-package-deployment.png)

4. Selecione **Sim** para confirmar que deseja atualizar a aplicação.

![Confirme a caixa de diálogo de atualização de aplicações](media/confirm-application-update.png)

A atualização de implementação e aplicação começará. 

Na página de **Detalhes do ambiente**, no canto superior direito, o estado do ambiente atualizará para **Em manutenção**. Em aproximadamente duas horas, a atualização estará completa. As informações de libertação da aplicação serão atualizadas para **Microsoft Dynamics 365 for Finance and Operations 10.0.15** e o estado do ambiente será atualizado para **Implementado**.


## <a name="update-your-dataverse-environment"></a><a name="update"></a>Atualizar o seu ambiente Dataverse

1. Inicie sessão no [centro de administração do Power Platform](https://admin.powerplatform.com/).
2. Na lista, encontre e abra o ambiente que usou para instalar o Project Operations.
3. Na página **Ambientes**, selecione **Recurso** > **apps Dynamics 365**.
4. Na lista, localizar **Microsoft Dynamics 365 Project Operations**, e na coluna **Estado**, selecione **Atualização disponível**.
5. Selecione **Concordo com os termos da caixa de verificação de serviço** e, em seguida, selecione **Atualizar**. A versão mais recente da solução será instalada.

Depois de concluída a instalação, terá a versão 4.5.0.134 instalada.

## <a name="configure-new-features"></a>Configurar novas funcionalidades

### <a name="enable-dual-write-mapping"></a>Possibilita o mapeamento de escrita dupla

Depois de concluir a atualização sobre as Finanças e ambientes Dataverse, pode ativar os mapeamentos de dupla escrita necessários. Conclua os seguintes procedimentos para possibilitar os mapeamentos de escrita dupla.

- [Atualizar definições de segurança no ambiente do Customer Engagement](#security)
- [Atualizar entidades de dados](#refresh)
- [Atualizar e executar os mapeamentos de dupla escrita](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a>Atualizar definições de segurança no ambiente do Dataverse

As seguintes atualizações aos privilégios de segurança para as entidades são necessárias como parte da atualização para UR5.

1. No seu ambiente Dataverse, vá a **Definições** e no grupo **Sistema**, selecione **Segurança**.

![Definições do ambiente Dataverse](media/Picture21.png)

2. Selecionar **Direitos de Acesso**.
3. A partir da lista de funções, selecione **utilizador de aplicações de dupla escrita** e selecione o separador **Entidades Personalizadas**. 
4. Verifique se a função tem permissões de **leitura** e **acrescentar a** para:

      - **Tipo de taxa de cambio de moeda**
      - **Tabela de contas** 
      - **Calendário Fiscal** 
      - **Livro-razão**

5. Depois de o direito de acesso ser atualizado, vá a **Definições** > **Segurança** > **Equipas**. Verifique se a função de **utilizador de aplicações de dupla escrita** foi aplicada à equipa. 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a>Atualizar entidades de dados a partir da atualização

1. No seu ambiente de Finanças, abra o espaço de trabalho de **gestão de dados** e, em seguida, abra a página de **parâmetros-quadro**.
2. No separador **definições de entidade**, selecione **Atualizar lista de entidades**.
3. Selecione **Fechar** para confirmar a atualização da entidade.

 > [!NOTE]
 > Este processo irá demorar cerca de 20 minutos a concluir. Será notificado quando a atualização estiver completa.

### <a name="update-dual-write-mappings"></a><a name="run"></a>Atualizar mapeamentos de escrita dupla

1. No espaço de trabalho de **gestão de dados**, selecione **Escrita dupla**.
2. Selecione **Aplicar soluções**, selecione ambas as soluções na lista e, em seguida, selecione **Aplicar**.
3. Na página de **escrita dupla**, selecione os seguintes mapas de tabela e, em seguida, selecione **Parar**.

    - **Valores reais de integração com o Project Operations (msdyn_actuals)**
    - **Categorias de despesas de projeto de integração do Project Operations (msdyn_expensecategories)**
    - **Entidade de exportação de despesas de projeto de integração de valores reais do Project Operations (msdyn_expenses)**

4. Na página da **versão do mapa de tabela**, aplique uma nova versão do mapa a cada uma das três entidades.
5. Na página de **escrita dupla**, selecione executar para reiniciar os mapas.
6. Na lista de mapas, selecione o mapa **Livro-razão (msdyn_ledgers)** com todos os pré-requisitos e selecione a caixa de verificação de **sincronização inicial**. 
7. No campo **Master para sincronização inicial**, selecione **apps Finance and Operations** e, em seguida, selecione **Executar**.
 
 ![Sincronização do mapa de livros](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]