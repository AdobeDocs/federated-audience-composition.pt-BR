---
audience: end-user
title: Usar a atividade Query incremental
description: Saiba como usar a atividade de Query incremental
hide: true
hidefromtoc: true
source-git-commit: 34d6fc8f97c491fcb91eebf8e1377018e5020a4a
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 19%

---

# Consulta incremental {#incremental-query}

<!-- Warning : contextual help IDs are declared in /start/get-started.md-->

A atividade de **Consulta incremental** permite consultar o banco de dados de forma agendada. Todas as vezes que essa atividade é executada, os resultados das execuções anteriores são excluídos. Ela permite direcionar somente elementos novos.

A atividade **[!UICONTROL Query incremental]** pode ser usada para vários tipos de usos:

* Segmentação de indivíduos para definir o público-alvo ou o público de uma mensagem, etc.
* Exportação de dados. Por exemplo, você pode usar a atividade para exportar regularmente novos logs em arquivos. Pode ser útil se você quiser usar seus dados de log em ferramentas externas de BI ou geração de relatórios.

A população já direcionada por execuções anteriores é armazenada na composição. Isso significa que duas composições iniciadas do mesmo modelo não compartilham o mesmo log. No entanto, duas tarefas baseadas no mesmo query incremental na mesma composição usam o mesmo log.

Se o resultado de um query incremental for igual a 0 durante uma de suas execuções, a composição será pausada até a próxima execução programada do query. As transições e as atividades que seguem o query incremental não são, portanto, processadas antes da execução a seguir.

## Configurar a atividade de query incremental {#incremental-query-configuration}

Siga estas etapas para configurar a atividade **Consulta incremental**:

1. Adicione uma atividade de **Consulta incremental** à sua composição.

1. Na seção **[!UICONTROL Público-alvo]**, escolha a **Dimensão de direcionamento** e clique em **[!UICONTROL Continuar]**.

   O targeting dimension permite definir a população-alvo da operação: destinatários, beneficiários(as) de contrato, operadores(as), assinantes, etc. Por padrão, o target é selecionado dos recipients. <!--[Learn more about targeting dimensions](../../audience/about-recipients.md#targeting-dimensions)-->

1. Use o modelador de consultas para definir seu query, da mesma forma que você cria um público-alvo ao criar um novo email. [Saiba como trabalhar com o modelador de consultas](../../query/query-modeler-overview.md)

1. Na seção **[!UICONTROL Dados processados]**, selecione o modo incremental a ser usado:

   * **[!UICONTROL Excluir resultados da execução anterior]**: cada vez que a atividade é executada, os resultados das execuções anteriores são excluídos.

     Os registros já direcionados em execuções anteriores podem ser registrados em um número máximo de dias a partir do dia em que foram direcionados. Para fazer isso, use o campo **[!UICONTROL Histórico em dias]**. Se esse valor for zero, os destinatários nunca serão removidos do log.

   * **[!UICONTROL Usar um campo de data]**: essa opção permite excluir resultados de execuções anteriores com base em um campo de data específico. Para fazer isso, escolha o campo de data desejado na lista de atributos disponíveis para o targeting dimension selecionado. Nas próximas execuções da composição, somente os dados que foram modificados ou criados após a última data de execução serão recuperados.

     Após a primeira execução da composição, o campo **[!UICONTROL Data da última execução]** ficará disponível. Especifica a data que será usada para a próxima execução e é atualizada automaticamente sempre que a composição for executada. Você ainda tem a possibilidade de substituir esse valor, inserindo manualmente um novo para que ele se ajuste às suas necessidades.

   >[!NOTE]
   >
   >O modo **[!UICONTROL Usar um campo de data]** permite mais flexibilidade dependendo do campo de data selecionado. Por exemplo, se o campo especificado corresponder a uma data de modificação, o modo de campo de data permitirá recuperar dados que foram atualizados recentemente, enquanto o outro modo simplesmente excluirá gravações que já foram direcionadas para uma execução anterior, mesmo que elas tenham sido modificadas desde a última execução da composição.

<!--

## Example {#incremental-query-example}

The following example shows the configuration of a workflow which filters every week the profiles in the Adobe Campaign database that are subscribed to the Yoga Newsletter service, to send them a welcome email.

![](../assets/incremental-query-example.png)

The workflow is made up of the following elements:

* A **[!UICONTROL Scheduler]** activity, to execute the workflow every Monday at 6 am.
* An **[!UICONTROL Incremental query]** activity, which targets all of the current subscribers during the first execution, then only the new subscribers of that week during the following executions.
* An **[!UICONTROL Email delivery]** activity.
-->
