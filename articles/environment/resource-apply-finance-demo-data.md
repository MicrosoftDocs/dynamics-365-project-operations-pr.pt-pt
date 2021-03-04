---
title: Aplicar dados de demonstração a um ambiente alojado no Finance Cloud
description: Este tópico explica como aplicar dados de demonstração do Project Operations a um ambiente alojado na Cloud do Dynamics 365 Finance.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a7cdbd2847ce45972aadd0d1a2d4f26270727ad9
ms.sourcegitcommit: d33ef0ae39f90fe3b0f6b4524f483e8052057361
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 11/03/2020
ms.locfileid: "4365252"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a>Aplicar dados de demonstração a um ambiente alojado no Finance Cloud

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

> [!IMPORTANT]
> Este tópico só é aplicável ao Microsoft Dynamics 365 Finance versão 10.0.13 e só pode ser executado num ambiente alojado na Cloud. Conclua os passos neste tópico **ANTES** de aplicar atualizações de qualidade ao ambiente.

1. No seu projeto LCS, abra a página **Detalhes do ambiente**. Note que inclui os detalhes necessários para ligar ao ambiente através do Protocolo RDP (Remote Desktop Protocol).

![Detalhes do ambiente ](./media/1EnvironmentDetails.png)

O primeiro conjunto de credenciais realçadas são as credenciais da conta local e contêm uma hiperligação à ligação de ambiente de trabalho remoto. As credenciais incluem o nome de utilizador e a palavra-passe do administrador do ambiente. O segundo conjunto de credenciais é utilizado para iniciar sessão no SQL Server neste ambiente.

2. Ligue-se remotamente ao ambiente pela hiperligação em **Contas Locais** e utilize as **Credenciais de Conta Local** autenticar.
3. Vá para **Serviços de Informação Internet** > **Conjuntos Aplicacionais** > **AOSService** e pare o serviço. Está a parar o serviço neste momento para poder continuar a substituir a base de dados SQL.

![Parar AOS](./media/2StopAOS.png)

4. Vá para **Serviços** e pare os seguintes dois itens:

- Microsoft Dynamics 365 Unified Operations: Serviço de Gestão em Lote
- Microsoft Dynamics 365 Unified Operations: Quadro de Importação/Exportação de Dados

![Parar Serviços](./media/3StopServices.png)

5. Abra o Microsoft SQL Server Management Studio. Inicie sessão com as credenciais de SQL Server e utilize o utilizador axdbadmin e a palavra-passe da página **Detalhes do ambiente** do LCS.

![SQL Server Management Studio](./media/4SSMS.png)

6. No Explorador de Objetos, **Bases de Dados** e localize **AXDB**. Irá substituir a base de dados por uma nova base de dados que está localizada no [Centro de Transferências](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip). 
7. Copie o ficheiro zip para a VM à qual está ligado remotamente e extraia o conteúdo do zip.
8. No SQL Server Management Studio, clique com o botão direito do rato em **AxDB** e, em seguida, selecione **Tarefas** > **Repor** > **Base de Dados**.

![Repor Base de Dados](./media/5RestoreDatabase.png)

9. Selecione **Dispositivo de Origem** navegue para o ficheiro extraído do ficheiro zip que copiou.

![Dispositivos de Origem](./media/6SourceDevice.png)

10. Selecione **Opções** e, em seguida, selecione **Substituir a base de dados existente** e **Fechar ligações existentes à base de dados de destino**. 
11. Selecione **OK**.

![Repor Definições](./media/7RestoreSetting.png)

Receberá a confirmação de que a reposição do AXDB foi concluída com êxito. Depois de receber esta confirmação, poderá fechar o SQL Services Management Studio.

12. Vá para **Serviços de Informação Internet** > **Conjuntos Aplicacionais** > **AOSService** e inicie o AOSService.
13. Vá para **Serviços** e inicie os dois serviços que parou anteriormente.

14. Localize a ferramenta AdminUserProvisioning nesta VM. Procure em K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.
15. Execute o ficheiro .ext através do seu endereço de utilizador no campo **Endereço de E-mail**. 
16. Selecione **Submeter**.

![Aprovisionamento de Utilizadores Administradores](./media/8AdminUserProvisioning.png)

Isto demora alguns minutos a concluir. Deve receber uma mensagem de confirmação de que o Utilizador administrador foi atualizado com sucesso.

17. Por último, execute a Linha de Comandos como Administrador e execute iisreset

![Reposição do IIS](./media/9IISReset.png)

18. Feche a sessão de ambiente de trabalho remota e utilize a página **Detalhes do ambiente** do LCS para iniciar sessão no ambiente para confirmar que está a funcionar conforme esperado.

![Finance and Operations](./media/10FinanceAndOperations.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]