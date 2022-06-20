---
title: Novidades de setembro de 2021 - Project Operations para cenários baseados em recursos/itens não existentes em stock
description: Este artigo fornece informações sobre as atualizações de qualidade disponíveis na versão de setembro de 2021 do Project Operations para cenários baseados em recursos/itens não existentes em stock.
author: sigitac
ms.date: 09/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: c7f764b3e8ee3775167ee57b4f034e383899aea3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923386"
---
# <a name="whats-new-september-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades de setembro de 2021 - Project Operations para cenários baseados em recursos/itens não existentes em stock

*Aplica-se A: Project Operations para cenários baseados em recursos/não armazenados*

Este artigo aplica-se aos seguintes componentes e versões do Dynamics 365 Project Operations:

   - Project Operations na versão de ambiente 4.14.0.99 do Microsoft Dataverse.
   - Gestão de projetos e contabilidade no ambiente do Dynamics 365 Finance versão 10.0.20.

## <a name="project-operations-dual-write-maps-updates"></a>Atualizações de mapas de escrita dupla do Project Operations

Não existem atualizações para os mapas de escrita dupla do Project Operations nesta versão. Para obter uma lista atual e as versões dos mapas de escrita dupla do Project Operations, consulte [Versões do mapa de escrita dupla do Project Operations](../environment/resource-dual-write-maps.md).

Execute sempre a versão mais recente do mapa no seu ambiente e ative todos os mapas de tabelas relacionados à medida que atualiza a sua solução do Project Operations Dataverse e a versão da solução Finance. Certas funcionalidades e capacidades podem não funcionar corretamente se a versão mais recente do mapa não estiver ativada. Pode ver a versão ativa do mapa na página **Escrita dupla** na coluna **Versão**. Para ativar uma nova versão do mapa, selecione **Versões do mapa de tabela**, selecione a versão mais recente e, em seguida, guarde a versão selecionada. Se tiver personalizado um mapa de tabela fora da caixa, reaplique as alterações. Para mais informações, consulte [Gestão do ciclo de vida da aplicação](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se ocorrer um problema ao iniciar o mapa, siga as instruções na secção [Problema de colunas de tabela em falta em mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) do guia de resolução de problemas do serviço Escrita Dupla.

## <a name="quality-updates"></a>Atualizações de qualidade

### <a name="project-operations-on-dataverse"></a>Project Operations no Dataverse

| **Área de funcionalidades** | **Número de referência** | **Atualização de qualidade** |
| --- | --- | --- |
| Tempo e despesa | 1811407 | Ajuste do direito de acesso de Aprovador do Projeto para aprovações de entradas de despesas. |
| Tempo e despesa | 1811438 | Ajuste do direito de acesso de Aprovador do Projeto para cancelamento de entradas de horas. |
| Tempo e despesa | 2370126 | Atualização dos ícones **Tarefa de Projeto** e **Função** na entidade **Entrada de Hora**. |
| Tempo e despesa | 2379879 | Correção da função **Copiar Semana** na entrada de hora quando é utilizado o Dynamics 365 para telemóveis. |
| Faturação e Preços | 2371906 | O montante total da fatura pró-forma não deve ser ajustável no Project Operations para implementações baseadas em recursos. |
| Faturação e Preços | 2385802 | Correção do que ocorre com horas reais negativas quando os totais do projeto são atualizados. |
| Faturação e Preços | 2389675 | Melhoramento do comportamento de confirmação da fatura pró-forma. A entidade de tarefas de execução prolongada deve ter em conta a atividade necessária para escrever resultados de confirmação para a contabilidade. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Gestão de projetos e contabilidade no Dynamics 365 Finance

| Área de funcionalidades | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Viagem e despesa | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Os montante das transações de fornecedores e imposto sobre vendas registados a partir de uma despesa criada a partir de uma transação de cartão de crédito estão incorretos. |
| Viagem e despesa | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | São criadas linhas de liquidação incorretas quando o diário de pagamentos é gerado. |
| Viagem e despesa | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Os montante das transações de imposto sobre vendas registados a partir de uma despesa criada a partir de uma transação de cartão de crédito estão incorretos. |
| Viagem e despesa | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | A eliminação de uma linha de despesa pode demorar muito tempo. |
| Gestão contabilística do projeto | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Depois de aplicar o BDC 4619395, a alteração da sequência de números para **Contínua** não é suportada e quando regista uma estimativa, ocorre o seguinte erro: "O sistema não suporta a configuração "contínua" da sequência de números em Proj_X". |
| Gestão contabilística do projeto | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Pode ocorrer uma falha no registo de uma fatura do fornecedor com a seguinte mensagem de erro: "As transações no voucher não têm um saldo de acordo com 5/17/2021. (moeda contabilística: 0,00 - moeda de relatório: 0,01)". |
