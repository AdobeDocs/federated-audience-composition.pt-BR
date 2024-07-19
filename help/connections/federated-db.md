---
audience: end-user
title: Introdução aos Bancos de dados federados
description: Saiba como criar e gerenciar bancos de dados federados
badge: label="Disponibilidade limitada" type="Informative"
source-git-commit: 2608a9864c605ea127183dd1658932cfc8a18cf8
workflow-type: tm+mt
source-wordcount: '1419'
ht-degree: 17%

---

# Introdução aos Bancos de dados federados {#federated-db}

>[!CONTEXTUALHELP]
>id="dc_connection_federated_database_menu"
>title="Bancos de dados federados"
>abstract="As conexões existentes com Bancos de dados federados estão listadas nesta tela. Para criar uma nova conexão, clique no botão **[!UICONTROL Adicionar banco de dados federados]**."

>[!CONTEXTUALHELP]
>id="dc_connection_federated_database_properties"
>title="Propriedades do Banco de dados federado"
>abstract="Insira o nome do novo banco de dados federado e selecione um tipo."

>[!CONTEXTUALHELP]
>id="dc_connection_federated_database_details"
>title="Detalhes do Banco de dados federado"
>abstract="Defina as configurações para se conectar ao novo banco de dados federado. Use o botão **[!UICONTROL Testar conexão]** para validar a configuração."

Criar, Configurar, Testar e Salvar a conexão com um banco de dados externo.



Bancos de dados externos suportados:

* Amazon Redshift
* Azure synapse
* Google Big Query
* Snowflake
* Vertica Analytics

## Snowflake {#snowflake}

Use Federated Databases para processar informações armazenadas em um banco de dados externo. Siga as etapas abaixo para configurar o acesso ao Snowflake.

1. No menu **[!UICONTROL Federated data]**, selecione **[!UICONTROL Federated databases]**.

1. Clique em **[!UICONTROL Adicionar banco de dados federado]**.

   ![](assets/federated_database_1.png)

1. Insira um **[!UICONTROL Nome]** no banco de dados Federate.

1. No menu suspenso **[!UICONTROL Type]**, selecione Snowflake.

   ![](assets/federated_database_2.png)

1. Defina as configurações de autenticação de Snowflake:

   * **[!UICONTROL Servidor]**: insira seu nome de Servidor.

   * **[!UICONTROL Usuário]**: digite seu Nome de Usuário.

   * **[!UICONTROL Senha]**: digite a senha da sua conta.

   * **[!UICONTROL Banco de dados]** (opcional): insira o nome do seu banco de dados se não estiver especificado no DSN.

   * **[!UICONTROL Esquema de trabalho]** (opcional): insira o nome do esquema de trabalho.

   * **[!UICONTROL Chave privada]**: clique no campo **[!UICONTROL Chave privada]** para selecionar seus arquivos .pem na pasta de localidade.

   * **[!UICONTROL Opções]**: o conector dá suporte às opções detalhadas na tabela abaixo.

1. Selecione a opção **[!UICONTROL Testar a conexão]** para verificar sua configuração.

1. Clique no botão **[!UICONTROL Implantar funções]** para criar as funções.

1. Quando a configuração estiver concluída, clique em **[!UICONTROL Adicionar]** para criar o banco de dados Federate.

O conector é compatível com as seguintes opções:

| Opção | Descrição |
|---|---|
| schema de trabalho | schema de banco de dados que deve ser usado para tabelas de trabalho |
| depósito | Nome do depósito padrão que deve ser usado. Ele substituirá o padrão do usuário. |
| TimeZoneName | É vazio por padrão, o que significa que o fuso horário do sistema do servidor de aplicativos Campaign Classic é usado. A opção pode ser usada para forçar o parâmetro da sessão TIMEZONE. <br>[Para obter mais informações, consulte esta página](https://docs.snowflake.net/manuals/sql-reference/parameters.html#timezone). |
| WeekStart | Parâmetro de sessão WEEK_START. Por padrão, defina como 0. <br>[Para obter mais informações, consulte esta página](https://docs.snowflake.com/br/sql-reference/parameters.html#week-start). |
| UseCachedResult | Parâmetro de sessão USE_CACHED_RESULTS. Por padrão, defina como TRUE. Esta opção pode ser usada para desativar os resultados em cache de Snowflake. <br>[Para obter mais informações, consulte esta página](https://docs.snowflake.net/manuals/user-guide/querying-persisted-results.html). |
| bulkThreads | Número de threads a serem usados para o carregador em massa Snowflake; mais threads significam melhor desempenho para cargas em massa maiores. Por padrão, defina como 1. O número pode ser ajustado, dependendo da contagem de threads do computador. |
| tamanhoParte | Determina o tamanho do arquivo do bloco do carregador em massa. Por padrão, defina como 128 MB. Pode ser modificado para obter um desempenho melhor, quando usado com bulkThreads. Mais threads ativos simultâneos significam melhor desempenho. <br>Para obter mais informações, consulte a [documentação sobre o Snowflake](https://docs.snowflake.net/manuals/sql-reference/sql/put.html). |
| NomeEstágio | Nome do estágio interno pré-provisionado. Ele será usado no carregamento em massa em vez de criar um novo estágio temporário. |

## Google Big Query {#google-big-query}

Use Federated Databases para processar informações armazenadas em um banco de dados externo. Siga as etapas abaixo para configurar o acesso ao Google Big Query.

1. No menu **[!UICONTROL Federated data]**, selecione **[!UICONTROL Federated databases]**.

1. Clique em **[!UICONTROL Adicionar banco de dados federado]**.

   ![](assets/federated_database_1.png)

1. Insira um **[!UICONTROL Nome]** no banco de dados Federate.

1. No menu suspenso **[!UICONTROL Type]**, selecione Google Big Query.

   ![](assets/federated_database_3.png)

1. Defina as configurações de autenticação do Google Big Query:

   * **[!UICONTROL Conta de serviço]**: digite o email da sua **[!UICONTROL Conta de serviço]**. Para obter mais informações, consulte a [documentação da Google Cloud](https://cloud.google.com/iam/docs/creating-managing-service-accounts).

   * **[!UICONTROL Projeto]**: insira o nome do seu **[!UICONTROL Projeto]**. Para obter mais informações, consulte a [documentação da Google Cloud](https://cloud.google.com/resource-manager/docs/creating-managing-projects).

   * **[!UICONTROL Conjunto de Dados]**: Insira o nome do seu **[!UICONTROL Conjunto de Dados]**. Para obter mais informações, consulte a [documentação da Google Cloud](https://cloud.google.com/bigquery/docs/datasets-intro).

   * **[!UICONTROL Caminho do arquivo de chave]**: carregue seu arquivo de chave no servidor. Somente arquivos .json são aceitos.

   * **[!UICONTROL Opções]**: o conector dá suporte às opções detalhadas na tabela abaixo.

1. Selecione a opção **[!UICONTROL Testar a conexão]** para verificar sua configuração.

1. Clique no botão **[!UICONTROL Implantar funções]** para criar as funções.

1. Quando a configuração estiver concluída, clique em **[!UICONTROL Adicionar]** para criar o banco de dados Federate.

| Opção | Descrição |
|:-:|:-:|
| ProxyType | Tipo de proxy usado para se conectar ao BigQuery por meio de conectores ODBC e SDK. </br>HTTP (padrão), http_no_tunnel, socks4 e socks5 são suportados no momento. |
| ProxyHost | Nome do host ou endereço IP onde o proxy pode ser acessado. |
| PortaProxy | Número da porta em que o proxy está sendo executado, por exemplo, 8080 |
| ProxyUid | Nome de usuário usado para o proxy autenticado |
| ProxyPwd | Senha do ProxyUid |
| bqpath | Observe que isso é aplicável somente para a ferramenta de carregamento em massa (SDK da nuvem). </br> Para evitar o uso da variável PATH ou se o diretório google-cloud-sdk tiver que ser movido para outro local, você poderá especificar com essa opção o caminho exato para o diretório bin do sdk da nuvem no servidor. |
| GCloudConfigName | Observe que isso é aplicável a partir da versão 7.3.4 e somente para a ferramenta de carregamento em massa (SDK da nuvem).</br> O SDK da Google Cloud usa configurações para carregar dados em tabelas do BigQuery. A configuração chamada `accfda` armazena os parâmetros para carregar os dados. No entanto, essa opção permite que os usuários especifiquem um nome diferente para a configuração. |
| GCloudDefaultConfigName | Observe que isso é aplicável a partir da versão 7.3.4 e somente para a ferramenta de carregamento em massa (SDK da nuvem).</br> A configuração ativa do SDK da Google Cloud não pode ser excluída sem antes transferir a marca ativa para uma nova configuração. Essa configuração temporária é necessária para recriar a configuração principal para carregar dados. O nome padrão para a configuração temporária é `default`, que pode ser alterado se necessário. |
| GCloudRecreateConfig | Observe que isso é aplicável a partir da versão 7.3.4 e somente para a ferramenta de carregamento em massa (SDK da nuvem).</br> Quando definido como `false`, o mecanismo de carregamento em massa não tenta recriar, excluir ou modificar as configurações do SDK da Google Cloud. Em vez disso, ele continua com o carregamento de dados usando a configuração existente na máquina. Esse recurso é importante quando outras operações dependem das configurações do SDK da Google Cloud. </br> Se o usuário habilitar esta opção de mecanismo sem uma configuração adequada, o mecanismo de carregamento em massa emitirá uma mensagem de aviso: `No active configuration found. Please either create it manually or remove the GCloudRecreateConfig option`. Para evitar mais erros, ele será revertido para o usando o mecanismo de carregamento em massa de Inserção de matriz ODBC padrão. |

## Azure synapse Redshift {#azure-synapse-redshift}

Use Federated Databases para processar informações armazenadas em um banco de dados externo. Siga as etapas abaixo para configurar o acesso ao Azure synapse Redshift.

1. No menu **[!UICONTROL Federated data]**, selecione **[!UICONTROL Federated databases]**.

1. Clique em **[!UICONTROL Adicionar banco de dados federado]**.

   ![](assets/federated_database_1.png)

1. Insira um **[!UICONTROL Nome]** no banco de dados Federate.

1. No menu suspenso **[!UICONTROL Type]**, selecione Azure synapse Redshift.

   ![](assets/federated_database_4.png)

1. Defina as configurações de autenticação do Azure synapse Redshift:

   * **[!UICONTROL Servidor]**: insira a URL do servidor do Azure synapse.

   * **[!UICONTROL Conta]**: insira o nome de usuário.

   * **[!UICONTROL Senha]**: digite a senha da conta.

   * **[!UICONTROL Banco de dados]** (opcional): insira o nome do seu banco de dados se não estiver especificado no DSN.

   * **[!UICONTROL Opções]**: o conector dá suporte às opções detalhadas na tabela abaixo.

1. Selecione a opção **[!UICONTROL Testar a conexão]** para verificar sua configuração.

1. Clique no botão **[!UICONTROL Implantar funções]** para criar as funções.

1. Quando a configuração estiver concluída, clique em **[!UICONTROL Adicionar]** para criar o banco de dados Federate.

| Opção | Descrição |
|:-:|:-:|
| Autenticação | Tipo de autenticação compatível com o conector. Valor com suporte atual: AtiveDirectoryMSI. Para obter mais informações, consulte [SQL doc](https://learn.microsoft.com/en-us/sql/connect/odbc/using-azure-active-directory?view=sql-server-ver15#example-connection-strings) (Exemplo de cadeias de conexão n°8) |

## Vertica Analytics {#vertica-analytics}

Use Federated Databases para processar informações armazenadas em um banco de dados externo. Siga as etapas abaixo para configurar o acesso ao Vertica Analytics.

1. No menu **[!UICONTROL Federated data]**, selecione **[!UICONTROL Federated databases]**.

1. Clique em **[!UICONTROL Adicionar banco de dados federado]**.

   ![](assets/federated_database_1.png)

1. Insira um **[!UICONTROL Nome]** no banco de dados Federate.

1. No menu suspenso **[!UICONTROL Tipo]**, selecione Verticas analytics.

   ![](assets/federated_database_5.png)

1. Defina as configurações de autenticação de Verticas analytics:

   * **[!UICONTROL Servidor]**: adicionar a URL do servidor [!DNL Vertica Analytics].

   * **[!UICONTROL Conta]**: adicionar o nome de usuário.

   * **[!UICONTROL Senha]**: adicione a senha da conta.

   * **[!UICONTROL Banco de dados]** (opcional): insira o nome do seu banco de dados se não estiver especificado no DSN.

   * **[!UICONTROL Esquema de trabalho]** (opcional): insira o nome do esquema de trabalho.

   * **[!UICONTROL Opções]**: o conector dá suporte às opções detalhadas na tabela abaixo.

1. Selecione a opção **[!UICONTROL Testar a conexão]** para verificar sua configuração.

1. Clique no botão **[!UICONTROL Implantar funções]** para criar as funções.

1. Quando a configuração estiver concluída, clique em **[!UICONTROL Adicionar]** para criar o banco de dados Federate.

O conector é compatível com as seguintes opções:

| Opção | Descrição |
|---|---|
| TimeZoneName | É vazio por padrão, o que significa que o fuso horário do sistema do servidor de aplicativos Campaign Classic é usado. A opção pode ser usada para forçar o parâmetro da sessão TIMEZONE. |

## Amazon Redshift {#amazon-redshift}

Use Federated Databases para processar informações armazenadas em um banco de dados externo. Siga as etapas abaixo para configurar o acesso ao Amazon Redshift.

1. No menu **[!UICONTROL Federated data]**, selecione **[!UICONTROL Federated databases]**.

1. Clique em **[!UICONTROL Adicionar banco de dados federado]**.

   ![](assets/federated_database_1.png)

1. Insira um **[!UICONTROL Nome]** no banco de dados Federate.

1. No menu suspenso **[!UICONTROL Type]**, selecione Amazon Redshift.

   ![](assets/federated_database_6.png)

1. Defina as configurações de autenticação do Amazon Redshift:

   * **[!UICONTROL Servidor]**: adicione o nome do DNS.

   * **[!UICONTROL Conta]**: adicionar o nome de usuário.

   * **[!UICONTROL Senha]**: adicione a senha da conta.

   * **[!UICONTROL Banco de dados]**: nome do banco de dados, se não estiver especificado no DSN. Pode ficar em branco, se estiver especificado no DSN

   * **[!UICONTROL Esquema de trabalho]**: nome do seu esquema de trabalho. [Saiba mais](https://docs.aws.amazon.com/redshift/latest/dg/r_Schemas_and_tables.html)

1. Selecione a opção **[!UICONTROL Testar a conexão]** para verificar sua configuração.

1. Clique no botão **[!UICONTROL Implantar funções]** para criar as funções.

1. Quando a configuração estiver concluída, clique em **[!UICONTROL Adicionar]** para criar o banco de dados Federate.