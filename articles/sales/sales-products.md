---
title: Produtos
description: Este tópico fornece informações sobre o catálogo de produtos que pode usar para fornecer informações aos clientes sobre os produtos e preços que a sua organização oferece.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 30633a7445baaf99af5be5c88e35b24824022b93
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121277"
---
# <a name="products"></a>Produtos

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Os produtos são espinha a dorsal do seu negócio. O catálogo de produtos no Dynamics 365 Sales Professional é uma coleção de produtos e informações sobre os preços. Faça com que seja mais fácil para os seus representantes de vendas aumentarem as respetivas vendas, criando um catálogo de produtos rapidamente.

## <a name="add-a-product"></a>Adicionar um produto

1.  Certifique-se de que possui a função de Gestor de vendas profissional ou Administrador de sistema para que possa adicionar produtos no Dynamics 365 Sales Professional.
2.  No mapa do site, em **Configuração**, selecione **Produtos**.
3.  Selecione **Adicionar Produto** e preencha as seguintes informações:

    -  **Nome**
    -  **ID do Produto**
    -  **Principal**: Selecione uma família de produtos principal para o produto. Se estiver a criar um produto subordinado numa família de produtos, o nome da família de produtos principal é preenchido aqui. Isto não pode ser alterado depois de o registo ser guardado.
    -  **Válido De**/**Válido Até**: Definir o período de tempo durante o qual o produto é válido, selecionando uma data **Válido De** e uma data **Válido Até**.
    -  **Grupo de Unidades**: Selecione um grupo de unidades. Um grupo de unidades é uma coleção de mais unidades de um produto é vendido e define como os itens individuais são agrupados em quantidades maiores. Por exemplo, se estiver a adicionar sementes como produto, podia ter criado um grupo de unidades denominado “Sementes” e definido a unidade primária como “pacote”.
    -  **Unidade Predefinida**: Selecione a unidade mais comum na qual o produto será vendido. As unidades são as quantidades ou medidas em que vende os produtos. Por exemplo, adicionar sementes como produto, pode vendê-las em pacotes, caixas ou paletes. Cada um destes torna-se uma unidade do produto. Se as sementes são vendidas na maior parte dos grupos, selecione como a que unidade.
    -  **Lista de Preços Predefinida**: No caso de se tratar de um produto novo, este campo é só de leitura. Para poder selecionar uma lista de preços predefinida, primeiro tem de preencher todos os campos necessários e guardar o registo. Apesar de a lista de preços predefinida não ser obrigatória, após guardar o registo de produto é aconselhável definir uma lista de preços predefinida para cada produto. Em seguida, se um registo de cliente não contiver uma lista de preços, o Sales poderá utilizar a lista de preços predefinida para gerar propostas, encomendas e faturas.
    -  **Decimais Suportados**: Introduza um número inteiro entre 0 e 5. Se não for possível dividir o produto em quantidades fracionais, introduza o valor 0. A precisão do campo **Quantidade** no registo da proposta, encomenda ou fatura do produto é validado de acordo com o valor neste campo, caso o produto não tenha uma lista de preços associada.
    -  **Assunto**: Associe este produto a um assunto. Pode utilizar assuntos para categorizar os produtos e filtrar relatórios.

4.  Selecione **Guardar**.
5.  No separador **Detalhes adicionais**, na secção **Itens da lista de preços**, selecione o ícone **Mais comandos** e, em seguida, selecione **Adicionar novo item da lista de preços**.
7.  No separador **Detalhes adicionais**, na secção **Relação de produtos**, selecione o ícone **Mais comandos** e, em seguida, selecione **Adicionar nova relação de produtos**.
8.  No formulário **Nova relação de produtos**, introduza os seguintes detalhes e, na barra de comandos, selecione **Guardar e Fechar**:

    -   **Produto relacionado**: Selecione um produto que pretende adicionar como produto relacionado com o registo de produto existente que está a trabalhar neste.
    -   **Tipo de relação de venda**: Selecione se pretende adicionar o produto como uma venda, acima- entre uma venda, um anexo, ou um produto de substituição.
    -   **Direção**: Selecione se a relação entre os produtos será unidirecional ou bidirecional. Quando seleciona unidirecional, o produto que selecionou em **Produto relacionado** será mostrado como recomendação do produto existente mas não vice-versa.

9.  No formulário do Produto, selecione **Guardar**.

## <a name="import-products"></a>Importar produtos

Pode utilizar os modelos de importação para trazer dados de produtos em massa para o Dynamics 365 Sales.

## <a name="revise-a-product"></a>Rever um produto

Mantenha o inventário de produto atualizar rapidamente revisando propriedades para os produtos, conforme necessário e republishing informações de que os agentes de vendas possam ver as alterações posteriores ao inventário.

1.  Certifique-se de que um dos direitos de acesso seguintes ou permissões equivalentes: Administrador de Sistema, Personalizador de Sistemas, Gestor de Vendas, Vice-Presidente de Vendas, Vice-Presidente de Marketing ou CEO-Gestor Empresarial.
2.  No mapa do site, selecione **Produtos**.
3.  Abra um produto ativo que pretende alterar e, na barra de comandos, selecione **Rever**.
4.  Na caixa de diálogo **Confirmar Revisão** selecione **Confirmar**. Isto altera o estado do produto a **Na revisão**.
5.  Depois de efetuar as alterações, na barra de comandos, selecione **Publicar**.

    > [!TIP]
    > Para reverter as alterações e continuar com a última versão ativa do produto, selecione **Reverter**. Isto altera o estado do produto da **Ativo**.

## <a name="clone-a-product"></a>Clonar um produto 

Quando estiver a criar um novo produto, poupe tempo clonando um existente. Cria uma cópia do registo original com todos os detalhes exceto nome e ID

1.  Certifique-se de que um dos direitos de acesso seguintes ou permissões equivalentes: Administrador de Sistema, Personalizador de Sistemas, Gestor de Vendas, Vice-Presidente de Vendas, Vice-Presidente de Marketing ou CEO-Gestor Empresarial.
2.  No mapa do site, selecione **Produtos**.
3.  Selecione o registo de um produto que pretende clonar e, na barra de comandos, selecione **Clonar**. É apresentada uma caixa de diálogo de confirmação.
4.  Selecione **Confirmar**.

Um novo registo de produto abre-se com os mesmos detalhes do original, à exceção do nome e ID.

## <a name="retire-a-product"></a>Extinguir um produto 

Se a sua organização não vender um produto, extinga-o para que o produto já não esteja disponível para os agentes de vendas.

1.  Certifique-se de que tem a função de Administrador de Sistema ou Gestor do Sales Professional ou permissões equivalentes.
2.  No mapa do site, selecione **Produtos**.
3.  Abra um produto ativo que pretende extinguir e, na barra de comandos, selecione **Extinguir**.
4.  Na caixa de diálogo **Confirmar Extinguir** selecione **Confirmar**.


## <a name="delete-a-product"></a>Eliminar um produto

Para parar a vender um produto, elimine-o.

> [!IMPORTANT]
> Não é possível recuperar registos eliminados.

1.  Certifique-se de que tem a função de Administrador de Sistema ou Gestor do Sales Professional ou permissões equivalentes.
2.  No mapa do site, selecione **Produtos**.
3.  Selecione o registo de um produto que pretende eliminar e, na barra de comandos, selecione **Eliminar**.
4.  Na caixa de diálogo **Confirmar Eliminar**, selecione **Continuar**.
 
 ## <a name="quantity-factors-for-products"></a>Fatores de quantidade para produtos

Fatores de quantidade suportam a venda de produtos baseados em subscrições. Para produtos baseados em subscrições, a quantidade na proposta ou item de contrato do projeto é expressa como o número de meses do utilizador.

Normalmente, o preço do software de subscrição é armazenado no catálogo como o preço por utilizador, por mês. No entanto, pode utilizar outras descrições de tempo. Durante o processo de vendas, o preço na linha de proposta é, normalmente, o preço por utilizador e por mês negociado e descontado pelo agente de vendas de TI. Cada negócio tem um número diferente de utilizadores e um número diferente de meses de subscrição. A quantidade que é utilizada para calcular o montante da linha de proposta é um produto do número de utilizadores e do número de meses de subscrição.

Os fatores de quantidade dependem dos atributos do produto. Quando configura propriedades específicas para um produto, pode sinalizar um subconjunto dessas propriedades, ou todas as propriedades, como fatores de quantidade.

O sistema valida que apenas as propriedades numéricas ou as propriedades de produto que têm um tipo de dados numérico são sinalizadas como fatores de quantidade. Quando um produto para o qual os fatores de quantidade estão configurados é adicionado a uma linha de proposta, o campo **Quantidade** na linha da proposta passa a ser um campo só de leitura. Depois de introduzir valores para propriedades de produto que são fatores de quantidade, é calculada a quantidade da linha de proposta.

Por exemplo, se existirem as seguintes propriedades: 

- **N.º de utilizadores**: O número de utilizadores 
- **N.º de Meses**: O número de meses da subscrição
- **SKU do Produto** 

O **N.º de Utilizadores** e **N.º de Meses** podem ser sinalizadas como fatores de quantidade editando as propriedades da linha de produto. 
