---
title: Notas de versão da Federated Audience Composition
description: Atualizações e notas de versão mais recentes da Composição de público-alvo federado.
exl-id: d4dcaf31-93cd-4a4e-888a-cf1bbdc4ca03
TQID: https://experienceleague.adobe.com/AqtqibUr1TNXwQ9lrtVoQ3CBNwyjSMS64e4s8y4iTSc
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
source-git-commit: 5cbe8da3f51b33b14f5c86648b3523ce6464b944
workflow-type: tm+mt
source-wordcount: 545
ht-degree: 11%

---

# Notas de versão

O [!DNL Federated Audience Composition] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Todas as alterações são consolidadas nestas notas de versão. O [!DNL Federated Audience Composition] é construído nativamente na [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=pt-BR){target="_blank"}.

## Versão de abril de 2026 {#fac-26-04}

A versão de abril do Federated Audience Composition é compatível com os seguintes recursos e melhorias:

### Novos recursos {#fac=26-04-feature}

| Novo conector - Teradata |
| --- |
| O conector do Teradata agora está disponível para uso com a Federated Audience Composition. Você pode usar o conector do Teradata para casos de uso de criação e enriquecimento de público. Para obter mais informações sobre o conector do Teradata, leia a [visão geral das conexões](/help/connections/home.md). |

### Aprimoramentos {#fac-26-04-improvements}

Esta versão vem com a seguinte melhoria.

- **Suporte a chave não criptografada para o Snowflake**

  Agora você pode usar chaves não criptografadas ao usar a autenticação de par de chaves para se conectar com data warehouses da Snowflake.

  Para saber mais sobre como usar chaves não criptografadas com o Snowflake, leia a [visão geral das conexões](/help/connections/home.md).

## Versão de março de 2026 {#fac-26-03}

A versão de março do Federated Audience Composition é compatível com os seguintes recursos:

### Novos recursos {#fac-26-03-feature}

| Segmentação baseada em IA |
| --- |
| Agora é possível criar composições de público-alvo federado de forma independente no Assistente do AI. Ao usar o Assistente do AI para criar o público-alvo, o Assistente do AI gera um plano que, após ser aprovado, será executado no navegador. Para obter mais informações sobre como usar o Assistente de IA para criar públicos, leia a [Visão geral do Assistente de IA](/help/start/ai-assistant.md). |

| Assistente de IA para Insights Operacionais |
| --- |
| Agora você pode fazer perguntas ao Assistente de IA sobre insights operacionais na Composição de público federado. As áreas compatíveis incluem conexões, esquemas e modelos de dados. Composições federadas **não** são compatíveis com esta versão. Para obter mais informações sobre o Assistente de IA na Composição de Público-Alvo Federado, leia a [Visão geral do Assistente de IA](/help/start/ai-assistant.md). |

## Versão de fevereiro de 2026 {#fac-26-02}

A versão de fevereiro do Federated Audience Composition é compatível com os seguintes recursos:

### Novos recursos {#fac-26-02-feature}

| Suporte ao enriquecimento de campo |
| --- |
| Agora você pode usar a atividade Salvar campo em suas composições. A atividade save field permite enriquecer esquemas do Experience Platform federando dados de depósitos externos, permitindo aprimorar esquemas do Experience Platform com atributos adicionais. A atividade de campo salvar suporta os esquemas B2B e B2C. Para obter mais informações sobre como usar esta atividade, leia a [visão geral das atividades](../compositions/activities.md#save-fields). |

| Suporte à autenticação avançada para databricks |
| --- |
| Agora você pode se conectar ao Federated Audience Composition com Databricks usando a autenticação da entidade de serviço ou usando o OAuth 2.0. Para obter mais informações sobre como criar uma conexão, leia a [visão geral das conexões](../connections/home.md#create). |

## Versão de janeiro de 2026 {#fac-26-01}

A versão de janeiro da Composição do Federated Audience oferece suporte aos seguintes novos recursos e melhorias:

### Novos recursos {#fac-26-01-feature}

| Suporte à Autenticação da Entidade de Serviço Azure Synapse |
| --- |
| Agora você pode se conectar ao Federated Audience Composition com o Azure Synapse usando uma Entidade de Serviço. Para obter mais informações sobre como criar uma conexão, leia a [visão geral das conexões](../connections/home.md#create). |

| Disponibilidade para clientes do Adobe Experience Platform no Amazon Web Services (AWS) |
| --- |
| Agora você pode usar a Composição de público federado se a instância do Experience Platform estiver no AWS. Para obter mais informações sobre o Experience Platform no AWS, leia a [visão geral das várias nuvens](https://experienceleague.adobe.com/pt-br/docs/experience-platform/landing/multi-cloud). |

### Aprimoramentos {#fac-26-01-improvements}

Esta versão vem com a seguinte melhoria.

- **Configuração de expiração de dados para públicos-alvo**

  Agora é possível definir uma expiração de dados ao usar a atividade **Salvar público-alvo** em uma composição.

  Para saber mais sobre as expirações de dados na Federated Audience Composition, leia o [guia de atividades](../compositions/activities.md#save-audience).
