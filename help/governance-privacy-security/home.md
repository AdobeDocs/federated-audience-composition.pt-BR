---
title: Privacidade e segurança na composição de público-alvo federado
description: Saiba como a composição de público-alvo federado lida com a privacidade e a segurança de dados do usuário, incluindo recursos como governança de dados, aplicação de consentimento, controle de acesso, criptografia de dados e conformidade de privacidade.
exl-id: 677e26e7-1294-4f62-a5ce-17b65e84c65e
source-git-commit: 65a69bf857ec1a0701534693600a8c6340179838
workflow-type: tm+mt
source-wordcount: '1182'
ht-degree: 77%

---

# Governança, privacidade e segurança de dados

>[!IMPORTANT]
>
>A Federated Audience Composition é totalmente compatível com a HIPAA e está disponível para uso do Healthcare Shield, bem como de clientes do Privacy and Security Shield.

A Federated Audience Composition fornece vários serviços e ferramentas que permitem a conformidade com suas práticas comerciais, obrigações legais e processos de desenvolvimento.

Esses serviços podem ser organizados em três categorias:

- [Governança de dados](#data-governance)
- [Privacidade](#privacy)
- [Segurança](#security)

## Governança de dados {#data-governance}

Você pode usar o controle de dados para gerenciar e identificar os dados do cliente, garantindo que eles sejam rotulados corretamente para cumprir as restrições definidas pela organização ou pelos regulamentos legais.

### Rótulos de uso de dados {#data-usage-labels}

Você pode usar rótulos de uso de dados para categorizar conjuntos de dados e campos com base nas políticas de governança que se aplicam a esses dados. Depois de criar um público-alvo usando composições, você pode aplicar os rótulos de dados apropriados ao esquema resultante para garantir que ele respeite as restrições de uso necessárias.

Para obter mais informações sobre como usar rótulos de dados na Composição de Público-Alvo Federado, leia a [seção Aplicar rótulos de acesso](../compositions/home.md#access-labels){target="_blank"}.

## Privacidade

A Federated Audience Composition fornece os dados federados para o Adobe Experience Platform e o Adobe Journey Optimizer usarem e garante que a privacidade dos dados do usuário seja respeitada.

### Privacy Service {#privacy-service}

Como a Federated Audience Composition **não** armazena os dados do cliente de qualquer data warehouse, você pode usar o Adobe Experience Platform Privacy Service para estar em conformidade com as solicitações de titular dos dados e de exclusão de dados.

Por exemplo, ao criar um público-alvo usando o bloco Salvar atividade na tela de composição, o público-alvo resultante é armazenado no data lake da Experience Platform como um público-alvo externo. Esse público-alvo externo é marcado com seu campo de identidade e namespace de identidade. Como resultado, você pode usar o serviço de privacidade para acessar e remover esses perfis com um público-alvo externo.

Como alternativa, depois de criar um enriquecimento de perfil usando a atividade Salvar perfil na tela de composição, o enriquecimento resultante é armazenado na Experience Platform como um esquema habilitado para perfil e conjunto de dados habilitado para perfil. Estes dados de enriquecimento são marcados com um campo de identidade e um namespace de identidade. Como resultado, você pode usar o serviço de privacidade para acessar e limpar esses perfis.

Para obter mais informações sobre o serviço de privacidade, leia a [Visão geral do serviço de privacidade](https://experienceleague.adobe.com/pt-br/docs/experience-platform/privacy/home){target="_blank"}.

### Solicitações de privacidade {#privacy-requests}

No serviço de privacidade, é possível criar e gerenciar solicitações de privacidade individuais para acessar e excluir dados do cliente da composição de público-alvo federado. O serviço de privacidade fornece uma [interface](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=pt-BR){target="_blank"} e uma [API RESTful](https://experienceleague.adobe.com/pt-br/docs/experience-platform/privacy/api/overview){target="_blank"} para ajudar você a gerenciar solicitações de dados de clientes.

Para obter mais informações sobre como criar e gerenciar solicitações de privacidade, leia sobre os [trabalhos de privacidade no guia da interface do serviço de privacidade](https://experienceleague.adobe.com/pt-br/docs/experience-platform/privacy/ui/user-guide){target="_blank"}.

### Aplicação da política de consentimento {#consent}

Por meio da Experience Platform, a composição de público-alvo federado oferece ferramentas que permitem automatizar a aplicação de consentimento, garantindo a ativação de públicos-alvo com base no consentimento fornecido aos clientes.

Por exemplo, ao criar um público-alvo usando o bloco Salvar atividade na tela de composição, o público-alvo resultante é armazenado no data lake da Experience Platform como um público-alvo externo. A Experience Platform oferece suporte automático à validação de consentimento durante a ativação. Para obter mais informações, leia as [Perguntas frequentes sobre o serviço de segmentação](https://experienceleague.adobe.com/pt-br/docs/experience-platform/segmentation/faq#consent){target="_blank"}.

Como alternativa, depois de criar um enriquecimento de perfil usando a atividade Salvar perfil na tela de composição, o enriquecimento resultante é armazenado na Experience Platform como um esquema habilitado para perfil e conjunto de dados habilitado para perfil. Para perfis existentes, os atributos de consentimento disponíveis são considerados automaticamente durante a ativação. Para novos perfis, os atributos de consentimento fornecidos durante a ingestão do perfil são considerados automaticamente durante a ativação. Para obter mais informações sobre como aplicar consentimentos a perfis, leia o [guia do grupo de campos de consentimento e preferências](https://experienceleague.adobe.com/pt-br/docs/experience-platform/xdm/field-groups/profile/consents){target="_blank"}.

Para obter mais informações sobre como aplicar consentimentos, leia o [guia da interface de gerenciamento de políticas](https://experienceleague.adobe.com/pt-br/docs/experience-platform/data-governance/policies/user-guide#consent-policy){target="_blank"}.

### Ciclo de vida dos dados {#data-lifecycle}

Visto que a composição de público-alvo federado **não** armazena dados do cliente de qualquer data warehouse, você pode usar a Experience Platform para lidar com o ciclo de vida dos dados. Com o Gerenciamento avançado do ciclo de vida dos dados, é possível gerenciar o ciclo de vida dos dados em nível de conjunto de dados e de registro.

Por exemplo, ao criar um público-alvo usando o bloco Salvar atividade na tela de composição, o público-alvo resultante é armazenado no data lake na Experience Platform como um público-alvo externo. Como esses dados **não** são armazenados na composição de público-alvo federado, os dados do público-alvo e os conjuntos de dados correspondentes são excluídos automaticamente quando o público-alvo é excluído no Portal de públicos-alvo.

Como alternativa, depois de criar um enriquecimento de perfil usando a atividade Salvar perfil na tela de composição, o enriquecimento resultante é armazenado na Experience Platform como um esquema habilitado para perfil e conjunto de dados habilitado para perfil. Como resultado, você pode usar o ciclo de vida dos dados para acessar e limpar os perfis.

Para obter mais informações sobre o uso do ciclo de vida de dados, leia a [Visão geral do ciclo de vida de dados](https://experienceleague.adobe.com/pt-br/docs/experience-platform/data-lifecycle/home){target="_blank"}.

## Segurança {#security}

A segurança de dados garante que seus dados sejam mantidos protegidos na Composição de público-alvo federado.

### Criptografia {#encryption}

A Federated Audience Composition fornece criptografia por meio de criptografia de dados inativos, criptografia de dados em trânsito e chaves gerenciadas pelo cliente.

Os dados em repouso se referem aos dados do cliente usados na composição de público-alvo federado. Os dados são criptografados pelo provedor de serviços na nuvem e usados na composição de público-alvo federado em sua forma criptografada.

Dados em trânsito se referem aos dados do cliente conforme são movidos de um componente para outro na composição de público-alvo federado. Os dados são mantidos criptografados em todos os componentes da composição de público-alvo federado usando TLS 1.3 por HTTPS.

Para obter mais informações sobre como a Adobe trata a criptografia de dados, leia o guia sobre [criptografia de dados na Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/landing/governance-privacy-security/encryption){target="_blank"}.

### Chaves gerenciadas pelo cliente {#customer-managed-keys}

As chaves gerenciadas pelo cliente permitem o controle dos dados, possibilitando o uso de suas próprias chaves de criptografia para criptografar os dados. Como a composição de público-alvo federado **não** armazena dados do cliente, você pode usar chaves gerenciadas pelo cliente diretamente nos públicos-alvo e enriquecimentos resultantes, pois elas serão armazenadas no data lake na Experience Platform.

Para obter mais informações sobre chaves gerenciadas pelo cliente, leia o [guia de chaves gerenciadas pelo cliente](https://experienceleague.adobe.com/pt-br/docs/experience-platform/landing/governance-privacy-security/customer-managed-keys/overview){target="_blank"}.

### Log de auditoria {#audit-log}

Todas as operações de criação, leitura, atualização e exclusão realizadas na composição de público-alvo federado são registradas na trilha de auditoria. Você pode usar esse log de auditoria para monitorar essas ações, impor a responsabilidade e dar suporte a auditorias de conformidade.

Para obter mais informações, leia a [Visão geral da trilha de auditoria](/help/admin/audit-trail.md){target="_blank"}.

### Controle de acesso {#access-control}

Você pode controlar o acesso à composição de público-alvo federado em nível de campo e de função. É possível usar esses controles de acesso para aplicar políticas de governança de dados, limitar a exposição de informações confidenciais e alinhar o acesso às responsabilidades do usuário.

Para obter mais informações sobre o controle de acesso na Federated Audience Composition, leia o [guia de controle de acesso](/help/governance-privacy-security/access-control.md){target="_blank"}.

### Localização de dados {#data-localization}

A composição de público-alvo federado **não** armazena dados de clientes. Como resultado, você deve se certificar de conectar seus bancos de dados externos **somente** à região de sandbox correspondente para manter os dados na mesma região. Se você conectar um banco de dados de uma região diferente a uma sandbox, a Adobe **não** será responsável pela localização de dados.

## Próximas etapas {#next-steps}

Depois de ler este guia, você compreenderá melhor os recursos de governança, privacidade e segurança de dados em uso na Federated Audience Composition, incluindo rótulos de uso de dados, conformidade com a privacidade, aplicação de consentimento, gerenciamento do ciclo de vida dos dados e controle de acesso.
