---
title: Perguntas frequentes
description: Perguntas frequentes sobre a Composição de público-alvo federado da Adobe Experience Platform
exl-id: 68cc0ae5-5c41-425f-8b10-ab3515294006
source-git-commit: 03e918ab8828f9a9a1fedeef173852d31f0af818
workflow-type: ht
source-wordcount: '897'
ht-degree: 100%

---

# Perguntas frequentes {#faq}

Veja a seguir uma lista das perguntas frequentes sobre a Composição de público-alvo federado da Adobe Experience Platform. As perguntas frequentes globais também estão disponíveis para o Serviço de Segmentação da Adobe Experience Platform [nesta página](https://experienceleague.adobe.com/pt-br/docs/experience-platform/segmentation/faq){target="_blank"}.


+++Quais são as permissões necessárias para acessar a Composição de público-alvo federado?

A Composição de público-alvo federado exige pacotes da Adobe Real-Time Customer Data Platform e do Adobe Journey Optimizer Prime ou Ultimate. Também é necessário adquirir o recurso Composição de público-alvo federado.

Para usar a Composição de público-alvo federado, cada usuário deve ser adicionado a um perfil específico criado para cada sandbox. Para obter mais informações, acesse a página [Acessar Composição de público-alvo federado](access-prerequisites.md).

+++

+++Quais warehouses na nuvem são compatíveis?

A lista de sistemas compatíveis com a Composição de público-alvo federado está disponível [nesta página](../start/access-prerequisites.md#supported-systems).

+++


+++É possível consultar vários data warehouses na mesma composição?

Sim, vários warehouses podem ser consultados na mesma composição e podem combinar dados de várias fontes.  Geralmente, cada [atividade de composição](../compositions/orchestrate-activities.md) (Consulta, Enriquecimento, Divisão, etc.) executa uma ou várias instruções SQL, dependendo da configuração da atividade, dos bancos de dados de destino (pode haver vários casos de Federated Data Access) e das saídas de uma ou mais tabelas de trabalho com o resultado da execução. Essas tabelas de trabalho são usadas como entrada para atividades consecutivas.

+++

+++ Posso acessar todo o meu banco de dados usando a Composição de público-alvo federado?

Não, é necessário configurar o acesso a um banco de dados/esquema dedicado ou compartilhado. Recomendamos a criação de um esquema dedicado para a Composição de público-alvo federado e a cópia/compartilhamento somente dos conjuntos de dados de Business Case.
+++

+++Tenho acesso a todas as tabelas no esquema dedicado?

Sim, depois de conectado, a Composição de público-alvo federado pode ser usada para descobrir todas as tabelas com base nos direitos iniciais definidos. Em seguida, é possível usar o editor visual de esquema para:

* Descobrir colunas e chaves primárias a partir das tabelas
* Criar rótulos amigáveis para essas tabelas
* Criar rótulos amigáveis para cada coluna
* Ocultar colunas desnecessárias
* Salvar a descrição dessas tabelas
+++

+++Há algum armazenamento temporário na Composição de público-alvo federado?

Não, a Composição de público-alvo federado armazena apenas metadados (descrições de esquema). Nenhum dado do cliente está em trânsito. <!--The Audience export flow is done directly from Adobe Experience Platform Audience Portal (via [Destination](../connections/destinations.md)) to the customer database. The creation and update flow is done directly from your data warehouse database to Adobe Experience Platform Audience Portal.-->

+++

+++A Composição de público-alvo federado armazena uma cópia física dessa lista de pessoas para enviar a sistemas downstream?

A Composição de público-alvo federado não mantém uma cópia física dos dados. A frequência é configurada na composição para definir com que frequência esses dados serão atualizados. Os dados de público-alvo resultantes não são armazenados pela Adobe Experience Platform por mais tempo do que o exigido pelos casos de uso do cliente ou ação.

Por exemplo:

* A criação de um público-alvo ocorre em seu warehouse, e você pode contar com a Composição de público-alvo federado para tarefas adicionais de composição e manipulação de dados. Em seguida, o público-alvo resultante e os atributos associados podem ser publicados por meio do Portal de público-alvo da Adobe Experience Platform. A definição do público-alvo e os atributos associados são fornecidos para a Adobe Experience Platform.
Observe que a expiração dos dados atuais para públicos-alvo gerados externamente é de 30 dias. Essa expiração de dados reduz a quantidade de dados em excesso armazenados em uma organização. Depois que o período de expiração dos dados passar, o conjunto de dados associado ainda estará visível no inventário do conjunto de dados, mas não será possível ativar o público-alvo e a contagem de perfis será exibida como zero. Saiba mais na [Documentação da Adobe Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/segmentation/faq#how-long-do-externally-generated-audiences-last-for){target="_blank"}.

* No caso de um enriquecimento de público-alvo, o ponto de partida é um público-alvo da Adobe Experience Platform já existente. Você pode ver dois cenários aqui:
   1. Trazer atributos adicionais de conteúdo de público-alvo do data warehouse federado: nesse caso, os atributos adicionais incluídos aparecerão como parte dessa definição de público-alvo. A expiração de dados para públicos-alvo gerados externamente é a mesma descrita acima, 30 dias.
   1. Refine o público-alvo existente da Adobe Experience Platform com base em atributos adicionais existentes em seu data warehouse.<!--For example, you have an audience of customers who have shown interest in a particular product on the website for the last two months. You now want to take this audience and further segment it using Federated Audience Composition to only include customers who have a high credit score. The credit score is deemed sensitive and individual credit score data points are not copied over from the data warehouse.-->
+++

+++Se os dados para os padrões de casos de uso de criação e enriquecimento de público-alvo não estão sendo mantidos, como eles estão sendo armazenados temporariamente?

Os dados resultantes do público-alvo não persistem indefinidamente na Adobe Experience Platform ou na Composição de público-alvo federado. Eles não serão retidos por mais tempo do que o exigido por seu caso de uso. Os atributos de público-alvo trazidos como parte do conteúdo do público-alvo persistirão apenas como parte da definição do público-alvo. A duração da persistência é baseada no TTL para qualquer público-alvo. O padrão é 30 dias.

+++

+++É possível excluir um público-alvo?

Não, na versão atual, não é possível excluir públicos da composição de público-alvo federado.

+++

+++Se eu combinar dados de várias fontes, como estamos unindo os dados? Estamos usando o serviço de identidade?

Não, o Serviço de identidade não está sendo usado durante uma composição. Os dados entre as várias fontes usadas na composição são unidos por meio de uma lógica definida pelo usuário (conforme expresso no modelo subjacente), por exemplo, ID de CRM, número de conta do usuário, etc. Você deve selecionar a identidade usada como o identificador no público-alvo para a seleção no data warehouse. Em um público-alvo resultante da Composição de público-alvo federado, é necessário identificar o namespace de identidade da identidade no conjunto de dados resultante.

+++

+++Como criar e gerenciar solicitações de privacidade com a composição de público-alvo federado?

É possível enviar solicitações individuais para acessar e excluir dados do consumidor da composição de público-alvo federado da Adobe de duas maneiras:

* Por meio da **interface do Privacy Service** da Adobe Experience Platform. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=pt-BR){target="_blank"}
* Por meio da **API do Privacy Service** da Adobe Experience Platform. [Saiba mais](https://experienceleague.adobe.com/pt-br/docs/experience-platform/privacy/api/overview){target="_blank"}

Todas as etapas para criar e gerenciar **solicitações de acesso** e **solicitações de exclusão** estão detalhadas na [documentação do perfil do cliente em tempo real](https://experienceleague.adobe.com/pt-br/docs/experience-platform/profile/privacy){target="_blank"}.

+++

<!--
+++How are customer consent preferences honored for externally generated audiences that are imported into Federated Audience Composition?

As customer data is captured from multiple channels, identity stitching and merge policies allow this data to be consolidated in a single Real-Time Customer Profile. Information on the customers' consent preferences are stored and evaluated at the profile level.

Downstream Real-Time CDP and Journey Optimizer destinations check each profile for consent preferences prior to activation. Each profile's consent information is compared against consent requirements for a particular destination. If the profile does not satisfy the requirements, that profile is not sent to a destination.

When an external audience is ingested into Federated Audience Composition, it is reconciliated with existing profiles using a primary ID such as email or ECID. As a result, the existing consent policies will remain in force throughout activation.

>[!NOTE]
>
>Since the payload variables are not stored in the profile but in the data lake, you should not include consent information in externally generated audiences. Instead, use other Adobe Experience Platform ingestion channels where profile data is imported.

+++
-->
