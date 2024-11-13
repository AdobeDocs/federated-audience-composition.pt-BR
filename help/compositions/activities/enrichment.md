---
audience: end-user
title: Usar a atividade de enriquecimento
description: Saiba como usar a atividade de enriquecimento
exl-id: 6bf12c25-fbef-4588-89d0-28215cbcbf58
source-git-commit: 65052ffcd8c70817aa428bea7f8b6baa0a49a1b0
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 48%

---

# Enriquecimento {#enrichment}

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment"
>title="Atividade Enriquecimento"
>abstract="A atividade **Enriquecimento** permite aprimorar os dados direcionados com informações adicionais do banco de dados. Normalmente, ela é usada em uma composição após atividades de segmentação."

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_data"
>title="Atividade Enriquecimento"
>abstract="Após a sua adição na composição, os dados de enriquecimento podem ser usados nas atividades adicionadas posteriormente à atividade **Enriquecimento** para segmentar perfis em grupos distintos com base em seus comportamentos, preferências e escolhas."

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
>abstract="Selecione os dados a serem usados para enriquecer a sua composição. Você pode selecionar dois tipos de dados de enriquecimento: um único atributo de enriquecimento do esquema, também conhecido como dimensão de direcionamento, ou um link de coleção, que é um link com cardinalidade 1-N entre tabelas."

A atividade **Enrichment** permite aprimorar os dados direcionados com informações adicionais do banco de dados federado. Normalmente, ela é usada em uma composição após atividades de segmentação.

Se você tiver configurado uma conexão com o destino Federated Audience Composition, poderá usar a atividade Enrichment para enriquecer dados que vêm do Adobe Experience Platform com atributos do banco de dados externo. [Saiba como enriquecer públicos do Adobe Experience Platform com dados externos](../../connections/destinations.md)

Os dados de Enriquecimento podem vir:

* **Da mesma tabela de trabalho** que a direcionada para a sua composição:

  *Direcione um grupo de clientes e adicione o campo &quot;Data de nascimento&quot; à tabela de trabalho atual*.

* **De outra tabela de trabalho**:

  *Direcione um grupo de clientes e adicione os campos &quot;Quantidade&quot; e &quot;Tipo de produto&quot; da tabela &quot;Compra&quot;*.

Após adicionar os dados de enriquecimento à composição, eles poderão ser usados nas atividades adicionadas após a atividade **Enriquecimento** para segmentar os clientes em grupos distintos com base em seus comportamentos, preferências e opções.

<!--For instance, you can add to the working table information related to customers' purchases and use this data to personalize emails with their latest purchase or the amount spent on these purchases.-->

## Configurar a atividade de enriquecimento {#enrichment-configuration}

Siga estas etapas para configurar a atividade **Enriquecimento**:

1. Adicione atividades como **Criar público-alvo** e **Combinar**.
1. Adicione uma atividade **Enriquecimento**

   ![](../assets/enrichment.png)

1. Se várias transições tiverem sido configuradas na sua composição, você poderá usar o campo **[!UICONTROL Conjunto principal]** para definir qual transição deve ser usada como conjunto principal para enriquecer com dados.

1. Clique em **Adicionar dados de enriquecimento** e selecione o atributo a ser usado para enriquecer os dados.

   ![](../assets/enrichment-add.png)

   >[!NOTE]
   >
   >O **botão Editar expressão** na tela de seleção de atributo permite criar expressões avançadas para selecionar o atributo.

<!--PAS VU SUR INSTANCE: You can select two types of enrichment data: a single enrichment attribute from the target dimension, or a collection link. Each of these types is detailed in the examples below:

    * [Single enrichment attribute](#single-attribute)
    * [Collection lnk](#collection-link)-->

<!--
## Examples {#example}

### Single enrichment attribute {#single-attribute}

Here, we are just adding a single enrichment attribute, for example, the date of birth. Follow these steps:

1. Click inside the **Attribute** field.
1. Select a simple field from the schema, also known as targeting dimension, the date of birth in our example. 
1. Click **Confirm**.
-->
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
