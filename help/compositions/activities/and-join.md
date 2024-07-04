---
audience: end-user
title: Usar a atividade AND-join
description: Saiba como usar a atividade AND-join
source-git-commit: 44be467650e2329a1fce6c5adb6d266d94efd1e2
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 57%

---

# AND-join {#join}

>[!CONTEXTUALHELP]
>id="dc_orchestration_and-join"
>title="Atividade AND-join"
>abstract="A variável **Associação AND** A atividade permite sincronizar várias ramificações de execução de uma composição. Ela é acionada quando todas as atividades anteriores forem concluídas. Isso permite verificar se determinadas atividades foram concluídas antes de continuar a executar a composição."

A variável **AND-join** A atividade permite sincronizar várias ramificações de execução de uma composição.

Essa atividade só acionará a transição de saída depois que todas as transições de entrada estiverem ativadas, ou seja, depois que todas as atividades anteriores estiverem concluídas. Isso permite verificar se determinadas atividades foram concluídas antes de continuar a executar a composição.

## Configurar a atividade AND-join {#and-join-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_and-join_merging"
>title="Configure a atividade AND-join"
>abstract="Selecione de quais atividades deseja juntar. No menu suspenso **Conjunto principal**, escolha a população de transição de entrada que deseja manter."

Siga estas etapas para configurar a atividade **AND-join**:

1. Adicione várias atividades para formar pelo menos duas ramificações de execução diferentes.
1. Adicione uma atividade **AND-join** a qualquer uma das ramificações.

   ![](../assets/and-join.png)

1. No **Opções de mesclagem** marque todas as atividades anteriores que deseja sincronizar.
1. No menu suspenso **Conjunto principal**, escolha a população de transição de entrada que deseja manter. A transição de saída só pode conter uma das populações de transição de entrada. Se a atividade não estiver configurada, a transição de saída selecionará aleatoriamente uma das populações de entrada.
