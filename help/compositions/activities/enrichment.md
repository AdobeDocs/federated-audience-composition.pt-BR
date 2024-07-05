---
audience: end-user
title: Usar a atividade de enriquecimento
description: Saiba como usar a atividade de enriquecimento
source-git-commit: 4ba457f1dcd8b7997931a70d93a95f6a54c51cb5
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 26%

---


# Enriquecimento {#enrichment}

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment"
>title="Atividade Enriquecimento"
>abstract="A atividade **Enriquecimento** permite aprimorar os dados direcionados com informações adicionais do banco de dados. Normalmente é usada em uma composição após atividades de segmentação."

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_data"
>title="Atividade Enriquecimento"
>abstract="Depois que os dados de enriquecimento forem adicionados à composição, eles poderão ser usados nas atividades adicionadas após a **Enriquecimento** atividade para segmentar perfis em grupos distintos com base em seus comportamentos, preferências e opções."

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_simplejoin"
>title="Definição de link"
>abstract="Crie um link entre os dados da tabela de trabalho e o banco de dados federado."

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_reconciliation"
>title="Reconciliação de enriquecimento"
>abstract="Defina os parâmetros de reconciliação."

>[!CONTEXTUALHELP]
>id="dc_targetdata_personalization_enrichmentdata"
>title="Dados de enriquecimento"
>abstract="Selecione os dados a serem usados para enriquecer sua composição. Você pode selecionar dois tipos de dados de enriquecimento: um único atributo de enriquecimento do schema, também conhecido como targeting dimension, ou um link de coleção, que é um link com uma cardinalidade 1-N entre as tabelas."

A variável **Enriquecimento** A atividade permite aprimorar os dados direcionados com informações adicionais do banco de dados federado. Normalmente, é usado em composições após atividades de segmentação.

Os dados de Enriquecimento podem vir:

* **Da mesma tabela de trabalho** como o direcionado para sua composição:

  *Direcione um grupo de clientes e adicione o campo &quot;Data de nascimento&quot; à tabela de trabalho atual*.

* **De outra tabela de trabalho**:

  *Direcione um grupo de clientes e adicione os campos &quot;Quantidade&quot; e &quot;Tipo de produto&quot; da tabela &quot;Compra&quot;*.

Após os dados de enriquecimento terem sido adicionados à composição, eles poderão ser usados nas atividades adicionadas após a **Enriquecimento** atividade para segmentar clientes em grupos distintos com base em seus comportamentos, preferências e opções.

<!--For instance, you can add to the working table information related to customers' purchases and use this data to personalize emails with their latest purchase or the amount spent on these purchases.-->

## Configurar a atividade de enriquecimento {#enrichment-configuration}

Siga estas etapas para configurar a atividade **Enriquecimento**:

1. Adicione atividades como **Criar público-alvo** e **Combinar**.
1. Adicione uma atividade **Enriquecimento**

   ![](../assets/enrichment.png)

1. Se várias transições tiverem sido configuradas na sua composição, você poderá usar o **[!UICONTROL Conjunto principal]** para definir qual transição deve ser usada como conjunto principal para enriquecer com dados.

1. Clique em **Adicionar dados de enriquecimento** e selecione o atributo a ser usado para enriquecer os dados.

   ![](../assets/enrichment-add.png)

   >[!NOTE]
   >
   >A variável **Botão Editar expressão** na tela seleção de atributo, você pode criar expressões avançadas para selecionar o atributo.

<!--PAS VU SUR INSTANCE: You can select two types of enrichment data: a single enrichment attribute from the target dimension, or a collection link. Each of these types is detailed in the examples below:

    * [Single enrichment attribute](#single-attribute)
    * [Collection lnk](#collection-link)-->

## Exemplos {#example}

### Atributo único de enriquecimento {#single-attribute}

Nesse caso, estamos apenas adicionando um atributo único de enriquecimento, por exemplo, a data de nascimento. Siga estas etapas:

1. Clique no campo **Atributo**.
1. Selecione um campo simples do esquema, também conhecido como targeting dimension, a data de nascimento em nosso exemplo.
1. Clique em **Confirmar**.

<!--### Collection link {#collection-link}

In this more complex use case, we will select a collection link which is a link with a 1-N cardinality between tables. Let's retrieve the three latest purchases that are less than 100$. For this you need to define:

* an enrichment attribute: the **Total amount** field
* the number of lines to retrieve: 3
* a filter: filter out items that are greater than 100$
* a sorting: descendant sorting on the **Order date** field. 

#### Add the attribute {#add-attribute}

This is where you select the collection link to use as enrichment data.

1. Click inside the **Attribute** field.
1. Click **Display advanced attributes**.
1. Select the **Total amount** field from the **Purchases** table. 

#### Define the collection settings{#collection-settings}

Then, define how the data is collected and the number of records to retrieve.

1. Select **Collect data** in the **Select how the data is collected** drop-down.
1. Type "3" in the **Lines to retrieve (Columns to create)** field. 

If you want, for example, to get the average amount of purchases for a customer, select **Aggregated data** instead, and select **Average** in the **Aggregate function** drop-down.

#### Define the filters{#collection-filters}

Here, we define the maximum value for the enrichment attribute. We filter out items that are greater than 100$. [Learn how to work with the query modeler](../../query/query-modeler-overview.md)

1. Click **Edit filters**.
1. Add the two following filters: **Total amount** exists AND **Total amount** is less than 100. The first one filters NULL values as they would appear as the greatest value.
1. Click **Confirm**.

#### Define the sorting{#collection-sorting}

We now need to apply sorting in order to retrieve the three **latest** purchases.

1. Activate the **Enable sorting** option.
1. Click inside the **Attribute** field.
1. Select the **Order date** field.
1. Click **Confirm**. 
1. Select **Descending** from the **Sort** drop-down.-->
