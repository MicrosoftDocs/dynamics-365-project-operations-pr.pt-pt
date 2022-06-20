---
title: Novidades de outubro de 2021 - Implementação do Project Operations Lite
description: Este artigo fornece informações sobre as atualizações de qualidade disponíveis na versão de outubro de 2021 da implementação do Project Operations Lite.
author: sigitac
ms.date: 10/05/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 7199853bea7e8e99a2a1ce19d6ce88736edb38f8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921960"
---
# <a name="whats-new-october-2021---project-operations-lite-deployment"></a>Novidades de outubro de 2021 - Implementação do Project Operations Lite

_Aplica-se a: Implementação lite – negócio para faturação pró-forma_

Este artigo aplica-se aos seguintes componentes e versões do Dynamics 365 Project Operations:

  - Project Operations na versão 4.25.0.91 do ambiente Microsoft Dataverse


## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versão

Estão incluídas nesta versão as seguintes funcionalidades:

[Gestão de subcontratos](../subcontracting/managing-subcontracts-overview.md): esta funcionalidade proporciona a capacidade para criar um subcontrato com o fornecedor, discriminar todas as compras como itens de linha no subcontrato, ajustar preços e associar contactos.


## <a name="quality-updates"></a>Atualizações de qualidade

| **Área de funcionalidades** | **Número de referência** | **Atualização de qualidade** |
| --- | --- | --- |
| Faturação e preços | 2209402 | Correção das validações que impediam a faturação dos montantes de retenção quando um contrato de projeto era confirmado. |
| Gestão de oportunidades | 2227414 | Os campos **Produto**, **Acrescentado Manualmente** e **IsProductOverriden** são copiados para os detalhes da linha de proposta e detalhes do item de contrato. |
| Faturação e preços | 2338357 | A moeda no registo de utilização do material deve assumir por predefinição a moeda do projeto quando o projeto é selecionado. |
| Tempo e despesa | 2414777 | Deve ser possível cancelar uma aprovação quando a despesa ou entrada de hora tem mais do que uma aprovação de projeto associada. |
