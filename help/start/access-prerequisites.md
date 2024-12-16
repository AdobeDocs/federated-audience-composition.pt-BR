---
title: Pré-requisitos e medidas de proteção para a Composição de público-alvo federado
description: Saiba mais sobre os pré-requisitos, as permissões e as medidas de proteção da Composição de público-alvo federado
exl-id: 661a838f-146e-4d68-bb2d-319827caee3a
source-git-commit: d26fa10fa7e28c1515a625e2e0b10a000aa2d7d5
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 82%

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

Saiba como criar uma conexão com esses sistemas [nesta página](../connections/connections.md).

<!--
## Sandboxes

When purchasing the Federated Audience Composition add-on, you are entitled to two sandboxes (one production sandbox and one non-production sandbox). For any additional sandbox provisioning requests, contact your Adobe representative.
-->

## Permissões {#permissions}

Ao comprar o complemento Composição de público-alvo federado, um perfil de produto é criado para cada sandbox ativa nesse momento. Esse perfil de produto é criado no Admin Console sob o cartão de produto **Adobe Experience Platform** e segue a seguinte convenção de nomeação: `ACP_FAC - <<SandboxName>> - admin.` Para acessar a Composição de público-alvo federado de uma sandbox específica, os usuários devem ser adicionados ao perfil de produto criado para essa sandbox.

Por exemplo, se uma nova sandbox chamada “fac-test” for ativada, um perfil de produto correspondente “ACP_FAC - fac-test - admin” será criado. Para acessar a Composição de público-alvo federado com esta sandbox, os usuários precisam ser adicionados a este perfil de produto.

## Lista de permissões de IP {#ip}

Para habilitar com segurança o Federated Audience Composition para acessar seus bancos de dados, você deve autorizar os endereços IP dos servidores do Federated Audience Composition que os acessarão. Esses endereços IP são exibidos ao adicionar um banco de dados federado na interface do usuário do Adobe Experience Platform. [Saiba mais](../connections/connections.md)

Adicione esses endereços IP à lista de permissões para conceder acesso à Composição de público-alvo federado.

## Medidas de proteção e limitações {#fac-guardrails}

* A Federated Audience Composition não está disponível no momento para clientes [assimilando dados de integridade](https://experienceleague.adobe.com/pt-br/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}<!-- and to Adobe Journey Optimizer Privacy and Security Shield customers-->. [Saiba mais](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/audiences-profiles-identities/audiences/about-audiences){target="_blank"}

<!--
* Federated Audience Composition is compatible with Privacy & Security Shield and can be used in all verticals except for healthcare industries. Currently, Federated Audience Composition cannot be licensed to customers looking to ingest health data. [Learn more](https://experienceleague.adobe.com/en/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}-->

* Direitos, limitações de produto e medidas de proteções de desempenho listados na documentação da Adobe Real-Time Customer Data Platform [](https://experienceleague.adobe.com/pt-br/docs/experience-platform/profile/guardrails){target="_blank"} se aplicam a este complemento.

