---
audience: end-user
title: Introdução a esquemas
description: Saiba como começar com esquemas
badge: label="Disponibilidade limitada" type="Informative"
source-git-commit: 883ba223f6c78783fae9f6c9617daa1a7e6635de
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 34%

---

# Introdução a esquemas {#schemas}


>[!CONTEXTUALHELP]
>id="dc_schema_create_select_tables"
>title="Selecionar tabelas"
>abstract="Selecione as tabelas a serem adicionadas para o modelo de dados."

>[!CONTEXTUALHELP]
>id="dc_schema_create_key"
>title="Chave"
>abstract="Selecione uma chave para reconciliação de dados."

>[!CONTEXTUALHELP]
>id="dc_schema_create_schema_name"
>title="Nome do esquema"
>abstract="Insira o nome do esquema."


>[!CONTEXTUALHELP]
>id="dc_schema_edit_description"
>title="Descrição do esquema"
>abstract="A descrição do esquema lista colunas, tipos e rótulos. Você também pode verificar a chave de reconciliação do esquema. Para atualizar a definição do esquema, clique no ícone de lápis."

>[!CONTEXTUALHELP]
>id="dc_schema_filter_sources"
>title="Selecione o banco de dados de origem a ser filtrado"
>abstract="Você pode filtrar os esquemas com base em sua origem. Selecione um ou vários Bancos de dados federados para exibir seus esquemas."


## O que é um esquema? {#schema-start}

Um esquema é um objeto no aplicativo que define como os dados são vinculados às tabelas do banco de dados.
Um esquema faz referência a uma tabela.

## Criar um esquema {#schema-create}

Na seção **[!UICONTROL DADOS FEDERADOS]**, acesse o link **[!UICONTROL Modelos]**. Você encontrará a guia **[!UICONTROL Esquema]**.
Clique no botão **[!UICONTROL Criar esquema]**.

![](assets/schema_create.png){zoomable="yes"}

Selecione o banco de dados de origem na lista suspensa e clique na guia **[!UICONTROL Adicionar tabelas]**

![](assets/schema_tables.png){zoomable="yes"}

Você terá acesso a todas as tabelas no banco de dados e para as quais poderá criar um schema.

Ao adicionar as tabelas, você terá acesso aos campos delas e poderá gerenciar para manter o que realmente precisa.

![](assets/schema_fields.png){zoomable="yes"}

## Editar um esquema {#schema-edit}

Para editar um esquema, clique no nome do seu esquema na pasta schemas. Você terá acesso à página abaixo.
Clique no botão **[!UICONTROL Editar]**.

![](assets/schema_edit.png){zoomable="yes"}

## Visualizar dados em um esquema {#schema-preview}

Para visualizar os dados na tabela representada pelo esquema, vá para a guia **[!UICONTROL Dados]**, conforme abaixo.

![](assets/schema_data.png){zoomable="yes"}

Você pode alterar a Visão geral dos dados clicando no botão **[!UICONTROL Configurar colunas]**.

![](assets/schema_columns.png){zoomable="yes"}

## Excluir um esquema {#schema-delete}

Para excluir um esquema, clique no botão **[!UICONTROL Mais]** e depois **[!UICONTROL Excluir]**.

![](assets/schema_delete.png){zoomable="yes"}