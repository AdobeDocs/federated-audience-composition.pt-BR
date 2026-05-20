---
audience: end-user
title: Criar e gerenciar conexões com bancos de dados federados
description: Saiba como criar e gerenciar conexões com bancos de dados federados
exl-id: ab65cd8a-dfa0-4f09-8e9b-5730564050a1
TQID: https://experienceleague.adobe.com/6-pzawt2ndn2MKLyYLXPMy-ec1SIOsQI5frTt9IqOX0
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2: id: fc7979f3-56c3-43ca-9784-f1ea3dc69c4b
topic_v2: id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: d095671a-1355-40aa-8b5f-06c33c68080bid: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 212090ab6e5537c4d23d73564affb64b146dada0
workflow-type: tm+mt
source-wordcount: 3543
ht-degree: 8%

---

# Criar conexões {#connections-fdb}

>[!AVAILABILITY]
>
>Para acessar conexões, você precisará de uma das seguintes permissões:
>
>-**Gerenciar Banco de Dados Federado**
>-**Exibir Banco de Dados Federado**
>
>Para mais informações sobre as permissões exigidas, leia o [guia de controle de acesso](/help/governance-privacy-security/access-control.md).

A Composição de público-alvo federado do Experience Platform permite criar e enriquecer públicos-alvo de data warehouses de terceiros e importar os públicos-alvo para o Adobe Experience Platform.

## Bancos de dados compatíveis {#supported-databases}

Para trabalhar com o banco de dados federado e o Adobe Experience Platform, primeiro é necessário estabelecer uma conexão entre as duas fontes. Com a Federated Audience Composition, você pode se conectar aos seguintes bancos de dados.

- Amazon Redshift
- Azure Synapse Analytics
- Databricks
- Google BigQuery
- Microsoft Fabric
- Oracle
- Snowflake
- Teradata
- Vertica Analytics

## Criar conexão {#create}

Para criar uma conexão, selecione **[!UICONTROL Federated databases]** na seção Federated data.

![O botão Federated Databases está realçado dentro da navegação à esquerda.](assets/home/select-federated.png){zoomable="yes" width="70%" align="center"}

A seção Federated databases é exibida. Selecione **[!UICONTROL Adicionar banco de dados federado]** para criar uma conexão.

![O botão Adicionar banco de dados federado está realçado na página de exibição do banco de dados federado.](assets/home/add-federated.png){zoomable="yes" width="70%" align="center"}

>[!NOTE]
>
>Para solicitar conectividade segura usando um link privado ou VPN, você **deve** ter licenciado o Privacy and Security Shield ou o Healthcare Shield.

O popover de propriedades da conexão é exibido. Você pode nomear sua conexão e selecionar o tipo de banco de dados que deseja criar.

![Os tipos de banco de dados federado são exibidos.](assets/home/select-type.png){zoomable="yes" width="70%" align="center"}

Após selecionar um tipo, a seção **[!UICONTROL Detalhes]** é exibida. Esta seção difere com base no tipo de banco de dados escolhido anteriormente.

>[!BEGINTABS]

>[!TAB Amazon Redshift]

>[!AVAILABILITY]
>
>Somente o Amazon Redshift AWS, o Amazon Redshift Spectrum e o Amazon Redshift Serverless são suportados.
>
>Além disso, o acesso seguro ao data warehouse externo do Amazon Redshift por meio de um link privado é suportado.

Depois de selecionar Amazon Redshift, você pode adicionar os seguintes detalhes:

| Campo | Descrição |
| ----- | ----------- |
| Servidor | O nome da fonte de dados. |
| Conta | O nome de usuário da conta. |
| Senha | A senha da conta. |
| Banco de dados | O nome do banco de dados. Se isso for especificado no nome do servidor, esse campo poderá ser deixado em branco. |
| Esquema de trabalho | O nome do esquema do banco de dados a ser usado para tabelas de trabalho. Mais informações sobre este recurso podem ser encontradas na [documentação de Esquemas do Amazon](https://docs.aws.amazon.com/redshift/latest/dg/r_Schemas_and_tables.html){target="_blank"}.<br/><br/>**Observação:** você pode usar qualquer esquema do banco de dados, incluindo esquemas usados para processamento temporário de dados, desde que tenha as permissões necessárias para se conectar a este esquema. No entanto, você **deve** usar esquemas de trabalho distintos ao conectar várias sandboxes com o mesmo banco de dados. |

>[!TAB Azure Synapse Analytics]

>[!NOTE]
>
>Se você quiser criar uma conexão segura usando o Azure Synapse Analytics, entre em contato com o representante do Atendimento ao cliente da Adobe.

Depois de selecionar o Azure Synapse Analytics, você pode adicionar os seguintes detalhes:

| Campo | Descrição |
| ----- | ----------- |
| Servidor | O URL do servidor Azure Synapse. |
| Conta | A ID do aplicativo (**ID do Cliente**) do registro do aplicativo Azure. |
| Senha | O valor **Segredo do cliente** do aplicativo Azure. |
| Banco de dados | O nome do banco de dados. Se isso for especificado no nome do servidor, esse campo poderá ser deixado em branco. |
| Opções | Opções adicionais para a conexão. Para o Azure Synapse Analytics, você pode especificar o tipo de autenticação compatível com o conector. Atualmente, a Composição de Público Federado dá suporte a `ActiveDirectoryMSI`. Para obter mais informações sobre cadeias de conexão, leia a [seção de exemplos de cadeias de conexão da documentação da Microsoft](https://learn.microsoft.com/pt-br/sql/connect/odbc/using-azure-active-directory?view=sql-server-ver15#example-connection-strings){target="_blank"}. |

Como alternativa, você pode configurar com segurança a conexão do Azure Synapse Analytics usando a autenticação da Entidade de serviço. Você deve usar a autenticação da Entidade de serviço para integrações de nível de produção, bem como cenários de automação.

+++ Pré-requisitos

Antes de configurar a autenticação da Entidade de Serviço, observe os seguintes pré-requisitos:

- Uma assinatura do Azure com acesso ao Microsoft Entra ID
- Um espaço de trabalho e banco de dados do Azure Synapse
- Permissão para criar o Registro do aplicativo
- Permissão para gerenciar funções de banco de dados do Azure Synapse
- Permissão para atualizar configurações do Federated Database

+++

No Portal do Azure, primeiro será necessário criar um novo registro de aplicativo. Selecione **Registrar** depois de dar um nome exclusivo ao aplicativo. A página **Visão geral** é exibida. Anote os valores de **ID do Aplicativo (Cliente)** e **ID do Diretório (Locatário)**.

![A ID do Aplicativo (Cliente) na página de visão geral está realçada.](/help/connections/assets/home/azure-client-id.png)

No aplicativo recém-registrado, selecione **Certificados e segredos**. Aqui, selecione **Novo segredo do cliente** na seção **Segredos do cliente** para criar um novo segredo do cliente. Depois de fornecer uma descrição e uma expiração, selecione **Adicionar** para gerar o segredo do cliente.

>[!IMPORTANT]
>
>Depois de gerar o segredo do cliente, copie e armazene com segurança o **Valor do Segredo do Cliente**. Este valor **não** ficará visível novamente.

Agora que você gerou o segredo do cliente, é necessário certificar-se de que você concedeu a identidade da **Entidade de serviço** ao recurso.

Para obter mais informações sobre como atribuir identidade a recursos, leia o [Guia de identidades gerenciadas para o Azure Synapse Analytics](https://learn.microsoft.com/en-us/azure/synapse-analytics/synapse-service-identity).

Como você concluiu todas as configurações do lado do Azure, agora é possível definir as configurações do lado do Federated-Audience-Composition.

Em sua conexão com o Azure Synapse, defina os seguintes detalhes de configuração:

| Campo | Descrição |
| ----- | ----------- |
| Servidor | O URL do servidor Azure Synapse. |
| Conta | A ID do aplicativo (**ID do Cliente**) do registro do aplicativo Azure. |
| Senha | O valor **Segredo do cliente** do aplicativo Azure. |
| Banco de dados | O nome do banco de dados. Se isso for especificado no nome do servidor, esse campo poderá ser deixado em branco. |
| Opções | Opções adicionais para a conexão. Para usar a autenticação da Entidade de Serviço, será necessário definir `Authentication="ActiveDirectoryServicePrincipal"`. |

>[!TAB Databricks]

>[!NOTE]
>
>Há suporte para o acesso seguro ao data warehouse externo do Databricks por meio de link privado. Isso inclui conexões seguras com bancos de dados do Databricks hospedados no Amazon Web Services (AWS) por meio de link privado e bancos de dados do Databricks hospedados no Microsoft Azure via VPN. Entre em contato com o representante da Adobe para obter assistência na configuração do acesso seguro.

Depois de selecionar Databricks, você pode escolher com o método de autenticação que deseja usar ao se conectar com a Federated Audience Composition.

Se você selecionar **Conta/Autenticação de senha**, poderá adicionar os seguintes detalhes de logon:

| Campo | Descrição |
| ----- | ----------- |
| Servidor | O nome do servidor Databricks. |
| Senha | O token de acesso para o servidor Databricks. Para obter mais informações sobre esse valor, leia a [documentação de Databricks sobre tokens de acesso pessoal](https://docs.databricks.com/aws/en/dev-tools/auth/pat){target="_blank"}. |

Se você selecionar **Autenticação da Entidade de Serviço**, poderá adicionar os seguintes detalhes:

| Campo | Descrição |
| ----- | ----------- |
| Servidor | O nome do servidor Databricks. |
| ID de cliente | A ID do cliente do servidor Databricks. Este campo atua como um nome de usuário para o seu projeto. |
| Segredo do cliente | O segredo do cliente do servidor Databricks. Este campo atua como uma senha para o seu projeto. |

Se você selecionar **OAuth 2.0**, poderá adicionar os seguintes detalhes:

| Campo | Descrição |
| ----- | ----------- |
| Servidor | O nome do servidor Databricks. |
| ID de cliente | A ID do cliente do servidor Databricks. Este campo é usado para identificar o aplicativo durante a autenticação do OAuth 2.0 e atua como um nome de usuário para o seu projeto. |
| Segredo do cliente | O segredo do cliente do servidor Databricks. Essa credencial confidencial é emitida com a ID do cliente e atua como uma senha para o projeto. |
| Escopo de acesso | Informações pré-preenchidas que listam os escopos para os quais seu token OAuth está autorizado no servidor do Databricks. |

Depois de inserir os detalhes de logon, é possível adicionar as seguintes informações:

| Campo | Descrição |
| ----- | ----------- |
| Caminho HTTP | O caminho para o Cluster ou Warehouse. Para obter mais informações sobre o caminho, leia a [documentação do Databricks sobre detalhes de conexão](https://docs.databricks.com/aws/en/integrations/compute-details){target="_blank"}. |
| Catálogo | O nome do Catálogo de Databricks. Para obter mais informações sobre catálogos em Databricks, leia a [documentação sobre Databricks em catálogos](https://docs.databricks.com/aws/en/catalogs/){target="_blank"} |
| Esquema de trabalho | O nome do esquema de banco de dados a ser usado para as tabelas de trabalho. <br/><br/>**Observação:** você pode usar o esquema **any** do banco de dados, incluindo esquemas usados para processamento temporário de dados, desde que tenha as permissões necessárias para se conectar a este esquema. No entanto, você **deve** usar esquemas de trabalho distintos ao conectar várias sandboxes com o mesmo banco de dados. |
| Opções | Opções adicionais para a conexão. As opções disponíveis estão listadas na tabela a seguir. |

Para Databricks, você pode definir as seguintes opções adicionais:

| Opções | Descrição |
| ------- | ----------- |
| TimeZoneName | O nome do fuso horário a ser usado. Este valor representa o parâmetro de sessão `TIMEZONE`. Para obter mais informações sobre fusos horários, leia a [documentação de Databricks sobre fusos horários](https://docs.databricks.com/aws/en/sql/language-manual/parameters/timezone#:~:text=The%20system%20default%20is%20UTC%20.){target="_blank"}. |

>[!TAB Google BigQuery]

>[!NOTE]
>
>O acesso seguro ao data warehouse externo do Google BigQuery por meio de VPN é compatível.

Depois de selecionar o Google BigQuery, você pode escolher qual método de autenticação deseja usar ao se conectar com a Federated Audience Composition.

Se você selecionar **[!UICONTROL Conta/Autenticação de senha]**, poderá adicionar as seguintes informações de logon:

| Campo | Descrição |
| ----- | ----------- |
| Conta de serviço | O endereço de email da sua conta de serviço. Para obter mais informações, leia a [documentação da conta do Google Cloud Service](https://cloud.google.com/iam/docs/service-accounts-create){target="_blank"}. |

Se você selecionar **[!UICONTROL OAuth 2.0]**, será possível adicionar as seguintes informações de logon:

>[!NOTE]
>
>Antes de se conectar ao Google BigQuery usando o OAuth 2.0, será necessário configurar o URL de redirecionamento no projeto do Google Cloud. Adicione a URL de redirecionamento `https://fac-oauth.adobe.io/oauth` ao seu projeto da Google Cloud na configuração da ID do cliente OAuth 2.0.

| Campo | Descrição |
| ----- | ----------- |
| ID de cliente | A ID do cliente do seu projeto do Google BigQuery. Este campo atua como um nome de usuário para o seu projeto. |
| Segredo do cliente | O segredo do cliente do seu projeto do Google BigQuery. Este campo atua como uma senha para o seu projeto. |
| Escopo de acesso | Informações pré-preenchidas que listam os escopos para os quais o token OAuth está autorizado nos recursos da Google Cloud. |

Selecione **[!UICONTROL Entrar]** para concluir sua autenticação.

Se você selecionar **[!UICONTROL WIF]**, **não** precisará fornecer informações de logon. No entanto, você **deve** adicionar a configuração da biblioteca do cliente como o **[!UICONTROL caminho do arquivo da chave]**. Para obter mais informações sobre a configuração da biblioteca do cliente, leia a [seção de configuração do Google BigQuery (Workload Identity Federation)](#wif-configuration).

Depois de inserir os detalhes de logon, é possível adicionar os seguintes detalhes:

| Campo | Descrição |
| ----- | ----------- |
| Projeto | A ID do seu projeto. Para obter mais informações, leia a [documentação do projeto do Google Cloud](https://cloud.google.com/resource-manager/docs/creating-managing-projects){target="_blank"}. |
| Conjunto de dados | O nome do conjunto de dados. Para obter mais informações, leia a [documentação do conjunto de dados da Google Cloud](https://cloud.google.com/bigquery/docs/datasets-intro){target="_blank"}. |
| Caminho do arquivo de chave | O arquivo de chave para o servidor. Somente `json` arquivos são suportados. |
| Opções | Opções adicionais para a conexão. As opções disponíveis estão listadas na tabela a seguir. |

Para o Google BigQuery, você pode definir as seguintes opções adicionais:

| Opções | Descrição |
| ------- | ----------- |
| ProxyType | O tipo de proxy usado para se conectar ao BigQuery. Os valores suportados incluem `HTTP`, `http_no_tunnel`, `socks4` e `socks5`. |
| ProxyHost | O hostname ou endereço IP onde o proxy pode ser alcançado. |
| ProxyUid | O número da porta em que o proxy está sendo executado. |
| ProxyPwd | A senha do proxy. |
| bgpath | **Observação:** isso só é aplicável para a **ferramenta de carregamento em massa** (Cloud SDK). <br/><br/> O caminho para o diretório bin do Cloud SDK no servidor. Você só precisa definir isso se tiver movido o diretório `google-cloud-sdk` para outro local ou se não quiser usar a variável PATH. |
| GCloudConfigName | **Observação:** isso só é aplicável para a **ferramenta de carregamento em massa** (Cloud SDK) acima da versão 7.3.4. <br/><br/> O nome da configuração que armazena os parâmetros para carregar os dados. Por padrão, este valor é `accfda`. |
| GCloudDefaultConfigName | **Observação:** isso só é aplicável para a **ferramenta de carregamento em massa** (Cloud SDK) acima da versão 7.3.4. <br/><br/> O nome da configuração temporária para recriar a configuração principal para carregar dados. Por padrão, este valor é `default`. |
| GCloudRecreateConfig | **Observação:** isso só é aplicável para a **ferramenta de carregamento em massa** (Cloud SDK) acima da versão 7.3.4. <br/><br/> Um valor booleano que permite decidir se o mecanismo de carregamento em massa deve recriar, excluir ou modificar automaticamente as configurações do Google Cloud SDK. Se esse valor estiver definido como `false`, o mecanismo de carregamento em massa carregará dados usando uma configuração existente na máquina. Se esse valor estiver definido como `true`, verifique se a configuração está definida corretamente; caso contrário, o erro `No active configuration found. Please either create it manually or remove the GCloudRecreateConfig option` será exibido e o mecanismo de carregamento será revertido para o mecanismo de carregamento padrão. |

>[!TAB Malha do Microsoft]

Depois de selecionar o Microsoft Fabric, você pode adicionar os seguintes detalhes:

| Campo | Descrição |
| ----- | ----------- |
| Servidor | O URL do servidor do Microsoft Fabric. |
| ID do aplicativo | A ID do aplicativo do Microsoft Fabric. Para obter mais informações sobre a ID do aplicativo, leia a [documentação do Microsoft Fabric sobre a configuração do aplicativo](https://learn.microsoft.com/en-us/fabric/workload-development-kit/create-entra-id-app){target="_blank"}. |
| Segredo do cliente | O segredo do cliente para o aplicativo. Para obter mais informações sobre o segredo do cliente, leia a [documentação do Microsoft Fabric sobre a configuração do aplicativo](https://learn.microsoft.com/en-us/fabric/workload-development-kit/create-entra-id-app#step-8-generate-a-secret-for-your-application){target="_blank"}. |
| Opções | Opções adicionais para a conexão. As opções disponíveis estão listadas na tabela a seguir. |

Para o Microsoft Fabric, você pode definir as seguintes opções adicionais:

| Opção | Descrição |
| ------ | ----------- |
| Autenticação | O tipo de autenticação usado pelo conector. Os valores suportados incluem: `ActiveDirectoryMSI`. Para obter mais informações, leia a [documentação do Microsoft sobre conectividade de warehouse](https://learn.microsoft.com/en-us/fabric/data-warehouse/connectivity){target="_blank"}. |

>[!TAB Oracle]

>[!NOTE]
>
>O Federated Audience Composition é compatível com a configuração de conexão federada com bancos de dados do Oracle na versão 11g ou superior e hospedado no AWS, Azure, Exadata ou em uma nuvem privada (desde que seja acessível por uma rede externa). Se você tiver mais dúvidas relacionadas à configuração do banco de dados do Oracle ou precisar criar uma conexão segura com o Oracle, entre em contato com o representante do Atendimento ao cliente da Adobe.

Depois de selecionar Oracle, você pode adicionar os seguintes detalhes:

| Campo | Descrição |
| ----- | ----------- |
| Servidor | O URL do servidor Oracle. |
| Conta | O nome de usuário da conta. |
| Senha | A senha da conta. |

>[!TAB Snowflake]

>[!NOTE]
>
>Há suporte para o acesso seguro ao data warehouse externo do Snowflake por meio de link privado. Observe que a conta do Snowflake deve estar hospedada no Amazon Web Services (AWS) ou Azure e localizada na mesma região do ambiente da Composição de público-alvo federado. Entre em contato com o representante da Adobe para obter assistência na configuração do acesso seguro à conta do Snowflake.

Depois de selecionar o Snowflake, você pode escolher qual método de autenticação deseja usar ao se conectar com a Federated Audience Composition.

Se você selecionar **[!UICONTROL Conta/Autenticação de senha]**, poderá adicionar as seguintes informações de logon:

| Campo | Descrição |
| ----- | ----------- |
| Servidor | O nome do servidor. |
| Usuário(a) | O nome de usuário da conta. |
| Senha | A senha da conta. |

Como alternativa, você também pode fornecer uma chave privada em vez de fornecer uma senha. Se você adicionar uma chave privada, precisará fornecer as seguintes informações:

| Campo | Descrição |
| ----- | ----------- |
| Servidor | O nome do servidor. |
| Usuário(a) | O nome de usuário da conta. |
| Chave privada | A chave privada da conta. Somente `.pem` arquivos são suportados. |
| Senha | (Opcional) A senha da conta. |

Se você selecionar **[!UICONTROL OAuth 2.0]**, será possível adicionar as seguintes informações de logon:

>[!NOTE]
>
>Antes de se conectar ao Snowflake usando o OAuth 2.0, será necessário configurar o URL de redirecionamento no objeto de integração do Snowflake OAuth. Adicione a URL de redirecionamento `https://fac-oauth.adobe.io/oauth` à sua configuração de integração do Snowflake OAuth.

| Campo | Descrição |
| ----- | ----------- |
| Servidor | O nome do servidor. |
| ID de cliente | A ID do cliente do seu projeto do Snowflake. Este campo atua como um nome de usuário para o seu projeto. |
| Segredo do cliente | O segredo do cliente do seu projeto do Snowflake. Este campo atua como uma senha para o seu projeto. |

Selecione **[!UICONTROL Entrar]** para concluir sua autenticação.

Depois de inserir os detalhes de logon, é possível adicionar os seguintes detalhes:

| Campo | Descrição |
| ----- | ----------- |
| Banco de dados | O nome do banco de dados. Se isso for especificado no nome do servidor, esse campo poderá ser deixado em branco. |
| Esquema de trabalho | O nome do esquema de banco de dados a ser usado para as tabelas de trabalho. <br/><br/>**Observação:** você pode usar o esquema **any** do banco de dados, incluindo esquemas usados para processamento temporário de dados, desde que tenha as permissões necessárias para se conectar a este esquema. No entanto, você **deve** usar esquemas de trabalho distintos ao conectar várias sandboxes com o mesmo banco de dados. |
| Chave privada | A chave privada da conexão de banco de dados. Você pode carregar um arquivo `.pem` do seu sistema local. |
| Opções | Opções adicionais para a conexão. As opções disponíveis estão listadas na tabela a seguir. |

Para o Snowflake, você pode definir as seguintes opções adicionais:

| Opções | Descrição |
| ------- | ----------- |
| esquema de trabalho | O nome do esquema de banco de dados a ser usado para tabelas de trabalho. |
| TimeZoneName | O nome do fuso horário a ser usado. Este valor representa o parâmetro de sessão `TIMEZONE`. Por padrão, o fuso horário do sistema será usado. Para obter mais informações sobre fusos horários, leia a [documentação do Snowflake sobre fusos horários](https://docs.snowflake.com/en/sql-reference/parameters#timezone){target="_blank"}. |
| WeekStart | O dia em que você deseja que a semana comece. Este valor representa o parâmetro de sessão `WEEK_START`. Para obter mais informações sobre o início da semana, leia a [documentação do Snowflake sobre o parâmetro de início da semana](https://docs.snowflake.com/en/sql-reference/parameters#week-start){target="_blank"} |
| UseCachedResult | Um booleano que determina se os resultados em cache do Snowflake serão usados. Este valor representa o parâmetro de sessão `USE_CACHED_RESULTS`. Por padrão, esse valor está definido como verdadeiro. Para obter mais informações sobre esse parâmetro, leia a [documentação do Snowflake sobre resultados persistentes](https://docs.snowflake.com/en/user-guide/querying-persisted-results){target="_blank"}. |
| bulkThreads | O número de threads a serem usados para o carregador em massa do Snowflake. Quanto mais threads forem adicionados, melhor será o desempenho para cargas em massa maiores. Por padrão, esse valor é definido como 1. |
| chunkSize | O tamanho do arquivo de cada parte do carregador em massa. Quando usado simultaneamente com mais threads, você pode melhorar o desempenho de seus carregamentos em massa. Por padrão, esse valor é definido como 128 MB. Para obter mais informações sobre tamanhos de partes, leia a [documentação do Snowflake sobre preparação de arquivos de dados](https://docs.snowflake.com/en/user-guide/data-load-considerations-prepare){target="_blank"}. |
| StageName | O nome de um ambiente de preparo interno pré-provisionado. Isso pode ser usado em carregamentos em massa em vez de criar um novo estágio temporário. |

>[!TAB Teradata]

>[!NOTE]
>
>Para se conectar ao Teradata, você **deve** atender a vários pré-requisitos, incluindo a instalação de drivers de banco de dados. Entre em contato com o representante do Atendimento ao cliente da Adobe para obter mais informações.

Depois de selecionar Teradata, você pode adicionar os seguintes detalhes:

| Campo | Descrição |
| ----- | ----------- |
| Servidor | O URL do servidor Teradata. |
| Conta | O nome de usuário que o banco de dados usa para a sessão ODBC (Open Database Connectivity). |
| Senha | A senha usada para conectar-se à sessão ODBC. |
| Banco de dados | O nome do banco de dados. |
| Opções | Opções adicionais para a conexão. Para o Teradata, ambas as opções listadas são **obrigatórias** para serem adicionadas. As opções disponíveis estão listadas na tabela a seguir. |

Para o Teradata, você pode definir as seguintes opções adicionais:

| Opções | Descrição |
| ------- | ----------- |
| `workTableSchema` | O nome do esquema das tabelas de trabalho. |
| `ODBCLib` | A localização da biblioteca ODBC do sistema, que você pode usar se estiver misturando Teradata com outro ODBC. |

>[!TAB Vertica Analytics]

Depois de selecionar Vertica Analytics, você pode adicionar os seguintes detalhes:

| Campo | Descrição |
| ----- | ----------- |
| Servidor | O URL do servidor Vertica Analytics. |
| Conta | O nome de usuário da conta. |
| Senha | A senha da conta. |
| Banco de dados | O nome do banco de dados. Se isso for especificado no nome do servidor, esse campo poderá ser deixado em branco. |
| Esquema de trabalho | O nome do esquema de banco de dados a ser usado para as tabelas de trabalho. <br/><br/>**Observação:** você pode usar o esquema **any** do banco de dados, incluindo esquemas usados para processamento temporário de dados, desde que tenha as permissões necessárias para se conectar a este esquema. No entanto, você **deve** usar esquemas de trabalho distintos ao conectar várias sandboxes com o mesmo banco de dados. |
| Opções | Opções adicionais para a conexão. As opções disponíveis estão listadas na tabela a seguir. |

Para o Vertica Analytics, você pode definir as seguintes opções adicionais:

| Opções | Descrição |
| ------- | ----------- |
| TimeZoneName | O nome do fuso horário a ser usado. Este valor representa o parâmetro de sessão `TIMEZONE`. Para obter mais informações sobre fusos horários, leia a [documentação do Vertica Analytics sobre fusos horários](https://docs.vertica.com/24.1.x/en/admin/configuring-db/config-procedure/using-time-zones-with/){target="_blank"} |

>[!ENDTABS]

Depois de adicionar os detalhes da conexão, observe as seguintes configurações adicionais:

>[!NOTE]
>
>Para usar a Federated Audience Composition para um determinado banco de dados, você deve lista de permissões **todos** os endereços IP associados a esse banco de dados.

| Configurações | Detalhes |
| -------- | ------- |
| Habilitar conexão | Um botão booleano que determina se a conexão será ativada automaticamente. |
| IPs do servidor | Um popover que exibe quais endereços IP precisam ser resolvidos para se conectar ao banco de dados. |
| Testar conexão | Permite verificar os detalhes da configuração. |

Agora você pode selecionar **[!UICONTROL Implantar funções]**, seguido de **[!UICONTROL Adicionar]** para finalizar a conexão entre o banco de dados federado e o Experience Platform.

## Apêndice {#appendix}

O apêndice a seguir descreve como configurar as conexões do lado da conta externa.

### Configuração do Google BigQuery (Workload Identity Federation) {#wif-configuration}

Antes de definir a configuração da Google Cloud Platform, você precisará dos seguintes valores:

- ID da conta do AWS
   - Entre em contato com seu representante da Adobe para obter esse valor.
- Nome da função do AWS IAM
   - O nome da função IAM do AWS segue o formato resultante: `arn:aws:iam::<ADOBE_AWS_ACCOUNT_ID>:role/fac-<CUSTOMER_IMS_ORG_ID>`

No Google Cloud Console, crie um **Pool de Identidade da Carga de Trabalho** na **seção IAM e Administrador**. Isso permite organizar e gerenciar identidades externas.

Selecione **Adicionar provedor** para criar um provedor de identidade. Isso configura uma confiança unidirecional entre o provedor de identidade na Google Cloud e o Pool de identidade do trabalhador, fornecendo os metadados relevantes sobre o provedor.

![O botão Adicionar provedor está realçado na Google Cloud.](/help/connections/assets/home/select-add-provider.png)

Ao criar um provedor, será necessário fornecer as seguintes informações:

| Campo | Descrição |
| ----- | ----------- |
| Nome | O nome do provedor do Pool de Identidades da Carga de Trabalho. |
| ID | A ID do provedor é gerada automaticamente. |
| ID da conta do AWS | A ID de conta da AWS fornecida anteriormente. |
| Provedor habilitado | Um booliano que determina se o provedor está ativado ou desativado. |
| Mapeamento de atributos | Os mapeamentos para corresponder às funções. Essas informações já estão presentes. |

Depois de criar o provedor, é necessário criar uma política IAM para permitir que as identidades do Pool de Identidades da Carga de Trabalho representem a Conta de Serviço. Selecione **Conceder acesso** para abrir a caixa de diálogo Conceder acesso à conta de serviço.

Na caixa de diálogo, selecione **Conceder acesso usando representação de conta de serviço**. Na seção **Selecionar principais**, será necessário criar mapeamentos de atributos.

Selecione **aws_role** e adicione `arn:aws:sts::AWSAccountID:assumed-role/AWSRoleName` como valor, substituindo `AWSAccountID` e `AWSRoleName` pelos valores fornecidos anteriormente.

![A caixa de diálogo Conceder acesso é exibida.](/help/connections/assets/home/aws_role.png)

Depois de conceder acesso à conta de serviço, baixe a configuração da biblioteca do cliente.

![O local para baixar a configuração da biblioteca é exibido.](/help/connections/assets/home/download-config.png)

Após baixar a configuração da biblioteca do cliente, agora é possível configurar uma conexão WIF com a Configuração do Federated Audience.
