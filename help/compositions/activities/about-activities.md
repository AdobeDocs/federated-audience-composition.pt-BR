---
audience: end-user
title: Trabalhar com atividades
description: Saiba como trabalhar com atividades
exl-id: 1e4e5f53-636f-4f1c-bf2f-cc3b5d6d6dda
source-git-commit: 95f262e44c392c1e3c861a2b77b7736657cb9371
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 35%

---

# Trabalhar com atividades {#activities}

Na Composição de público-alvo federado, você pode criar composições usando dois tipos de atividades:

* **As atividades de direcionamento** permitem criar um ou mais destinos definindo um público-alvo e dividindo ou combinando esses públicos-alvo usando operações de interseção, união ou exclusão.
* As atividades de **Controle de fluxo** são específicas para organizar e executar composições. Sua principal tarefa é coordenar as outras atividades.

## Atividades de direcionamento

>[!NOTE]
>
>Ao trabalhar com atividades de composição, os nomes de atributo **não podem** conter espaços.

* [Criar atividade de público-alvo](build-audience.md): defina sua população de destino. Você pode selecionar um público-alvo já existente ou usar o modelador de consultas para definir a sua própria consulta.
* [Alterar fonte de dados](./change-data-source.md): altere a fonte de dados usada pela sua composição.
* [Alterar dimensão](change-dimension.md): altere o esquema, também conhecido como targeting dimension, à medida que você constrói sua composição.
* [Combinar](combine.md): aplique uma segmentação à sua população de entrada. Você pode usar uma união, uma interseção ou uma exclusão.
* [Desduplicação](deduplication.md): exclua duplicatas no(s) resultado(s) das atividades de entrada.
* [Enriquecimento](enrichment.md): defina dados adicionais para processar em sua composição. Com essa atividade, você pode aproveitar a transição de entrada e configurar a atividade para concluir a transição de saída com dados adicionais.
* [Reconciliação](reconciliation.md): defina o vínculo entre os dados no banco de dados e os dados em uma tabela de trabalho, por exemplo, dados carregados de um arquivo externo.
* [Salvar público-alvo](save-audience.md): atualize um público-alvo existente ou crie um novo público-alvo a partir da população computada upstream em uma composição.
* [Divisão](split.md): segmente a população de entrada em vários subconjuntos.

## Atividades de controle do fluxo

* [AND-join](and-join.md): sincroniza várias ramificações de execução de uma composição.
* **Fim**: marca graficamente o fim de uma composição. Essa atividade não tem impacto funcional e, portanto, é opcional.
* [Bifurcação](fork.md): crie transições de saída para iniciar várias atividades ao mesmo tempo.
* [Agendador](scheduler.md): agenda quando a composição é iniciada.
* [Aguardar](wait.md): pausar momentaneamente a execução de uma parte de uma composição.
