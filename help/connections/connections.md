---
audience: end-user
title: Criar e gerenciar conexões com bancos de dados federados
description: Saiba como criar e gerenciar conexões com bancos de dados federados
badge: label="Disponibilidade limitada" type="Informative"
exl-id: ab65cd8a-dfa0-4f09-8e9b-5730564050a1
source-git-commit: ef72fe2c94c0dc9eb0432d092a6e4f01de8b9845
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 5%

---

# Criar conexões {#connections-fdb}

A Composição de público-alvo federado do Experience Platform permite que o Cliente crie e enriqueça públicos-alvo de data warehouses de terceiros e importe os públicos-alvo para a Adobe Experience Platform. Os datawarehouses com suporte estão listados em [esta seção](../start/access-prerequisites.md#supported-systems).

Para trabalhar com o banco de dados federado e o Adobe Experience Platform, primeiro é necessário estabelecer uma conexão. Essa conexão é configurada em uma interface de usuário dedicada disponível na interface do usuário do Adobe Experience Platform, conforme detalhado nesta página.

Para configurar uma conexão com seu banco de dados, siga estas etapas:

1. Navegue até a seção **[!UICONTROL DADOS FEDERADOS]** no painel esquerdo.

1. No link **[!UICONTROL Federated databases]**, clique no botão **[!UICONTROL Adicionar banco de dados federado]**.

   ![](assets/connections_list.png){zoomable="yes"}

1. Defina a conexão **[!UICONTROL Propriedades]**, com o nome e o tipo do banco de dados.

   ![](assets/connections_name.png){zoomable="yes"}

   Selecionar o tipo dá acesso a outras propriedades para preencher. Saiba mais aqui sobre os bancos de dados compatíveis em [esta página](federated-db.md).

   ![](assets/connections_details.png){zoomable="yes"}

   As configurações dependem do tipo do banco de dados. Navegue pelos links abaixo para acessar os detalhes necessários para configurar a conexão:

   * [Amazon Redshift](federated-db.md#amazon-redshift)
   * [Azure Synapse](federated-db.md#azure-synapse-redshift)
   * [Databricks](federated-db.md#databricks)
   * [Google Big Query](federated-db.md#google-big-query)
   * [Snowflake](federated-db.md#snowflake)
   * [Vertica Analytics](federated-db.md#vertica-analytics)

1. Depois de preencher os detalhes, clique no botão **[!UICONTROL Testar conexão]** e no botão **[!UICONTROL Implantar funções]**.

   ![](assets/connections_testdeploy.png){zoomable="yes"}

1. Conclua a criação da sua conexão clicando no botão **[!UICONTROL Salvar]**.

   Uma visão geral da sua conexão com o Federated database está disponível, conforme mostrado abaixo:

   ![](assets/connections_overview.png){zoomable="yes"}
