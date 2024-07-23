---
audience: end-user
title: Criar e gerenciar conexões com Bancos de Dados Federados
description: Saiba como criar e gerenciar conexões com Bancos de Dados Federados
badge: label="Disponibilidade limitada" type="Informative"
source-git-commit: c1c035d3783af6c3bc94f2ba0aff7ba515fb68e2
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 5%

---

# Criar conexões {#connections-fdb}

Trabalhar com um banco de dados Federado diretamente na AEP implica em estabelecer uma conexão com ele.

Para configurar uma conexão com seu banco de dados, vá para a seção **[!UICONTROL DADOS FEDERADOS]** e, no link **[!UICONTROL Bancos de Dados Federados]**, clique no botão **[!UICONTROL Adicionar banco de dados federado]**.

![](assets/connections_list.png){zoomable="yes"}

Você acessará a janela da conexão **[!UICONTROL Propriedades]**, com o nome e o tipo do banco de dados.

![](assets/connections_name.png){zoomable="yes"}

Selecionar o tipo dará acesso a outras propriedades para preenchimento. [Saiba mais aqui sobre os bancos de dados com suporte](federated-db.md).

![](assets/connections_details.png){zoomable="yes"}

De acordo com o tipo de banco de dados, saiba nos links abaixo as informações necessárias para configurar a conexão:

* [Amazon Redshift](federated-db.md#amazon-redshift)
* [Azure synapse](federated-db.md#azure-synapse-redshift)
* [Google Big Query](federated-db.md#google-big-query)
* [Snowflake](federated-db.md#snowflake)
* [Vertica Analytics](federated-db.md#vertica-analytics)

Depois de preencher os detalhes, clique no botão **[!UICONTROL Testar conexão]** e no botão **[!UICONTROL Implantar funções]**.
Conclua a criação da sua conexão clicando no botão **[!UICONTROL Salvar]**.

![](assets/connections_testdeploy.png){zoomable="yes"}

Você terá uma visão geral da sua conexão com o Federated Database desta forma:

![](assets/connections_overview.png){zoomable="yes"}
