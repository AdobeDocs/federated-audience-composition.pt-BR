---
audience: end-user
title: Usar a atividade Criar público-alvo
description: Saiba como usar a atividade Criar público
source-git-commit: 4ba457f1dcd8b7997931a70d93a95f6a54c51cb5
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 37%

---


# Criar público-alvo {#build-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience"
>title="Atividade criar público-alvo"
>abstract="A variável **Criar público-alvo** A atividade permite definir o público-alvo que entrará na composição."

A variável **Criar público-alvo** A atividade permite definir o público-alvo que entrará na composição.

Para definir o público-alvo, você pode:

<!--* Select an existing audience, created as a list in the client console.-->
* Selecionar um público-alvo da Adobe Experience Platform.
* Crie um novo público-alvo com o construtor do modelador de consultas definindo e combinando critérios de filtragem.

A variável **Criar público-alvo** A atividade pode ser colocada no início da composição ou após qualquer outra atividade. Qualquer atividade pode ser colocada após a variável **Criar público-alvo**.

## Configurar a atividade Criar público-alvo {#build-audience-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience_audienceselector"
>title="Público-alvo"
>abstract="Selecione seu público."

Siga estas etapas para configurar a atividade **Criar público-alvo**:

1. Adicione uma atividade **Criar público-alvo**.
1. Defina um rótulo.
1. Defina o tipo de público-alvo: **Crie o seu próprio** ou **Ler público-alvo**.
1. Configure seu público seguindo as etapas detalhadas nas guias abaixo.

>[!BEGINTABS]

>[!TAB Crie o seu próprio (consulta)]

Para criar sua própria query, siga estas etapas:

1. Selecione **Crie sua própria (consulta)**.
1. Escolha a **Dimensão de direcionamento**. O targeting dimension permite definir a população-alvo da operação: destinatários, beneficiários(as) de contrato, operadores(as), assinantes, etc. Por padrão, o target é selecionado dos recipients.<!-- [Learn more about targeting dimensions](../../audience/about-recipients.md#targeting-dimensions)-->
1. Clique em **Continuar**.
1. Use o modelador de consultas para definir seu query, da mesma forma que você cria um público-alvo ao criar um novo email. <!--[Learn how to work with the query modeler](../../query/query-modeler-overview.md)-->

>[!TAB Ler público-alvo]

Para selecionar um público-alvo existente, siga estas etapas:

1. Selecione **Ler público-alvo**.
1. Clique em **Continuar**.
1. Selecione seu público, da mesma forma que você usa um público ao criar um novo delivery. <!--Refer to this [section](../../audience/add-audience.md).-->

>[!ENDTABS]

<!--
## Examples{#build-audience-examples}

Here is an example of a workflow with two **Build audience** activities. The first one targets the poker players audience, followed by an email delivery. The second one targets the VIP clients audience, followed by an SMS delivery.

![](../assets/workflow-audience-example.png)
-->
