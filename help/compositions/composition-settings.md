---
audience: end-user
title: Criar composições
description: Saiba como criar composições
source-git-commit: 4ccf3be01abb8d6cb2834f49d83b677edaa61ef7
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 2%

---


# Definir as configurações da composição {#settings}

>[!CONTEXTUALHELP]
>id="dc_composition_settings_properties"
>title="Propriedades de composição"
>abstract="Esta seção fornece propriedades de composição genéricas que também são acessíveis ao criar a composição."

>[!CONTEXTUALHELP]
>id="dc_composition_settings_segmentation"
>title="Segmentação de composição"
>abstract="Por padrão, somente as tabelas de trabalho da última execução da composição são mantidas. Você pode ativar essa opção para manter as tabelas de trabalho para fins de teste. Deve ser usado **somente** em ambientes de desenvolvimento ou de preparo. Nunca deve ser verificado em um ambiente de produção."

>[!CONTEXTUALHELP]
>id="dc_composition_settings_error"
>title="Configurações de gerenciamento de erros"
>abstract="Nesta seção, você pode definir como gerenciar erros durante a execução. Você pode optar por pausar o processo, ignorar um determinado número de erros ou interromper a execução da composição."

Ao acessar uma composição, você pode acessar configurações avançadas que permitem, por exemplo, definir como a composição deve se comportar em caso de erro ou gerenciar o atraso após o qual o histórico de composição deve ser removido.

Para acessar opções adicionais para sua composição, clique no link **Configurações** botão localizado acima da tela.

![](assets/composition-create-settings.png)

As configurações disponíveis são as seguintes:

* **[!UICONTROL Rótulo]**: altere o rótulo da composição.

* **[!UICONTROL Manter o resultado de públicos provisórios entre duas execuções]**: por padrão, somente as tabelas de trabalho da última execução da composição são mantidas. As tabelas de trabalho das execuções anteriores são removidas por uma composição técnica, executada diariamente.

  Se essa opção estiver ativada, as tabelas de trabalho serão mantidas mesmo após a execução da composição. Você pode usá-lo para fins de teste e, portanto, deve ser usado **somente** em ambientes de desenvolvimento ou de preparo. Ele nunca deve ser verificado em uma composição de produção.

* **[!UICONTROL Gerenciamento de erros]**: esta seção permite que você defina as ações que serão executadas se uma atividade de composição tiver erros. Há três opções possíveis:

   * **[!UICONTROL Suspender processo]**: a composição é pausada automaticamente e seu status é alterado para **[!UICONTROL Failed]**. Quando o problema for resolvido, retome a composição usando o **[!UICONTROL Retomar]** botões.
   * **[!UICONTROL Ignorar]**: O status da tarefa que provocou o erro muda para **[!UICONTROL Failed]**, mas a composição mantém o **[!UICONTROL Iniciado]** status.
   * **[!UICONTROL Interromper o processo]**: a composição é interrompida automaticamente e seu status muda para **[!UICONTROL Failed]**. Quando o problema for resolvido, reinicie a composição usando o **[!UICONTROL Início]** botão.

* **[!UICONTROL Consecutive errors]**: especifique o número de erros que podem ser ignorados antes que o processo seja interrompido. Após esse número ser alcançado, o status da composição será alterado para **[!UICONTROL Failed]**. Se o valor desse campo for 0, a composição nunca será interrompida, independentemente do número de erros.
