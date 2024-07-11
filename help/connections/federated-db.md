---
audience: end-user
title: Introdução aos Bancos de dados federados
description: Saiba como criar e gerenciar bancos de dados federados
source-git-commit: 847da9a5eeb28199010f8491f7eebba4a60a83f1
workflow-type: tm+mt
source-wordcount: '890'
ht-degree: 26%

---

# Introdução aos Bancos de dados federados {#federated-db}


>[!CONTEXTUALHELP]
>id="dc_connection_federated_database_menu"
>title="Bancos de dados federados"
>abstract="As conexões existentes com Bancos de dados federados estão listadas nesta tela. Para criar uma nova conexão, clique no botão **Adicionar banco de dados federados**."


>[!CONTEXTUALHELP]
>id="dc_connection_federated_database_properties"
>title="Propriedades do Banco de dados federado"
>abstract="Insira o nome do novo banco de dados federado e selecione um tipo."


>[!CONTEXTUALHELP]
>id="dc_connection_federated_database_details"
>title="Detalhes do Banco de dados federado"
>abstract="Defina as configurações para se conectar ao novo banco de dados federado. Use o botão **Testar conexão** para validar a configuração."

Criar, Configurar, Testar e Salvar a conexão com um banco de dados externo.

Bancos de dados externos suportados:

* Snowflake
* Google Big Query
* Azure synapse
* Vertica Analytics
* Amazon Redshift

## Snowflake {#snowflake}

* **[!UICONTROL Servidor]**:

* **[!UICONTROL Usuário]**: Nome do usuário.

* **[!UICONTROL Senha]**: Senha da conta do usuário.

* **[!UICONTROL Banco de dados]**:

* **[!UICONTROL Esquema de trabalho]**:

* **[!UICONTROL Chave privada]**: somente arquivos .pem são aceitos

* **[!UICONTROL Opções]**: o conector é compatível com as opções detalhadas na tabela abaixo.

| Opção | Descrição |
|---|---|
| schema de trabalho | schema de banco de dados que deve ser usado para tabelas de trabalho |
| depósito | Nome do depósito padrão que deve ser usado. Ele substituirá o padrão do usuário. |
| TimeZoneName | É vazio por padrão, o que significa que o fuso horário do sistema do servidor de aplicativos Campaign Classic é usado. A opção pode ser usada para forçar o parâmetro da sessão TIMEZONE. <br>[Para obter mais informações, consulte esta página](https://docs.snowflake.net/manuals/sql-reference/parameters.html#timezone). |
| WeekStart | Parâmetro de sessão WEEK_START. Por padrão, defina como 0. <br>[Para obter mais informações, consulte esta página](https://docs.snowflake.com/br/sql-reference/parameters.html#week-start). |
| UseCachedResult | Parâmetro de sessão USE_CACHED_RESULTS. Por padrão, defina como TRUE. Esta opção pode ser usada para desativar os resultados em cache de Snowflake. <br>[Para obter mais informações, consulte esta página](https://docs.snowflake.net/manuals/user-guide/querying-persisted-results.html). |
| bulkThreads | Número de threads a serem usados para o carregador em massa Snowflake; mais threads significam melhor desempenho para cargas em massa maiores. Por padrão, defina como 1. O número pode ser ajustado, dependendo da contagem de threads do computador. |
| tamanhoParte | Determina o tamanho do arquivo do bloco do carregador em massa. Por padrão, defina como 128 MB. Pode ser modificado para obter um desempenho melhor, quando usado com bulkThreads. Mais threads ativos simultâneos significam melhor desempenho. <br>Para obter mais informações, consulte [Documentação do Snowflake](https://docs.snowflake.net/manuals/sql-reference/sql/put.html). |
| NomeEstágio | Nome do estágio interno pré-provisionado. Ele será usado no carregamento em massa em vez de criar um novo estágio temporário. |

## Google Big Query {#google-big-query}

* **[!UICONTROL Conta de serviço]**: Email do **[!UICONTROL Conta de serviço]**. Para obter mais informações, consulte [Documentação da Google Cloud](https://cloud.google.com/iam/docs/creating-managing-service-accounts).

* **[!UICONTROL Projeto]**: Nome do seu **[!UICONTROL Projeto]**. Para obter mais informações, consulte [Documentação da Google Cloud](https://cloud.google.com/resource-manager/docs/creating-managing-projects).

* **[!UICONTROL Conjunto de dados]**: Nome do seu **[!UICONTROL Conjunto de dados]**. Para obter mais informações, consulte [Documentação da Google Cloud](https://cloud.google.com/bigquery/docs/datasets-intro).

* **[!UICONTROL Caminho do arquivo de chave]**: carregue o arquivo de chave no servidor. Somente arquivos .json são aceitos.

* **[!UICONTROL Opções]**: o conector é compatível com as opções detalhadas na tabela abaixo.

| Opção | Descrição |
|:-:|:-:|
| ProxyType | Tipo de proxy usado para se conectar ao BigQuery por meio de conectores ODBC e SDK. </br>HTTP (padrão), http_no_tunnel, socks4 e socks5 são suportados no momento. |
| ProxyHost | Nome do host ou endereço IP onde o proxy pode ser acessado. |
| PortaProxy | Número da porta em que o proxy está sendo executado, por exemplo, 8080 |
| ProxyUid | Nome de usuário usado para o proxy autenticado |
| ProxyPwd | Senha do ProxyUid |
| bqpath | Observe que isso é aplicável somente para a ferramenta de carregamento em massa (SDK da nuvem). </br> Para evitar o uso da variável PATH ou se o diretório google-cloud-sdk tiver que ser movido para outro local, é possível especificar com essa opção o caminho exato para o diretório bin do sdk da nuvem no servidor. |
| GCloudConfigName | Observe que isso é aplicável a partir da versão 7.3.4 e somente para a ferramenta de carregamento em massa (SDK da nuvem).</br> O SDK da Google Cloud usa configurações para carregar dados em tabelas do BigQuery. A configuração chamada `accfda` armazena os parâmetros para carregar os dados. No entanto, essa opção permite que os usuários especifiquem um nome diferente para a configuração. |
| GCloudDefaultConfigName | Observe que isso é aplicável a partir da versão 7.3.4 e somente para a ferramenta de carregamento em massa (SDK da nuvem).</br> A configuração ativa do SDK da Google Cloud não pode ser excluída sem antes transferir a tag ativa para uma nova configuração. Essa configuração temporária é necessária para recriar a configuração principal para carregar dados. O nome padrão para a configuração temporária é `default`, isso poderá ser alterado, se necessário. |
| GCloudRecreateConfig | Observe que isso é aplicável a partir da versão 7.3.4 e somente para a ferramenta de carregamento em massa (SDK da nuvem).</br> Quando definido como `false`, o mecanismo de carregamento em massa evita tentar recriar, excluir ou modificar as configurações do SDK da Google Cloud. Em vez disso, ele continua com o carregamento de dados usando a configuração existente na máquina. Esse recurso é importante quando outras operações dependem das configurações do SDK da Google Cloud. </br> Se o usuário ativar essa opção de mecanismo sem uma configuração adequada, o mecanismo de carregamento em massa emitirá uma mensagem de aviso: `No active configuration found. Please either create it manually or remove the GCloudRecreateConfig option`. Para evitar mais erros, ele será revertido para o usando o mecanismo de carregamento em massa de Inserção de matriz ODBC padrão. |

## Azure synapse Redshift {#azure-synapse-redshift}

* **[!UICONTROL Servidor]**: o URL do servidor do Azure synapse

* **[!UICONTROL Conta]**: Nome do usuário

* **[!UICONTROL Senha]**: Senha da conta do usuário

* **[!UICONTROL Banco de dados]**: Nome do banco de dados

* **[!UICONTROL Options]**

## Vertica Analytics {#vertica-analytics}

* **[!UICONTROL Servidor]**: O URL do [!DNL Vertica Analytics] server

* **[!UICONTROL Conta]**: Nome do usuário

* **[!UICONTROL Senha]**: Senha da conta do usuário

* **[!UICONTROL Banco de dados]**: Nome do banco de dados

* **[!UICONTROL Esquema de trabalho]**: Nome do esquema de trabalho.

* **[!UICONTROL Opções]**: o conector é compatível com as opções detalhadas na tabela abaixo.

O conector é compatível com as seguintes opções:

| Opção | Descrição |
|---|---|
| TimeZoneName | É vazio por padrão, o que significa que o fuso horário do sistema do servidor de aplicativos Campaign Classic é usado. A opção pode ser usada para forçar o parâmetro da sessão TIMEZONE. |


## Amazon Redshift {#amazon-redshift}

* **[!UICONTROL Servidor]**: Nome do DNS

* **[!UICONTROL Conta]**: Nome do usuário

* **[!UICONTROL Senha]**: Senha da conta do usuário

* **[!UICONTROL Banco de dados]**: nome do banco de dados, se não estiver especificado no DSN. Pode ficar em branco, se estiver especificado no DSN

* **[!UICONTROL Esquema de trabalho]**: Nome do esquema de trabalho. [Saiba mais](https://docs.aws.amazon.com/redshift/latest/dg/r_Schemas_and_tables.html)

