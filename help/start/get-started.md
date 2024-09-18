---
title: Introdução à Composição de público-alvo federado da Experience Platform
description: Saiba o que é a Composição de público-alvo federado da Adobe e como usá-la na Adobe Experience Platform
badge: label="Disponibilidade limitada" type="Informative"
exl-id: 43464aea-9c1d-4f1f-859f-82f209f350b7
source-git-commit: 8b67aa9258b05a6ca239dd54ebb10273826ea550
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 97%

---

# Introdução à Composição de público-alvo federado {#gs-fac}

A Composição de público-alvo federado é um complemento para a [Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/segmentation/home){target="_blank"} e o [Adobe Journey Optimizer](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/ajo-home){target="_blank"} com o qual é possível criar e enriquecer públicos-alvos a partir de data warehouses de terceiros e importá-los para a Adobe Experience Platform. A Composição de público-alvo federado oferece uma solução fácil e eficiente para conectar o seu data warehouse corporativo diretamente à Adobe Real-time Customer Data Platform e/ou Adobe Journey Optimizer e realizar consultas nas tabelas do seu data warehouse.

A Composição de público-alvo federado da Adobe ajuda os usuários de aplicativos da Adobe Experience Platform a acessar os dados de clientes armazenados nos data warehouses e plataformas de armazenamento na nuvem, como o Amazon Redshift, o Azure Synapse Analytics entre outros. Os dados do cliente podem residir em vários data warehouses e agora podem ser acessados instantaneamente, sem replicação. As plataformas compatíveis são listadas [nesta página](../connections/federated-db.md#supported-db).

## Recursos {#rn-capabilities}

A Composição de público-alvo federado amplia o valor da Real-Time CDP e do Journey Optimizer com uma abordagem abrangente em relação à curadoria e ativação de público-alvo:

* Amplie o acesso a conjuntos de dados críticos baseados em data warehouse para criar públicos-alvo de alto valor: utilize data warehouses existentes como o principal sistema de registro e, ao mesmo tempo, aproveite os melhores aplicativos do setor para potencializar excelentes experiências do cliente.

* Suporte abrangente para casos de uso de engajamento avançado: a Composição de público-alvo federado, juntamente com a Real-Time CDP ou o Journey Optimizer, oferece suporte a experiências personalizadas iniciadas pela marca com públicos-alvo federados e fornece experiências instantâneas acionadas por eventos em tempo real, combinadas com atributos pessoais para atender aos requisitos de caso de uso em todas as equipes.

* Minimizar a movimentação e a duplicação de dados: crie públicos-alvo de conjuntos de dados contidos em um data warehouse corporativo sem copiar dados subjacentes para gerenciar perfis e públicos-alvo de marketing acionáveis.

* Utilize um único sistema para fluxos de trabalho orientados por experiência: prepare públicos-alvo assimilados e federados na Adobe Experience Platform e coordene experiências de saída em todos os canais.

## Casos de uso {#rn-uc}

Por meio de uma interface amigável de marketing, crie regras de segmento que consultem o data warehouse para obter uma lista de usuários que se qualificam para um segmento específico necessário para campanhas de marketing, acesse públicos do warehouse para ativação ou enriqueça os públicos-alvo da Adobe Experience Platform com pontos de dados adicionais do warehouse.

Nesta versão, dois casos de uso estão disponíveis:

1. Criação de público-alvo: crie novos públicos-alvo a partir de conjuntos de dados corporativos sem copiar os dados subjacentes e ative-os com destinos pré-criados.

1. Enriquecimento de público-alvo: enriqueça os públicos-alvo existentes na Adobe Experience Platform utilizando dados de públicos-alvo compostos que foram federados a partir do data warehouse corporativo. Esses dados não serão mantidos nos perfis de clientes da Adobe Experience Platform.

![diagrama](assets/fac-use-cases.png){zoomable="yes"}{width="75%" align="center"}

## Principais etapas {#gs-steps}

A Composição de público-alvo federado da Adobe permite criar e atualizar públicos-alvo da Adobe Experience Platform diretamente do seu banco de dados, sem nenhum processo de ingestão.

<!--![diagram](assets/steps-diagram.png){zoomable="yes"}{width="85%" align="center"}-->

Etapas principais:

1. **Integração de Dados**: reúna dados de várias fontes e mescle-os em um conjunto de dados unificado. Saiba como conectar aplicativos da Adobe Experience Platform a seu data warehouse corporativo, quais bancos de dados são compatíveis e como configurá-los [nesta seção](../connections/federated-db.md).

1. **Modelagem de dados**: projete e crie modelos de dados e esquemas que definam a estrutura, as relações e as restrições dos dados. Saiba mais sobre esquemas [nesta página](../customer/schemas.md). Aprenda a criar links para o modelo de dados [nesta página](../data-management/gs-models.md).

1. **Transformação de dados**: aplique técnicas de manipulação de dados para modificar o formato, a estrutura ou os valores de elementos de dados para torná-los compatíveis ou adequados para análise ou aplicativos específicos.

1. **Uso de dados**: crie, orquestre e construa públicos-alvo. Saiba como compor públicos-alvo [nesta página](../compositions/gs-compositions.md). Também é possível atualizar ou reutilizar públicos-alvo por meio do Portal de público-alvo da Adobe Experience Platform e destinos. Saiba mais [nesta página](../connections/destinations.md)

>[!NOTE]
>
>Depois de executar a composição, o público-alvo resultante é salvo como externo na Adobe Experience Platform e disponibilizado na Adobe Real-time Customer Data Platform e/ou no Adobe Journey Optimizer. Ele é disponibilizado no menu **Públicos-alvo**. [Saiba mais](https://experienceleague.adobe.com/pt-br/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}

## Saiba mais {#learn}

<!-- Workflow + Workflow activities-->


Saiba como acessar a Composição de público-alvo federado, as medidas de proteção e as limitações [nesta página](access-prerequisites.md).

Veja também as perguntas frequentes [nesta página](faq.md).


>[!CONTEXTUALHELP]
>id="dc_workflow_settings_execution"
>title="Configurações de execução"
>abstract="Nesta seção, é possível definir as configurações relacionadas à execução do fluxo de trabalho, de modo que o número de dias do histórico da composição seja mantido."

>[!CONTEXTUALHELP]
>id="dc_orchestration_query_enrichment_noneditable"
>title="Atividade não editável"
>abstract="Quando uma atividade de **Consulta** ou **Enriquecimento** é configurada com dados adicionais no console, os dados de enriquecimento são levados em consideração e transmitidos para a transição de saída, mas não podem ser editados."

<!-- Create a link -->

>[!CONTEXTUALHELP]
>id="dc_federated_database_create_link"
>title="Criar um link"
>abstract="Defina as configurações do link."
