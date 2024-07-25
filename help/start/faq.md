---
title: Perguntas frequentes
description: Perguntas frequentes
badge: label="Disponibilidade limitada" type="Informative"
exl-id: 68cc0ae5-5c41-425f-8b10-ab3515294006
source-git-commit: b8cd36152433272277e7e694c8147211deae88bf
workflow-type: tm+mt
source-wordcount: '916'
ht-degree: 2%

---

# Perguntas frequentes {#faq}

Veja a seguir uma lista das perguntas frequentes sobre a Composição de público-alvo federado. As perguntas frequentes globais também estão disponíveis para o Serviço de Segmentação da Adobe Experience Platform em [esta página](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/faq){target="_blank"}.


+++Quais são as permissões necessárias para acessar o Federated Audience Composition?

Não há permissões específicas para a Composição de público-alvo federado. O único pré-requisito para acessar esse recurso é ter adquirido o complemento Federated Audience Composition.

+++

+++Quais depósitos na nuvem são compatíveis?

Para esta versão, o Federated Audience Composition é compatível com:

* Amazon Redshift
* Azure synapse
* Google Big Query
* Snowflake
* Vertica Analytics

+++


+++É possível consultar vários data warehouses na mesma composição?

Sim, vários depósitos podem ser consultados na mesma composição e podem combinar dados de várias origens.  Normalmente, cada [atividade de composição](../compositions/orchestrate-activities.md) (Query, Enriquecimento, Split, etc.) O executa uma ou várias instruções SQL dependendo da configuração da atividade, dos bancos de dados de destino (pode haver vários casos de acesso a dados federados) e das saídas de uma ou mais tabelas de trabalho com o resultado da execução. Essas tabelas de trabalho são usadas como entrada para atividades consecutivas.

+++

+++ Posso acessar todo o meu banco de dados usando a Composição de público-alvo federado?

Não, depende de você configurar o acesso a um banco de dados/esquema dedicado ou compartilhado. Recomendamos que você crie um esquema dedicado para a Composição de público-alvo federado e copie/compartilhe conjuntos de dados de business case somente.
+++



+++Tenho acesso a todas as tabelas no esquema dedicado?

Sim, depois de conectado, a Federated Audience Composition pode ser usada para descobrir todas as tabelas com base nos direitos iniciais definidos, então você pode usar o editor visual de esquema para:

* Descobrir colunas e chaves primárias a partir das tabelas
* Criar rótulos amigáveis para essas tabelas
* Criar rótulos amigáveis para cada coluna
* Ocultar colunas desnecessárias
* Salvar a descrição dessas tabelas
+++


+++Há algum armazenamento temporário na Federated Audience Composition?

Não, a Federated Audience Composition armazena apenas metadados (descrições de esquema). Nenhum dado do cliente está em trânsito. O fluxo de exportação de público é feito diretamente do Portal de público-alvo da Adobe Experience Platform (via [Destino](../connections/destinations.md)) para o banco de dados do cliente. O fluxo de criação e atualização é feito diretamente do banco de dados do data warehouse para o Adobe Experience Platform Audience Portal.

+++

+++A Federated Audience Composition armazena uma cópia física dessa lista de pessoas para enviar a sistemas downstream?

A Federated Audience Composition não mantém uma cópia física dos dados. A frequência é configurada na composição para definir com que frequência esses dados serão atualizados. Os dados do público-alvo resultantes não são armazenados pela Adobe Experience Platform por mais tempo do que o exigido pelos casos de uso ou pela ação do cliente.

Por exemplo:

* No caso de uma Criação de público-alvo, o público-alvo é criado no warehouse e você pode usar a Composição de público-alvo federado para tarefas de composição adicionais e manipulação de dados antes de publicar o público-alvo resultante e os atributos associados pelo Adobe Experience Platform Audience Portal. A definição do público-alvo e os atributos associados são fornecidos para o Adobe Experience Platform.
Observe que a expiração dos dados atuais para públicos-alvo gerados externamente é de 30 dias. Essa expiração de dados reduz a quantidade de dados em excesso armazenados em uma organização. Depois que o período de expiração dos dados passar, o conjunto de dados associado ainda estará visível no inventário do conjunto de dados, mas você não poderá ativar o público-alvo e a contagem de perfis será exibida como zero. Saiba mais em [documentação do Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/faq#how-long-do-externally-generated-audiences-last-for){target="_blank"}.

* No caso de um Enriquecimento de público-alvo, o ponto de partida é um público-alvo existente do Adobe Experience Platform. Você pode ver dois cenários aqui:
   1. Trazer atributos adicionais de carga de público-alvo do federated data warehouse: nesse caso, os atributos adicionais que são adicionados aparecerão como parte dessa definição de público-alvo. A expiração dos dados para públicos-alvo gerados externamente é a mesma descrita acima, 30 dias.
   1. Refine o público-alvo existente do Adobe Experience Platform com base nos atributos adicionais existentes no data warehouse. Por exemplo, você tem um público-alvo de clientes que demonstraram interesse em um produto específico no site nos últimos dois meses. Agora, você deseja segmentar esse público e segmentá-lo ainda mais usando a Composição de público federado para incluir apenas clientes que têm uma pontuação de crédito alta. A pontuação de crédito é considerada confidencial e os pontos de dados individuais da pontuação de crédito não são copiados do data warehouse.
+++

+++Se os dados para padrões de casos de uso de Criação de público-alvo e Enriquecimento de público não estiverem sendo mantidos, como eles estão sendo armazenados temporariamente?

Os dados resultantes do Público-alvo não persistem indefinidamente no Adobe Experience Platform ou na Composição do Público-alvo federado. Ele não será retido por mais tempo do que o exigido por seu caso de uso. Os atributos de público-alvo trazidos como parte da carga do público-alvo persistirão apenas como parte da definição do público-alvo. A duração da persistência é baseada no TTL para qualquer público-alvo. O padrão é 30 dias.

+++

+++É possível excluir um público-alvo carregado personalizado?

Você pode excluir públicos-alvo que não são usados na ativação downstream diretamente no Portal de público-alvo simplesmente selecionando Excluir no menu de ações. Saiba mais em [documentação do Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/faq#how-do-i-put-an-audience-in-the-deleted-state){target="_blank"}.

+++

+++Se eu combinar dados de várias fontes, como estamos unindo os dados? Estamos usando o serviço de identidade?

Não, o Serviço de identidade não está sendo aproveitado durante uma composição. Os dados entre as várias fontes usadas na composição são unidos por meio de uma lógica definida pelo usuário (conforme expresso no modelo subjacente), por exemplo, ID de CRM, número de conta do usuário etc. Você deve selecionar a identidade usada como o identificador no público-alvo para seleção no data warehouse. Em um público-alvo resultante da Composição de público-alvo federado, é necessário identificar o namespace de identidade da identidade no conjunto de dados resultante.

+++

<!--
+++If I want to combine federated data with datasets that live in Adobe Experience Platform, how is this done?

Likewise, the Identity Service is not being leveraged in this scenario either. The data model underpinning a composition needs to express how the data warehouse data and the audience to be enriched are related. e.g. assume an existing audience in Adobe Experience Platform contains several attributes, among which is the CRM ID. Assume transactional data is in the data warehouse containing purchases with various attributes, including the CRM ID of the purchaser. The end-user would have to specify that the CRM ID for both objects is used to stitch the two objects together.

+++
-->
