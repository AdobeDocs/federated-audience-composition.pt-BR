---
audience: end-user
title: Visão geral dos esquemas
description: Saiba como criar e usar esquemas para a Composição de público federado na interface do usuário do Adobe Experience Platform.
TQID: https://experienceleague.adobe.com/cpkFeiskYDpixNo01llqC3UKK8XfewN7XC2yAf1wOYQ
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: Experience Cloud
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
    internal-label: Governance
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
source-git-commit: 3b159f95e28414b75b44e41e822e9e3d0e35b537
workflow-type: tm+mt
source-wordcount: '796'
ht-degree: 3%
---
# Visão geral dos esquemas {#schemas}

>[!AVAILABILITY]
>
>A experiência de novos esquemas só está disponível para clientes selecionados. Para obter mais informações, entre em contato com o Atendimento ao cliente da Adobe.
>
>Se você não tiver acesso à nova experiência de esquemas, leia a [visão geral dos esquemas](./schemas.md).
>
>Para acessar esquemas, você precisará de uma das seguintes permissões:
>
>-**Gerenciar Esquema Federado**
>-**Exibir Esquema Federado**
>
>Para mais informações sobre as permissões exigidas, leia o [guia de controle de acesso](/help/governance-privacy-security/access-control.md).

Um schema é uma representação de uma tabela do banco de dados. É um objeto dentro do aplicativo que define como os dados são vinculados às tabelas do banco de dados.

Ao criar um esquema, você pode definir uma representação da tabela na Composição do público-alvo federado do Experience Platform:

* Dê a ele um nome e uma descrição amigáveis para simplificar a compreensão do usuário
* Decidir a visibilidade de cada campo, de acordo com seu uso real
* Selecione sua chave primária para vincular esquemas entre elas, conforme necessário no [modelo de dados](../data-modelling/models.md#data-model-start)

>[!CAUTION]
>
>Ao conectar várias sandboxes com o mesmo banco de dados, você deve usar esquemas de trabalho distintos.

## Criar um esquema {#create}

>[!CONTEXTUALHELP]
>id="platform_schemas_manageconfiguration"
>title="Gerenciar configuração"
>abstract="Conteúdo temporariamente em branco."

Para criar um esquema na Composição de Público-Alvo Federado, selecione **[!UICONTROL Esquemas]** na seção **[!UICONTROL Gerenciamento de Dados]** da interface do usuário do Experience Platform. Na interface de Esquemas, selecione **[!UICONTROL Criar esquema]**.

![Os botões Esquemas e Criar esquema estão realçados na interface do usuário Esquemas.](/help/data-modelling/assets/integrated/select-create-schema.png)

Quando o popover Criar esquema for exibido, selecione **[!UICONTROL Relacional]**, seguido de **[!UICONTROL Descobrir esquemas]** e **[!UICONTROL Próximo]** para criar um esquema para a Composição de Público-Alvo Federado.

![O botão Descobrir esquemas está realçado no popover Criar um esquema relacional.](/help/data-modelling/assets/integrated/select-discover-schemas.png)

O popover **[!UICONTROL Selecionar banco de dados federado]** é exibido. Neste pop-over, você pode selecionar o [banco de dados de origem](/help/connections/home.md), seguido de **[!UICONTROL Próximo]**.

![O popover Selecionar banco de dados federado é exibido.](/help/data-modelling/assets/integrated/select-federated-database.png)

## Definir esquema {#define}

>[!CONTEXTUALHELP]
>id="platform_schemas_primarycompositekey"
>title="Chave composta"
>abstract="Uma chave de esquema composta de várias colunas de esquema. Marque as colunas que deseja usar como chave composta."

Após escolher o banco de dados federado, você pode definir seu esquema. A tela **[!UICONTROL Adicionar dados]** é exibida. Nesta página, você pode selecionar **[!UICONTROL Adicionar tabela]** para escolher quais tabelas deseja adicionar ao esquema.

![O botão Adicionar tabela está realçado na tela Adicionar dados.](/help/data-modelling/assets/integrated/select-add-table.png)

O popover **[!UICONTROL Selecionar tabela]** é exibido. Nesse popover, é possível selecionar as tabelas que deseja usar para criar o schema.

![O popover Selecionar tabela é exibido.](/help/data-modelling/assets/integrated/select-table.png){zoomable="yes"}

Cada tabela selecionada gera um esquema com as colunas escolhidas. Para cada tabela, você pode alterar o rótulo do esquema, adicionar uma descrição, renomear o rótulo do campo, definir a visibilidade do rótulo do campo e selecionar a chave primária do esquema.

![As tabelas selecionadas são exibidas na página Adicionar dados.](/help/data-modelling/assets/integrated/tables-added.png){zoomable="yes"}

>[!NOTE]
>
>Se você escolher **[!UICONTROL Chave Composta]**, mas selecionar apenas uma chave a ser usada, ela será tratada como uma chave primária de esquema padrão.

Além disso, você pode criar uma chave composta de várias colunas de esquema. Selecione **[!UICONTROL Chave Composta]** e marque as chaves que deseja usar como sua chave composta.

![O botão Chave Composta e os esquemas estão selecionados.](/help/data-modelling/assets/integrated/composite-key.png){zoomable="yes"}

Após concluir a configuração, selecione **[!UICONTROL Concluído]** para concluir a criação do esquema.

## Editar um esquema {#schema-edit}

Para editar um esquema, selecione o ![ícone de reticências](/help/assets/icons/more.png) ao lado do esquema criado anteriormente na página **Esquemas**, seguido de **[!UICONTROL Editar]**.

![O botão Editar esquema está realçado.](/help/data-modelling/assets/integrated/edit-schema.png)

Na janela **[!UICONTROL Editar esquema]**, você pode ver o Editor de esquemas. Para obter mais informações sobre como usar o Editor de Esquemas, leia o [guia da interface do usuário do esquema](https://experienceleague.adobe.com/pt-br/docs/experience-platform/xdm/ui/resources/schemas#customize-schema).

![O Editor de Esquemas é exibido.](/help/data-modelling/assets/integrated/schema-editor.png)

### Editar relacionamentos {#relationship-edit}

Para editar as relações de um esquema, selecione **[!UICONTROL Exibir diagrama de entidade]** no Editor de esquemas.

![O botão Exibir diagrama de entidade está realçado.](/help/data-modelling/assets/integrated/view-entity-diagram.png)

A página do diagrama de entidade é exibida. Nesta página, você pode criar links para estabelecer relações entre seus esquemas.

![O diagrama de entidade é exibido.](/help/data-modelling/assets/integrated/entity-diagram.png)

Para obter mais informações sobre como criar links, leia a guia Exibição da tela da [visão geral dos modelos de dados](/help/data-modelling/models.md#data-model-links).

## Visualizar dados em um esquema {#schema-preview}

Para visualizar os dados na tabela representada pelo esquema, vá para a seção **[!UICONTROL Conjuntos de Dados]** e selecione **[!UICONTROL Procurar]**.

![Os botões &#39;Procurar&#39; e &#39;Conjuntos de dados&#39; estão realçados.](/help/data-modelling/assets/integrated/datasets-browse.png)

Selecione os ![três pontos](/help/assets/icons/more.png), seguido por **[!UICONTROL Visualizar conjunto de dados]** para ver uma visualização dos dados no esquema.

![O botão Visualizar conjunto de dados está realçado.](/help/data-modelling/assets/integrated/select-preview-dataset.png)

## Atualizar um esquema {#schema-refresh}

As tabelas em um banco de dados federado podem ser atualizadas, adicionadas ou removidas. Nesses casos, você deve atualizar o esquema no Adobe Experience Platform para alinhar-se às alterações mais recentes. Para atualizar o esquema, selecione o botão **[!UICONTROL Mais]**, seguido por **[!UICONTROL Gerenciar configuração]**.

![O botão Gerenciar configuração está realçado.](/help/data-modelling/assets/integrated/manage-configuration.png)

O popover **[!UICONTROL Editar configuração]** é exibido. Selecione **[!UICONTROL Atualizar]** para atualizar o esquema.

![O botão Atualizar esquema está realçado.](/help/data-modelling/assets/integrated/refresh-schema.png)

## Excluir um esquema {#schema-delete}

Para excluir um esquema no Editor de Esquemas, selecione **[!UICONTROL Mais]**, seguido por **[!UICONTROL Excluir]**.

![O botão Excluir esquema está realçado.](/help/data-modelling/assets/integrated/delete-schema.png)
