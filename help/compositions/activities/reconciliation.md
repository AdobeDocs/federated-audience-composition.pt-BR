---
audience: end-user
title: Usar a atividade de reconciliação
description: Saiba como usar a atividade de Reconciliação
badge: label="Disponibilidade limitada" type="Informative"
exl-id: 933c3cba-9120-4a93-a668-866fb65ee197
source-git-commit: 682695357a9bd8f351b5152becd33088fa16f622
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 41%

---

# Reconciliação {#reconciliation}

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation"
>title="Atividade de reconciliação"
>abstract="A atividade **Reconciliação** permite definir o vínculo entre os dados no banco de dados os dados em uma tabela de trabalho."

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

A atividade **Reconciliation** permite definir o vínculo entre os dados no banco de dados e os dados em uma tabela de trabalho, por exemplo, dados carregados de um sistema externo.

<!--For example, the **Reconciliation** activity can be placed after a **Load file** activity to import non-standard data into the database. In this case, the **Reconciliation** activity lets you define the link between the data in the Adobe Campaign database and the data in the work table.-->

Ela permite vincular dados não identificados aos recursos existentes. A operação de reconciliação implica que os dados que você está unindo já estão no banco de dados. Por exemplo, se você deseja reconciliar as informações de compras mostrando qual produto foi comprado, em que momento, por qual cliente, etc., o produto e o cliente já devem existir no banco de dados.

## Configurar a atividade de reconciliação {#reconciliation-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_targeting"
>title="Esquema"
>abstract="Selecione o novo esquema a ser aplicado aos dados. Um esquema, também conhecido como dimensão de direcionamento, permite definir a população direcionada: destinatários, assinantes de aplicativos, operadores, assinantes etc. Por padrão, o esquema atual da composição está selecionado."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_rules"
>title="Regras de reconciliação"
>abstract="Selecione as regras de reconciliação a serem usadas para a desduplicação. Para usar atributos, selecione a opção **Atributos simples** e escolha os campos origem e destino. Para criar sua própria condição de reconciliação usando o modelador de consultas, selecione a opção **Condições de reconciliação avançadas**."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_targeting_selection"
>title="Selecione a dimensão de direcionamento"
>abstract="Selecione o esquema, também conhecido como dimensão de direcionamento, com o qual seus dados de entrada serão reconciliados."

>[!CONTEXTUALHELP]
>id="dc_orchestration_keep_unreconciled_data"
>title="Manter dados não reconciliados"
>abstract="Por padrão, os dados não reconciliados são mantidos na transição de saída e disponibilizados na tabela de trabalho para uso futuro. Para remover dados não reconciliados, desative a opção **Manter dados não reconciliados**."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_attribute"
>title="Atributo de reconciliação"
>abstract="Selecione o atributo a ser usado para reconciliar dados e confirme."

Siga estas etapas para configurar a atividade **Reconciliação**:

1. Adicione uma atividade de **Reconciliação** à sua composição.

1. Selecione o **Novo esquema**. Um esquema, também conhecido como targeting dimension, permite definir a população direcionada: recipients, assinantes de aplicativos, operadores, assinantes etc.

1. Selecione os campos a serem usados para a reconciliação. É possível usar um ou mais critérios de reconciliação.

   1. Para usar atributos para reconciliar dados, selecione a opção **Simple attributes** e clique no botão **Add rule**.
   1. Selecione os campos **Source** e **Destination** para a reconciliação. O campo **Source**. O campo **Destination** corresponde aos campos do esquema selecionado.

      Os dados são reconciliados quando a origem e o destino são iguais. Por exemplo, selecione os campos **Email** para desduplicar perfis com base em seus endereços de email.

      Para adicionar outro critério de reconciliação, clique no botão **Adicionar regra**. Se várias condições de associação forem especificadas, TODAS elas deverão ser verificadas para que os dados possam ser vinculados.

      ![](../assets/reconciliation-rules.png)

   1. Para usar outros atributos para reconciliar dados, selecione a opção **Condições avançadas de reconciliação** e clique no botão **Criar condições**. Em seguida, você pode criar sua própria condição de reconciliação usando o modelador de consultas. [Saiba como trabalhar com o modelador de consultas](../../query/query-modeler-overview.md)

      ![](../assets/reconciliation-advanced.png)

1. Você pode filtrar dados para reconciliar usando o botão **Criar filtro**. Isso permite criar uma condição personalizada usando o modelador de consultas.

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
