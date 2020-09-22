---
title: Como posso personalizar o fluxo do processo do Project Stages?
description: Uma descrição geral para personalizar o fluxo do processo de negócio das Fases do Projeto.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x
author: JohnPBurrows
ms.assetid: 36f7df9e-117d-4f85-af4b-d842e93321bd
ms.author: john.burrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: d4b99f67e929ebcd1a684bcd1124756140107d17
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754491"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a>Como posso personalizar o fluxo do processo do Project Stages?
[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

Não existe uma limitação conhecida em versões anteriores da aplicação Project Service em que os nomes das fases no fluxo do processo de negócio no Project Stages devem corresponder exatamente aos nomes de inglês esperados (**Quote**, **Plan**, **Close**). Caso contrário, a lógica de negócio, que utiliza os nomes de fase em inglês, não funciona conforme esperado. É por essa razão que não vê ações familiares tal como **Alternar Processo** ou **Editar Processo** disponíveis no formulário de projeto e personalizar o fluxo do processo de negócio não é recomendável. 

Esta limitação foi resolvida na versão 2.4.5.48 e posterior. Se necessitar de personalizar o fluxo do processo de negócio predefinido em versões anteriores, este artigo fornece soluções sugeridas.  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a>A lógica de negócio requer uma correspondência exata com nomes de fase em inglês

O fluxo do processo de negócio do Project Stages inclui lógica de negócio que aciona os seguintes comportamentos na aplicação:
- Quando o projeto está associado a uma proposta, o código define fluxo do processo de negócio para a fase **Quote**.
- Quando o projeto está associado a um contrato, o código define fluxo do processo de negócio para a fase **Plan**.
- Quando o fluxo do processo de negócio é avançado para a fase **Close**, o registo de projeto é desativado. Quando do projeto é desativado, o formulário de projeto e a estrutura hierárquica do trabalho (WBS) são definidos como só de leitura, as reservas de recurso nomeadas são libertadas e quaisquer listas de preços associadas são desativadas.

Esta lógica de negócio utiliza os nomes em inglês para as fases de projeto. Este dependência nos nomes de fase em inglês é o principal motivo por que a personalização do fluxo do processo de negócio do Project Stages não é encorajada, assim como, o motivo porque não visualiza as ações comuns do fluxo do processo de negócio como **Alternar Proces** ou **Editar Processo** na entidade do projeto.

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a>O que acontece se os nomes de fase não corresponderem aos nomes em inglês?

Na versão 1.x da aplicação Project Service na plataforma 8.2, quando os nomes de fase do processo de negócio não correspondem exatamente aos das fases em inglês, a lógica de negócio que define a fase adequada para propostas ou contratos, ou que fecha do projeto, é ignorada. Nenhuma mensagem de erro é apresentada. Por conseguinte, parece que pode personalizar o fluxo do processo de negócio do Project Stages. No entanto, não verá qualquer um dos processos automáticos a trabalhar para cotações, contratos e fecho do projeto.

Na versão 2.4.4.30 da aplicação Project Service ou anterior na plataforma 9.0, ocorreu uma alteração significativa na arquitetura dos fluxos de processo de negócio, que necessitou de uma nova programação da lógica de negócio do fluxo de processo de negócio. Consequentemente, se os nomes de fase do processo não corresponderem aos nomes em inglês esperados, irá receber uma mensagem de erro. 

Por conseguinte, se pretender personalizar o fluxo do processo de negócio do Project Stages para a entidade de projeto, só pode adicionar novas fases ao fluxo do processo de negócio predefinido para a entidade de projeto e manter as fases **Quote**, **Plan** e **Fases** tal como estão. Esta restrição assegura que não tem erros da lógica de negócio que espera os nomes de fase em inglês no fluxo do processo de negócio.

Na versão 2.4.5.48 ou posterior, a lógica de negócio descrita neste artigo foi removida do fluxo do processo de negócio predefinido para a entidade de projeto. Atualizar para essa versão ou posterior permitirá personalizar ou substituir o fluxo do processo de negócio predefinido com um dos seus. 

## <a name="workarounds-for-earlier-versions"></a>Soluções para as versões anteriores

Se a atualização não for uma opção, pode personalizar o fluxo do processo de negócio do Project Stages para a entidade de projeto de uma destas duas formas:

1. Adicionar fases adicionais à configuração predefinida, mantendo os nomes de fase em inglês para **Quote**, **Plan** e **Close**.

   > [!div class="mx-imgBorder"] 
   > ![Captura de ecrã de adição de fases à configuração predefinida](media/FAQ-Customize-BPF-1.png)
 
2. Criar o seu próprio fluxo do processo de negócio e torná-lo o fluxo do processo de negócio principal para a entidade de projeto, o que lhe permite ter os nomes de fase que pretender. No entanto, se quiser utilizar as mesmas fases de projeto padrão **Quote**, **Plan** e **Close**, necessita de efetuar algumas personalizações que partem dos nomes de fase personalizados. A lógica mais complexa está no encerramento do projeto, o qual ainda poderá acionar bastando desativar o registo de projeto.

   > [!div class="mx-imgBorder"] 
   > ![Captura de ecrã da Personalização BPF](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a>Considerações adicionais para a versão 2.4.4.30 ou anterior da aplicação Project Service na plataforma 9.0

No Project Service 2.4.4.30 ou anterior na plataforma 9.0, com um fluxo do processo de negócio personalizado o campo **Nome de Fase** na entidade de projeto utilizada nas vistas de lista do gráfico e projeto **Projeto por Fase** não atualizam porque está junto ao fluxo do processo de negócio predefinido do Project Stages. Isto pode ser abordado com os seguintes passos:

- Adicione um campo personalizado para capturar a fase de fluxo de processo de negócio atual que é atualizada à medida que o utilizador avança pelo fluxo do processo de negócio personalizado.

- Modifique o gráfico **Projeto por Fase** para trabalhar com o campo personalizado em vez da configuração predefinida.

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a>Passos para criar o seu próprio fluxo do processo de negócio para a entidade de projeto

Para criar o seu próprio fluxo do processo de negócio para a entidade de projeto faça o seguinte:

1. Aceda a **Definições** > **Centro de Processos**. Não copie o fluxo do processo de negócio do Project Stages visto que também copia a lógica de negócio do Project Service.

   > [!div class="mx-imgBorder"] 
   > ![Captura de ecrã da Personalização BPF](media/FAQ-Customize-BPF-3.png)

2. Utilize o Designer de Processo para criar os nomes de fase pretendidos. Se pretender a mesma funcionalidade das fases predefinidas para **Quote**, **Plan** e **Close**, terá de criar isso com base nos nomes de fase do seu fluxo processo de negócio personalizados.

   > [!div class="mx-imgBorder"] 
   > ![Captura de ecrã do Designer de Processo utilizado para personalizar BPF](media/FAQ-Customize-BPF-4.png) 

3. No Designer de Processo, clique em **Fluxo do Processo de Encomenda** para tornar o fluxo do processo de negócio personalizadas no principal para a entidade de projeto movendo-o acima do fluxo do processo de negócio do Project Stages para o topo da lista.

   > [!div class="mx-imgBorder"] 
   > ![Captura de ecrã de utilização do Fluxo do Processo de Encomenda](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a>Os seguintes passos aplicam-se a aplicação Project Service 2.4.4.30 ou anterior na plataforma 9.0

4. Adicione um novo campo personalizado para a entidade de projeto para capturar as fases personalizadas no seu fluxo do processo de negócio personalizado. Terá de adicionar lógica de negócio (plug-in/fluxo de trabalho) para atualizar este campo quando é atualizada a fase no fluxo do processo de negócio personalizado.

   > [!div class="mx-imgBorder"] 
   > ![Captura de ecrã de personalização da Entidade de projeto](media/FAQ-Customize-BPF-6-720.png)

5. Modifique o gráfico **Projeto por Fase** para utilizar o novo campo personalizado para fases.

   > [!div class="mx-imgBorder"] 
   > ![Captura de ecrã de utilização do gráfico Projeto por Fase](media/FAQ-Customize-BPF-7-720.png)

6. Modifique quaisquer vistas para a entidade de projeto para incluir o novo campo personalizado para fases.

   > [!div class="mx-imgBorder"] 
   > ![Captura de ecrã de modificação de vistas de Entidade de projeto](media/FAQ-Customize-BPF-8-720.png)

