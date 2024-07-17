---
audience: end-user
title: Usar a atividade Criar público-alvo
description: Saiba como usar a atividade Criar público
badge: label="Disponibilidade limitada" type="Informative"
source-git-commit: 7a3d03543f6f903c3f7f66299b600807cf15de5e
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 40%

---


# Criar público-alvo {#build-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience"
>title="Atividade Criar público-alvo"
>abstract="A atividade **Criar público-alvo** permite definir o público-alvo que entrará na composição."

A atividade **Criar público-alvo** permite definir o público-alvo que entrará na composição.

Para definir o público-alvo, você pode:

<!--* Select an existing audience, created as a list in the client console.-->
* Selecionar um público-alvo da Adobe Experience Platform.
* Crie um novo público-alvo com o construtor do modelador de consultas definindo e combinando critérios de filtragem.

A atividade **Criar público-alvo** pode ser colocada no início da composição ou após qualquer outra atividade. Qualquer atividade pode ser colocada após a **Criar público-alvo**.

## Configurar a atividade Criar público-alvo {#build-audience-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience_audienceselector"
>title="Público-alvo"
>abstract="Selecione o público-alvo."

Siga estas etapas para configurar a atividade **Criar público-alvo**:

1. Adicione uma atividade **Criar público-alvo**.
1. Defina um rótulo.
1. Especifique se deseja criar um público-alvo ou selecione um existente.
1. Configure seu público seguindo as etapas detalhadas nas guias abaixo.

>[!BEGINTABS]

>[!TAB Criar público-alvo]

Para criar seu próprio público-alvo, siga estas etapas:

1. Selecione **Criar audiência**.
1. Escolha o **Esquema**, também conhecido como targeting dimension. O schema permite definir o público alvo da operação: recipients, beneficiários de contrato, operadores, assinantes, etc. Por padrão, o schema é selecionado dos recipients.
1. Clique em **Continuar**.
1. Use o modelador de consultas para definir sua consulta. [Saiba como trabalhar com o modelador de consultas](../../query/query-modeler-overview.md)

>[!TAB Ler público-alvo]

Para selecionar um público-alvo existente, siga estas etapas:

1. Selecione **Ler público-alvo**.
1. Clique em **Continuar**.
1. Selecione o público-alvo.

>[!ENDTABS]

<!--
## Examples{#build-audience-examples}

Here is an example of a workflow with two **Build audience** activities. The first one targets the poker players audience, followed by an email delivery. The second one targets the VIP clients audience, followed by an SMS delivery.

![](../assets/workflow-audience-example.png)
-->
