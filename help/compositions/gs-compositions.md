---
audience: end-user
title: Introdução a composições
description: Saiba como começar com composições
source-git-commit: 0d6930b15be5013b57b8859dd3d21a5d3367ecae
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 11%

---

# Introdução a composições {#compositions}

## O que é uma composição? {#what}

A Composição de dados de Adobe permite criar composições, onde você pode aproveitar várias atividades (dividir, excluir...) em uma tela visual para criar públicos. Depois de concluído, os públicos-alvo resultantes são salvos na Adobe Experience Platform junto com os públicos-alvo existentes e podem ser aproveitados em destinos como o Journey Optimizer para direcionar clientes.

![](assets/composition-example.png)

## Acessar e gerenciar composições {#access}

>[!CONTEXTUALHELP]
>id="dc_composition_list"
>title="Composições"
>abstract="Nesta tela, é possível acessar a lista completa de composições, verificar o status atual, as datas da última/próxima execução e criar uma nova composição."

As composições podem ser acessadas no Adobe Experience Platform **[!UICONTROL Públicos-alvo]** no menu, no **Composições federadas** guia.

Nessa tela, é possível criar novas composições e acessar as existentes. Também é possível duplicar ou excluir uma composição existente clicando no botão de reticências ao lado do nome.

![](assets/compositions-list.png)

Para refinar a lista e encontrar facilmente a composição que está procurando, você pode pesquisar a lista e filtrar as composições por status ou datas do último processamento.

Você também pode personalizar a lista adicionando ou removendo colunas. Para fazer isso, clique no link **Configurar coluna** s e adicionar ou remover as colunas de saída desejadas.

![](assets/compositions-columns.png)

## Status das composições {#status}

As composições podem ter vários status:

* **[!UICONTROL Rascunho]**: A composição foi criada e salva.
* **[!UICONTROL Em andamento]**: A composição foi executada e está em execução no momento.
* **[!UICONTROL Parado]**: a execução da composição foi interrompida.
* **[!UICONTROL Pausado]**: a execução da composição foi pausada.
* **[!UICONTROL Errado]**: a execução da composição encontrou um erro. Abra a composição e acesse os logs e as tarefas para identificar o erro e resolvê-lo.

Informações detalhadas sobre como iniciar e monitorar uma composição estão disponíveis em [nesta seção](../compositions/start-monitor-composition.md).