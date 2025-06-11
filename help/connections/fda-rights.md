---
title: Permissões para acessar um banco de dados externo
description: Saiba quais permissões são necessárias para acessar e executar tarefas em cada mecanismo de banco de dados
exl-id: 287fb4a4-5767-4337-96be-dceca55f756d
source-git-commit: 530a8709a67fabec1a36e1661b922f3e9a9e6996
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 25%

---

# Matriz de direitos do Federated Data Access (FDA) {#fda-rights}

A tabela a seguir descreve as permissões de banco de dados necessárias para cada sistema, permitindo executar operações em bancos de dados externos por meio do FDA (Federated Data Access — Acesso a Dados Federados).

|   | Snowflake | Redshift | Google BigQuery | Databricks |
|:-:|:-:|:-:|:-:|:-:|
| **Conexão com o banco de dados remoto** | Privilégios `USAGE ON WAREHOUSE`, `USAGE ON DATABASE` e `USAGE ON SCHEMA` | Criar um usuário vinculado à conta do AWS | Criar uma conta de serviço e conceder acesso principal ao projeto | Permissão `USE CATALOG` no Catálogo e permissão `CAN_USE` no SQL Warehouse |
| **Criar tabelas** | Privilégio `CREATE TABLE ON SCHEMA` | `CREATE` permissão | A função atribuída à conta de serviço deve conter: `bigquery.jobs.create` e `bigquery.tables.create` permissões | `USE SCHEMA` e `CREATE TABLE` permissões |
| **Criar índices** | N/D | `CREATE` permissão | O BigQuery só oferece suporte a índices de pesquisa. A função atribuída à conta de serviço deve conter: `bigquery.jobs.create`, `bigquery.tables.getData` e `bigquery.tables.createIndex` permissões | N/D |
| **Criar funções** | Privilégio `CREATE FUNCTION ON SCHEMA` | `USAGE ON LANGUAGE plpythonu` permissão para chamar scripts Python externos | A função atribuída à conta de serviço deve conter: `bigquery.jobs.create` e `bigquery.routines.create` permissões | `CREATE FUNCTION` permissão |
| **Criar procedimentos** | N/D | `USAGE ON LANGUAGE plpythonu` permissão para chamar scripts Python externos | A função atribuída à conta de serviço deve conter: `bigquery.jobs.create` e `bigquery.routines.create` permissões |  N/D |
| **Remover objetos (tabelas, índices, funções, procedimentos)** | Propriedade do objeto | Ter o objeto ou ser um superusuário | A função atribuída à conta de serviço deve conter: `bigquery.jobs.create`, `bigquery.routines.delete`, `bigquery.tables.delete` e `bigquery.tables.deleteIndex` permissões | N/D |
| **Monitoramento de execuções** | Privilégio `MONITOR` no objeto necessário | Nenhuma permissão necessária para usar o comando `EXPLAIN` | Função de `monitoring.viewer` | `CAN_VIEW` permissão |
| **Gravação de dados** | Privilégios `INSERT` e/ou `UPDATE` (dependendo da operação de gravação) | `INSERT` e `UPDATE` permissões | A função atribuída à conta de serviço deve conter: `bigquery.jobs.create` e `bigquery.tables.updateData` | `MODIFY` permissão |
| **Carregamento de dados em tabelas** | `CREATE STAGE ON SCHEMA`, `SELECT` e `INSERT` sobre os privilégios de tabela de destino | `SELECT` e `INSERT` permissões | A função atribuída à conta de serviço deve conter: `bigquery.jobs.create`, `bigquery.tables.getData` e `bigquery.tables.updateData` | `SELECT` e `MODIFY` permissões |
| **Acesso aos dados do cliente** | Privilégio(s) `SELECT on (FUTURE) TABLE(S)` ou `VIEW(S)` | `SELECT` permissão | A função atribuída à conta de serviço deve conter: `bigquery.jobs.create` e `bigquery.tables.getData` para tabelas ou a função `bigquery.dataViewer` | `SELECT` permissão |
| **Acesso aos metadados** | Privilégio `SELECT on INFORMATION_SCHEMA SCHEMA` | `SELECT` permissão | Função de `bigquery.metadataViewer` |  `SELECT on INFORMATION_SCHEMA SCHEMA` permissão |


|   | Microsoft Fabric | Azure Synapse Analytics | Vertica |
|:-:|:-:|:-:|:-:|
| **Conexão com o banco de dados remoto** | Permissão de leitura (padrão) | `CONNECT` permissão | Não é necessário nenhum privilégio |
| **Criar tabelas** | `CREATE TABLE ON DATABASE` (warehouse) e `ALTER ON SCHEMA` | `CREATE TABLE` permissão | Privilégio `CREATE ON SCHEMA` |
| **Criar índices** | N/D | `ALTER` permissão | N/D |
| **Criar funções** | N/D | `CREATE FUNCTION` permissão | Privilégio `CREATE ON SCHEMA` |
| **Criar procedimentos** | `CREATE PROCEDURE ON DATABASE` (warehouse) e `ALTER ON SCHEMA` | `CREATE PROCEDURE` permissão | Privilégio `CREATE ON SCHEMA` |
| **Remover objetos (tabelas, índices, funções, procedimentos)** | `ALTER ON SCHEMA` | `ALTER` permissão | Propriedade do objeto ou do privilégio `DROP` no objeto |
| **Monitoramento de execuções** | Workspace Contributor ou permissões acima (`queryinsights.exec_requests_history`) | `CONTROL` permissão | Não é necessário nenhum privilégio para usar a instrução `EXPLAIN` |
| **Gravação de dados** | `INSERT` e/ou `UPDATE ON OBJECT` | `INSERT` e `UPDATE` permissões | Privilégios de `INSERT` e `UPDATE` |
| **Carregamento de dados em tabelas** | `SELECT ON OBJECT` e `INSERT ON OBJECT` | `CREATE TABLE`, `EXECUTE`, `SELECT`, `INSERT`, `UPDATE` e `ALTER` permissões | Privilégio `INSERT` na tabela, privilégio `USAGE` no esquema |
| **Acesso aos dados do cliente** | `SELECT ON OBJECT` | `SELECT` permissão | Privilégio `SELECT` |
| **Acesso aos metadados** | `SELECT ON INFORMATION_SCHEMA` | Não é necessária nenhuma permissão para descrever a tabela | `USAGE ON SCHEMA`, `SELECT on TABLE` e também privilégios nas tabelas `v_catalog.columns` e `v_catalog.view_columns` |
