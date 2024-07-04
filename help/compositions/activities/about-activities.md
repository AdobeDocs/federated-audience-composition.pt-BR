---
audience: end-user
title: Trabalhar com atividades
description: Saiba como trabalhar com atividades
source-git-commit: 13e7e75fe1dc175fce9464fa58c7a50b5e6107d4
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 16%

---


# Trabalhar com atividades {#activities}

Na Composição de público-alvo federado, você pode criar composições usando dois tipos de atividades:

* **Atividades de direcionamento** As permitem criar um ou mais públicos-alvo definindo um público-alvo e dividindo ou combinando-os usando operações de interseção, união ou exclusão.
* **Controle de fluxo** As atividades do são específicas para organizar e executar composições. Sua principal tarefa é coordenar as outras atividades.

## Atividades de direcionamento

* [Criar atividade de público](build-audience.md): defina a população do target. Você pode selecionar um público existente ou usar o modelador de consultas para definir sua própria consulta.
* [Alterar dimensão](change-dimension.md): altere o targeting dimension enquanto constrói sua composição.
* [Combinar](combine.md): execute a segmentação na população de entrada. Você pode usar uma união, uma interseção ou uma exclusão.
* [Desduplicação](deduplication.md): exclua duplicatas no(s) resultado(s) das atividades de entrada.
* [Enriquecimento](enrichment.md): Defina dados adicionais para processar na sua composição. Com essa atividade, você pode aproveitar a transição de entrada e configurar a atividade para concluir a transição de saída com dados adicionais.
* [Reconciliação](reconciliation.md): defina o link entre os dados no banco de dados e os dados em uma tabela de trabalho, por exemplo, dados carregados de um arquivo externo.
* [Salvar público-alvo](save-audience.md): atualize um público-alvo ou crie um novo público-alvo a partir da população computada upstream em uma composição.
* [Split](split.md): segmente a população de entrada em vários subconjuntos.

## Atividades de controle de fluxo

* [AND-join](and-join.md): sincronize várias ramificações de execução de um fluxo de trabalho.
* **Fim** : marca graficamente o fim de um workflow. Essa atividade não tem impacto funcional e, portanto, é opcional.
* [Bifurcar](fork.md): crie transições de saída para iniciar várias atividades ao mesmo tempo.
* [Scheduler](scheduler.md): agenda quando o fluxo de trabalho é iniciado.
* [Aguardar](wait.md): pausa momentaneamente a execução de uma parte de um workflow.
