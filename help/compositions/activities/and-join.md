---
audience: end-user
title: Usar a atividade AND-join
description: Saiba como usar a atividade AND-join
source-git-commit: e2e708a21aa0e2d1724f5ba79caf10ef803ae818
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 66%

---

# AND-join {#join}

>[!CONTEXTUALHELP]
>id="dc_orchestration_and-join"
>title="Atividade AND-join"
>abstract="A variável **Associação AND** A atividade permite sincronizar várias ramificações de execução de uma composição. Ela é acionada quando todas as atividades anteriores forem concluídas. Isso permite verificar se determinadas atividades foram concluídas antes de continuar a executar a composição."

A variável **Associação AND** A atividade permite sincronizar várias ramificações de execução de uma composição.

Essa atividade só acionará a transição de saída depois que todas as transições de entrada estiverem ativadas, ou seja, depois que todas as atividades anteriores estiverem concluídas. Isso permite verificar se determinadas atividades foram concluídas antes de continuar a executar a composição.

## Configurar a atividade AND-join {#and-join-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_and-join_merging"
>title="Configure a atividade AND-join"
>abstract="Selecione de quais atividades deseja juntar. No menu suspenso **Conjunto principal**, escolha a população de transição de entrada que deseja manter."

Siga estas etapas para configurar a atividade **AND-join**:

1. Adicione várias atividades, como atividades de canal, para formar pelo menos duas ramificações de execução diferentes.
1. Adicione uma atividade **AND-join** a qualquer uma das ramificações.
1. Na seção **Opções de mesclagem**, marque todas as atividades anteriores que você deseja mesclar.
1. No menu suspenso **Conjunto principal**, escolha a população de transição de entrada que deseja manter. A transição de saída só pode conter uma das populações de transição de entrada.

