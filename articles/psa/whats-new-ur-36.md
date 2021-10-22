---
title: Novidades ou alterações na Versão da Atualização 36 do Project Service Automation, V3
description: Este tópico lista as funcionalidades e correções que estão disponíveis na Versão de Atualização 36 do Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/06/2021
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
ms.openlocfilehash: 9b85aed79acb7e7784a23f54a2e9af1cc83f5f4d
ms.sourcegitcommit: 6d9fc4dc851814664bf71729904ab4bedd85fe70
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/06/2021
ms.locfileid: "7606803"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-36-v3"></a>Novidades ou alterações na Versão da Atualização 36 do Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Temos o prazer de anunciar a atualização mais recente para a aplicação Microsoft Dynamics 365 Project Service Automation. Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização. É compatível com o Dynamics 365, versão 9.x. Para atualizar para esta versão, visite a página de soluções online do Centro de Administração do Dynamics 365 e instale a atualização. Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).

Este tópico lista as funcionalidades e correções novas ou alteradas para o Project Service Automation V3, Versão da Atualização 36, V3. Esta versão tem um número de compilação de V3.10.57.152 e está geralmente disponível através de uma Atualização automática em outubro de 2021.

## <a name="update-release-36"></a>Versão da Atualização 36

### <a name="bug-fixes"></a>Correções de erros

Foram corrigidos os seguintes problemas.

**Geral**
- O nome do campo **Modelo de Horas de Trabalho Predefinido** é traduzido incorretamente na página **Parâmetros do Projeto**.
- Os plug-ins assíncronos não estão a processar corretamente as exceções relacionadas com **SharedVariableService**.

**Tempo e Despesa**
- Quando faltam linhas de diário ou se o utilizador não tiver os privilégios corretos para ler linhas de diário, ocorre um erro incorreto quando as aprovações do projeto são canceladas.
- Os utilizadores não conseguem cancelar uma aprovação quando uma despesa ou entrada de hora tem mais do que uma aprovação de projeto associada.
- **Ausência** e **Férias** têm traduções incorretas no idioma chinês numa pesquisa na página de criação rápida de **Entrada de Hora**.

**Gestão de recursos**
- O utilizador não consegue procurar recursos no **Assistente da Agenda** quando o modo de vista está definido como **Dia**, **Semana** ou **Mês**.
- Pode ser atribuída uma permissão incorreta aos recursos genéricos para poderem ter nomes de cargos vazios. 
- Fechar um contrato como perdido não cancela reservas futuras.

**Vendas**
- Quando um ambiente tem um grande volume de produtos, o desempenho degrada-se na grelha **Estimativa de Materiais**.
- Ao criar um projeto a partir de um modelo, a moeda do projeto não assume por predefinição a unidade de contratação do respetivo Gestor de Projeto.
- Os montantes reais nem sempre correspondem ao refletido no projeto devido ou os montantes tornam-se negativos em cenários de recuperação específicos.
- Ocorre um erro quando associa um projeto criado a partir do modelo do projeto para um item de contrato.
- Os utilizadores podem eliminar um item de contrato com os marcos **Pronto para faturar** e **Fatura Criada**. Tal não deve ser permitido.
- Quando as estimativas são importadas a partir de um projeto, a exigibilidade de detalhe da linha de proposta é definida incorretamente quando a faturação baseada em tarefas é ativada para a linha da proposta.
- Quando adiciona um marco de faturação de preço fixo, o marco só é refletido na subgrelha de marcos quando a página é atualizada.
- É gerada uma exceção de referência nula quando cria um contrato de projeto com um nome de proposta nulo.
- As tarefas do modo manual em que a moeda do projeto é diferente da moeda do recurso resultam em estimativas de preço incorretas.
- Os utilizadores não podem recuperar uma transação corrigida com êxito por uma fatura de correção.
- As categorias de transações desativadas aparecem na grelha **Estimativas de Despesas**.



