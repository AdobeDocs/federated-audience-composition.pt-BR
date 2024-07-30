---
title: Pré-requisitos e medidas de proteção para a Composição de Público-Alvo Federado
description: Saiba mais sobre os pré-requisitos, as permissões e as medidas de proteção da Composição de público-alvo federado
badge: label="Disponibilidade limitada" type="Informative"
source-git-commit: e6858ecd06e97b952e59738f299afc90fddeafb7
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 2%

---

# Pré-requisitos e medidas de proteção {#fac-access}

A Federated Audience Composition requer os pacotes **Prime** ou **Ultimate** do Adobe Real-time Customer Data Platform e/ou Adobe Journey Optimizer. Para acessar esse recurso, é necessário ter adquirido o complemento Federated Audience Composition.

>[!AVAILABILITY]
>
>Depois que você recebeu a notificação por email de boas-vindas do Adobe, pode levar mais algumas horas para que a interface seja atualizada e os recursos fiquem disponíveis.

## Permissões {#permissions}

Ao comprar o complemento Federated Audience Composition, um perfil de produto é criado para cada sandbox ativa nesse momento. Este perfil de produto foi criado no Admin Console sob o cartão de produto **Adobe Experience Platform** e segue esta convenção de nomenclatura: `ACP_FAC - <<SandboxName>> - admin.` Para acessar a Composição de Público Federado de uma sandbox específica, os usuários devem ser adicionados ao perfil de produto criado para essa sandbox.

Por exemplo, se uma nova sandbox chamada &quot;fac-test&quot; for ativada, um perfil de produto correspondente &quot;ACP_FAC - fac-test - admin&quot; será criado. Para acessar a Federated Audience Composition com esta sandbox, os usuários precisam ser adicionados a este perfil de produto.

## Lista de permissões de IP {#ip}

Para habilitar com segurança o Federated Audience Composition para acessar seus bancos de dados, entre em contato com o representante da Adobe para obter os endereços IP dos servidores do Federated Audience Composition que irão acessá-los.

Adicione esses endereços IP à lista de permissões para conceder acesso à Federated Audience Composition.

## Medidas de proteção e limitações {#fac-guardrails}

* A Federated Audience Composition é compatível com o Privacy &amp; Security Shield e pode ser usada em todos os mercados verticais, exceto no setor de saúde. Atualmente, a Federated Audience Composition não pode ser licenciada para clientes que procuram assimilar dados de integridade. [Saiba mais](https://experienceleague.adobe.com/en/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}

* Qualificações, limitações de produto e medidas de proteção de desempenho listadas na [documentação do Adobe Real-time Customer Data Platform](https://experienceleague.adobe.com/en/docs/experience-platform/profile/guardrails){target="_blank"} se aplicam a este complemento.
