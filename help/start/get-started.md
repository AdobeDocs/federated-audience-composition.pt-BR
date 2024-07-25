---
title: Introdução à composição de público-alvo federado
description: Saiba o que é a composição de público-alvo federado do Adobe e como usá-la no Adobe Experience Platform
badge: label="Disponibilidade limitada" type="Informative"
exl-id: 43464aea-9c1d-4f1f-859f-82f209f350b7
source-git-commit: 3b4f5284cd65cd5cd30c4223fe2df3ffff7c0905
workflow-type: tm+mt
source-wordcount: '510'
ht-degree: 11%

---

# Introdução à composição de público-alvo federado {#gs-fac}

A Federated Audience Composition é um complemento para o Adobe Real-time Customer Data Platform e o Adobe Journey Optimizer que permite criar e enriquecer públicos-alvo de seus data warehouses de terceiros e importar os públicos-alvo para a Adobe Experience Platform. A Federated Audience Composition oferece uma solução fácil e eficiente para conectar seu data warehouse corporativo diretamente na Adobe Real-time Customer Data Platform e/ou Adobe Journey Optimizer e realizar consultas nas tabelas de seu data warehouse.

A Composição de público-alvo federado do Adobe ajuda os usuários de aplicativos da Adobe Experience Platform a acessar os dados de clientes armazenados em seus data warehouses e plataformas de armazenamento na nuvem, como o Amazon Redshift, o Azure synapse Analytics e muito mais. Os dados do cliente podem residir em vários data warehouses e agora podem ser acessados instantaneamente, sem replicação. As plataformas com suporte estão listadas em [esta página](../connections/federated-db.md#supported-db).

## Casos de uso {#rn-uc}

Por meio de uma interface amigável de marketing, crie regras de segmento que consultem seu data warehouse para obter uma lista de usuários que se qualificam para um segmento específico necessário para campanhas de marketing, acesse públicos existentes no warehouse para ativação ou enriqueça os públicos-alvo da Adobe Experience Platform com pontos de dados adicionais que existem no warehouse.

Nesta versão, dois casos de uso estão disponíveis: Criação de público-alvo e Enriquecimento de público-alvo.

![diagrama](assets/fac-use-cases.png){zoomable="yes"}{width="75%" align="center"}

## Principais etapas {#gs-steps}

A composição do público-alvo federado do Adobe permite criar e atualizar públicos-alvo do Adobe Experience Platform diretamente do banco de dados, sem nenhum processo de assimilação.

![diagrama](assets/steps-diagram.png){zoomable="yes"}{width="85%" align="center"}

Principais etapas:

1. **Integração de dados**: reúna dados de várias fontes e mescle-os em um conjunto de dados unificado. Saiba como conectar aplicativos Adobe Experience Platform e seu data warehouse corporativo, bancos de dados com suporte e como configurá-los estão detalhados em [esta seção](../connections/federated-db.md).

2. **Modelagem de Dados**: projete e crie modelos de dados e esquemas que definam a estrutura, as relações e as restrições dos dados. Saiba mais sobre esquemas em [esta página](../customer/schemas.md). Saiba como criar links para seu modelo de dados no [nesta página](../data-management/gs-models.md).

3. **Transformação de Dados**: aplique técnicas de manipulação de dados para modificar o formato, a estrutura ou os valores de elementos de dados para torná-los compatíveis ou adequados para análise ou aplicativos específicos.

4. **Uso de dados**: crie, organize e compile públicos-alvo. Saiba como compor públicos-alvo em [esta página](../compositions/gs-compositions.md). Você também pode atualizar ou reutilizar públicos-alvo existentes por meio do portal de público-alvo e de Destinos da Adobe Experience Platform. Saiba mais [nesta página](../connections/destinations.md)


>[!NOTE]
>
>Depois de executar a composição, o público resultante é salvo na Adobe Experience Platform como um público externo e disponível no Adobe Real-time Customer Data Platform e/ou no Adobe Journey Optimizer. Ele se tornou acessível no menu **Públicos-alvo**. [Saiba mais](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}
>



## Saiba mais {#learn}

<!-- Workflow + Workflow activities-->

Consulte as Perguntas Frequentes em [esta página](faq.md).

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_execution"
>title="Configurações de execução"
>abstract="Nesta seção, você pode definir configurações relacionadas à execução do fluxo de trabalho, como o número de dias em que o histórico de composição é mantido."




>[!CONTEXTUALHELP]
>id="dc_orchestration_query_enrichment_noneditable"
>title="Atividade não editável"
>abstract="Quando uma atividade de **Consulta** ou **Enriquecimento** é configurada com dados adicionais no console, os dados de enriquecimento são levados em consideração e transmitidos para a transição de saída, mas não podem ser editados."

<!-- Create a link -->

>[!CONTEXTUALHELP]
>id="dc_federated_database_create_link"
>title="Criar um link"
>abstract="Defina as configurações do link."
