---
title: Pré-requisitos e medidas de proteção para a Composição de Público-Alvo Federado
description: Saiba mais sobre os pré-requisitos, as permissões e as medidas de proteção da Composição de público-alvo federado
badge: label="Disponibilidade Limitada" type="Informative"
source-git-commit: 07170ee709c9e3c4ad0bb2390aa0d44adae3b059
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 14%

---

# Pré-requisitos e medidas de proteção {#fac-access}

A Federated Audience Composition requer os pacotes **Prime** ou **Ultimate** do Adobe Real-time Customer Data Platform e/ou Adobe Journey Optimizer. Para acessar esse recurso, é necessário ter adquirido o complemento Federated Audience Composition.

>[!AVAILABILITY]
>
>Após receber a notificação de boas-vindas da Adobe por email, pode levar mais algumas horas para que a interface seja atualizada e os recursos fiquem disponíveis.

## Permissões {#permissions}

Ao comprar o complemento Federated Audience Composition, um perfil de produto é criado para cada sandbox ativa nesse momento. Este perfil de produto foi criado no Admin Console sob o cartão de produto **Adobe Experience Platform** e segue esta convenção de nomenclatura: `ACP_FAC - <<SandboxName>> - admin.` Para acessar a Composição de Público Federado de uma sandbox específica, os usuários devem ser adicionados ao perfil de produto criado para essa sandbox.

Por exemplo, se uma nova sandbox chamada &quot;fac-test&quot; for ativada, um perfil de produto correspondente &quot;ACP_FAC - fac-test - admin&quot; será criado. Para acessar a Federated Audience Composition com esta sandbox, os usuários precisam ser adicionados a este perfil de produto.

## Lista de permissões de IP {#ip}

Para habilitar com segurança o Federated Audience Composition para acessar seus bancos de dados, entre em contato com o representante da Adobe para obter os endereços IP dos servidores do Federated Audience Composition que irão acessá-los.

Adicione esses endereços IP à lista de permissões para conceder acesso à Federated Audience Composition.

## Medidas de proteção e limitações {#fac-guardrails}

* O Federated Audience Composition não está disponível no momento para clientes [assimilando dados de integridade](https://experienceleague.adobe.com/pt-br/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"} e para clientes do Adobe Journey Optimizer Privacy and Security Shield. [Saiba mais](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/audiences-profiles-identities/audiences/about-audiences){target="_blank"}.

<!--
* Federated Audience Composition is compatible with Privacy & Security Shield and can be used in all verticals except for healthcare industries. Currently, Federated Audience Composition cannot be licensed to customers looking to ingest health data. [Learn more](https://experienceleague.adobe.com/en/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}-->

* Qualificações, limitações de produto e medidas de proteção de desempenho listadas na [documentação do Adobe Real-time Customer Data Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/profile/guardrails){target="_blank"} se aplicam a este complemento.
