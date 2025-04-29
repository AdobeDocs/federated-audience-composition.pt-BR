---
title: Permissões para acessar um banco de dados externo
description: Saiba mais sobre os direitos específicos de cada mecanismo de banco de dados
source-git-commit: 8cd1b967e004d84fda3788e442e41d2010f5ec24
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 46%

---

# Matriz de direitos FDA {#fda-rights}

A tabela abaixo descreve os privilégios de banco de dados necessários para cada sistema, permitindo que os usuários executem operações em bancos de dados externos por meio do FDA.

|   | Snowflake | Redshift | Google BigQuery | Databricks |
|:-:|:-:|:-:|:-:|:-:|
| **Conexão com o banco de dados remoto** | Privilégios de USAGE ON WAREHOUSE, USAGE ON DATABASE e USAGE ON SCHEMA | Criar um usuário vinculado à conta AWS | Criar uma conta de serviço e conceder acesso principal ao projeto | Privilégio USE CATALOG no Catálogo e privilégio CAN_USE no SQL Warehouse |
| **Criar tabelas** | Privilégio CRIAR TABELA NO SCHEMA | Privilégio CRIAR | A função atribuída à conta de serviço deve conter: permissões bigquery.jobs.create e bigquery.tables.create | Privilégio USAR ESQUEMA e privilégio CRIAR TABELA |
| **Criar índices** | N/D | Privilégio CRIAR | O BigQuery só oferece suporte a índices de pesquisa. A função atribuída à conta de serviço deve conter: permissões bigquery.jobs.create, bigquery.tables.getData e bigquery.tables.createIndex | N/D |
| **Criar funções** | Privilégio CRIAR FUNÇÃO NO SCHEMA | Privilégio plpythonu USO EM IDIOMA para poder chamar scripts python externos | A função atribuída à conta de serviço deve conter: permissões bigquery.jobs.create e bigquery.routines.create | Privilégio CRIAR FUNÇÃO |
| **Criar procedimentos** | N/D | Privilégio plpythonu USO EM IDIOMA para poder chamar scripts python externos | A função atribuída à conta de serviço deve conter: permissões bigquery.jobs.create e bigquery.routines.create |  N/D |
| **Remover objetos (tabelas, índices, funções, procedimentos)** | Propriedade do objeto | Ter o objeto ou ser um superusuário | A função atribuída à conta de serviço deve conter: permissões bigquery.jobs.create, bigquery.routines.delete, bigquery.tables.delete e bigquery.tables.deleteIndex |
| **Monitoramento de execuções** | Privilégio MONITORAR no objeto necessário | Não é necessário nenhum privilégio para usar o comando EXPLICAR | função monitoring.viewer | Privilégio CAN_VIEW |
| **Gravação de dados** | Privilégios INSERIR e/ou ATUALIZAR (que depende da operação de gravação) | Privilégios INSERIR e ATUALIZAR | A função atribuída à conta de serviço deve conter: bigquery.jobs.create e bigquery.tables.updateData |  Privilégio MODIFICAR |
| **Carregamento de dados em tabelas** | Privilégios CRIAR ETAPA NO SCHEMA, SELECIONAR e INSERIR na tabela do direcionamento | Privilégios SELECIONAR e INSERIR | A função atribuída à conta de serviço deve conter: bigquery.jobs.create, bigquery.tables.getData e bigquery.tables.updateData | Privilégios SELECIONAR e MODIFICAR |
| **Acesso aos dados do cliente** | Privilégio(s) SELECIONAR em (FUTURO) TABELA(S) ou VISUALIZAÇÃO(es) | Privilégio SELECIONAR | A função atribuída à conta de serviço deve conter: bigquery.jobs.create e bigquery.tables.getData para tabelas ou função bigquery.dataViewer |  Privilégio SELECT |
| **Acesso aos metadados** | Privilégio SELECIONAR no ESQUEMA de INFORMATION_SCHEMA | Privilégio SELECIONAR | função bigquery.metadataViewer |  Privilégio SELECIONAR no ESQUEMA INFORMATION_SCHEMA |


|   | Microsoft Fabric | Azure Synapse Analytics | Vertica |
|:-:|:-:|:-:|:-:|
| **Conexão com o banco de dados remoto** | Permissão de leitura (padrão) | Permissão CONECTAR | Não é necessário nenhum privilégio |
| **Criar tabelas** | CRIAR TABELA NO BANCO DE DADOS (warehouse) e ALTERAR NO SCHEMA | Permissão CRIAR TABELA | Privilégio CRIAR EM SCHEMA |
| **Criar índices** | N/D | Permissão ALTERAR | N/D |
| **Criar funções** | N/D | Permissão CRIAR FUNÇÃO | Privilégio CRIAR EM SCHEMA |
| **Criar procedimentos** | CRIAR PROCEDIMENTO NO BANCO DE DADOS (warehouse) e ALTERAR NO SCHEMA | Permissão CRIAR PROCEDIMENTO | Privilégio CRIAR EM SCHEMA |
| **Remover objetos (tabelas, índices, funções, procedimentos)** | ALTERAR NO ESQUEMA | Permissão ALTERAR | Propriedade do objeto ou privilégio SOLTAR no objeto |
| **Monitoramento de execuções** | Permissões do Workspace Contributor ou superior (queryinsights.exec_requests_history)  | Permissão CONTROLE | Não é necessário nenhum privilégio para usar a instrução EXPLICAR |
| **Gravação de dados** | INSERIR e/ou ATUALIZAR NO OBJETO | Permissões INSERIR e ATUALIZAR | Privilégios INSERIR e ATUALIZAR |
| **Carregamento de dados em tabelas** | SELECIONAR NO OBJETO e INSERIR NO OBJETO | CRIAR TABELA, EXECUTAR, SELECIONAR, INSERIR, ATUALIZAR, ALTERAR permissões | Privilégio INSERIR na tabela, privilégio USO no esquema |
| **Acesso aos dados do cliente** | SELECIONAR NO OBJETO | Permissão SELECIONAR  | Privilégio SELECIONAR |
| **Acesso aos metadados** | SELECIONAR EM INFORMATION_SCHEMA | Não é necessária nenhuma permissão para descrever a tabela | USO NO ESQUEMA, SELECT na TABELA e também privilégios em tabelas v_catalog.columns e v_catalog.view_columns |
