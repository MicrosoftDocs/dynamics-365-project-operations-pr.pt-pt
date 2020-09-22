---
title: Gerir projetos e reservas no seu calendário do Office 365
description: Como gerir projetos e reservas no seu calendário do Office 365
author: ruhercul
manager: kfend
ms.service: dynamics-365-projectservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 92428956-1058-4490-934f-907fbbdc8f25
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 5c075e0b63db35c1e189a62a6b5b00f5bcb7ea97
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754452"
---
# <a name="manage-projects-and-bookings-in-your-calendar-project-service"></a>Gerir projetos e reservas no seu calendário (Project Service)

> [!Note]
> PRETERIDO: esta funcionalidade foi preterida e já não está disponível.

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 

Veja os compromissos pessoais, as reservas de trabalho do projeto e atribuições de ordens de intervenção do [!INCLUDE[pn_office_365](../includes/pn-office-365.md)].  
  
 Com tudo num só local é fácil gerir o seu dia. As reuniões, compromissos, reservas e tarefas estão todos disponíveis no seu calendário do [!INCLUDE[pn_office_365](../includes/pn-office-365.md)].  
  
 Se estiver a utilizar o [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], também pode introduzir os compromissos pessoais na vista de entrada de hora do Project Service. Isto permite aos gestores de projetos e recursos conhecer a disponibilidade para os projetos. Também poupa tempo, uma vez que não tem de introduzir informações duas vezes sobre os seus compromissos pessoais. Basta importar os seus compromissos pessoais a partir do seu calendário para a vista de entrada de hora do Project Service.  
  
 O seu calendário irá sincronizar as reservas de ordens de intervenção e do projeto desde hoje até às quatro semanas seguintes. Não é possível alterar esta definição.  
  
 A sincronização só é suportada num sentido, do PSA para o seu calendário do [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]. É possível sincronizar na ordem inversa. 
  
 Para obter informações sobre como utilizar o seu calendário do [!INCLUDE[pn_office_365](../includes/pn-office-365.md)], consulte [Calendário no Outlook na Web para empresas](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936).  
  
## <a name="setup"></a>Configuração  
 Antes de conseguir ver e gerir as suas reservas no seu calendário do [!INCLUDE[pn_office_365](../includes/pn-office-365.md)], terá de efetuar algumas definições.  
  
- Terá de ter credenciais de Administrador Global ou Administrador de Sistema do [!INCLUDE[pn_office_365](../includes/pn-office-365.md)].  
  
- O seu Administrador terá de configurar o perfil de servidor do e-mail e cada utilizador terá de configurar a respetiva caixa de correio. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Configurar o processamento de e-mail através da sincronização do lado do servidor](../admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks.md)  
  
## <a name="turn-on-synchronization-for-your-organization-admin-task"></a>Ativar a sincronização para a sua organização (tarefa de administração)  
  
1.  No menu principal, clique em **Definições** > **Administração**.  
  
2.  Clique em **Definições do Sistema**.  
  
3.  Clique no separador **Sincronização**.  
  
4.  Em **Selecionar a ativação ou não da sincronização das reservas de recursos com o**, selecione **Sincronizar reservas de recursos com o Outlook**.  
  
## <a name="turn-on-synchronization-for-your-user-profile-user-task"></a>Ativar sincronização para o seu perfil de utilizador (tarefa de utilizador)  
  
1.  Clique no botão **Definições** no canto superior direito do ecrã.  
  
2.  Clique em **Opções**.  
  
3.  Clique no separador **Sincronização**.  
  
4.  Em **Sincronização de reservas de recursos com o Outlook**, selecione **Sincronização de reservas de recursos com o Outlook**.  
  
## <a name="import-your-personal-appointments-user-task"></a>Importar os seus compromissos pessoais (tarefa de utilizador)  
 Poderá importar os seus compromissos pessoais a partir do seu calendário para a vista de entrada de hora do Project Service Automation.  
  
1. Abra o calendário do [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] e clique em **Importar Dados**.  
  
2. No ecrã Filtros, selecione **Compromissos do Exchange** e clique em **Aplicar**.  
  
3. O sistema irá solicitar os compromissos para a vista de entrada de hora sob a forma de entradas sugeridas a partir da semana atual. Para adicionar entradas para outra semana, clique em **Anterior** ou **Seguinte**.  
  
4. Selecione o compromisso que pretende adicionar à vista de entrada de hora Project Service Automation.  
  
5. Na caixa de pop-up **Entrada de Hora**, selecione as opções adequadas para converter o compromissos numa vista de entrada de hora do Project Service Automation.  
  
6. Clique em **Guardar**.  
  
### <a name="see-also"></a>Consulte Também  
 [Guia de Tempo, Despesa e Colaboração](../project-service/time-expense-collaboration-guide.md)
