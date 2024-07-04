---
audience: end-user
title: Usar a atividade de reconciliação
description: Saiba como usar a atividade de Reconciliação
source-git-commit: b21306cefe6e9e66263012110a7f89f2d92b38a5
workflow-type: tm+mt
source-wordcount: '534'
ht-degree: 41%

---


# Reconciliação {#reconciliation}

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation"
>title="Atividade de reconciliação"
>abstract="A variável **Reconciliação** A atividade permite definir o vínculo entre os dados no banco de dados e os dados em uma tabela de trabalho."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_field"
>title="Campo de seleção de reconciliação"
>abstract="Campo de seleção de reconciliação"

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_condition"
>title="Condição de criação de reconciliação"
>abstract="Condição de criação de reconciliação"

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_complement"
>title="Complemento de geração de reconciliação"
>abstract="Complemento de geração de reconciliação"

A variável **Reconciliação** A atividade permite definir o link entre os dados no banco de dados e os dados em uma tabela de trabalho, por exemplo, dados carregados de um sistema externo.

<!--For example, the **Reconciliation** activity can be placed after a **Load file** activity to import non-standard data into the database. In this case, the **Reconciliation** activity lets you define the link between the data in the Adobe Campaign database and the data in the work table.-->

## Práticas recomendadas {#reconciliation-best-practices}

Embora a **Enriquecimento** atividade de permite definir dados adicionais para processar em sua composição (você pode usar uma **Enriquecimento** para combinar dados provenientes de vários conjuntos ou para criar links para um recurso temporário), a variável **Reconciliação** A atividade permite vincular dados não identificados aos recursos existentes.

>[!NOTE]
>A operação de reconciliação implica que os dados das dimensões vinculadas já estão no banco de dados.  Por exemplo, se você importar um arquivo de compras que mostre qual produto foi comprado, em que momento, por qual cliente, etc., o produto e o cliente já deverão existir no banco de dados.

## Configurar a atividade de reconciliação {#reconciliation-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_targeting"
>title="Dimensão de direcionamento"
>abstract="Selecione a nova dimensão de direcionamento. Uma dimensão permite definir a população direcionada: destinatários, assinantes de aplicativos, operadores, assinantes etc. Por padrão, a dimensão de direcionamento atual é selecionada."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_rules"
>title="Regras de reconciliação"
>abstract="Selecione as regras de reconciliação a serem usadas para a desduplicação. Para usar atributos, selecione a opção **Atributos simples** e escolha os campos origem e destino. Para criar sua própria condição de reconciliação usando o modelador de consultas, selecione a opção **Condições de reconciliação avançadas**."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_targeting_selection"
>title="Selecione a dimensão de direcionamento"
>abstract="Selecione a dimensão de direcionamento com a qual seus dados de entrada devem se reconciliar."

>[!CONTEXTUALHELP]
>id="dc_orchestration_keep_unreconciled_data"
>title="Manter dados não reconciliados"
>abstract="Por padrão, os dados não reconciliados são mantidos na transição de saída e disponibilizados na tabela de trabalho para uso futuro. Para remover dados não reconciliados, desative a opção **Manter dados não reconciliados**."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_attribute"
>title="Atributo de reconciliação"
>abstract="Selecione o atributo a ser usado para reconciliar dados e confirme."

Siga estas etapas para configurar o **Reconciliação** atividade:

1. Adicionar um **Reconciliação** atividade na sua composição. <!--This activity should be added following a transition containing a population whose targeting dimension does not directly come from Adobe Campaign. -->

1. Selecione a nova dimensão de direcionamento. Uma dimensão permite definir a população direcionada: recipients, assinantes de aplicativos, operadores, assinantes, etc. <!--[Learn more about targeting dimensions](../../audience/about-recipients.md#targeting-dimensions).-->

1. Selecione os campos a serem usados para a reconciliação. É possível usar um ou mais critérios de reconciliação.

   1. Para usar atributos para reconciliar dados, selecione o **Atributos simples** opção. A variável **Source** field lista os campos disponíveis na transição de entrada, que devem ser reconciliados. A variável **Destino** field corresponde aos campos da targeting dimension selecionada. Os dados são reconciliados quando a origem e o destino são iguais. Por exemplo, selecione a variável **E-mail** para desduplicar perfis com base em seus endereços de email.

      Para adicionar outro critério de reconciliação, clique no link **Adicionar regra** botão. Se várias condições de associação forem especificadas, TODAS elas deverão ser verificadas para que os dados possam ser vinculados.

   <!--     ![](../assets/workflow-reconciliation-criteria.png)-->

   1. Para usar outros atributos para reconciliar dados, selecione o **Condições de reconciliação avançadas** opção. Em seguida, você pode criar sua própria condição de reconciliação usando o modelador de consultas. <!--[Learn how to work with the query modeler](../../query/query-modeler-overview.md).-->

1. É possível filtrar dados para reconciliar usando o **Criar filtro** botão. Isso permite criar uma condição personalizada usando o modelador de consultas. <!--[Learn how to work with the query modeler](../../query/query-modeler-overview.md)-->

Por padrão, os dados não reconciliados são mantidos na transição de saída e disponibilizados na tabela de trabalho para uso futuro. Para remover dados não reconciliados, desative a opção **Manter dados não reconciliados**.

<!--
## Example {#reconciliation-example}

The following example demonstrates a workflow that creates an audience of profiles directly from an imported file containing new clients. It is made up of the following activities:

The workflow is designed as follows:

![](../assets/workflow-reconciliation-sample-1.0.png)

 
It is built with the following activities:

* A [Load file](load-file.md) activity uploads a file containing profiles data that were extracted from an external tool.

    For example:

    ```
    lastname;firstname;email;birthdate;
    JACKMAN;Megan;megan.jackman@testmail.com;07/08/1975;
    PHILLIPS;Edward;phillips@testmail.com;09/03/1986;
    WEAVER;Justin;justin_w@testmail.com;11/15/1990;
    MARTIN;Babe;babeth_martin@testmail.net;11/25/1964;
    REESE;Richard;rreese@testmail.com;02/08/1987;
    ```

* A **Reconciliation** activity which identifies the incoming data as profiles, by using the **email** and **Date of birth** fields as reconciliation criteria.

    ![](../assets/workflow-reconciliation-sample-1.1.png)

* A [Save audience](save-audience.md) activity to create a new audience based on these updates. You can also replace the **Save audience** activity by an **End** activity if no specific audience needs to be created or updated. Recipient profiles are updated in any case when you run the workflow.


## Compatibility {#reconciliation-compat}

The **Reconciliation** activity does not exist in the Client console. All **Enrichments** activities created in the Client console with the reconciliation options enabled are displayed as **Reconciliation** activities in Campaign Web user interface.
-->
