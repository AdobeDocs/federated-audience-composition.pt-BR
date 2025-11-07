---
title: Novidades na Composição de público-alvo federado da Experience Platform
description: Atualizações e notas de versão mais recentes
exl-id: d4dcaf31-93cd-4a4e-888a-cf1bbdc4ca03
source-git-commit: 1806603f14a775cb7209e9f36283deabe5c07559
workflow-type: tm+mt
source-wordcount: '1740'
ht-degree: 98%

---

# Notas de versão {#rn-new}

O [!DNL Federated Audience Composition] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Todas as alterações são consolidadas nestas notas de versão. O [!DNL Federated Audience Composition] é construído nativamente na [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=pt-BR){target="_blank"}.

## Versão de outubro de 2025 {#fac-25-10}

### Novos recursos {#fac-25-10-feature}

<!-- <table>
<thead>
<tr>
<th><strong>Availability for Adobe Experience Platform customers on Amazon Web Services (AWS)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use Federated Audience Composition if your Experience Platform instance is on AWS.</p>
<p>For more information about Experience Platform on AWS, please read the <a href="https://experienceleague.adobe.com/pt-br/docs/experience-platform/landing/multi-cloud">multi-cloud overview</a>.</p>
</br>
</td>
</tr>
</tbody>
</table> -->

<table>
<thead>
<tr>
<th><strong>Autenticação OAuth para o Google BigQuery e Snowflake</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode se conectar ao Google BigQuery e ao Snowflake usando OAuth.</p>
<p>Para obter mais informações sobre como criar conexões, leia a <a href="../connections/home.md#create">visão geral das conexões</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

## Versão de agosto de 2025 {#fac-25-8}

### Novos recursos {#fac-25-08-feature}

<table>
<thead>
<tr>
<th><strong>Compatibilidade com chave composta na descoberta de esquemas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora, é possível combinar colunas para criar uma chave composta para o seu esquema.</p>
<p>Para mais informações sobre esquemas, leia a <a href="../customer/schemas.md#create">visão geral dos esquemas</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Adicionar várias associações em um link para modelos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora, é possível adicionar várias associações em um mesmo link para os seus modelos.</p>
<p>Para mais informações sobre modelos, leia a <a href="../data-management/gs-models.md#create">visão geral dos modelos</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

### Aprimoramentos {#fac-25-8-improvements}

Esta versão inclui os seguintes aprimoramentos:

* **Adição da função `StringAgg`**

  Agora, você pode usar a função `StringAgg` para bancos de dados do Amazon Redshift Spectrum ao usar o editor de expressões.

* Função **`Replace`**

  A descrição e a sintaxe da função `Replace` foram esclarecidas na documentação.

### Compatibilidade {#fac-25-8-compatibility}

* **Bancos de dados do Azure Synapse**

  Agora, você pode se conectar com segurança aos bancos de dados do Azure Synapse com PrivateLink ou VPN. Entre em contato com o atendimento ao cliente da Adobe para mais informações.

* **Banco de dados da Oracle**

  Agora, você pode se conectar com segurança aos bancos de dados da Oracle. Entre em contato com o atendimento ao cliente da Adobe para mais informações.

Para mais informações sobre os bancos de dados compatíveis com a composição de público-alvo federado, leia a [visão geral das conexões](../connections/home.md).

## Versão de julho de 2025 {#fac-25-7}

### Novos recursos {#fac-25-07-feature}

<table>
<thead>
<tr>
<th><strong>Novo conector - Oracle</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O conector do Oracle agora está disponível para uso com a composição de público-alvo federado.</p>
<p>É possível usar o conector do Oracle para casos de uso de criação e enriquecimento de público-alvo.</p>
<p>Para obter mais informações sobre a conexão do Oracle, leia a <a href="../connections/home.md#create">visão geral das conexões</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Alertas de composição</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível assinar alertas para saber mais sobre as execuções bem-sucedidas e com falha da composição</p>
<p>Para obter mais informações sobre como assinar notificações para as execuções da composição, leia o <a href="../compositions/start-monitor-composition.md#alerts">guia de início e monitoramento da composição</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

### Aprimoramentos {#fac-25-07-improvements}

Esta versão inclui os seguintes aprimoramentos:

* **Aumento do limite de caracteres no servidor**

  Ao configurar os bancos de dados federados, agora é possível usar até 255 caracteres, em vez dos 80 caracteres anteriores.

## Versão de junho de 2025 {#fac-25-6}

### Aprimoramentos {#fac-25-06-improvements}

Esta versão inclui os seguintes aprimoramentos:

* **Disponibilidade geral para clientes do Adobe Healthcare Shield**

  A composição de público-alvo federado estará disponível para clientes do Adobe Healthcare Shield para casos de uso de criação de público-alvo, enriquecimento e enriquecimento de perfil até o fim de junho.

  Mais informações sobre privacidade e segurança na Composição de público-alvo federado podem ser encontradas no [Guia de governança, privacidade e segurança de dados](/help/governance-privacy-security/home.md).

* **Controle de acesso no nível dos objetos**

  A composição de público-alvo federado agora é compatível com o controle de acesso no nível dos objetos para aplicar rótulos de acesso às suas composições especificadas.

  Mais informações sobre o uso de rótulos de acesso no nível de objetos podem ser encontradas no [guia de composições](/help/compositions/gs-compositions.md).

* **Funções padrão**

  Agora, você pode usar uma das funções padrão para gerenciar permissões de usuários para acessar a composição de público-alvo federado.

  Mais informações sobre as funções padrão podem ser encontradas no [guia de acesso à Composição de público-alvo federado](/help/governance-privacy-security/access-control.md).

* **Atualizações incrementais em casos de uso de enriquecimento de perfil**

  A atividade “Salvar perfis” agora permite atualizações incrementais. Com as atualizações incrementais, você pode consultar e atualizar dados incrementais enquanto enriquece perfis com dados de data warehouses externos.

  Mais informações sobre o uso da atividade salvar perfis podem ser encontradas no [guia da atividade salvar perfis](/help/compositions/activities/save-profiles.md).

## Versão de maio de 2025 {#fac-25-5}

### Novos recursos {#fac-25-05-feature}

<table>
<thead>
<tr>
<th><strong>Visualização da tela do modelo de dados: disponibilidade geral</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O modelo de dados com a visualização de tela já está disponível para todos os clientes.</p>
<p>A visualização de tela da seção “Modelos de dados” aprimora a experiência ao permitir a visualização de modelos de dados e seus links em um layout de tela, juntamente com a visualização em tabelas existente. </p>
<p>Para mais informações sobre a visualização de tela, leia a <a href="../data-management/gs-models.md">visão geral dos modelos de dados</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

### Aprimoramentos {#fac-25-5-improvements}

Esta versão inclui os aprimoramentos a seguir.

* **Controle de acesso baseado na função**

  A partir da versão de maio, o [!DNL Federated Audience Composition] oferece novas permissões granulares para controle de acesso. Os usuários podem atribuir essas permissões a funções de usuários a fim de obter um acesso mais preciso ao [!DNL Federated Audience Composition].

  Para saber mais sobre as novas permissões, leia o [guia de acesso à composição de público-alvo federado](/help/governance-privacy-security/access-control.md).

## Versão de abril de 2025 {#fac-25-4}

### Novos recursos {#fac-25-04-feature}

<table>
<thead>
<tr>
<th><strong>Visualização da tela do modelo de dados - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A visualização de tela da seção “Modelos de dados” aprimora a experiência ao permitir a visualização de modelos de dados e seus links em um layout de tela, juntamente com a visualização em tabelas existente. </p>
<p>O modelo de dados com visualização de tela está atualmente disponível na versão beta apenas para usuários selecionados.</p>
<p>Para obter mais informações, consulte a <a href="../data-management/gs-models.md">documentação detalhada</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Suporte do Assistente de IA para conhecimento do produto</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Assistente de IA é um recurso da interface projetado para ajudar você a navegar e entender conceitos da Adobe, além de obter insights operacionais para seu ambiente específico. Ele está disponível em vários produtos na Adobe Experience Cloud, inclusive na Composição de público-alvo federado.</p>
<p>Para obter mais informações, consulte a <a href="../start/ai-assistant.md">documentação detalhada</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Atividade Salvar perfis</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p> A composição de público-alvo federado agora é compatível com o caso de uso de enriquecimento de perfil, permitindo que os clientes aprimorem perfis existentes da Experience Platform com dados de seus data warehouses externos.
</p>
<p>Para obter mais informações, consulte a <a href="../compositions/activities/save-profiles.md">documentação detalhada</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

### Aprimoramentos {#fac-25-4-improvements}

Esta versão inclui as melhorias listadas abaixo.

* **Nome do modelo de dados**

  No menu Públicos-alvo, a guia **Composições federadas** agora exibe o nome do modelo de dados em vez da ID, melhorando a clareza e a usabilidade geral.

* **Público-alvo**

  O menu Público-alvo agora exibe o nome ou rótulo do modelo de dados selecionado ao selecionar um modelo sem públicos-alvo associados.

* **Exportação de públicos-alvo grandes**

  A composição de público-alvo federado agora é compatível com a exportação de públicos-alvo grandes, com tamanhos de arquivo superiores a 1 GB.

* **Atividade Salvar público-alvo**

  Uma observação foi adicionada à atividade **Salvar público-alvo**, lembrando os usuários de colaborar com admins de dados para aplicar rótulos de governança a novos esquemas e conjuntos de dados gerados durante a etapa de criação e enriquecimento do público-alvo.
  [Saiba mais sobre rótulos de uso de dados](https://experienceleague.adobe.com/pt-br/docs/experience-platform/data-governance/labels/user-guide)

### Compatibilidade {#fac-25-4-compat}

* **Conexão segura do Amazon Redshift**

  Com esta nova versão, a composição de público-alvo federado oferece suporte a conexões de links privados seguros com bancos de dados do Amazon Redshift. [Saiba mais](../connections/home.md#amazon-redshift)

* **Google BigQuery**

  Nesta nova versão, a composição de público-alvo federado oferece suporte a conexões VPN seguras com bancos de dados do Google BigQuery. [Saiba mais](../connections/home.md#google-bigquery)

## Versão de março de 2025 {#fac-25-3}

### Aprimoramentos {#fac-25-3-improvements}

Esta versão inclui as melhorias listadas abaixo.

* **Permissões da composição de público-alvo federado**

  A partir da versão de março, o recurso [!DNL Federated Audience Composition] começará a impor o acesso às interfaces de **gestão de dados federados** e **composições federadas** ao usuário que receber a permissão para **gerenciar dados federados**.

  Recomendamos que os usuários entrem em contato com os(as) admins, para que essa permissão seja adicionada à sua função a fim de manter o acesso à interface do [!DNL Federated Audience Composition].

  Para saber como conceder essa permissão, consulte a [documentação detalhada](/help/governance-privacy-security/access-control.md).

### Compatibilidade {#fac-25-3-compat}

* **Conexão do Databricks**

  Com esta nova versão, a composição de público-alvo federado agora é compatível com a conectividade por link privado para conexões de bancos de dados do Databricks.
Isso inclui conexões seguras com bancos de dados do Databricks hospedados no Amazon Web Services (AWS) por meio de link privado e bancos de dados do Databricks hospedados no Microsoft Azure via VPN. [Saiba mais](../connections/home.md#databricks)

* **Suporte para clientes B2B da CDP**

  A composição de público-alvo federado agora está disponível para clientes B2B (Business-to-Business) da plataforma de dados do cliente (CDP) para casos de uso de públicos-alvo baseados em pessoas.

* **Conexão segura do Snowflake**

  Com esta nova versão, a composição de público-alvo federado é compatível com conexões seguras por links privados para bancos de dados do Snowflake hospedados no Microsoft Azure. [Saiba mais](../connections/home.md#snowflake)

## Versão de fevereiro de 2025 {#fac-25-2}

Esta versão inclui as alterações listadas abaixo.

* **Suporte ao Microsoft Fabric**

  Agora é possível estabelecer conexões com bancos de dados do Microsoft Fabric por meio da composição de público-alvo federado. [Saiba mais](../connections/home.md)

* **Suporte ao Amazon Redshift Spectrum**

  O Amazon Redshift Spectrum agora é compatível com as conexões do banco de dados do Amazon Redshift. [Saiba mais](../connections/home.md#amazon-redshift)

* **Experiência aprimorada de criação de esquemas**

  O processo de criação de esquemas foi aprimorado por meio de uma interface atualizada, projetada para ser mais intuitiva e fácil de navegar. Esses aprimoramentos oferecem aos profissionais de dados uma maneira mais suave e eficiente de desenvolver modelos de dados. [Saiba mais](../customer/schemas.md)

* **Suporte ao enriquecimento de público-alvo para Databricks**

  Agora você pode usar o Databricks no fluxo Ler público-alvo, habilitando a atividade para bancos de dados do Databricks e permitindo que seja definido como o novo destino. [Saiba mais](../connections/destinations.md)

## Versão de novembro de 2024 {#fac-24-11}

### Aprimoramentos {#fac-24-11-improvements}

Esta versão inclui as melhorias listadas abaixo.

* **Lista de permissões de endereços IP**

  Ao adicionar um banco de dados federado na interface do usuário da Adobe Experience Platform, agora é possível visualizar diretamente os endereços IP associados às instâncias da composição de público-alvo federado. Isso permite copiar e autorizar facilmente esses IPs a conectarem-se ao banco de dados para aumentar a segurança e a flexibilidade. [Saiba mais](../connections/home.md)

## Versão de outubro de 2024 {#fac-24-10}

>[!AVAILABILITY]
>
>Anteriormente disponível para algumas organizações (disponibilidade limitada), a Composição de público-alvo federado da Adobe Experience Platform agora está disponível para todos os usuários (disponibilidade geral). Este recurso é ativado com base na sua oferta e só é visível com as permissões associadas. [Saiba mais](access-prerequisites.md)

### Compatibilidade {#fac-24-10-compat}

Com esta nova versão, a Composição de público-alvo federado agora é compatível com os sistemas listados abaixo.

* **Compatibilidade com o Databricks**

  Agora é possível estabelecer conexões com bancos de dados do Databricks por meio da Composição de público-alvo federado. [Saiba mais](../connections/home.md#databricks)

* **Suporte para acesso seguro ao Snowflake pelo AWS PrivateLink**

  Agora é possível ter acesso seguro ao seu data warehouse externo do Snowflake por meio de um link privado. Observe que a conta do Snowflake deve estar hospedada no Amazon Web Services (AWS) e localizada na mesma região do ambiente da Composição de público-alvo federado. Entre em contato com o representante da Adobe para obter assistência na configuração do acesso seguro à conta do Snowflake. [Saiba mais](../connections/home.md#snowflake)

* **Suporte ao Amazon Redshift Serverless**

  Com esta nova versão, a Composição de público-alvo federado oferece suporte ao [Amazon Redshift Serverless](https://aws.amazon.com/pt/redshift/redshift-serverless/){target="_blank"}.

### Aprimoramentos {#fac-24-10-improvements}

Esta versão vem com as melhorias listadas abaixo.

* **Atualizar esquemas existentes**

  Ao criar, modificar ou excluir uma coluna em um banco de dados federado, agora é possível detectar e aplicar as alterações clicando no botão **[!UICONTROL Atualizar esquema]** no esquema correspondente. [Saiba mais](../customer/schemas.md#schema-refresh)

* **Associar um modelo de dados a uma nova composição**

  Ao criar uma composição, agora é possível selecionar o modelo de dados para associar a ela. Com essa nova opção, a configuração das atividades é mais fácil, pois somente as tabelas do modelo de dados associado estão disponíveis. [Saiba mais](../compositions/create-composition.md)

## Versão de julho de 2024: Composição de público-alvo federado (Disponibilidade limitada) {#fac-la}

A composição de público-alvo federado fornece às empresas acesso flexível e expandido a warehouses de dados empresariais, para compor públicos-alvo por meio de conjuntos de dados empresariais cruciais e potencializar experiências iniciadas pela marca e experiências em tempo real. Com essa nova abordagem, como usuário da [Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/segmentation/home){target="_blank"} e/ou do [Adobe Journey Optimizer](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/ajo-home){target="_blank"} é possível federar dados de públicos-alvo diretamente do seu data warehouse existente para enriquecer os públicos-alvo da Adobe Experience Platform em um sistema.

A composição de público-alvo federado supre o aumento das demandas do mercado de empresas que precisam de flexibilidade para compor públicos-alvo com conjuntos de dados de uma warehouse. Dessa forma, as empresas podem reduzir a movimentação de dados, além de disponibilizar dados cruciais do público-alvo, para que as equipes de marketing satisfaçam os requisitos de casos de uso e potencializem experiências personalizadas.

Saiba mais sobre os recursos da composição de público-alvo federado [nesta página](get-started.md) e nas [Perguntas frequentes](faq.md).

Para obter informações detalhadas dos pré-requisitos para acessar Composição de público-alvo federado e as medidas de proteção atuais, consulte [esta página](access-prerequisites.md).
