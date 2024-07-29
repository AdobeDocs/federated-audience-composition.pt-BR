---
audience: end-user
title: Usar a atividade de desduplicação
description: Saiba como usar a atividade de desduplicação
badge: label="Disponibilidade limitada" type="Informative"
exl-id: 55db2461-fcfb-4284-9ab7-7cb01071ed1c
source-git-commit: f549f1611bfe6deb6dc684e3a0d9c968ba7c184a
workflow-type: tm+mt
source-wordcount: '565'
ht-degree: 46%

---

# Desduplicação {#deduplication}

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_fields"
>title="Campos para identificar duplicatas"
>abstract="Na seção **[!UICONTROL Campos para identificar duplicatas]**, clique no botão **[!UICONTROL Adicionar atributo]** para especificar os campos nos quais os valores idênticos permitem a identificação de duplicatas, como: endereço de email, nome, sobrenome, etc. A ordem dos campos permite especificar os que devem ser processados primeiro."

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication"
>title="Atividade Desduplicação"
>abstract="A atividade **Desduplicação** permite excluir duplicatas nos resultados das atividades de entrada. Ela é usada principalmente após atividades de direcionamento e antes de atividades que permitem o uso de dados direcionados."

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_complement"
>title="Gerar um complemento"
>abstract="É possível gerar uma transição de saída adicional com a população restante, que foi excluída como uma duplicata. Para fazer isso, ative a opção **[!UICONTROL Gerar complemento]**"

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_settings"
>title="Configurações de desduplicação"
>abstract="Para excluir duplicatas nos dados recebidos, defina o método de desduplicação nos campos abaixo. Por padrão, somente um registro é mantido. Também é necessário selecionar o modo de desduplicação com base em uma expressão ou um atributo. Por padrão, o registro a ser mantido fora das duplicatas é selecionado aleatoriamente."

A atividade **Deduplication** permite excluir duplicados no(s) resultado(s) das atividades de entrada, por exemplo, perfis duplicados na lista de destinatários. A atividade **Deduplication** geralmente é usada após as atividades de direcionamento e antes das atividades que permitem o uso de dados direcionados.

## Configurar a atividade de desduplicação{#deduplication-configuration}

Siga estas etapas para configurar a atividade **Desduplicação**:

1. Adicione uma atividade **Deduplication** à sua composição.

1. Se a atividade tiver várias transições de entrada, selecione a transição a ser usada para executar a desduplicação na lista suspensa **[!UICONTROL Conjunto principal]**

1. Na seção **[!UICONTROL Campos para identificar duplicatas]**, clique no botão **[!UICONTROL Adicionar atributo]** para especificar os campos nos quais os valores idênticos permitem a identificação de duplicatas, como: endereço de email, nome, sobrenome, etc. A ordem dos campos permite especificar os que devem ser processados primeiro.

   ![](../assets/deduplication.png)

1. Na seção **[!UICONTROL Configurações de desduplicação]**, selecione o número de **[!UICONTROL Duplicatas exclusivas a serem mantidas]**. O valor padrão para este campo é **1**. O valor **0** permite manter todas as duplicatas.

   Por exemplo, se os registros A e B forem considerados duplicatas do registro Y, e um registro C for considerado uma duplicata do registro Z:

   * Se o valor do campo for **1**: somente os registros Y e Z serão mantidos.
   * Se o valor do campo for **0**: todos os registros são mantidos.
   * Se o valor do campo for **2**: os registros C e Z são mantidos e dois registros de A, B e Y são mantidos por acaso ou dependendo do método de desduplicação selecionado posteriormente.

1. Selecione o **[!UICONTROL Método de desduplicação]** a ser usado:

   * **[!UICONTROL Seleção aleatória]**: seleciona aleatoriamente o registro a ser mantido fora das duplicatas.
   * **[!UICONTROL Usando uma expressão]**: mantenha os registros nos quais o valor da expressão inserida é o menor ou o maior.
   * **[!UICONTROL Valores não vazios]**: mantém os registros para os quais a expressão não está vazia.
   * **[!UICONTROL Seguindo uma lista de valores]**: defina uma prioridade de valor para um ou mais campos. Para definir os valores, clique em **[!UICONTROL Atributo]** para selecionar um campo ou criar uma expressão e, em seguida, adicione o(s) valor(es) à tabela apropriada. Para definir um novo campo, clique no **[!UICONTROL botão Adicionar]** localizado acima da lista de valores.

1. Marque a opção **[!UICONTROL Gerar complemento]** se desejar explorar a população restante. O complemento consiste de todas as duplicatas. Uma transição adicional será adicionada à atividade.

<!--
## Example{#deduplication-example}

In the following example, use a deduplication activity to exclude duplicates from the target before sending a delivery. The identified duplicated profiles are added to a dedicated audience that can be reused if necessary. Choose the **Email** address to identify the duplicates. Keep 1 entry and select the **Random** deduplication method.

![](../assets/workflow-deduplication-example.png)
-->
