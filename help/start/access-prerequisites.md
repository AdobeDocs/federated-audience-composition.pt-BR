---
title: Pré-requisitos e medidas de proteção para a Composição de público-alvo federado
description: Saiba mais sobre os pré-requisitos, as permissões e as medidas de proteção da Composição de público-alvo federado
exl-id: 661a838f-146e-4d68-bb2d-319827caee3a
source-git-commit: 97bda9d08eead79e6172e3b5bb746e7516bf6d85
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 73%

---

# Pré-requisitos e medidas de proteção {#fac-access}

A Composição de público-alvo federado exige os pacotes **Prime** ou **Ultimate** da Adobe Real-time Customer Data Platform e/ou do Adobe Journey Optimizer. Para acessar esse recurso, você deve ter adquirido o complemento Composição de público-alvo federado.

>[!AVAILABILITY]
>
>Após receber a notificação de boas-vindas da Adobe por email, pode levar mais algumas horas para que a interface seja atualizada e os recursos fiquem disponíveis.

## Sistemas compatíveis {#supported-systems}

A Composição de público-alvo federado é compatível com os seguintes warehouses na nuvem:

* Amazon Redshift
* Azure Synapse
* Databricks
* Google Big Query
* Snowflake
* Vertica Analytics
* Microsoft Fabric

Saiba como criar uma conexão com esses sistemas [nesta página](../connections/connections.md).

## Sandboxes

Ao comprar a Federated Audience Composition, você tem direito a duas sandboxes. Para solicitações adicionais de provisionamento de sandbox, entre em contato com o seu representante da Adobe.

Para exibir a lista de suas sandboxes ativas do Federated Audience Composition, siga as etapas abaixo:

1. Na Federated Audience Composition, acesse o menu **[!UICONTROL Uso da licença]** em **[!UICONTROL Administração]**.

1. Clique no ícone ![](assets/do-not-localize/Smock_InfoOutline_18_N.svg) em **[!UICONTROL Volume total de saída de dados]** para acessar as propriedades da sandbox.

   ![](assets/sandbox_1.png)

1. As informações sobre sua sandbox são mostradas no popover Propriedades.

   ![](assets/sandbox_2.png)

## Permissões {#permissions}

Para acessar a composição de público-alvo federado, os usuários devem ser adicionados ao perfil de produto específico da sandbox criado após a compra e atribuído à permissão **[!UICONTROL Gerenciar dados federados]**. [Saiba mais](feature-access.md)

## Lista de permissões de IP {#ip}

Para permitir que a composição de público-alvo federado acesse os seus bancos de dados com segurança, será necessário autorizar os endereços IP dos servidores da composição de público-alvo federado que os acessarão. Esses endereços IP são exibidos ao adicionar um banco de dados federado à interface do usuário da Adobe Experience Platform. [Saiba mais](../connections/connections.md)

Adicione esses endereços IP à lista de permissões para conceder acesso à Composição de público-alvo federado.

## Medidas de proteção e limitações {#fac-guardrails}

* A composição de público-alvo federado não está disponível no momento para clientes que estiverem [assimilando dados de integridade](https://experienceleague.adobe.com/pt-br/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}. [Saiba mais](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/audiences-profiles-identities/audiences/about-audiences){target="_blank"}

<!--
* Federated Audience Composition is compatible with Privacy & Security Shield and can be used in all verticals except for healthcare industries. Currently, Federated Audience Composition cannot be licensed to customers looking to ingest health data. [Learn more](https://experienceleague.adobe.com/en/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}-->

* Os direitos, as limitações de produto e as medidas de proteção de desempenho listados na [documentação do Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/profile/guardrails){target="_blank"} aplicam-se à Federated Audience Composition.

<!--* Federated Audience Composition supports the export of large audiences, with file sizes greater than 1 GB. For optimal performance, the maximum recommended file size is up to 20 GB.
-->

