---
title: Novidades na Composição de público-alvo federado da Experience Platform
description: Atualizações e notas de versão mais recentes
hide: true
hidefromtoc: true
exl-id: 23ea1a5d-a0e4-4f47-b0f8-56009bbc0a4a
source-git-commit: 83d6074da966553caec36908729729445246ea2f
workflow-type: tm+mt
source-wordcount: '802'
ht-degree: 90%

---

# Notas de versão {#rn-new}

O [!DNL Federated Audience Composition] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Todas as alterações são consolidadas nestas notas de versão. O [!DNL Federated Audience Composition] é construído nativamente na [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=pt-BR){target="_blank"}.

## Versão de março de 2025 {#fac-25-3}

### Melhorias {#fac-25-3-improvements}

Esta versão inclui as melhorias listadas abaixo.

* **Permissões da composição de público-alvo federado**

  A partir da versão de março, o recurso [!DNL Federated Audience Composition] começará a impor o acesso às interfaces de **gestão de dados federados** e **composições federadas** ao usuário que receber a permissão para **gerenciar dados federados**.

  Recomendamos que os usuários entrem em contato com os(as) admins, para que essa permissão seja adicionada à sua função a fim de manter o acesso à interface do [!DNL Federated Audience Composition].

  Para saber como conceder essa permissão, consulte a [documentação detalhada](feature-access.md).

<!--
* **Data model Canvas view**

    The Canvas view for the Data Models section improves the experience by enabling the visualization of data models and their links in a canvas layout, alongside the existing tabular view. [Learn more](../data-management/gs-models.md)


* **AI Assistant**

    AI Assistant is a user interface feature designed to help you navigate and understand Adobe concepts and get operational insights for your specific environment. It is available in several products across Adobe Experience Cloud, including Federated Audience Composition. [Learn more](ai-assistant.md)
-->

### Compatibilidade {#fac-25-3-compat}

* **Conexão do Databricks**

  Com esta nova versão, a composição de público-alvo federado agora é compatível com a conectividade por link privado para conexões de bancos de dados do Databricks.
Ela também possibilita conexões seguras com bancos de dados do Databricks hospedados no Amazon Web Services (AWS). [Saiba mais](../connections/federated-db.md#databricks)

* **Suporte para clientes B2B da CDP**

  A composição de público-alvo federado agora está disponível para clientes B2B (Business-to-Business) da plataforma de dados do cliente (CDP) para casos de uso de públicos-alvo baseados em pessoas.

* **Conexão segura do Snowflake**

  Com esta nova versão, a composição de público-alvo federado é compatível com conexões seguras por links privados para bancos de dados do Snowflake hospedados no Microsoft Azure. [Saiba mais](../connections/federated-db.md#snowflake)

## Versão de fevereiro de 2025 {#fac-25-2}

Esta versão inclui as alterações listadas abaixo.

* **Suporte ao Microsoft Fabric**

  Agora é possível estabelecer conexões com bancos de dados do Microsoft Fabric por meio da composição de público-alvo federado. [Saiba mais](../connections/federated-db.md)

* **Suporte ao Amazon Redshift Spectrum**

  O Amazon Redshift Spectrum agora é compatível com as conexões do banco de dados do Amazon Redshift. [Saiba mais](../connections/federated-db.md#amazon-redshift)

* **Experiência aprimorada de criação de esquemas**

  O processo de criação de esquemas foi aprimorado por meio de uma interface atualizada, projetada para ser mais intuitiva e fácil de navegar. Esses aprimoramentos oferecem aos profissionais de dados uma maneira mais suave e eficiente de desenvolver modelos de dados. [Saiba mais](../customer/schemas.md)

* **Suporte ao enriquecimento de público-alvo para Databricks**

  Agora você pode usar o Databricks no fluxo Ler público-alvo, habilitando a atividade para bancos de dados do Databricks e permitindo que seja definido como o novo destino. [Saiba mais](../connections/destinations.md)

## Versão de novembro de 2024 {#fac-24-11}

### Melhorias {#fac-24-11-improvements}

Esta versão inclui as melhorias listadas abaixo.

* **Lista de permissões de endereços IP**

  Ao adicionar um banco de dados federado na interface do usuário da Adobe Experience Platform, agora é possível visualizar diretamente os endereços IP associados às instâncias da composição de público-alvo federado. Isso permite copiar e autorizar facilmente esses IPs a conectarem-se ao banco de dados para aumentar a segurança e a flexibilidade. [Saiba mais](../connections/connections.md)

## Versão de outubro de 2024 {#fac-24-10}

>[!AVAILABILITY]
>
>Anteriormente disponível para algumas organizações (disponibilidade limitada), a Composição de público-alvo federado da Adobe Experience Platform agora está disponível para todos os usuários (disponibilidade geral). Este recurso é ativado com base na sua oferta e só é visível com as permissões associadas. [Saiba mais](access-prerequisites.md)
>

### Compatibilidade {#fac-24-10-compat}

Com esta nova versão, a Composição de público-alvo federado agora é compatível com os sistemas listados abaixo.

* **Compatibilidade com o Databricks**

  Agora é possível estabelecer conexões com bancos de dados do Databricks por meio da Composição de público-alvo federado. [Saiba mais](../connections/federated-db.md#databricks)

* **Suporte para acesso seguro ao Snowflake pelo AWS PrivateLink**

  Agora é possível ter acesso seguro ao seu data warehouse externo do Snowflake por meio de um link privado. Observe que a conta do Snowflake deve estar hospedada no Amazon Web Services (AWS) e localizada na mesma região do ambiente da Composição de público-alvo federado. Entre em contato com o representante da Adobe para obter assistência na configuração do acesso seguro à conta do Snowflake. [Saiba mais](../connections/federated-db.md#snowflake)

* **Suporte ao Amazon Redshift Serverless**

  Com esta nova versão, a Federated Audience Composition oferece suporte ao [Amazon Redshift Serverless](https://aws.amazon.com/pt/redshift/redshift-serverless/){target="_blank"}.

### Melhorias {#fac-24-10-improvements}

Esta versão vem com as melhorias listadas abaixo.

* **Atualizar esquemas existentes**

  Ao criar, modificar ou excluir uma coluna em um banco de dados federado, agora é possível detectar e aplicar as alterações clicando no botão **[!UICONTROL Atualizar esquema]** no esquema correspondente. [Saiba mais](../customer/schemas.md#schema-refresh)

* **Associar um modelo de dados a uma nova composição**

  Ao criar uma composição, agora é possível selecionar o modelo de dados para associar a ela. Com essa nova opção, a configuração das atividades é mais fácil, pois somente as tabelas do modelo de dados associado estão disponíveis. [Saiba mais](../compositions/create-composition.md)

## Versão de julho de 2024: Composição de público-alvo federado (Disponibilidade limitada) {#fac-la}

A composição de público-alvo federado fornece às empresas acesso flexível e expandido a warehouses de dados empresariais, para compor públicos-alvo por meio de conjuntos de dados empresariais cruciais e potencializar experiências iniciadas pela marca e experiências em tempo real. Com essa nova abordagem, como usuário do [Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/segmentation/home){target="_blank"} e/ou do [Adobe Journey Optimizer](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/ajo-home){target="_blank"}, você pode federar dados de público-alvo diretamente do data warehouse existente para enriquecer públicos-alvo da Adobe Experience Platform em um sistema.

A composição de público-alvo federado supre o aumento das demandas do mercado de empresas que precisam de flexibilidade para compor públicos-alvo com conjuntos de dados de uma warehouse. Dessa forma, as empresas podem reduzir a movimentação de dados, além de disponibilizar dados cruciais do público-alvo, para que as equipes de marketing satisfaçam os requisitos de casos de uso e potencializem experiências personalizadas.

Saiba mais sobre os recursos de Composição de Público Federado [nesta página](get-started.md) e nas [Perguntas Frequentes](faq.md).

Para obter informações detalhadas dos pré-requisitos para acessar Composições de público-alvo federado e as medidas de proteção atuais, consulte [esta página](access-prerequisites.md).
