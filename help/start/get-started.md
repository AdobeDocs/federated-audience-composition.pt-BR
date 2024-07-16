---
title: Introdução à composição de público-alvo federado
description: Saiba o que é a composição de público-alvo federado do Adobe e como usá-la no Adobe Experience Platform
source-git-commit: 25f623cde151824effddea34127a82e8d920f3e2
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 34%

---


# Introdução à composição de público-alvo federado {#gs-fac}

A Composição de público-alvo federado do Adobe ajuda os usuários de aplicativos da Adobe Experience Platform a acessar os dados de clientes armazenados no data warehouse corporativo. Os dados do cliente podem residir em vários data warehouses e devem estar acessíveis instantaneamente, sem replicação.

O Adobe Experience Platform Federated Audience Composition oferece uma solução fácil e eficiente para conectar seu data warehouse corporativo diretamente no Adobe Real-time Customer Data Platform e realizar consultas nas tabelas de seu data warehouse.

## Principais etapas {#gs-steps}

A composição do público-alvo federado do Adobe permite criar e atualizar públicos-alvo do Adobe Experience Platform diretamente do banco de dados, sem nenhum processo de assimilação.

![diagrama](assets/FAC-diagram.png)

Principais etapas:

* **Configuração**

   1. Conecte o Adobe Experience Platform e o data warehouse da sua empresa.
Os seguintes bancos de dados são suportados: Snowflake, Google Big Query, Azure synapse, Redshift.
Saiba mais [nesta página](../connections/federated-db.md)
   1. Crie esquemas para selecionar quais dados devem estar acessíveis na interface do usuário.
Saiba mais [nesta página](../customer/schemas.md)
   1. Crie links para seu modelo de dados.
Saiba mais [nesta página](../data-management/gs-models.md)

* **Compor públicos-alvo**

   1. Projete e execute composições para criar públicos.
Saiba mais [nesta página](../compositions/gs-compositions.md)
   1. Atualize ou reutilize públicos-alvo existentes por meio do portal de público-alvo e de Destinos da Adobe Experience Platform.
Saiba mais [nesta página](../connections/destinations.md)

## Saiba mais {#learn}

<!-- Workflow + Workflow activities-->



>[!CONTEXTUALHELP]
>id="dc_workflow_settings_execution"
>title="Configurações de execução"
>abstract="Nesta seção, é possível definir configurações relacionadas à execução do fluxo de trabalho, de modo que o número de dias do histórico do fluxo de trabalho seja mantido."




>[!CONTEXTUALHELP]
>id="dc_orchestration_query_enrichment_noneditable"
>title="Atividade não editável"
>abstract="Quando uma atividade de **Consulta** ou **Enriquecimento** é configurada com dados adicionais no console, os dados de enriquecimento são levados em consideração e transmitidos para a transição de saída, mas não podem ser editados."

<!-- Create a link -->

>[!CONTEXTUALHELP]
>id="dc_federated_database_create_link"
>title="Criar um link"
>abstract="Defina as configurações do link."
