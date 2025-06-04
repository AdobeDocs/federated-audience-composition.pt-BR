---
title: Privacidade e segurança na composição do público-alvo federado
description: Saiba como a Federated Audience Composition lida com a privacidade e a segurança para dados do usuário, incluindo recursos como governança de dados, aplicação de consentimento, controle de acesso, criptografia de dados e conformidade com a privacidade.
source-git-commit: b505a4f0ac9ac7350e2879f4f54f93a69b73f96c
workflow-type: tm+mt
source-wordcount: '1085'
ht-degree: 1%

---


# Privacidade e segurança na composição do Federated Audience

A Federated Audience Composition está em conformidade com várias práticas de segurança para proteger seus dados durante o processamento.

## Privacy Service {#privacy}

A Federated Audience Composition fornece os dados federados para o Adobe Experience Platform e o Adobe Journey Optimizer usarem. No entanto, a Federated Audience Composition **não** armazena os dados do cliente de qualquer data warehouse. Como resultado, você pode usar o Adobe Experience Platform Privacy Service para estar em conformidade com as solicitações de titular dos dados e de exclusão de dados.

Por exemplo, ao criar um público-alvo usando o bloco de atividade Salvar na tela de composição, o público-alvo resultante é armazenado no data lake na Experience Platform como um público externo. Esse público-alvo externo é marcado com seu campo de identidade e namespace de identidade. Como resultado, você pode usar o Privacy Service para acessar e remover esses perfis com um público-alvo externo.

Como alternativa, depois de criar um enriquecimento de perfil usando a atividade Salvar perfil na tela de composição, o enriquecimento resultante é armazenado no Experience Platform como um esquema habilitado para perfil e conjunto de dados habilitado para perfil. Estes dados de enriquecimento são marcados com um campo de identidade e um namespace de identidade. Como resultado, você pode usar o Privacy Service para acessar e limpar esses perfis.

Para obter mais informações sobre o Privacy Service, leia a [visão geral do Privacy Service](https://experienceleague.adobe.com/pt-br/docs/experience-platform/privacy/home){target="_blank"}.

### Solicitações de privacidade {#privacy-requests}

No Privacy Service, você pode criar e gerenciar solicitações individuais de privacidade para acessar e excluir dados do cliente da Federated Audience Composition. A Privacy Service fornece uma [interface de usuário](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=pt-BR){target="_blank"} e uma [API RESTful](https://experienceleague.adobe.com/pt-br/docs/experience-platform/privacy/api/overview){target="_blank"} para ajudar você a gerenciar solicitações de dados do cliente.

Para obter mais informações sobre como criar e gerenciar solicitações de privacidade, leia os [trabalhos de privacidade no guia da interface do Privacy Service](https://experienceleague.adobe.com/pt-br/docs/experience-platform/privacy/ui/user-guide){target="_blank"}.

## Aplicação da política de consentimento {#consent}

A Composição de público-alvo federado, por meio do Experience Platform, oferece ferramentas que permitem automatizar a aplicação de consentimento, garantindo a ativação de públicos-alvo com base no consentimento fornecido aos clientes.

Por exemplo, ao criar um público-alvo usando o bloco de atividade Salvar na tela de composição, o público-alvo resultante é armazenado no data lake na Experience Platform como um público externo. O Experience Platform oferece suporte automático à validação de consentimento durante a ativação. Para obter mais informações, leia as [Perguntas frequentes sobre o Serviço de Segmentação](https://experienceleague.adobe.com/pt-br/docs/experience-platform/segmentation/faq#consent){target="_blank"}.

Como alternativa, depois de criar um enriquecimento de perfil usando a atividade Salvar perfil na tela de composição, o enriquecimento resultante é armazenado no Experience Platform como um esquema habilitado para perfil e conjunto de dados habilitado para perfil. Para perfis existentes, os atributos de consentimento disponíveis são honrados automaticamente durante a ativação. Para novos perfis, os atributos de consentimento fornecidos durante a assimilação do perfil são automaticamente honrados durante a ativação. Para obter mais informações sobre como aplicar consentimentos a perfis, leia o [guia do grupo de campos de consentimentos e preferências](https://experienceleague.adobe.com/pt-br/docs/experience-platform/xdm/field-groups/profile/consents){target="_blank"}.

Para obter mais informações sobre como aplicar consentimentos, leia o [guia da interface do usuário para gerenciar políticas](https://experienceleague.adobe.com/pt-br/docs/experience-platform/data-governance/policies/user-guide#consent-policy){target="_blank"}.

## Ciclo de vida dos dados {#data-lifecycle}

Como a Federated Audience Composition **não** armazena dados do cliente de qualquer data warehouse, você pode usar o Experience Platform para lidar com o ciclo de vida dos dados. Com o Gerenciamento avançado do ciclo de vida dos dados, é possível gerenciar o ciclo de vida dos dados em nível de conjunto de dados e de registro.

Por exemplo, ao criar um público-alvo usando o bloco de atividade Salvar na tela de composição, o público-alvo resultante é armazenado no data lake na Experience Platform como um público externo. Como esses dados **não** são armazenados na Composição de Público-Alvo Federado, os dados do público-alvo e os conjuntos de dados correspondentes são excluídos automaticamente quando o público-alvo é excluído no Portal de Público-alvo.

Como alternativa, depois de criar um enriquecimento de perfil usando a atividade Salvar perfil na tela de composição, o enriquecimento resultante é armazenado no Experience Platform como um esquema habilitado para perfil e conjunto de dados habilitado para perfil. Como resultado, você pode usar o Ciclo de vida dos dados para acessar e limpar os perfis.

Para obter mais informações sobre como usar o Ciclo de Vida dos Dados, leia a [visão geral do Ciclo de Vida dos Dados](https://experienceleague.adobe.com/pt-br/docs/experience-platform/data-lifecycle/home){target="_blank"}.

## Rótulos de uso de dados {#data-usage-labels}

Os rótulos de uso de dados permitem categorizar conjuntos de dados e campos com base nas políticas de governança que se aplicam a esses dados. Depois de criar um público-alvo usando composições, você pode aplicar os rótulos de dados apropriados ao esquema resultante para garantir que ele respeite as restrições de uso necessárias.

Para obter mais informações sobre o uso de rótulos de dados, leia a [visão geral dos rótulos de uso de dados](https://experienceleague.adobe.com/pt-br/docs/experience-platform/data-governance/labels/overview){target="_blank"}.

## Criptografia {#encryption}

A composição flexível do público-alvo fornece criptografia por meio de criptografia de dados em repouso, criptografia de dados em trânsito e chaves gerenciadas pelo cliente.

Os dados em repouso se referem aos dados do cliente usados na Composição do público-alvo federado. Os dados são criptografados pelo provedor de serviços de nuvem e usados na Federated Audience Composition em sua forma criptografada.

Os dados em trânsito se referem aos dados do cliente à medida que se movem de um componente para outro na Composição do público-alvo federado. Os dados são mantidos criptografados em todos os componentes da Composição de público federado usando TLS 1.3 em HTTPS.

Para obter mais informações sobre como o Adobe trata a criptografia de dados, leia o manual sobre [criptografia de dados no Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/landing/governance-privacy-security/encryption){target="_blank"}.

### Chaves gerenciadas pelo cliente {#customer-managed-keys}

As chaves gerenciadas pelo cliente permitem que você tenha controle sobre seus dados, permitindo que você use suas próprias chaves de criptografia para criptografar seus dados. Como a Composição de Público Federado **não** armazena dados do cliente, você pode usar chaves gerenciadas pelo cliente diretamente nos públicos-alvo e enriquecimentos resultantes, pois elas serão armazenadas no data lake na Experience Platform.

Para obter mais informações sobre chaves gerenciadas pelo cliente, leia o [guia de chaves gerenciadas pelo cliente](https://experienceleague.adobe.com/pt-br/docs/experience-platform/landing/governance-privacy-security/customer-managed-keys/overview){target="_blank"}.

## Log de auditoria {#audit-log}

Todas as operações de criação, leitura, atualização e exclusão realizadas na Composição do Federated Audience são registradas na trilha de auditoria. Você pode usar esse log de auditoria para rastrear essas ações, impor a responsabilidade e dar suporte a auditorias de conformidade.

Para obter mais informações, leia a [Visão geral da trilha de auditoria](/help/admin/audit-trail.md){target="_blank"}.

## Controle de acesso {#access-control}

Você pode controlar o acesso à Composição de público-alvo federado em nível de campo e de função. Você pode usar esses controles de acesso para aplicar políticas de controle de dados, limitar a exposição de informações confidenciais e alinhar o acesso às responsabilidades do usuário.

Para obter mais informações sobre o controle de acesso na Federated Audience Composition, leia o [Guia de Composição do Federated Audience](/help/start/feature-access.md){target="_blank"}.

## Localização de dados {#data-localization}

A Federated Audience Composition **não** armazena dados de clientes. Como resultado, você precisa garantir que **somente** conecte seus bancos de dados externos à região de sandbox correspondente para manter seus dados na mesma região. Se você conectar um banco de dados de região diferente a uma sandbox, a Adobe **não** será responsável pela localização dos dados.

## Próximas etapas {#next-steps}

Depois de ler este guia, você terá uma melhor compreensão dos recursos de privacidade e segurança em uso na Federated Audience Composition, incluindo governança de dados, conformidade com a privacidade, aplicação de consentimento, gerenciamento do ciclo de vida dos dados e controle de acesso.
