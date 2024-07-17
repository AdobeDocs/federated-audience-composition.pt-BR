---
audience: end-user
title: Criar a primeira consulta usando o modelador de consultas
description: Saiba como criar sua primeira consulta no modelador de consultas
source-git-commit: 5fe470ce83a5c3d3df7717bc1203849d99edf430
workflow-type: tm+mt
source-wordcount: '2066'
ht-degree: 11%

---

# Criar a primeira consulta {#build-query}

Para começar a criar uma consulta, acesse o modelador de consultas do local de sua escolha, dependendo da ação que deseja executar. O modelador de Consulta é aberto com uma tela em branco. Clique no botão **+** para configurar o primeiro nó da consulta.

Você pode adicionar dois tipos de elementos:

* **Os componentes de filtragem** (Condição personalizada, Selecionar público) permitem que você crie suas próprias regras ou selecione um público para refinar sua consulta. Elas são adicionadas no início da query e em transições pontilhadas. [Saiba como trabalhar com componentes de filtragem](#filtering)

  Exemplo: *Destinatários que assinaram o informativo &quot;Esportes&quot;*. *Recipients morando em Nova York*, *Recipients morando em São Francisco*

  ![](assets/query-add-component.png){zoomable="yes"}

* **Operadores de grupo** (AND, OR, EXCEPT) permitem agrupar componentes de filtragem no diagrama. Eles são adicionados em transições existentes antes de um componente de filtragem. [Saiba como trabalhar com operadores](#filtering)

  Exemplo: *Recipients que assinaram o informativo &quot;Esportes&quot;**AND**que vivem em Nova York **OR**San Francisco*.

  ![](assets/query-add-operator.png){zoomable="yes"}

## Adicionar componentes de filtragem {#filtering}

Os componentes de filtragem permitem refinar a consulta usando:

* **[Condições personalizadas](#custom-condition)**: filtre sua consulta criando sua própria condição com atributos do banco de dados e expressões avançadas.
* **[Públicos](#audiences)**: filtre sua consulta usando um público existente.

### Configurar uma ação personalizada {#custom-condition}

>[!CONTEXTUALHELP]
>id="dc_orchestration_querymodeler_customcondition"
>title="Condição personalizada"
>abstract="As condições personalizadas são componentes de filtragem que permitem filtrar sua consulta criando sua própria condição com atributos do banco de dados e expressões avançadas."

Para filtrar sua consulta usando uma condição personalizada, siga estas etapas:

1. Clique no botão **+** no nó desejado e selecione **[!UICONTROL Condição personalizada]**. O painel de propriedades de condição personalizada é aberto no lado direito.

1. No campo **Atributo**, selecione o atributo do banco de dados que você deseja usar para criar sua condição. A lista de atributos inclui todos os atributos do banco de dados, incluindo atributos de tabelas vinculadas.

   ![](assets/query-custom-condition-fields.png){zoomable="yes"}

   >[!NOTE]
   >
   >O botão **Editar expressão** permite que você aproveite o editor de expressão para definir manualmente uma expressão usando campos do banco de dados e funções auxiliares. [Saiba como editar expressões](expression-editor.md)

1. Selecione o operador a ser aplicado na lista suspensa. Vários operadores estão disponíveis para uso. Observe que os operadores disponíveis na lista suspensa dependem do tipo de dados do atributo.

   +++Lista de operadores disponíveis

   | Operador | Finalidade | Exemplo |
   |  ---  |  ---  |  ---  |
   | Igual a | Retorna um resultado idêntico aos dados inseridos na segunda coluna de valor. | Last name (@lastName) equal to &#39;Jones&#39;, retornará apenas destinatários cujo sobrenome seja Jones. |
   | Não é igual a | Retorna todos os valores não idênticos ao valor inserido. | Idioma (@language) a ser igual a &#39;English&#39; |
   | Maior que | Retorna um valor maior que o valor digitado. | Age (@age) greater than 50</strong>, retornará todos os valores maiores que &#39;50&#39;, ou seja, &#39;51&#39;, &#39;52&#39; etc. |
   | Menor que | Retorna um valor menor que o valor digitado. | Creation date (@created) before &#39;DaysAgo(100)&#39;</strong>, retornará todos os destinatários criados menos de 100 dias atrás. |
   | Maior que ou igual a | Retorna todos os valores iguais ou maiores que o valor inserido. | Age (@age) greater than or equal to &#39;30&#39;</strong>, retornará todos os destinatários maiores de 30 anos ou mais. |
   | Menor que ou igual a | Retorna todos os valores iguais ou inferiores ao valor inserido. | Age (@age) less than or equal to &#39;60&#39;</strong>, retornará todos os destinatários com 60 anos ou menos. |
   | Incluído em | Retorna resultados incluídos nos valores indicados. Esses valores devem ser separados por vírgula. | Birth date (@birthDate) is included in &#39;12/10/1979,12/10/1984&#39; retornará os destinatários nascidos entre essas datas. |
   | Não está em | Funciona como o operador Is included in. Aqui, queremos excluir destinatários com base nos valores inseridos. | A data de nascimento (@birthDate) não está incluída em &#39;12/10/1979,12/10/1984&#39;. Ao contrário do exemplo anterior, os destinatários nascidos nessas datas não serão retornados. |
   | Está vazio | Nesse caso, o resultado que estamos procurando corresponde a um valor vazio na segunda coluna de valor. | Mobile (@mobilePhone) is empty retorna todos os destinatários que não têm número de celular. |
   | Não está vazio | Funciona de forma inversa ao operador Is empty. Não é necessário inserir dados na segunda coluna de valor. | O email (@email) não está vazio. |
   | Inicia com | Retorna os resultados iniciando com o valor inserido. | Account # (@account) começa com &#39;32010&#39;. |
   | Não inicia com | Retorna os resultados que não começam com o valor inserido | Account # (@account) não começa com &#39;20&#39; |
   | Contains | Retorna os resultados contendo pelo menos o valor inserido. | Email domain (@domain) contains &#39;mail&#39;</strong> retornará todos os nomes de domínio que contêm &#39;mail&#39;. Portanto, o domínio &quot;gmail.com&quot; também será retornado. |
   | Não contém | Retorna resultados não contendo o valor inserido. | O domínio de email (@domain) não contém &#39;vo&#39;</strong>. Nesse caso, nomes de domínio que contêm &#39;vo&#39; não serão retornados. O nome de domínio &#39;voila.fr&#39; não aparecerá nos resultados. |
   | Curtir | Like é muito semelhante ao operador Contains. Permite inserir um caractere curinga % no valor. | Sobrenome (@lastName) como &#39;Jon%s&#39;. Aqui, o caractere curinga é usado como &quot;joker&quot; para localizar o nome &quot;Jones&quot;, o operador esqueceu a letra ausente entre o &#39;n&#39; e o &#39;s&#39;. |
   | Not like | Like é muito semelhante ao operador Contains. Permite inserir um caractere curinga % no valor. | Sobrenome (@lastName) diferente de &#39;Smi%h&#39;. Aqui, os destinatários que têm &#39;Smi%h&#39; como sobrenome não serão retornados. |

+++

1. No campo **Value**, defina o valor esperado. Você também pode aproveitar o editor de expressão para definir manualmente uma expressão usando campos do banco de dados e funções auxiliares. Para fazer isso, clique no botão **Editar expressão**. [Saiba como editar expressões](expression-editor.md)

   *Exemplo de consulta retornando todos os perfis com 21 anos ou mais:*

   ![](assets/query-custom-condition.png){zoomable="yes"}

#### Condições personalizadas em tabelas vinculadas (links 1-1 e 1-N){#links}

As condições personalizadas permitem consultar tabelas vinculadas à tabela usada atualmente pela regra. Isso inclui tabelas com um link de cardinalidade 1-1 ou tabelas de coleção (link 1-N).

Para um link **1-1**, navegue até a tabela vinculada, selecione o atributo desejado e defina o valor esperado.

Você também pode selecionar diretamente um link de tabela no seletor de **Valor** e confirmar. Nesse caso, os valores disponíveis para a tabela selecionada precisam ser selecionados usando um seletor dedicado, como mostrado no exemplo abaixo.

+++Exemplo de consulta

Aqui, a consulta está direcionando marcas cujo rótulo é &quot;running&quot;.

1. Navegue dentro da tabela **Marca** e selecione o atributo **Etiqueta**.

   ![](assets/1-1-attribute.png){zoomable="yes"}{width="85%" align="center"}

1. Defina o valor esperado para o atributo.

   ![](assets/1-1-table.png){zoomable="yes"}{width="85%" align="center"}

Esta é uma amostra de consulta em que um link de tabela foi selecionado diretamente. Os valores disponíveis para esta tabela devem ser selecionados em um seletor dedicado.

![](assets/1-1-table-direct.png){zoomable="yes"}{width="85%" align="center"}

+++

Para um link **1-N**, você pode definir subcondições para refinar sua consulta, como mostrado no exemplo abaixo.

+++Exemplo de consulta

Aqui, o query é direcionado a recipients que fizeram compras relacionadas ao produto BrewMaster, para um valor total de pelo menos 100$.

1. Selecione a tabela **Compras** e confirme.

   ![](assets/1-N-collection.png){zoomable="yes"}{width="50%" align="center"}

1. Uma transição de saída é adicionada, permitindo criar subcondições.

   ![](assets/1-n-subcondition.png){zoomable="yes"}{width="85%" align="center"}

1. Selecione o atributo **Preço** e direcione compras de US$ 1000 ou mais

   ![](assets/1-n-price.png){zoomable="yes"}{width="85%" align="center"}

1. Adicione subcondições para atender às suas necessidades. Aqui adicionamos uma condição aos perfis do público-alvo que compraram um produto BrewMaster.

   ![](assets/custom-condition-1-N.png){zoomable="yes"}{width="85%" align="center"}

+++

#### Trabalhar com dados agregados {#aggregate}

As condições personalizadas permitem executar operações agregadas. Para fazer isso, você precisa selecionar diretamente um atributo de uma tabela de coleção:

1. Navegue dentro da tabela de coleção desejada e selecione o atributo no qual deseja executar uma operação agregada.

   ![](assets/aggregate-attribute.png){zoomable="yes"}{width="85%" align="center"}

1. No painel de propriedades, alterne a opção **Aggregate data** e selecione a função de agregação desejada.

   ![](assets/aggregate.png){zoomable="yes"}{width="85%" align="center"}

### Selecionar um público-alvo {#audiences}

>[!CONTEXTUALHELP]
>id="dc_orchestration_querymodeler_selectaudience"
>title="Selecionar público-alvo"
>abstract="A opção **Selecionar público-alvo** permite escolher o público-alvo pelo qual deseja filtrar a sua consulta."

Para filtrar sua query usando um público existente, siga estas etapas:

1. Clique no botão **+** no nó desejado e escolha **[!UICONTROL Selecionar público-alvo]**.

1. O painel de propriedades **Selecionar público-alvo** é aberto no lado direito. Escolha o público-alvo que deseja usar para filtrar o query.

   *Exemplo de consulta retornando todos os perfis que pertencem ao público-alvo do &quot;Festival Goers&quot;:*

   ![](assets/query-audience.png){zoomable="yes"}

### Usar um filtro predefinido {#predefined-filters}

>[!CONTEXTUALHELP]
>id="dc_orchestration_querymodeler_predefinedfilter"
>title="Filtro predefinido"
>abstract="A opção **Filtro predefinido** permite selecionar um filtro predefinido na lista de filtros personalizados ou nos favoritos."

Para filtrar sua query usando um filtro predefinido, siga estas etapas:

1. Clique no botão **+** no nó desejado e selecione **[!UICONTROL Filtro predefinido]**.

1. O painel de propriedades **Filtro predefinido** é aberto no lado direito. Selecione um filtro predefinido na lista de filtros personalizados ou nos favoritos.

   *Exemplo de consulta retornando todos os perfis correspondentes ao filtro predefinido &quot;Clientes inativos&quot;:*

   ![](assets/query-predefined-filter.png){zoomable="yes"}

### Copiar e colar componentes {#copy}

O modelador de query permite copiar um ou vários componentes de filtragem e colá-los no final de uma transição. Essa operação pode ser executada na tela de consulta atual ou em qualquer tela na instância.

>[!NOTE]
>
>A seleção copiada é mantida enquanto você estiver trabalhando na instância. Se você fizer logoff e logon novamente, sua seleção não estará mais disponível para colagem.

Para copiar e colar componentes de filtragem, siga estas etapas:

1. Selecione o componente de filtragem que deseja copiar clicando nele na tela de consulta. Para selecionar vários componentes, use a ferramenta de seleção múltipla disponível na barra de ferramentas, localizada no canto superior direito da tela.

1. Clique no botão **[!UICONTROL Copiar]** no painel de propriedades do componente ou na faixa de opções azul na parte inferior da tela se tiver selecionado vários componentes.

   | Copiar um único componente | Copiar vários componentes |
   |  ---  |  ---  |
   | ![](assets/copy-single-component.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} | ![](assets/copy-multiple-components.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |

1. Para colar o(s) componente(s), clique no botão + no final da transição desejada e selecione **Colar n itens**.

   ![](assets/copy-paste.png){zoomable="yes"}

## Combinar componentes de filtragem com operadores {#operators}

>[!CONTEXTUALHELP]
>id="dc_orchestration_querymodeler_group"
>title="Grupo"
>abstract="Nesse painel, é possível alterar o operador usado para vincular as condições do filtro."

Sempre que um novo componente de filtragem é adicionado à consulta, ele é automaticamente vinculado ao outro componente por um operador **AND**. Isso significa que os resultados dos dois componentes de filtragem são combinados.

Neste exemplo, adicionamos novos componentes de filtragem do tipo público-alvo na segunda transição. O componente está vinculado à condição de filtro predefinida com um operador **AND**, o que significa que os resultados da consulta incluem destinatários direcionados pelo filtro predefinido &quot;Madridians&quot; E pertencentes ao público &quot;Discount hunters&quot;.

![](assets/query-operator.png){zoomable="yes"}

Para alterar o operador usado para vincular as condições do filtro, clique nele e selecione o operador desejado no painel **Grupo** que será aberto no lado direito.

Os operadores disponíveis são:

* **AND (Interseção)**: combina resultados que correspondem a todos os componentes de filtragem nas transições de saída.
* **OR (União)**: inclui resultados que correspondem a pelo menos um dos componentes de filtragem nas transições de saída.
* **EXCETO (Exclusão)**: exclui resultados que correspondem a todos os componentes de filtragem na transição de saída.

![](assets/query-operator-change.png){zoomable="yes"}

Além disso, você pode criar grupos intermediários de componentes clicando no botão **+** em uma transição. Isso permite adicionar um operador nesse local específico para agrupar vários componentes e refinar sua consulta.

No exemplo abaixo, criamos um grupo intermediário para incluir resultados dos públicos &quot;VIP para recompensar&quot; ou &quot;Super VIP&quot;.

![](assets/query-intermediate-group.png){zoomable="yes"}

## Verificar e validar sua consulta

>[!CONTEXTUALHELP]
>id="dc_orchestration_querymodeler_ruleproperties"
>title="Propriedades da regra"
>abstract="Depois de criar a consulta na tela, é possível verificá-la usando o painel **Propriedades da regra** localizado no lado direito.<br/>Esse painel permite exibir os dados resultantes, recuperar uma versão de código SQL da consulta e verificar o número de registros direcionados.<br/>Use o botão **Selecionar ou salvar filtro** para salvar sua consulta como um filtro predefinido ou substituir o conteúdo da tela por um filtro."

Depois de criar a consulta na tela, você pode verificá-la usando o painel **Propriedades da regra**, localizado no lado direito. Este painel é exibido ao criar uma consulta para criar um público-alvo. As operações disponíveis são:

* **Exibir resultados:** Exibe os dados resultantes da sua consulta.
* **Visualização de código**: exibe uma versão baseada em código da consulta no SQL.
* **Calcular**: atualiza e exibe o número de registros direcionados por sua consulta.
* **Selecionar ou salvar filtro**: escolha um filtro predefinido existente para usar na tela ou salve sua consulta como um filtro predefinido para reutilização futura.

  >[!IMPORTANT]
  >
  >Selecione um filtro predefinido no painel de propriedades Regra para substituir a consulta criada na tela pelo filtro selecionado.

Quando a consulta estiver pronta, clique no botão **[!UICONTROL Confirmar]** no canto superior direito para salvá-la.

Você pode modificar sua query a qualquer momento abrindo-a. Lembre-se de que, ao abrir uma consulta existente, ela é exibida em uma exibição simplificada, sem a visibilidade dos botões **+**. Para adicionar novos elementos à consulta, selecione um componente ou operador na tela para exibir os botões **+**.

![](assets/edit-audience.png){zoomable="yes"}
