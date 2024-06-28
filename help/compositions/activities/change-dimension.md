---
audience: end-user
title: Usar a atividade Change dimension
description: Saiba como usar a atividade Change dimension
source-git-commit: 92d4a7cf1414ae74b2684619d295eca065a92ce2
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 41%

---

# Mudar dimensão {#change-dimension}

>[!CONTEXTUALHELP]
>id="dc_orchestration_dimension_complement"
>title="Gerar um complemento"
>abstract="É possível gerar uma transição de saída adicional com a população restante, que foi excluída como uma duplicata. Para fazer isso, ative a opção **Gerar complemento**"

>[!CONTEXTUALHELP]
>id="dc_orchestration_change_dimension"
>title="Atividade Mudar dimensão"
>abstract="Essa atividade permite alterar o targeting dimension à medida que você constrói um público-alvo. Ela desloca o eixo dependendo do modelo de dados e da dimensão de entrada. Por exemplo, você pode mudar da dimensão “contratos” para a dimensão “clientes”."

A variável **Alterar dimensão** A atividade permite alterar o targeting dimension à medida que você constrói seu público-alvo. Ele desloca o eixo dependendo do template de dados e da dimensão de entrada. <!--[Learn more on targeting dimensions](../../audience/about-recipients.md#targeting-dimensions)-->


## Configurar a atividade Change dimension {#configure}

Siga estas etapas para configurar o **Alterar dimensão** atividade:

1. Adicionar um **Alterar dimensão** atividade para sua composição.

1. Defina o **Nova dimensão de destino**. Durante a alteração de dimensão, todos os registros são mantidos.

1. Execute a composição para visualizar o resultado. Compare os dados nas tabelas antes e depois da atividade de alteração de dimensão e compare a estrutura das tabelas de composição.

<!--
## Example {#example}

In this example, we want to send an SMS delivery to all the profiles who have made a purchase. To do this, we first use a **[!UICONTROL Build audience]** activity linked to a custom "Purchase" targeting dimension to target all purchases that occurred.

We then use a **[!UICONTROL Change dimension]** activity to switch the workflow targeting dimension to "Recipients". This allows us to be able to target the recipients who match the query.
-->
