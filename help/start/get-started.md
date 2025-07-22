---
title: Introdução à Composição de público-alvo federado da Experience Platform
description: Saiba o que é a Composição de público-alvo federado da Adobe e como usá-la na Adobe Experience Platform
exl-id: 43464aea-9c1d-4f1f-859f-82f209f350b7
source-git-commit: bb3e01b11d34568b61fdd98eedaa59af5267fd87
workflow-type: tm+mt
source-wordcount: '1236'
ht-degree: 76%

---

# Introdução à Composição de público-alvo federado {#gs-fac}

A Composição de público-alvo federado está disponível para ambientes da [Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/segmentation/home){target="_blank"} e do [Adobe Journey Optimizer](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/ajo-home){target="_blank"}. Ela permite que clientes criem e enriqueçam públicos-alvo de warehouses de dados externas e importem esses públicos-alvo para a Adobe Experience Platform. A Composição de público-alvo federado oferece uma solução fácil e eficiente para conectar o seu data warehouse corporativo diretamente à Adobe Real-time Customer Data Platform e/ou Adobe Journey Optimizer e realizar consultas nas tabelas do seu data warehouse.

A Composição de público-alvo federado da Adobe ajuda os usuários de aplicativos da Adobe Experience Platform a acessar os dados de clientes armazenados nos data warehouses e plataformas de armazenamento na nuvem, como o Amazon Redshift, o Azure Synapse Analytics entre outros. Os dados do cliente podem residir em vários data warehouses e agora podem ser acessados instantaneamente, sem replicação. As plataformas compatíveis estão listadas [nesta página](../connections/federated-db.md#supported-db).

>[!INFO]
>
>Siga este [guia passo a passo](https://experienceleague.adobe.com/pt-br/docs/platform-learn/tutorial-comprehensive-technical/datacollection/module13/fac) para saber como criar públicos-alvo usando a composição de público-alvo federado.

## Recursos {#rn-capabilities}

A Composição de público-alvo federado amplia o valor da Real-Time CDP e do Journey Optimizer com uma abordagem abrangente em relação à curadoria e ativação de público-alvo:

* Amplie o acesso a conjuntos de dados críticos baseados em data warehouse para criar públicos-alvo de alto valor: utilize data warehouses existentes como o principal sistema de registro e, ao mesmo tempo, aproveite os melhores aplicativos do setor para potencializar excelentes experiências do cliente.

* Suporte abrangente para casos de uso de engajamento avançado: a Composição de público-alvo federado, juntamente com a Real-Time CDP ou o Journey Optimizer, oferece suporte a experiências personalizadas iniciadas pela marca com públicos-alvo federados e fornece experiências instantâneas acionadas por eventos em tempo real, combinadas com atributos pessoais para atender aos requisitos de caso de uso em todas as equipes.

* Minimizar a movimentação e a duplicação de dados: crie públicos-alvo de conjuntos de dados contidos em um data warehouse corporativo sem copiar dados subjacentes para gerenciar perfis e públicos-alvo de marketing acionáveis.

* Utilize um único sistema para fluxos de trabalho orientados por experiência: prepare públicos-alvo assimilados e federados na Adobe Experience Platform e coordene experiências de saída em todos os canais.

* Os clientes da CDP B2C e B2B agora podem aproveitar a Composição de público-alvo federado para criar públicos-alvo com base em pessoas, integrando dados de data warehouses empresariais compatíveis. Além disso, eles podem enriquecer os públicos-alvo já existentes da AEP incorporando atributos relevantes disponíveis no data warehouse empresarial, aprimorando seus perfis de público-alvo para um engajamento mais personalizado e direcionado.

## Casos de uso {#use-cases}

A Federated Audience Composition oferece suporte a **três** categorias de casos de uso: criação de público, enriquecimento de público e enriquecimento de perfil do cliente.

* Criação de público-alvo: você pode criar públicos-alvo a partir de um data warehouse e federá-los no Experience Platform para uso no Real-Time CDP ou no Journey Optimizer por meio de uma interface de usuário de arrastar e soltar amigável para profissionais de marketing. Como resultado, você pode consultar seus data warehouses sem copiar dados subjacentes confidenciais ou duplicar dados existentes.
   * **Exemplo:** crie um público-alvo de compradores anteriores de alto valor usando dados de transações de histórico no depósito, sem copiar essas transações para o Experience Platform.

* Enriquecimento de público: você pode adicionar mais detalhes aos públicos existentes no Experience Platform usando conjuntos de dados adicionais dos data warehouses e sobrepondo seus públicos-alvo com essas informações, tudo sem copiar os dados subjacentes para o Experience Platform. Com o enriquecimento de público, você pode fornecer personalização aprimorada com o público enriquecido.
   * **Exemplo:** enriqueça um público-alvo de abandonadores de carrinho do Experience Platform com o público-alvo de Composição de público-alvo de compradores anteriores de alto valor para fornecer uma oferta direcionada.

* Enriquecimento de perfil: você pode selecionar atributos de clientes individuais no data warehouse para aprimorar os perfis do Experience Platform. Com dados federados adicionados a esses perfis, você pode potencializar melhor as experiências instantâneas acionadas pelos sinais de entrada do cliente.
   * **Exemplo:** enriqueça um perfil do Experience Platform com informações do público federado. Agora você pode vender para um visitante do site que pertence ao público federado de compradores anteriores de alto valor com uma oferta direcionada que é acionada por seu comportamento no site.

![diagrama](assets/fac-use-cases.png){zoomable="yes"}{width="75%" align="center"}

Para obter mais informações sobre casos de uso da Composição de Público Federado, leia o [whitepaper Composição de Público Federado](https://business.adobe.com/resources/sdk/flexibly-access-enterprise-data-with-federated-audience-composition.html).

## Principais etapas {#gs-steps}

A Composição de público-alvo federado da Adobe permite criar e atualizar públicos-alvo da Adobe Experience Platform diretamente do seu banco de dados, sem nenhum processo de ingestão.

<!--![diagram](assets/steps-diagram.png){zoomable="yes"}{width="85%" align="center"}-->

Etapas principais:

1. **Integração de Dados**: reúna dados de várias fontes e mescle-os em um conjunto de dados unificado. Saiba como conectar aplicativos da Adobe Experience Platform a seu data warehouse corporativo, quais bancos de dados são compatíveis e como configurá-los [nesta seção](../connections/federated-db.md).

1. **Modelagem de dados**: projete e crie modelos de dados e esquemas que definam a estrutura, as relações e as restrições dos dados. Saiba mais sobre esquemas [nesta página](../customer/schemas.md). Saiba como criar links para o modelo de dados [nesta página](../data-management/gs-models.md).

1. **Transformação de dados**: aplique técnicas de manipulação de dados para modificar o formato, a estrutura ou os valores de elementos de dados para torná-los compatíveis ou adequados para análise ou aplicativos específicos.

1. **Uso de dados**: crie, orquestre e construa públicos-alvo. Saiba como compor públicos-alvo [nesta página](../compositions/gs-compositions.md). Também é possível atualizar ou reutilizar públicos-alvo por meio do portal de público-alvo da Adobe Experience Platform e destinos. Saiba mais [nesta página](../connections/destinations.md)

>[!NOTE]
>
>Depois de executar a composição, o público-alvo resultante é salvo no Adobe Experience Platform como um público-alvo externo e está disponível no Adobe Real-Time Customer Data Platform e/ou Adobe Journey Optimizer. Ele é disponibilizado no menu **Públicos-alvo**. [Saiba mais](https://experienceleague.adobe.com/pt-br/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}

## Governança, privacidade e segurança {#governance-privacy-security}

### Solicitações de privacidade {#gov-privacy-requests}

Depois de criar uma composição, os públicos-alvo resultantes são salvos na Adobe Experience Platform.

É possível fazer solicitações de privacidade para acessar e/ou excluir dados de perfil correspondentes a esses públicos-alvo por meio do Adobe Experience Platform **Privacy Service**, que fornece uma [interface](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=pt-BR){target="_blank"} e uma [API RESTful](https://experienceleague.adobe.com/pt-br/docs/experience-platform/privacy/api/overview){target="_blank"} para ajudar a gerenciar solicitações de dados de clientes.

>[!NOTE]
>
>Para mais informações sobre o Privacy Service, consulte a [documentação da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=pt-BR){target="_blank"}.

É possível criar e gerenciar solicitações individuais para acessar e excluir dados de clientes da composição de público-alvo federado da Adobe. As etapas para enviar **solicitações de acesso** e **solicitações de exclusão** estão detalhadas na [documentação do perfil do cliente em tempo real](https://experienceleague.adobe.com/pt-br/docs/experience-platform/profile/privacy){target="_blank"}.

### Trilha de auditoria {#gov-audit-trail}

O recurso de trilha de auditoria fornece um registro detalhado e cronológico de todas as ações e eventos que ocorreram no ambiente em tempo real. [Saiba mais](../admin/audit-trail.md)

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
>title="Modo query incremental"
>abstract="O query incremental permite realizar a mesma consulta várias vezes, excluindo os resultados das anteriores a cada nova execução."

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalmode_custom"
>title="Modo query incremental"
>abstract="O query incremental permite realizar a mesma consulta várias vezes, considerando apenas os resultados em que o campo de data é posterior ou igual à data da última execução da atividade de query incremental."

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience_dimension"
>title="Selecione a dimensão de direcionamento"
>abstract="A dimensão de direcionamento permite definir a população-alvo da operação: destinatários, beneficiários(as) de contrato, operadores(as), assinantes, etc. Por padrão, para emails e SMS, o público-alvo é selecionado na tabela integrada Destinatários. Para notificações por push, a dimensão de direcionamento padrão é Aplicativos do assinante."

