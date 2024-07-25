---
title: Introdução à composição de público-alvo federado do Experience Platform
description: Saiba o que é a composição de público-alvo federado do Adobe e como usá-la no Adobe Experience Platform
badge: label="Disponibilidade limitada" type="Informative"
exl-id: 43464aea-9c1d-4f1f-859f-82f209f350b7
source-git-commit: 75f997e4b1c0338a635dff43e2254757fbc5ec69
workflow-type: tm+mt
source-wordcount: '708'
ht-degree: 8%

---

# Introdução à composição de público-alvo federado {#gs-fac}

A Federated Audience Composition é um recurso complementar do [Adobe Real-time Customer Data Platform](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/home){target="_blank"} e do [Adobe Journey Optimizer](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/ajo-home?lang=pt-BR){target="_blank"} que permite compilar e enriquecer públicos de data warehouses de terceiros e importar os públicos para a Adobe Experience Platform. A Federated Audience Composition oferece uma solução fácil e eficiente para conectar seu data warehouse corporativo diretamente na Adobe Real-time Customer Data Platform e/ou Adobe Journey Optimizer e realizar consultas nas tabelas de seu data warehouse.

A Composição de público-alvo federado do Adobe ajuda os usuários de aplicativos da Adobe Experience Platform a acessar os dados de clientes armazenados em seus data warehouses e plataformas de armazenamento na nuvem, como o Amazon Redshift, o Azure synapse Analytics e muito mais. Os dados do cliente podem residir em vários data warehouses e agora podem ser acessados instantaneamente, sem replicação. As plataformas com suporte estão listadas em [esta página](../connections/federated-db.md#supported-db).

## Capacidades {#rn-capabilities}

A Federated Audience Composition amplia o valor do Real-Time CDP e do Journey Optimizer com uma abordagem abrangente para a curadoria e ativação de público:

* Amplie o acesso a conjuntos de dados críticos baseados em data warehouse para criar públicos de alto valor: utilize data warehouses existentes como o principal sistema de registro e, ao mesmo tempo, aproveite os melhores aplicativos do setor para potencializar excelentes experiências do cliente.

* Suporte abrangente para casos de uso de envolvimento avançado: a Federated Audience Composition, combinada com o Real-Time CDP ou o Journey Optimizer, oferece suporte a experiências personalizadas iniciadas pela marca com públicos federados e fornece experiências instantâneas acionadas por eventos em tempo real, combinadas com atributos de pessoa para atender aos requisitos de caso de uso em todas as equipes.

* Minimizar a movimentação e a duplicação de dados: crie públicos-alvo a partir de conjuntos de dados que residem em um data warehouse corporativo sem copiar dados subjacentes para gerenciar perfis e públicos de marketing acionáveis.

* Utilize um único sistema para fluxos de trabalho orientados por experiência: prepare públicos-alvo assimilados e federados no Adobe Experience Platform e coordene experiências de saída em todos os canais.

## Casos de uso {#rn-uc}

Por meio de uma interface amigável de marketing, crie regras de segmento que consultem seu data warehouse para obter uma lista de usuários que se qualificam para um segmento específico necessário para campanhas de marketing, acesse públicos existentes no warehouse para ativação ou enriqueça os públicos-alvo da Adobe Experience Platform com pontos de dados adicionais que existem no warehouse.

Nesta versão, dois casos de uso estão disponíveis:

1. Criação de público-alvo: crie novos públicos-alvo a partir de conjuntos de dados corporativos sem copiar os dados subjacentes e ative-os com destinos pré-criados.&#x200B;

1. Enriquecimento de público-alvo: enriqueça os públicos-alvo existentes no Adobe Experience Platform utilizando dados de público-alvo compostos que foram federados a partir do data warehouse corporativo. Esses dados não serão mantidos nos perfis de clientes do Adobe Experience Platform.

![diagrama](assets/fac-use-cases.png){zoomable="yes"}{width="75%" align="center"}

## Principais etapas {#gs-steps}

A composição do público-alvo federado do Adobe permite criar e atualizar públicos-alvo do Adobe Experience Platform diretamente do banco de dados, sem nenhum processo de assimilação.

![diagrama](assets/steps-diagram.png){zoomable="yes"}{width="85%" align="center"}

Principais etapas:

1. **Integração de dados**: reúna dados de várias fontes e mescle-os em um conjunto de dados unificado. Saiba como conectar aplicativos Adobe Experience Platform e seu data warehouse corporativo, bancos de dados com suporte e como configurá-los estão detalhados em [esta seção](../connections/federated-db.md).

2. **Modelagem de Dados**: projete e crie modelos de dados e esquemas que definam a estrutura, as relações e as restrições dos dados. Saiba mais sobre esquemas em [esta página](../customer/schemas.md). Saiba como criar links para seu modelo de dados no [nesta página](../data-management/gs-models.md).

3. **Transformação de Dados**: aplique técnicas de manipulação de dados para modificar o formato, a estrutura ou os valores de elementos de dados para torná-los compatíveis ou adequados para análise ou aplicativos específicos.

4. **Uso de dados**: crie, organize e compile públicos-alvo. Saiba como compor públicos-alvo em [esta página](../compositions/gs-compositions.md). Você também pode atualizar ou reutilizar públicos-alvo existentes por meio do portal de público-alvo e de Destinos da Adobe Experience Platform. Saiba mais [nesta página](../connections/destinations.md)


>[!NOTE]
>
>Depois de executar a composição, o público resultante é salvo na Adobe Experience Platform como um público externo e disponível no Adobe Real-time Customer Data Platform e/ou no Adobe Journey Optimizer. Ele se tornou acessível no menu **Públicos-alvo**. [Saiba mais](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}
>



## Saiba mais {#learn}

<!-- Workflow + Workflow activities-->

Consulte as Perguntas Frequentes em [esta página](faq.md).

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_execution"
>title="Configurações de execução"
>abstract="Nesta seção, você pode definir configurações relacionadas à execução do fluxo de trabalho, como o número de dias em que o histórico de composição é mantido."




>[!CONTEXTUALHELP]
>id="dc_orchestration_query_enrichment_noneditable"
>title="Atividade não editável"
>abstract="Quando uma atividade de **Consulta** ou **Enriquecimento** é configurada com dados adicionais no console, os dados de enriquecimento são levados em consideração e transmitidos para a transição de saída, mas não podem ser editados."

<!-- Create a link -->

>[!CONTEXTUALHELP]
>id="dc_federated_database_create_link"
>title="Criar um link"
>abstract="Defina as configurações do link."
