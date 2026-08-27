---
title: Conectar-se à Composição de Público Federado usando uma conexão privada
description: Saiba como configurar e se conectar à Federated Audience Composition usando uma conexão privada. Isso inclui PrivateLink ou VPN site a site.
source-git-commit: c4096e842caf383dee2e43bc80e18e1ac2036faf
workflow-type: tm+mt
source-wordcount: '1634'
ht-degree: 0%

---


# Conectividade privada com a Federated Audience Composition

A Federated Audience Composition oferece suporte a conexões privadas com vários bancos de dados. As conexões privadas permitem que você se conecte a data warehouses hospedados pelo cliente sem atravessar a Internet pública.

## Bancos de dados compatíveis {#supported-databases}

Os seguintes bancos de dados oferecem suporte à conectividade privada com a Federated Audience Composition:

| Banco de dados | Nuvem | Tipo de conexão privada |
| -------- | ----- | ----------------------- |
| [!DNL Snowflake] | [!DNL Amazon Web Services] (AWS) | AWS PrivateLink (endpoint da interface do VPC) |
| [!DNL Snowflake] | [!DNL Microsoft Azure] | Azure PrivateLink (Ponto de extremidade privado) |
| [!DNL Amazon Redshift] | [!DNL Amazon Web Services] (AWS) | AWS PrivateLink (endpoint do Managed VPC) |
| [!DNL Databricks] | [!DNL Amazon Web Services] (AWS) | AWS PrivateLink (endpoint da interface do VPC) |
| [!DNL Databricks] | [!DNL Microsoft Azure] | VPN site a site |
| [!DNL Databricks] | [!DNL Google Cloud Platform] (GCP) | VPN site a site |
| [!DNL Azure Synapse Analytics] | [!DNL Microsoft Azure] | VPN site a site |
| [!DNL Google BigQuery] | [!DNL Google Cloud Platform] (GCP) | VPN site a site |

## Snowflake {#snowflake}

>[!AVAILABILITY]
>
>Para usar a conectividade privada com [!DNL Snowflake], você **deve** estar pelo menos na camada Crítico para Negócios ou superior em [!DNL Snowflake]. Para obter mais informações sobre conectividade privada com o [!DNL Snowflake], leia o [guia de conectividade privada na documentação do Snowflake](https://docs.snowflake.com/en/user-guide/private-connectivity-inbound).

O uso da conectividade privada com [!DNL Snowflake] depende de em qual provedor de nuvem sua instância [!DNL Snowflake] está.

### Amazon Web Services (AWS) {#snowflake-aws}

>[!IMPORTANT]
>
>Antes de continuar, obtenha a ID de conta da AWS do Atendimento ao cliente da Adobe. Depois de obter sua ID de conta da AWS, contate o suporte do [!DNL Snowflake] para que o [!DNL Snowflake] possa autorizar sua conta da AWS a usar o PrivateLink.

Depois que sua conta do AWS for autorizada para uso com o [!DNL Snowflake], você precisará obter valores como `privatelink-vpce-id`, `privatelink-account-url` e `privatelink_ocsp-url` para obter o ponto de extremidade da interface do VPC.

Para obter esses valores, execute os seguintes comandos na conta do [!DNL Snowflake] como ACCOUNTADMIN:

`SELECT SYSTEM$GET_PRIVATELINK_CONFIG();`
`SELECT SYSTEM$ALLOWLIST_PRIVATELINK();`

Depois de executar esses comandos, você poderá enviar a saída completa do SQL para o Atendimento ao cliente da Adobe, para que a Adobe possa criar o endpoint da interface do VPC para você.

Para obter informações mais detalhadas sobre como criar uma conexão PrivateLink com o AWS, leia o [Guia do AWS PrivateLink](https://docs.snowflake.com/en/user-guide/admin-security-privatelink).

Se você quiser autorizar o PrivateLink para uso com um ambiente de preparo interno, entre em contato com o Atendimento ao cliente da Adobe para ativar o ambiente.

Para obter informações mais detalhadas sobre como criar uma conexão PrivateLink com o AWS para ambientes internos de preparo, leia o [manual de endpoints da interface do AWS VPC para estágios internos](https://docs.snowflake.com/en/user-guide/private-internal-stages-aws).

### Microsoft Azure {#snowflake-azure}

Para o Microsoft Azure, será necessário obter valores como `privatelink-pls-id`, `privatelink-account-url` e `privatelink_ocsp-url` para criar o ponto de extremidade privado do Azure.

Você pode obter esses valores executando os seguintes comandos na conta do Snowflake:

`SELECT SYSTEM$GET_PRIVATELINK_CONFIG();`
`SELECT SYSTEM$ALLOWLIST_PRIVATELINK();`

Depois de executar esses comandos, você poderá enviar a saída completa do SQL para o Atendimento ao cliente da Adobe, para que a Adobe possa criar o endpoint privado da Azure para você.

Depois que o Adobe criar o endpoint privado do Azure, você poderá obter sua ID de recurso de endpoint privado. Agora que você tem a ID de recurso do ponto de extremidade privado, contate o suporte do [!DNL Snowflake] para autorizar a conta do [!DNL Snowflake] e, ao mesmo tempo, forneça a ID do recurso.

Para obter informações mais detalhadas sobre como criar uma conexão PrivateLink com o Azure, leia o [Guia do Azure PrivateLink](https://docs.snowflake.com/en/user-guide/privatelink-azure).

Se você quiser autorizar o PrivateLink para uso com um ambiente de preparo interno, execute o seguinte comando em [!DNL Snowflake], enquanto fornece a ID do recurso de preparo interno fornecida pelo Atendimento ao cliente da Adobe:

`SELECT SYSTEM$AUTHORIZE_STAGE_PRIVATELINK_ACCESS('<internal-stage-private-endpoint-resource-id>');`

Para obter informações mais detalhadas sobre como criar uma conexão PrivateLink com o Azure para ambientes internos de preparo, leia o [guia de endpoints privados do Azure para estágios internos](https://docs.snowflake.com/en/user-guide/private-internal-stages-azure).

## Amazon Redshift {#amazon-redshift}

Os clusters provisionados e o Redshift ServerLless oferecem suporte a conexões privadas com o Federated Audience Composition.

>[!IMPORTANT]
>
>Antes de iniciar, entre em contato com o Atendimento ao cliente da Adobe para receber a ID da conta da Amazon Web Services (AWS) e a ID da Virtual Private Cloud (VPC). Você precisará de **ambos** desses valores para obter acesso ao ponto de extremidade entre contas. Para obter informações mais detalhadas sobre como conceder acesso à VPC, leia o [guia sobre concessão de acesso à VPC](https://docs.aws.amazon.com/redshift/latest/mgmt/managing-cluster-cross-vpc-console-grantor.html).

Depois de ter as IDs do AWS e do VPC, acesse o AWS Management Console para conceder acesso entre contas a um endpoint gerenciado do VPC.

Para um cluster provisionado, observe os valores de **ID de Cluster Redshift** e **ID de conta de AWS do proprietário do cluster**. Para um sem servidor Redshift, observe os valores de **nome do grupo de trabalho** e **ID da conta de AWS do proprietário**.

Depois de obter esses valores, compartilhe esses detalhes com o Atendimento ao cliente da Adobe para que a Adobe possa criar o endpoint gerenciado da VPC. O Adobe compartilhará os seguintes detalhes de conexão com você: **URL do ponto de extremidade Redshift**, **URL do Redshift JDBC** e **URL do Redshift ODBC**.

## Databricks {#databricks}

>[!AVAILABILITY]
>
>Para usar conectividade privada com Databricks, você **deve** estar em um plano Enterprise em Databricks. Para obter mais informações sobre conectividade privada com Databricks, leia o [guia de conceitos de link privado](https://docs.databricks.com/aws/en/security/network/concepts/privatelink-concepts).

O uso de conectividade privada com Databricks depende de em qual provedor de nuvem sua instância do Databricks está.

### Amazon Web Services {#databricks-aws}

Antes de configurar com o Amazon Web Services, entre em contato com o Atendimento ao cliente da Adobe para que ele possa criar um endpoint de interface de front-end (entrada) do VPC que aponte para Databricks. Esse endpoint aborda a conectividade ODBC do Federated Audience Composition com o espaço de trabalho dos Databricks.

Depois de obter a ID do endpoint da VPC e a região do AWS no Atendimento ao cliente da Adobe, será necessário registrar o endpoint da VPC com as informações fornecidas pela Adobe.

Depois de registrar o endpoint do VPC, será necessário criar um objeto Private Access Settings (PAS). Ao criar o ponto de extremidade, defina o **Nível de Acesso Privado** para um nível de **Ponto de Extremidade** e selecione o ponto de extremidade do VPC criado anteriormente. Para obter mais informações sobre como criar configurações de acesso privado, leia o [guia de configuração de PrivateLink de entrada](https://docs.databricks.com/aws/en/security/network/front-end/front-end-private-connect#step-3-create-private-access-settings).

Após definir as configurações de acesso privado, é possível anexar o endpoint do VPC ao espaço de trabalho. Para obter mais informações sobre como criar seu espaço de trabalho com o PrivateLink, leia o [guia de configuração do PrivateLink de entrada](https://docs.databricks.com/aws/en/security/network/front-end/front-end-private-connect#step-4-create-your-workspace-with-private-link-objects).

Agora que todas as configurações foram definidas, você pode compartilhar o URL do espaço de trabalho dos Databricks com o Atendimento ao cliente da Adobe. Depois de compartilhar a URL do espaço de trabalho dos Databricks, o Adobe pode definir as configurações de DNS necessárias para rotear solicitações para o ponto de extremidade do espaço de trabalho.

### Microsoft Azure {#databricks-azure}

Uma VPN site a site é usada para se conectar com segurança do Adobe ao espaço de trabalho do Databricks no Azure. Você precisará configurar um gateway de VPN Azure para estabelecer o túnel VPN para transmitir com segurança seus dados ao Adobe.

Depois de configurar seu Azure VPN Gateway e o ponto de extremidade privado dos Databricks, compartilhe os seguintes detalhes com o representante do Atendimento ao cliente da Adobe: **Gateway de Rede Virtual da Azure**, **IP do Ponto de Extremidade Privado dos Databricks**, **URL do Databricks Workspace** e **ASN (Número de Sistema Autônomo)**.

Com esses detalhes, o Adobe pode estabelecer os túneis VPN necessários para sua conexão. Depois de estabelecer os túneis VPN, a Adobe fornece os **endereços IP público e privado de Túnel VPN**, as **chaves pré-compartilhadas** e o **número de sistema autônomo**.

Agora você pode configurar seus túneis VPN no Azure VPN Gateway. Para obter mais informações, leia o [guia do gateway de VPN para conectar o AWS e o Azure](https://learn.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-howto-aws-bgp).

### Google Cloud Platform {#databricks-gcp}

Uma VPN site a site é usada para se conectar com segurança do Adobe ao espaço de trabalho do Databricks na Google Cloud Platform. Você precisará configurar um gateway de VPN de alta disponibilidade e um roteador de nuvem da Google Cloud Platform para estabelecer o túnel de VPN e transmitir com segurança seus dados para a Adobe.

Depois de configurar o gateway HA VPN GCP e o roteador de nuvem, compartilhe os seguintes detalhes com o representante do Atendimento ao cliente da Adobe: **Gateway HA VPN GCP**, **URL do Workspace Databricks**, **IP da PSC (Conexão de Serviço Privado)** e o **ASN (Número de Sistema Autônomo)**.

Com esses detalhes, o Adobe pode estabelecer os túneis VPN necessários para sua conexão. Depois de estabelecer os túneis VPN, a Adobe fornece os **endereços IP público e privado de Túnel VPN**, as **chaves pré-compartilhadas** e o **número de sistema autônomo**.

Agora você pode configurar os túneis VPN na sua conta da Google Cloud Platform. Para obter mais informações, leia o [guia Criar conexões VPN HA](https://docs.cloud.google.com/network-connectivity/docs/vpn/tutorials/create-ha-vpn-connections-google-cloud-aws).

## Azure Synapse Analytics {#azure-synapse}

Para se conectar com o Azure Synapse Analytics, primeiro será necessário criar um gateway de rede virtual do Azure e um terminal privado do Synapse. O gateway de rede virtual do Azure permite enviar tráfego criptografado entre uma rede virtual Azure para o Synapse, enquanto o endpoint privado do Synapse permite que você tenha uma conexão privada para transmitir seus dados com segurança.

Depois de configurar o gateway de rede virtual do Azure e o ponto de extremidade privado do Synapse, compartilhe os seguintes detalhes com o representante do Atendimento ao cliente da Adobe: **Gateway de Rede Virtual do Azure**, **IP do Ponto de Extremidade Privado do Synapse**, **URL do Synapse Workspace** e **ASN (Número de Serviço Autônomo)**.

Com esses detalhes, o Adobe pode estabelecer os túneis VPN necessários para sua conexão. Depois de estabelecer os túneis VPN, a Adobe fornece os **pares de túnel VPN**, **chaves pré-compartilhadas**, bem como um **número de sistema autônomo**.

Agora você pode configurar seus túneis VPN no Azure VPN Gateway. Para obter mais informações, leia o [guia do gateway de VPN para conectar o AWS e o Azure](https://learn.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-howto-aws-bgp).

## Google Big Query {#gbq}

Para se conectar com o Google Big Query, primeiro será necessário criar um gateway de VPN de alta disponibilidade da Google Cloud Platform e um roteador de nuvem.

Depois de configurar o gateway HA VPN GCP e o roteador de nuvem, compartilhe os seguintes detalhes com o representante do Atendimento ao cliente da Adobe: **Gateway HA VPN GCP**, **IP de PSC (Conexão de Serviço Privado)** e o **ASN (Número de Sistema Autônomo)**.

Com esses detalhes, o Adobe pode estabelecer os túneis VPN necessários para sua conexão. Depois de estabelecer os túneis VPN, a Adobe fornece os **endereços IP público e privado de Túnel VPN**, as **chaves pré-compartilhadas** e o **número de sistema autônomo**.

Agora você pode configurar os túneis VPN na sua conta da Google Cloud Platform. Para obter mais informações, leia o [guia Criar conexões VPN HA](https://docs.cloud.google.com/network-connectivity/docs/vpn/tutorials/create-ha-vpn-connections-google-cloud-aws).
