---
title: Pré-requisitos e medidas de proteção para a Composição de público-alvo federado
description: Saiba mais sobre os pré-requisitos, as permissões e as medidas de proteção da Composição de público-alvo federado
exl-id: 661a838f-146e-4d68-bb2d-319827caee3a
TQID: https://experienceleague.adobe.com/VBIotVn1VyiFJChb3mM0VDLUSbG9aQOmbfGnfGgqvhU
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: fda4d9d7b45833d7e080ae80f42b7ca5ce36b3ad
workflow-type: tm+mt
source-wordcount: 386
ht-degree: 100%

---

# Pré-requisitos e medidas de proteção {#fac-access}

A Composição de público-alvo federado exige os pacotes **Prime** ou **Ultimate** da Adobe Real-time Customer Data Platform e/ou do Adobe Journey Optimizer. Para acessar esse recurso, você deve ter adquirido o complemento Composição de público-alvo federado.

>[!AVAILABILITY]
>
>Após receber a notificação do email de boas-vindas da Adobe, pode levar mais algumas horas para que a interface seja atualizada e os recursos fiquem disponíveis.

## Sistemas compatíveis {#supported-systems}

A Composição de público-alvo federado é compatível com os seguintes warehouses na nuvem:

* Amazon Redshift
* Azure Synapse
* Databricks
* Google BigQuery
* Snowflake
* Vertica Analytics
* Microsoft Fabric

Você pode aprender a criar uma conexão com esses sistemas na [visão geral das conexões](../connections/home.md).

## Sandboxes

Ao adquirir a composição de público-alvo federado, você tem direito a duas sandboxes. Para solicitações adicionais de provisionamento de sandbox, entre em contato com o seu representante da Adobe.

Para exibir a lista de sandboxes ativas da composição de público-alvo federado, siga as etapas abaixo:

1. Na Composição de público-alvo federado, acesse o menu **[!UICONTROL Uso da licença]** em **[!UICONTROL Administração]**.

1. Clique no ícone ![](assets/do-not-localize/Smock_InfoOutline_18_N.svg) em **[!UICONTROL Volume total de saída de dados]** para acessar as propriedades da sandbox.

   ![](assets/sandbox_1.png)

1. As informações sobre a sandbox são mostradas no popover Propriedades.

   ![](assets/sandbox_2.png)

## Permissões {#permissions}

Para acessar a composição de público-alvo federado, os usuários devem ser adicionados ao perfil de produto específico da sandbox criado após a compra e atribuído à permissão **[!UICONTROL Gerenciar dados federados]**. [Saiba mais](/help/governance-privacy-security/access-control.md)

## Lista de permissões de IP {#ip}

Para permitir que a composição de público-alvo federado acesse os seus bancos de dados com segurança, será necessário autorizar os endereços IP dos servidores da composição de público-alvo federado que os acessarão. Esses endereços IP são exibidos ao adicionar um banco de dados federado à interface do usuário da Adobe Experience Platform. [Saiba mais](../connections/home.md)

Adicione esses endereços IP à lista de permissões para conceder acesso à composição de público-alvo federado.

## Mesclar políticas {#merge-policies}

Se sua sandbox usa uma política de mesclagem de **precedência de conjunto de dados**, entre em contato com o atendimento ao cliente da Adobe para adicionar o conjunto de dados `Halos UPS` à política de mesclagem.

Para obter mais informações sobre políticas de mesclagem, leia a [visão geral das políticas de mesclagem](https://experienceleague.adobe.com/pt-br/docs/experience-platform/profile/merge-policies/overview).

## Medidas de proteção e limitações {#fac-guardrails}

* Os direitos, as limitações do produto e medidas de proteção de desempenho listados na [documentação da Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/profile/guardrails){target="_blank"} aplicam-se à composição de público-alvo federado.

* A composição de público-alvo federado é compatível com a exportação de públicos-alvo grandes, com tamanhos de arquivo superiores a 1 GB. Para um desempenho ideal, o tamanho máximo recomendado de arquivo é de até 20 GB.
