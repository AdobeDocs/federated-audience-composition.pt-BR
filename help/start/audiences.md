---
audience: end-user
title: Trabalhar com públicos-alvo
description: Saiba como trabalhar com públicos
badge: label="Disponibilidade limitada" type="Informative"
exl-id: c6507624-1dc9-43f9-a3ad-c3dc9689f8c7
source-git-commit: 3b891232a3a671f8ec12e06b19086f12ef849f1e
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 2%

---

# Trabalhar com públicos-alvo {#gs-audiences}

A Composição de público-alvo federado do Experience Platform permite [criar composições](../compositions/gs-compositions.md), onde você pode aproveitar várias atividades em uma tela visual para criar públicos-alvo e armazená-los no Adobe Experience Platform Audience Portal.

Em seguida, você pode direcionar esses públicos-alvo no Journey Optimizer ou ativá-los para qualquer destino compatível com o Adobe Experience Platform.

## Criação de público usando composições {#creation}

Para criar públicos usando a composição de Público-alvo federado, você precisa criar uma composição que inclua uma atividade **[!UICONTROL Salvar público-alvo]**. Essa atividade permite salvar o público no Audience Portal e selecionar campos de seus bancos de dados externos para incluir no público. [Saiba como configurar uma atividade Save audience](../compositions/activities/save-audience.md)

O público-alvo criado usando o Adobe Federated Data Composition inclui todos os campos selecionados na atividade **[!UICONTROL Salvar público-alvo]** e é armazenado no Portal de Público junto com todos os públicos-alvo da Adobe Experience Platform.

Depois de executar a composição, o público resultante é salvo na Adobe Experience Platform como um público externo e disponível no Adobe Real-time Customer Data Platform e/ou no Adobe Journey Optimizer.

Você pode ativar esses públicos-alvo para qualquer destino compatível com o Adobe Experience Platform. [Saiba como trabalhar com destinos](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/home)

>[!NOTE]
>
>Os públicos-alvo criados usando o Adobe Federated Audience Composition não podem ser editados. Para fazer modificações em um desses públicos-alvo, é necessário criar um novo público-alvo usando uma composição.

## Acessar seu público-alvo no Adobe Experience Platform {#access-audience}

Os públicos-alvo criados usando a Composição de público-alvo federado ficam acessíveis no Portal de público-alvo, que pode ser acessado pelo menu **Públicos-alvo**.

A guia **[!UICONTROL Procurar]** lista todos os públicos existentes armazenados no Adobe Experience Platform. Você pode identificar públicos-alvo de Composição de Público-Alvo Federado na lista usando a coluna **[!UICONTROL Origin]** ou os filtros disponíveis no painel esquerdo.

![](assets/audiences-list.png)

Para obter mais informações sobre como trabalhar com públicos no Adobe Experience Platform, consulte a [documentação do Portal de público-alvo](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal)

<!-- add link to this donc once published: https://jira.corp.adobe.com/browse/PLAT-198674-->