---
audience: end-user
title: Usar a atividade Scheduler
description: Saiba como usar a atividade Scheduler
source-git-commit: 4dca96ae81d1f70c8f20509fdbd9ec31e05c01dc
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 33%

---


# Scheduler {#scheduler}

>[!CONTEXTUALHELP]
>id="dc_orchestration_scheduler"
>title="Atividade Scheduler"
>abstract="A atividade **Scheduler** permite programar quando o fluxo de trabalho será iniciado. Esta atividade deve ser considerada como um início programado. Ela só pode ser usada como a primeira atividade do fluxo de trabalho."

A atividade **Scheduler** é uma atividade de **Controle de fluxo**. Ele permite programar quando a composição será iniciada. Esta atividade deve ser considerada como um início programado. Ela só pode ser usada como a primeira atividade da composição.

## Configuração de atividade do scheduler {#scheduler-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_schedule_validity"
>title="Validade do Scheduler"
>abstract="É possível definir um período de validade para o Scheduler. Pode ser permanente (padrão) ou pode ser válido até uma data específica."

>[!CONTEXTUALHELP]
>id="dc_orchestration_schedule_options"
>title="Opções do Scheduler"
>abstract="Defina a frequência do scheduler. Pode ser executado em um momento específico, uma ou várias vezes por dia, semana ou mês."

Siga estas etapas para configurar a atividade **Scheduler**:

1. Adicione uma atividade **Scheduler** ao seu fluxo de trabalho.

1. Configure a **Frequência de execução**:

   * **Uma vez**: a composição é executada uma única vez.

   * **Diariamente**: a composição é executada em um horário específico, uma vez por dia.

   * **Várias vezes ao dia:** a composição é executada regularmente várias vezes ao dia. Você pode configurar as execuções em horários específicos ou periodicamente.

     >[!NOTE]
     >
     >Não agende uma composição para execução por mais de 15 minutos, pois pode atrapalhar o desempenho geral do sistema e criar bloqueios no banco de dados.

   * **Semanalmente**: a composição é executada em um momento especificado, uma ou várias vezes por semana.

   * **Monthly**: a composição é executada em um momento especificado, uma ou várias vezes por mês. Você pode selecionar meses quando precisar que a composição seja executada. Você também pode configurar as execuções em dias da semana especificados do mês, como a segunda terça-feira do mês.

1. Defina os detalhes da execução de acordo com a frequência selecionada. Os campos de detalhes podem variar dependendo da frequência usada (tempo, frequência de repetição, dias especificados etc.).

1. Clique em **Visualizar horários de inicialização** para verificar o agendamento das próximas dez execuções da sua composição.

1. Defina o período de validade do scheduler:

   * **Permanente (nunca expira)**: a composição é executada, de acordo com a frequência especificada, sem limites para o intervalo de tempo ou o número de iterações.

   * **Período de validade**: a composição é executada de acordo com a frequência especificada, até uma data específica. É necessário especificar datas de início e término.

>[!NOTE]
>
>Se quiser iniciar a composição imediatamente, clique em **Executar tarefa pendente** na barra de ação superior do agendador. Esse botão só estará disponível quando você tiver iniciado a composição.

<!--## Example{#scheduler-example}

In the following example, the activity is configured so that the composition runs several times a day at 9 and 12 AM, every day of the week from October 1st, 2023 to January 1st, 2024.-->

