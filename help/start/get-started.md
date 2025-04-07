---
title: Introdução à Composição de público-alvo federado da Experience Platform
description: Saiba o que é a Composição de público-alvo federado da Adobe e como usá-la na Adobe Experience Platform
exl-id: 43464aea-9c1d-4f1f-859f-82f209f350b7
source-git-commit: 97bda9d08eead79e6172e3b5bb746e7516bf6d85
workflow-type: ht
source-wordcount: '1146'
ht-degree: 100%

---

# Introdução à Composição de público-alvo federado {#gs-fac}

A composição de público-alvo federado está disponível para ambientes da [Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/segmentation/home){target="_blank"} e do [Adobe Journey Optimizer](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/ajo-home){target="_blank"}. Ela permite que clientes criem e enriqueçam públicos-alvo de warehouses de dados externas e importem esses públicos-alvo para a Adobe Experience Platform. A Composição de público-alvo federado oferece uma solução fácil e eficiente para conectar o seu data warehouse corporativo diretamente à Adobe Real-time Customer Data Platform e/ou Adobe Journey Optimizer e realizar consultas nas tabelas do seu data warehouse.

A Composição de público-alvo federado da Adobe ajuda os usuários de aplicativos da Adobe Experience Platform a acessar os dados de clientes armazenados nos data warehouses e plataformas de armazenamento na nuvem, como o Amazon Redshift, o Azure Synapse Analytics entre outros. Os dados do cliente podem residir em vários data warehouses e agora podem ser acessados instantaneamente, sem replicação. As plataformas compatíveis são listadas [nesta página](../connections/federated-db.md#supported-db).

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

## Casos de uso {#rn-uc}

Por meio de uma interface amigável de marketing, crie regras de segmento que consultem o data warehouse para obter uma lista de usuários que se qualificam para um segmento específico necessário para campanhas de marketing, acesse públicos do warehouse para ativação ou enriqueça os públicos-alvo da Adobe Experience Platform com pontos de dados adicionais do warehouse.

Nesta versão, dois casos de uso estão disponíveis:

1. Criação de público-alvo: crie novos públicos-alvo a partir de conjuntos de dados corporativos sem copiar dados subjacentes e ative-os com destinos pré-criados.

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

## Governança, privacidade e segurança {#governance-privacy-security}

### Solicitações de privacidade {#gov-privacy-requests}

Depois de criar uma composição, os públicos-alvo resultantes são salvos na Adobe Experience Platform.

É possível fazer solicitações de privacidade para acessar e/ou excluir dados de perfil correspondentes a esses públicos-alvo por meio do **Privacy Service** da Adobe Experience Platform, que fornece uma [interface](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=pt-BR){target="_blank"} e uma [API RESTful](https://experienceleague.adobe.com/pt-br/docs/experience-platform/privacy/api/overview){target="_blank"} para ajudar a gerenciar solicitações de dados de clientes.

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
>abstract="O targeting dimension permite definir a população-alvo da operação: destinatários, beneficiários(as) de contrato, operadores(as), assinantes, etc. Por padrão, para emails e SMS, o público-alvo é selecionado na tabela integrada Destinatários. Para notificações por push, a dimensão de direcionamento padrão é Aplicativos do assinante."


<!-- save profile IDs-->

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile"
>title="Salvar perfil"
>abstract="Salvar perfil"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_aepschemalist"
>title="Salvar perfil Lista de esquemas da AEP"
>abstract="Salvar perfil Lista de esquemas da AEP"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_selectaepattribute"
>title="Salvar perfil Atributo de Esquema da AEP"
>abstract="Salvar perfil Atributo de Esquema da AEP"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_primaryidentitynamespace"
>title="Selecionar campo de identificação primário"
>abstract="Campo de identificação primário a ser usado para os perfis."

>[!CONTEXTUALHELP]
>id="ddc_orchestration_saveprofile_selectdataset"
>title="Conjunto de dados da AEP"
>abstract="Selecione o conjunto de dados da AEP a ser usado para os perfis."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_selectaepschema"
>title="Salvar perfil Selecionar esquema da AEP"
>abstract="Selecione o esquema da AEP a ser usado para os perfis."
