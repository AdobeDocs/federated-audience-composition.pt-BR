---
audience: end-user
title: Criar composições
description: Saiba como criar composições
exl-id: 4f510805-b700-444d-89bb-832eaa1e3242
source-git-commit: 65052ffcd8c70817aa428bea7f8b6baa0a49a1b0
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 22%

---

# Criar e configurar a composição {#create}

A primeira etapa para criar uma composição é definir seu rótulo e definir configurações adicionais, se necessário.

## Criar a composição {#create-the-composition}

1. Acesse o menu **[!UICONTROL Públicos-alvo]** e selecione a guia **[!UICONTROL Composições federadas]**.

1. Clique no botão **[!UICONTROL Criar composição]**.

   ![](assets/composition-create.png)

1. Na seção **[!UICONTROL Propriedades]**, especifique um rótulo para a composição e selecione um modelo de dados. Somente os esquemas associados a esse modelo de dados estarão disponíveis nas atividades de sua composição.

   ![](assets/composition-select-schema.png)

1. Clique em **[!UICONTROL Criar]**. A tela de composição é exibida. Agora você pode configurar sua composição adicionando quantas atividades forem necessárias para atender às suas necessidades antes de executá-la:

   * [Saiba como organizar atividades](orchestrate-activities.md)
   * [Saiba como iniciar e monitorar uma composição](start-monitor-composition.md)

## Definir as configurações da composição {#settings}

>[!CONTEXTUALHELP]
>id="dc_composition_settings_properties"
>title="Propriedades da composição"
>abstract="Esta seção fornece propriedades de composição genéricas que também podem ser acessadas ao criar a composição."

>[!CONTEXTUALHELP]
>id="dc_composition_settings_segmentation"
>title="Segmentação da composição"
>abstract="Por padrão, somente as tabelas de trabalho da última execução da composição são mantidas. Você pode habilitar essa opção para manter as tabelas de trabalho para fins de teste. Deve ser usada **somente** em ambientes de desenvolvimento ou de preparo. Essa opção nunca deve ser marcada em um ambiente de produção."

>[!CONTEXTUALHELP]
>id="dc_composition_settings_error"
>title="Configurações de gerenciamento de erros"
>abstract="Nesta seção, é possível definir como gerenciar erros durante a execução. É possível optar por pausar o processo, ignorar um determinado número de erros ou interromper a execução da composição."

Ao acessar uma composição, você pode acessar configurações avançadas que permitem, por exemplo, definir como a composição deve se comportar em caso de erro. Para acessar essas opções adicionais, clique no botão **[!UICONTROL Configurações]** localizado na seção superior da tela de criação da composição.

![](assets/composition-create-settings.png)

As configurações disponíveis são as seguintes:

* **[!UICONTROL Rótulo]**: altere o rótulo da composição.

* **[!UICONTROL Manter o resultado de populações interinas entre duas execuções]**: por padrão, somente as tabelas de trabalho da última execução da composição são mantidas. As tabelas de trabalho das execuções anteriores são removidas por uma composição técnica, executada diariamente.

  Se essa opção estiver ativada, as tabelas de trabalho serão mantidas mesmo após a execução da composição. Você pode usá-lo para fins de teste e, portanto, deve ser usado **somente** em ambientes de desenvolvimento ou de preparo. Ele nunca deve ser verificado em uma composição de produção.

* **[!UICONTROL Gerenciamento de erros]**: essa opção permite que você defina as ações a serem executadas se uma atividade de composição tiver erros. Há três opções possíveis:

   * **[!UICONTROL Suspender o processo]**: a composição é pausada automaticamente e seu status muda para **[!UICONTROL Falha]**. Quando o problema for resolvido, retome a composição usando os botões **[!UICONTROL Retomar]**.
   * **[!UICONTROL Ignorar]**: o status da tarefa que provocou o erro muda para **[!UICONTROL Falha]**, mas a composição mantém o status **[!UICONTROL Iniciado]**.
   * **[!UICONTROL Anular o processo]**: a composição é automaticamente interrompida e seu status muda para **[!UICONTROL Falha]**. Quando o problema for resolvido, reinicie a composição usando o botão **[!UICONTROL Iniciar]**.

* **[!UICONTROL Erros consecutivos]**: especifique o número de erros que podem ser ignorados antes que o processo seja interrompido. Após esse número ser alcançado, o status da composição será alterado para **[!UICONTROL Falha]**. Se o valor desse campo for 0, a composição nunca será interrompida, independentemente do número de erros.
