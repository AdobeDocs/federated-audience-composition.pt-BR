---
audience: end-user
title: Usar a atividade de espera
description: Saiba como usar a atividade de espera
source-git-commit: b21306cefe6e9e66263012110a7f89f2d92b38a5
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 60%

---

# Aguardar {#wait}

>[!CONTEXTUALHELP]
>id="dc_orchestration_wait"
>title="Atividade Aguardar"
>abstract="A atividade **Aguardar** é usada para atrasar a transição de uma atividade para outra."

A variável **Aguardar** atividade permitem que um determinado período transcorra entre duas atividades que estão sendo executadas. Por exemplo, a espera de vários dias após uma atividade de entrega de email para depois analisar as aberturas e os cliques gerados durante esse período antes de executar qualquer operação de acompanhamento (email de lembrete, criação de público-alvo, etc.).

## Configuração{#wait-configuration}

Siga estas etapas para configurar a atividade **Aguardar**:

1. Adicionar um **Aguardar** atividade na sua composição.

1. Especifique a **Duração** da espera entre as transições de entrada e saída.

1. Selecione a unidade de tempo na variável **Períodos** campo: segundos, minutos, horas, dias.


