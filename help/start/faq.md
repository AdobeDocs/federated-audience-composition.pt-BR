---
title: Perguntas frequentes
description: Perguntas frequentes sobre a Composição de público-alvo federado da Adobe Experience Platform
badge: label="Disponibilidade limitada" type="Informative"
exl-id: 68cc0ae5-5c41-425f-8b10-ab3515294006
source-git-commit: dd19c6a8170a87c10fd8534bf2aa63adcf360529
workflow-type: ht
source-wordcount: '834'
ht-degree: 100%

---

# Perguntas frequentes {#faq}

Veja a seguir uma lista das perguntas frequentes sobre a Composição de público-alvo federado da Adobe Experience Platform. As perguntas frequentes globais também estão disponíveis para o Serviço de Segmentação da Adobe Experience Platform [nesta página](https://experienceleague.adobe.com/pt-br/docs/experience-platform/segmentation/faq){target="_blank"}.


+++Quais são as permissões necessárias para acessar a Composição federada de público-alvo?

A Composição de público-alvo federado exige pacotes da Adobe Real-Time Customer Data Platform e do Adobe Journey Optimizer Prime ou Ultimate. Também é preciso ter adquirido o complemento Composição de público-alvo federado.

Para usar a Composição de público-alvo federado, cada usuário deve ser adicionado a um perfil específico criado para cada sandbox. Para obter mais informações, acesse a página [Acessar Composição de público-alvo federado](access-prerequisites.md).

+++

+++Quais warehouses na nuvem são compatíveis?

Para esta versão, a Composição federada de público-alvo é compatível com:

* Amazon Redshift
* Azure Synapse
* Google Big Query
* Snowflake
* Vertica Analytics

+++


+++É possível consultar vários data warehouses na mesma composição?

Sim, vários warehouses podem ser consultados na mesma composição e podem combinar dados de várias fontes.  Normalmente, cada [atividade de composição](../compositions/orchestrate-activities.md) (Consulta, Enriquecimento, Divisão, etc.) executa uma ou várias instruções SQL dependendo da configuração da atividade, dos bancos de dados de destino (pode haver vários casos de Federated Data Access) e das saídas de uma ou mais tabelas de trabalho com o resultado da execução. Essas tabelas de trabalho são usadas como entrada para atividades consecutivas.

+++

+++ Posso acessar todo o meu banco de dados usando a Composição federada de público-alvo?

Não, é necessário configurar o acesso a um banco de dados/esquema dedicado ou compartilhado. Recomendamos a criação de um esquema dedicado para a Composição federada de público-alvo e a cópia/compartilhamento somente dos conjuntos de dados de Business Case.
+++



+++Tenho acesso a todas as tabelas no esquema dedicado?

Sim, depois de conectado, a Composição federada de público-alvo pode ser usada para descobrir todas as tabelas com base nos direitos iniciais definidos. Em seguida, é possível usar o editor visual de esquema para:

* Descobrir colunas e chaves primárias a partir das tabelas
* Criar rótulos amigáveis para essas tabelas
* Criar rótulos amigáveis para cada coluna
* Ocultar colunas desnecessárias
* Salvar a descrição dessas tabelas
+++


+++Há algum armazenamento temporário na Composição federada de público-alvo?

Não, a Composição federada de público-alvo armazena apenas metadados (descrições de esquema). Nenhum dado do cliente está em trânsito. <!--The Audience export flow is done directly from Adobe Experience Platform Audience Portal (via [Destination](../connections/destinations.md)) to the customer database. The creation and update flow is done directly from your data warehouse database to Adobe Experience Platform Audience Portal.-->

+++

+++A Composição federada de público-alvo armazena uma cópia física dessa lista de pessoas para enviar a sistemas downstream?

A Composição federada de público-alvo não mantém uma cópia física dos dados. A frequência é configurada na composição para definir com que frequência esses dados serão atualizados. Os dados de público-alvo resultantes não são armazenados pela Adobe Experience Platform por mais tempo do que o exigido pelos casos de uso do cliente ou ação.

Por exemplo:

* A criação de um público-alvo ocorre em seu warehouse, e você pode contar com a Composição de público-alvo federado para tarefas adicionais de composição e manipulação de dados. Em seguida, o público-alvo resultante e os atributos associados podem ser publicados por meio do Portal de público-alvo da Adobe Experience Platform. A definição do público-alvo e os atributos associados são fornecidos para a Adobe Experience Platform.
Observe que a expiração dos dados atuais para públicos-alvo gerados externamente é de 30 dias. Essa expiração de dados reduz a quantidade de dados em excesso armazenados em uma organização. Depois que o período de expiração dos dados passar, o conjunto de dados associado ainda estará visível no inventário do conjunto de dados, mas não será possível ativar o público-alvo e a contagem de perfis será exibida como zero. Saiba mais na [Documentação da Adobe Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/segmentation/faq#how-long-do-externally-generated-audiences-last-for){target="_blank"}.

* No caso de um enriquecimento de público-alvo, o ponto de partida é um público-alvo da Adobe Experience Platform já existente. Você pode ver dois cenários aqui:
   1. Trazer atributos adicionais de conteúdo de público-alvo do data warehouse federado: nesse caso, os atributos adicionais incluídos aparecerão como parte dessa definição de público-alvo. A expiração de dados para públicos-alvo gerados externamente é a mesma descrita acima, 30 dias.
   1. Refine o público-alvo existente da Adobe Experience Platform com base em atributos adicionais existentes em seu data warehouse.<!--For example, you have an audience of customers who have shown interest in a particular product on the website for the last two months. You now want to take this audience and further segment it using Federated Audience Composition to only include customers who have a high credit score. The credit score is deemed sensitive and individual credit score data points are not copied over from the data warehouse.-->
+++

+++Se os dados para os padrões de casos de uso de criação e enriquecimento de público-alvo não estão sendo mantidos, como eles estão sendo armazenados temporariamente?

Os dados resultantes do público-alvo não persistem indefinidamente na Adobe Experience Platform ou na Composição federada de público-alvo. Eles não serão retidos por mais tempo do que o exigido por seu caso de uso. Os atributos de público-alvo trazidos como parte do conteúdo do público-alvo persistirão apenas como parte da definição do público-alvo. A duração da persistência é baseada no TTL para qualquer público-alvo. O padrão é 30 dias.

+++

+++É possível excluir um público-alvo personalizado enviado?

Não, na versão atual, não é possível excluir públicos-alvo personalizados carregados. <!--that are not used in downstream activation directly in Audience Portal by simply selecting delete from the actions menu. Learn more in [Adobe Experience Platform documentation](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/faq#how-do-i-put-an-audience-in-the-deleted-state){target="_blank"}.-->

+++

+++Se eu combinar dados de várias fontes, como estamos unindo os dados? Estamos usando o serviço de identidade?

Não, o Serviço de identidade não está sendo usado durante uma composição. Os dados entre as várias fontes usadas na composição são unidos por meio de uma lógica definida pelo usuário (conforme expresso no modelo subjacente), por exemplo, ID de CRM, número de conta do usuário, etc. Você deve selecionar a identidade usada como o identificador no público-alvo para a seleção no data warehouse. Em um público-alvo resultante da Composição federada de público-alvo, é necessário identificar o namespace de identidade da identidade no conjunto de dados resultante.

+++

<!--
+++If I want to combine federated data with datasets that live in Adobe Experience Platform, how is this done?

Likewise, the Identity Service is not being leveraged in this scenario either. The data model underpinning a composition needs to express how the data warehouse data and the audience to be enriched are related. e.g. assume an existing audience in Adobe Experience Platform contains several attributes, among which is the CRM ID. Assume transactional data is in the data warehouse containing purchases with various attributes, including the CRM ID of the purchaser. The end-user would have to specify that the CRM ID for both objects is used to stitch the two objects together.

+++
-->
