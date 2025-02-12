---
title: Novidades na Composição de público-alvo federado da Experience Platform
description: Atualizações e notas de versão mais recentes
exl-id: d4dcaf31-93cd-4a4e-888a-cf1bbdc4ca03
source-git-commit: 81ac7595196aeff30f1d09d66779ca4392f7bb19
workflow-type: tm+mt
source-wordcount: '590'
ht-degree: 88%

---

# Notas de versão {#rn-new}

O [!DNL Federated Audience Composition] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Todas as alterações são consolidadas nestas notas de versão. O [!DNL Federated Audience Composition] é construído nativamente na [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=pt-BR){target="_blank"}.


## Atualização de fevereiro de 25 {#fac-25-01}

A partir da versão de março, o [!DNL Federated Audience Composition] começará a impor o acesso das interfaces do **Federated data management** e **Federated Compositions** ao usuário ao qual foi concedida a permissão **Gerenciar Dados Federados**.

Recomendamos que os usuários contatem os administradores para que essa permissão seja adicionada à sua função para continuar acessando a interface de usuário do [!DNL Federated Audience Composition].

Para saber como atribuir esta permissão, consulte a [documentação detalhada](feature-access.md).

## Versão de novembro de 2024 {#fac-24-11}

### Melhorias {#fac-24-11-improvements}

Esta versão inclui as melhorias listadas abaixo.

* **Lista de permissões de endereços IP**

  Ao adicionar um banco de dados federado na interface do usuário da Adobe Experience Platform, agora é possível visualizar diretamente os endereços IP associados às instâncias da composição de público-alvo federado. Isso permite copiar e autorizar facilmente esses IPs a conectarem-se ao banco de dados para aumentar a segurança e a flexibilidade. [Saiba mais](../connections/connections.md)

## Versão de outubro de 2024 {#fac-24-10}

>[!AVAILABILITY]
>
>Anteriormente disponível para algumas organizações (disponibilidade limitada), a Composição de público-alvo federado da Adobe Experience Platform agora está disponível para todos os usuários (disponibilidade geral). Este complemento é ativado com base na sua oferta e só é visível com as permissões associadas. [Saiba mais](access-prerequisites.md)
>

### Compatibilidade {#fac-24-10-compat}

Com esta nova versão, a Composição de público-alvo federado agora é compatível com os sistemas listados abaixo.

* **Compatibilidade com o Databricks**

  Agora é possível estabelecer conexões com bancos de dados do Databricks por meio da Composição de público-alvo federado. [Saiba mais](../connections/federated-db.md#databricks)

* **Suporte para acesso seguro ao Snowflake pelo AWS PrivateLink**

  Agora é possível ter acesso seguro ao seu data warehouse externo do Snowflake por meio de um link privado. Observe que a conta do Snowflake deve estar hospedada no Amazon Web Services (AWS) e localizada na mesma região do ambiente da Composição de público-alvo federado. Entre em contato com o representante da Adobe para obter assistência na configuração do acesso seguro à conta do Snowflake. [Saiba mais](../connections/federated-db.md#snowflake)

* **Suporte ao Amazon Redshift Serverless**

  Com esta nova versão, a Composição de público-alvo federado oferece suporte ao [Amazon Redshift Serverless](https://aws.amazon.com/pt/redshift/redshift-serverless/){target="_blank"}.

### Melhorias {#fac-24-10-improvements}

Esta versão vem com as melhorias listadas abaixo.

* **Atualizar esquemas existentes**

  Ao criar, modificar ou excluir uma coluna em um banco de dados federado, agora é possível detectar e aplicar as alterações clicando no botão **[!UICONTROL Atualizar esquema]** no esquema correspondente. [Saiba mais](../customer/schemas.md#schema-refresh)

* **Associar um modelo de dados a uma nova composição**

  Ao criar uma composição, agora é possível selecionar o modelo de dados para associar a ela. Com essa nova opção, a configuração das atividades é mais fácil, pois somente as tabelas do modelo de dados associado estão disponíveis. [Saiba mais](../compositions/create-composition.md)

## Versão de julho de 2024: Composição de público-alvo federado (Disponibilidade limitada) {#fac-la}

A Composição de público-alvo federado é um recurso complementar que fornece às empresas acesso flexível e expandido a data warehouses empresariais. Isso possibilita a composição de públicos-alvo usando conjuntos de dados empresariais críticos e a potencialização de experiências iniciadas pela marca e no momento. Com essa nova abordagem, por usar a [Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/segmentation/home){target="_blank"} e/ou o [Adobe Journey Optimizer](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/ajo-home){target="_blank"}, você pode federar dados de públicos-alvo diretamente do seu data warehouse existente para enriquecer os públicos-alvo da Adobe Experience Platform em um sistema.

A Composição de público-alvo federado atende ao aumento das demandas do mercado para empresas que precisam de flexibilidade para compor públicos-alvo com conjuntos de dados de warehouse. Dessa forma, as empresas podem reduzir a movimentação de dados, além de disponibilizar dados críticos do público-alvo para que as equipes de marketing atendam aos requisitos de casos de uso e potencializem experiências personalizadas. 

Saiba mais sobre os recursos da Composição de público-alvo federado [nesta página](get-started.md) e nas [Perguntas frequentes](faq.md).

Para obter informações detalhadas dos pré-requisitos para acessar Composições de público-alvo federado e as medidas de proteção atuais, consulte [esta página](access-prerequisites.md).

