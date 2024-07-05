---
audience: end-user
title: Usar a atividade Change dimension
description: Saiba como usar a atividade Change dimension
source-git-commit: 4ba457f1dcd8b7997931a70d93a95f6a54c51cb5
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 18%

---


# Mudar dimensão {#change-dimension}

>[!CONTEXTUALHELP]
>id="dc_orchestration_dimension_complement"
>title="Gerar um complemento"
>abstract="É possível gerar uma transição de saída adicional com a população restante, que foi excluída como uma duplicata. Para fazer isso, ative a opção **Gerar complemento**"

>[!CONTEXTUALHELP]
>id="dc_orchestration_change_dimension"
>title="Atividade Mudar dimensão"
>abstract="Essa atividade permite alterar o esquema, também conhecido como targeting dimension, conforme você cria um público-alvo. Ele desloca o eixo dependendo do template de dados e do schema de entrada. Por exemplo, você pode alternar do schema &quot;contratos&quot; para o schema &quot;clientes&quot;."

A variável **Alterar dimensão** A atividade permite alterar o esquema, também conhecido como targeting dimension, à medida que você constrói seu público-alvo. Ele desloca o eixo dependendo do template de dados e do schema de entrada.

## Configurar a atividade Change dimension {#configure}

Siga estas etapas para configurar o **Alterar dimensão** atividade:

1. Adicionar um **Alterar dimensão** atividade para sua composição.

   ![](../assets/change-dimension.png)

1. Defina o **Novo esquema**. Durante a alteração do schema, todos os registros são mantidos.

1. Execute a composição para visualizar o resultado. Comparar os dados nas tabelas antes e depois da variável **Alterar dimensão** atividade e comparar a estrutura das tabelas de composição.

<!--
## Example {#example}

In this example, we want to send an SMS delivery to all the profiles who have made a purchase. To do this, we first use a **[!UICONTROL Build audience]** activity linked to a custom "Purchase" targeting dimension to target all purchases that occurred.

We then use a **[!UICONTROL Change dimension]** activity to switch the workflow targeting dimension to "Recipients". This allows us to be able to target the recipients who match the query.
-->



<!-- on parle de dimension, mais dans UI "schema", va rester comme ça ?-->