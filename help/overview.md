---
title: Visão geral da composição do Federated Audience
description: Saiba mais sobre a Composição de público federado do Adobe e como usá-la em serviços downstream, como o Adobe Experience Platform e o Adobe Journey Optimizer
exl-id: 43464aea-9c1d-4f1f-859f-82f209f350b7
source-git-commit: 65a69bf857ec1a0701534693600a8c6340179838
workflow-type: tm+mt
source-wordcount: '1203'
ht-degree: 51%

---

# Visão geral da composição do Federated Audience

A Composição de público-alvo federado permite criar e enriquecer públicos-alvo de data warehouses de terceiros e importar os públicos-alvo para a Adobe Experience Platform. Isso oferece uma solução fácil e eficiente para conectar seu data warehouse corporativo diretamente a serviços downstream como Adobe Real-Time Customer Data Platform ou Adobe Journey Optimizer e realizar consultas nas tabelas do data warehouse. Como resultado, você pode acessar os dados do cliente armazenados em data warehouses e plataformas de armazenamento na nuvem, como o Amazon Redshift e o Azure Synapse Analytics.

## Recursos {#rn-capabilities}

A Composição de público-alvo federado amplia o valor da Real-Time CDP e do Journey Optimizer com uma abordagem abrangente em relação à curadoria e ativação de público-alvo:

* **Expanda o acesso a conjuntos de dados críticos baseados em warehouse para criar públicos-alvo de alto valor**: você pode usar data warehouses existentes como o principal sistema de registro, aproveitando os melhores aplicativos para potencializar experiências de cliente excelentes.

* **Suporte abrangente para casos de uso de engajamento avançado**: a Federated Audience Composition, combinada com a Real-Time CDP ou a Journey Optimizer, oferece suporte a experiências personalizadas iniciadas pela marca com públicos federados e fornece experiências no momento acionadas por eventos em tempo real, combinadas com atributos de pessoa para atender aos requisitos de caso de uso em todas as equipes.

* **Minimizar a movimentação e a duplicação de dados**: você pode criar públicos-alvo a partir de conjuntos de dados que residem em data warehouses corporativos sem copiar os dados subjacentes para gerenciar perfis e públicos de marketing acionáveis.

* **Utilizar um único sistema para fluxos de trabalho orientados por experiência**: você pode preparar públicos assimilados e federados na Adobe Experience Platform e coordenar experiências de saída em todos os canais.

* **Suporte a várias edições**: os clientes de CDP B2C e B2B podem aproveitar a Federated Audience Composition para criar públicos com base em pessoas, integrando dados de data warehouses empresariais compatíveis. Além disso, elas podem enriquecer os públicos-alvo com base em pessoas do Experience Platform incorporando atributos relevantes disponíveis no data warehouse corporativo, aprimorando seus perfis de público-alvo para um envolvimento mais personalizado e direcionado.

## Casos de uso {#use-cases}

A composição de público-alvo federado oferece suporte a **três** categorias de casos de uso: criação de público-alvo, enriquecimento de público-alvo e enriquecimento de perfil do cliente.

* **Criação de público-alvo**: você pode criar públicos-alvo de um data warehouse e federá-los no Experience Platform para uso no Real-Time CDP ou no Journey Optimizer por meio de uma interface de usuário de arrastar e soltar amigável para profissionais de marketing. Como resultado, você pode consultar seus data warehouses sem copiar dados subjacentes confidenciais ou duplicar dados existentes.
   * **Exemplo:** crie um público-alvo de compradores anteriores de alto valor usando dados de transações de histórico no warehouse, sem copiar essas transações para a Experience Platform.

* **Enriquecimento de público-alvo**: você pode adicionar mais detalhes aos seus públicos-alvo existentes no Experience Platform usando conjuntos de dados adicionais de seus data warehouses e sobrepondo seus públicos-alvo com essas informações - tudo isso sem copiar os dados subjacentes para o Experience Platform. Com o enriquecimento de público-alvo, você pode fornecer uma personalização aprimorada com o público-alvo enriquecido.
   * **Exemplo:** enriqueça um público-alvo da Experience Platform de pessoas que abandonaram o carrinho com o público-alvo de composição de público-alvo federado de compradores anteriores de alto valor para fornecer uma oferta direcionada.

* **Enriquecimento de perfil**: você pode selecionar atributos de clientes individuais no data warehouse para aprimorar os perfis do Experience Platform. Com dados federados adicionados a esses perfis, você pode potencializar melhor as experiências instantâneas acionadas pelos sinais de entrada do cliente.
   * **Exemplo:** enriqueça um perfil da Experience Platform com informações do público-alvo federado. Agora você pode anunciar para um visitante do site que pertence ao público-alvo federado de compradores anteriores de alto valor com uma oferta direcionada que é acionada por seu comportamento no site.

![diagrama](assets/overview/fac-use-cases.png){zoomable="yes"}{width="75%" align="center"}

Para obter mais informações sobre casos de uso da composição de público-alvo federado, leia o [whitepaper Composição de público-alvo federado](https://business.adobe.com/resources/sdk/flexibly-access-enterprise-data-with-federated-audience-composition.html).

## Principais etapas {#gs-steps}

A Composição de público-alvo federado da Adobe permite criar e atualizar públicos-alvo da Adobe Experience Platform diretamente do seu banco de dados, sem nenhum processo de ingestão.

<!--![diagram](assets/steps-diagram.png){zoomable="yes"}{width="85%" align="center"}-->

1. **Criar uma conexão**: reúna dados de várias fontes e mescle-os em um conjunto de dados unificado. Para obter mais informações sobre como conectar aplicativos Adobe Experience Platform ao data warehouse da sua empresa, bancos de dados com suporte e configurar sua conexão, leia a [visão geral das conexões](./connections/home.md).

2. **Modelar seus dados**: projete e crie esquemas e modelos de dados que definam a estrutura, as relações e as restrições dos dados. Para obter mais informações sobre esquemas, leia a [visão geral do esquema](./data-modelling/schemas.md). Para obter mais informações sobre modelos de dados, leia a [visão geral do modelo de dados](./data-modelling/models.md).

3. **Transformar seus dados**: aplique técnicas de manipulação de dados para modificar o formato, a estrutura ou os valores dos elementos de dados para torná-los compatíveis ou adequados para análises ou aplicativos específicos.

4. **Compor seu público-alvo**: crie, organize e compile públicos-alvo. Para obter mais informações sobre a composição de públicos, leia a [visão geral da composição](./compositions/home.md). Também é possível atualizar ou reutilizar públicos-alvo por meio do portal de público-alvo da Adobe Experience Platform e destinos. Saiba mais [nesta página](./connections/destinations.md)

>[!NOTE]
>
>Depois de executar a composição, o público-alvo resultante é salvo como externo na Adobe Experience Platform e disponibilizado na Adobe Real-time Customer Data Platform e/ou no Adobe Journey Optimizer. Ele é disponibilizado no menu **Públicos-alvo**. [Saiba mais](https://experienceleague.adobe.com/pt-br/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}

## Governança, privacidade e segurança {#governance-privacy-security}

### Solicitações de privacidade {#gov-privacy-requests}

Depois de criar uma composição, os públicos-alvo resultantes são salvos na Adobe Experience Platform.

É possível fazer solicitações de privacidade para acessar e/ou excluir dados de perfil correspondentes a esses públicos-alvo por meio do Adobe Experience Platform **Privacy Service**, que fornece uma [interface](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=pt-BR){target="_blank"} e uma [API RESTful](https://experienceleague.adobe.com/pt-br/docs/experience-platform/privacy/api/overview){target="_blank"} para ajudar a gerenciar solicitações de dados de clientes.

>[!NOTE]
>
>Para mais informações sobre o Privacy Service, consulte a [documentação da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=pt-BR){target="_blank"}.

É possível criar e gerenciar solicitações individuais para acessar e excluir dados de clientes da composição de público-alvo federado da Adobe. As etapas para enviar **solicitações de acesso** e **solicitações de exclusão** estão detalhadas na [documentação do perfil do cliente em tempo real](https://experienceleague.adobe.com/pt-br/docs/experience-platform/profile/privacy){target="_blank"}.

### Trilha de auditoria {#gov-audit-trail}

O recurso de trilha de auditoria fornece um registro detalhado e cronológico de todas as ações e eventos que foram feitos em seu ambiente em tempo real. Para saber mais sobre a trilha de auditoria, leia a [visão geral da trilha de auditoria](./admin/audit-trail.md).

## Saiba mais {#learn}

<!-- Workflow + Workflow activities-->

Saiba como acessar a Composição de público-alvo federado, as medidas de proteção e as limitações [nesta página](./start/access-prerequisites.md).

Para obter respostas para perguntas frequentes, leia as [Perguntas frequentes sobre a Composição do Público-Alvo Federado](./faq.md).

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


<!-- incremental query IDs -->

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery"
>title="Consulta incremental"
>abstract="A atividade **Consulta incremental** permite consultar o banco de dados usando o Modelador de consulta. Todas as vezes que essa atividade é executada, os resultados das execuções anteriores são excluídos. Ela permite direcionar somente elementos novos."

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery_history"
>title="Histórico de consultas incrementais"
>abstract="Histórico de consultas incrementais"

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery_processeddata"
>title="Dados processados da consulta incremental"
>abstract="Dados processados da consulta incremental"

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalmode_standard"
>title="Modo consulta incremental"
>abstract="O query incremental permite realizar a mesma consulta várias vezes, excluindo os resultados das anteriores a cada nova execução."

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalmode_custom"
>title="Modo consulta incremental"
>abstract="O query incremental permite realizar a mesma consulta várias vezes, considerando apenas os resultados em que o campo de data é posterior ou igual à data da última execução da atividade de query incremental."

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience_dimension"
>title="Selecione a dimensão de direcionamento"
>abstract="A dimensão de direcionamento permite definir a população-alvo da operação: destinatários, beneficiários(as) de contrato, operadores(as), assinantes, etc. Por padrão, para emails e SMS, o público-alvo é selecionado na tabela integrada Destinatários. Para notificações por push, a dimensão de direcionamento padrão é Aplicativos do assinante."

