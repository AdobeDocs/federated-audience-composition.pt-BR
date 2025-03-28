---
audience: end-user
title: Usar a atividade Change dimension
description: Saiba como usar a atividade Change dimension
exl-id: e71017bd-6d2f-4ace-b2d9-cbfbb537d127
source-git-commit: 65052ffcd8c70817aa428bea7f8b6baa0a49a1b0
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 42%

---

# Mudar dimensão {#change-dimension}

>[!CONTEXTUALHELP]
>id="dc_orchestration_dimension_complement"
>title="Gerar um complemento"
>abstract="É possível gerar uma transição de saída adicional com a população restante, que foi excluída como uma duplicata. Para fazer isso, ative a opção **[!UICONTROL Gerar complemento]**"

>[!CONTEXTUALHELP]
>id="dc_orchestration_change_dimension"
>title="Atividade Mudar dimensão"
>abstract="Esta atividade permite alterar o esquema, também conhecido como dimensão de direcionamento, à medida que você constrói um público-alvo. Ela desloca o eixo dependendo do modelo de dados e do esquema de entrada. Por exemplo, você pode mudar do esquema “contratos” para o esquema “clientes”."

A atividade **Alterar dimensão** permite alterar o esquema, também conhecido como targeting dimension, à medida que você constrói seu público-alvo. Ele desloca o eixo dependendo do template de dados e do schema de entrada.

## Configurar a atividade Change dimension {#configure}

Siga estas etapas para configurar a atividade **Alterar dimensão**:

1. Adicione uma atividade **Change dimension** à sua composição.

   ![](../assets/change-dimension.png)

1. Defina o **Novo esquema**. Durante a alteração do schema, todos os registros são mantidos.

1. Execute a composição para visualizar o resultado. Compare os dados nas tabelas antes e depois da atividade **Change dimension** e compare a estrutura das tabelas de composição.

<!--
## Example {#example}

In this example, we want to send an SMS delivery to all the profiles who have made a purchase. To do this, we first use a **[!UICONTROL Build audience]** activity linked to a custom "Purchase" targeting dimension to target all purchases that occurred.

We then use a **[!UICONTROL Change dimension]** activity to switch the workflow targeting dimension to "Recipients". This allows us to be able to target the recipients who match the query.
-->

