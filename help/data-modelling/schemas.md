---
audience: end-user
title: Introdução a esquemas
description: Saiba como começar com esquemas
exl-id: 2c939185-f1c1-4f2b-ae1b-e2539e121eff
source-git-commit: 9b951f74443ac149e837c3f52ca265acabd407b9
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 16%

---

# Visão geral dos esquemas {#schemas}

>[!AVAILABILITY]
>
>Para acessar esquemas, você precisará de uma das seguintes permissões:
>
>-**Gerenciar Esquema Federado**
>-**Exibir Esquema Federado**
>
>Para mais informações sobre as permissões exigidas, leia o [guia de controle de acesso](/help/governance-privacy-security/access-control.md).

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
>abstract="A descrição do esquema lista colunas, tipos e rótulos. Você também pode verificar a chave de reconciliação do esquema. Para atualizar a definição do schema, selecione o ícone de lápis."

>[!CONTEXTUALHELP]
>id="dc_schema_filter_sources"
>title="Selecione o banco de dados de origem a ser filtrado"
>abstract="Você pode filtrar os esquemas com base em sua origem. Selecione um ou vários Bancos de dados federados para exibir seus esquemas."

Um schema é uma representação de uma tabela do banco de dados. É um objeto dentro do aplicativo que define como os dados são vinculados às tabelas do banco de dados.

Ao criar um esquema, você pode definir uma representação da tabela na Composição do público-alvo federado do Experience Platform:

* Dê a ele um nome e uma descrição amigáveis para simplificar a compreensão do usuário
* Decidir a visibilidade de cada campo, de acordo com seu uso real
* Selecione sua chave primária para vincular esquemas entre elas, conforme necessário no [modelo de dados](../data-modelling/models.md#data-model-start)

>[!CAUTION]
>
>Ao conectar várias sandboxes com o mesmo banco de dados, você deve usar esquemas de trabalho distintos.

## Criar um esquema {#schema-create}

Para criar um esquema na Composição de Público Federado, selecione **[!UICONTROL Modelos]** na seção **[!UICONTROL Dados Federados]**. Na guia **[!UICONTROL Esquema]**, selecione **[!UICONTROL Criar esquema]**.

![O botão Criar esquema está realçado na seção de esquema Composição de Público-Alvo Federado.](assets/schemas/schema_create.png){zoomable="yes"}

O popover **[!UICONTROL Selecionar banco de dados federado]** é exibido. Neste pop-over, você pode selecionar o [banco de dados de origem](/help/connections/home.md), seguido de **[!UICONTROL Próximo]**.


![](assets/schemas/schema_tables.png){zoomable="yes"}

O popover **Selecionar tabela** é exibido. Nesse popover, é possível selecionar as tabelas que deseja usar para criar o schema.

![O popover Selecionar tabela é exibido.](assets/schemas/select-table.png){zoomable="yes"}

Cada tabela selecionada gera um esquema com as colunas escolhidas. Para cada tabela, você pode alterar o rótulo do esquema, adicionar uma descrição, renomear o rótulo do campo, definir a visibilidade do rótulo do campo e selecionar a chave primária do esquema.

![](assets/schemas/schema-fields.png){zoomable="yes"}

>[!NOTE]
>
>Se você habilitar **[!UICONTROL Usar Chave Composta]**, mas selecionar apenas uma chave a ser usada, ela será tratada como uma chave primária de esquema padrão.

Além disso, você pode criar uma chave composta de várias colunas de esquema. Ative **[!UICONTROL Usar chave composta]** e marque as chaves que deseja usar como sua chave composta.

![](assets/schemas/composite-key.png){zoomable="yes"}

Após concluir a configuração, selecione **[!UICONTROL Concluído]** para concluir a criação do esquema.

## Editar um esquema {#schema-edit}

Para editar um esquema, selecione o esquema criado anteriormente na página **Esquemas**.

A página de detalhes do esquema é exibida. Selecione o ![ícone de lápis](/help/assets/icons/edit.png) para editar o esquema.

![](assets/schemas/schema_edit.png){zoomable="yes"}

Na janela **[!UICONTROL Editar esquema]**, você pode acessar e configurar as mesmas opções de quando [criar um esquema](#schema-create).

![](assets/schemas/schema_edit_orders.png){zoomable="yes"}

## Visualizar dados em um esquema {#schema-preview}

Para visualizar os dados na tabela representada pelo seu esquema, navegue até a guia **[!UICONTROL Dados]**, conforme abaixo.

Selecione o link **[!UICONTROL Calcular]** para visualizar o número total de gravações.

![](assets/schemas/schema_data.png){zoomable="yes"}

Selecione o botão **[!UICONTROL Configurar colunas]** para alterar a exibição de dados.

![](assets/schemas/schema_columns.png){zoomable="yes"}

## Atualizar um esquema {#schema-refresh}

As tabelas em um banco de dados federado podem ser atualizadas, adicionadas ou removidas. Nesses casos, você deve atualizar o esquema no Adobe Experience Platform para alinhar-se às alterações mais recentes. Para fazer isso, selecione o ![ícone de três pontos](/help/assets/icons/more.png) ao lado do nome do esquema seguido por **[!UICONTROL Atualizar esquema]**.

Também é possível atualizar a definição do schema ao editá-lo.

![](assets/schemas/schema_refresh.png){zoomable="yes"}

## Excluir um esquema {#schema-delete}

Para excluir um esquema, selecione o ![ícone de três pontos](/help/assets/icons/more.png), seguido de **[!UICONTROL Excluir]**.

![](assets/schemas/schema_delete.png){zoomable="yes"}
