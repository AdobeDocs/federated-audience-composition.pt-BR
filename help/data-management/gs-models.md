---
audience: end-user
title: Introdução a modelos de dados
description: Saiba como começar a usar modelos de dados
exl-id: 8f9e9895-dcd7-4718-8922-4f7fefe9ed94
source-git-commit: 61a7b66d16358a4a1c3d4b2ae153e856d8f682f7
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 15%

---

# Introdução a modelos de dados {#data-model}

>[!CONTEXTUALHELP]
>id="dc_model_menu"
>title="Trabalhar com modelos"
>abstract="Esquemas e modelos de dados estão listados nesta tela. Você pode criar esquemas e modelos de dados com o botão **Criar**."

>[!CONTEXTUALHELP]
>id="dc_datamodel_add_schema"
>title="Selecionar esquemas"
>abstract="Selecione os esquemas para o modelo de dados."


>[!CONTEXTUALHELP]
>id="dc_datamodel_add_audience"
>title="Selecionar um público-alvo"
>abstract="Selecione o público-alvo para o modelo de dados."

>[!CONTEXTUALHELP]
>id="dc_datamodel_properties"
>title="Propriedades do modelo de dados"
>abstract="Insira o rótulo do modelo de dados."


## O que é um modelo de dados {#data-model-start}

Um modelo de dados é um conjunto de esquemas, públicos-alvo e links entre eles. É usado para federar públicos-alvo com dados de bancos de dados.

Saiba mais sobre [esquemas](../customer/schemas.md#schema-start).

Saiba mais sobre [públicos-alvo](../start/audiences.md).

Por exemplo, você pode ver abaixo uma representação de um modelo de dados : as tabelas com seu nome e os links entre elas.

![](assets/datamodel.png){zoomable="yes"}

Na Composição de público federado, é possível criar muitos modelos de dados.

A criação será baseada no caso de uso: você escolhe as tabelas necessárias e as vincula de acordo com suas necessidades.

## Criar um modelo de dados {#data-model-create}

Para criar um modelo de dados, siga estas etapas:

1. Na seção **[!UICONTROL Dados Federados]**, acesse o menu **[!UICONTROL Modelos]** e navegue até a guia **[!UICONTROL Modelo de Dados]**.

   Clique no botão **[!UICONTROL Criar modelo de dados]**.

   ![](assets/datamodel_create.png){zoomable="yes"}

1. Defina o nome do seu modelo de dados e clique no botão **[!UICONTROL Criar]**.

1. No painel do modelo de dados, clique em **[!UICONTROL Adicionar esquemas]** para escolher o esquema associado ao seu modelo de dados.

   ![](assets/datamodel_schemas.png){zoomable="yes"}

1. Clique em **[!UICONTROL Adicionar públicos-alvo]** para definir seus grupos-alvo.

1. Estabeleça conexões entre tabelas em seu modelo de dados para garantir relações de dados precisas. [Saiba mais](#data-model-links)

1. Após concluir a configuração, clique em **[!UICONTROL Salvar]** para aplicar as alterações.

## Criar links {#data-model-links}

Para criar links entre tabelas do seu modelo de dados, siga estas etapas:

1. Clique no menu **[!UICONTROL Criar link]** de uma das tabelas ou clique no botão **[!UICONTROL Criar links]** e escolha as duas tabelas:

   ![](assets/datamodel_createlinks.png){zoomable="yes"}

1. Preencha o formulário fornecido para definir o link.

   ![](assets/datamodel_link.png){zoomable="yes"}

   **Cardinalidade**

   * **1-N**: uma ocorrência da tabela de origem pode ter várias ocorrências correspondentes da tabela de destino, mas uma ocorrência da tabela de destino pode ter no máximo uma ocorrência correspondente da tabela de origem.

   * **N-1**: uma ocorrência da tabela de destino pode ter várias ocorrências correspondentes da tabela de origem, mas uma ocorrência da tabela de origem pode ter no máximo uma ocorrência correspondente da tabela de destino.

   * **1-1**: uma ocorrência da tabela de origem pode ter no máximo uma ocorrência correspondente da tabela de destino.

Todos os links definidos para seu modelo de dados estão listados abaixo:

![](assets/datamodel_alllinks.png){zoomable="yes"}

## Como fazer vídeo {#data-model-video}

Saiba como criar um modelo de dados neste vídeo:

>[!VIDEO](https://video.tv.adobe.com/v/3432020)
