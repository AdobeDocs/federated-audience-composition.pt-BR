---
audience: end-user
title: Introdução a composições
description: Saiba como começar com composições
source-git-commit: 8f4242b02f2cd135bf4adc3a69db08fe1f812e4e
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 9%

---

# Introdução a composições {#compositions}

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_properties"
>title="Propriedades de composição"
>abstract="Esta seção fornece propriedades de composição genéricas que também são acessíveis ao criar a composição."

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_segmentation"
>title="Segmentação de composição"
>abstract="Por padrão, somente as tabelas de trabalho da última execução da composição são mantidas. Você pode ativar essa opção para manter as tabelas de trabalho para fins de teste. Deve ser usado **somente** em ambientes de desenvolvimento ou de preparo. Nunca deve ser verificado em um ambiente de produção."




## O que é uma composição? {#compositions-start}


>[!CONTEXTUALHELP]
>id="dc_workflow_list"
>title="Composições"
>abstract="Nesta tela, você pode acessar a lista completa de composições, verificar o status atual, as datas de última/próxima execução e criar uma nova composição."


## Configurações de gerenciamento de erros  {#error-settings}

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_error"
>title="Configurações de gerenciamento de erros"
>abstract="Nesta seção, você pode definir como gerenciar erros durante a execução. Você pode optar por pausar o processo, ignorar um determinado número de erros ou interromper a execução da composição."

* **[!UICONTROL Gerenciamento de erros]**: este campo permite que você defina as ações que serão executadas se uma atividade de composição tiver erros.
Há três opções possíveis:

   * **[!UICONTROL Suspender processo]**: a composição é pausada automaticamente e seu status é alterado para **[!UICONTROL Failed]**. Quando o problema for resolvido, retome a composição usando o **[!UICONTROL Retomar]** botões.
   * **[!UICONTROL Ignorar]**: O status da tarefa que provocou o erro muda para **[!UICONTROL Failed]**, mas a composição mantém o **[!UICONTROL Iniciado]** status.
   * **[!UICONTROL Interromper o processo]**: a composição é interrompida automaticamente e seu status muda para **[!UICONTROL Failed]**. Quando o problema for resolvido, reinicie a composição usando o **[!UICONTROL Início]** botão.

* **[!UICONTROL Consecutive errors]**: este campo fica disponível quando o **[!UICONTROL Ignorar]** valor estiver selecionado na variável **[!UICONTROL No caso de erros]** campo. Você pode especificar quantos erros podem ser ignorados antes que o processo seja interrompido. Após esse número ser alcançado, o status da composição será alterado para **[!UICONTROL Failed]**. Se o valor desse campo for 0, a composição nunca será interrompida, independentemente do número de erros.
