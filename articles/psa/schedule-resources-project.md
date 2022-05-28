---
title: Agendar recursos para um projeto
description: Como agendar recursos para um projeto no Project Service
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: f3b7ea1a2b81b86bedc85b77689145ba5afb579d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583138"
---
# <a name="schedule-resources-for-a-project-project-service"></a>Agendar recursos para um projeto (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Pode verificar a disponibilidade de recursos para obter uma visão global das reservas dos seus recursos ou filtrar a vista por competências, equipa, localização, entre outras opções.  
  
O quadro da agenda mostra a lista de recursos e a respetiva disponibilidade. Selecione um modo de vista para mostrar a disponibilidade por **Horas**, **Dia**, **Semana** ou **Mês**.  
  
Antes de utilizar o quadro da agenda, é importante configurá-lo. Para mais informações, consulte [Configurar o quadro da agenda (Field Service ou Project Service Automation)](/dynamics365/field-service/configure-schedule-board).
  
Se estiver a utilizar uma versão mais antiga, para a disponibilidade de recursos, consulte [Ver disponibilidade de recursos](../psa/view-resource-availability.md).  

> [!IMPORTANT]
>  Para utilizar a funcionalidade de reserva do quadro da agenda, a geocodificação e os serviços de localização é necessário ativar os mapas.  
> 
> 1. No menu principal, selecione **Agendamento de Recursos** > **Administração**.  
> 2. Clique em **Parâmetros de agendamento**.  
> 3. Abra o registo e desloque-se para baixo para a secção **Resource Scheduling Optimization**.  
> 4. No campo **Ligar a Mapas**, escolha **Sim**.  
> 5. Aceitar termos e guardar o registo.  
> 6. No menu principal, selecione **Project Service** > **Quadro da agenda**. A partir daqui, existem várias formas de agendar manualmente um requisito de reserva. Escolha o método que funciona para si.
  
## <a name="find-available-resources"></a>Localizar recursos disponíveis

1.  A partir da lista **Requisitos de Reserva**, clique com o botão direito do rato numa reserva não agendada e escolha uma das seguintes opções:  
  
- Escolha **Localizar disponibilidade - Recursos Atuais** para localizar um recurso disponível a partir da lista no quadro da agenda.  
- Escolha **Localizar disponibilidade - Todos os Recursos** para localizar um recurso disponível a partir dos recursos no sistema  
   > [!NOTE]
   >  Quando o fizer, os filtros mostrarão as opções para o requisito de reserva selecionado.  
  
2. Quando o horário disponível for apresentado, clique com o botão direito do rato no horário no quadro da agenda e escolha **Reservar**. Em alternativa, arraste e largue o requisito de reserva para o horário disponível.  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a>Agendar um recurso através da vista diária e determinar quem está sub-reservado
  
1.  No quadro da agenda, selecione **Modo de Vista** e selecione **Dias**.  
  
    Mostra uma vista de grelha com o número de horas que um recurso está reservado por dia e em que dias está livre.  
  
2.  Clique no nome do recurso que pretende reservar e, em seguida, selecione **Reservar**.  
  
3.  Na caixa de diálogo **Reserva de recursos (criar)**, escolha o projeto para o qual pretende reservar o recurso, juntamente com o método de reserva e as horas de início e de fim.  
  
4.  Quando terminar, selecione **Reservar**.  
  
## <a name="view-to-the-schedule-board"></a>Ver o quadro da agenda
  
1.  Selecione um requisito de reserva com agendamento anulado na lista na parte inferior.  
  
2.  Arraste o requisito de reserva para um recurso/intervalo de tempo disponível no quadro da agenda.  
  
3.  Quando terminar, selecione **Reservar**.  
  
### <a name="additional-resources"></a>Recursos adicionais  
 [Manual do gestor de recursos](../psa/resource-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
