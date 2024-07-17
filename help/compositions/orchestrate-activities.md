---
audience: end-user
title: Criar composições
description: Saiba como criar composições
source-git-commit: 4a73702c99762a5e9ab73485fa46916b9c28fcc3
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 0%

---


# Orquestrar atividades de composição {#activities}

Depois de criar uma composição, você pode começar a orquestrar as diferentes tarefas que ela executará. Para fazer isso, é fornecida uma tela visual, que permite construir o diagrama de composição. Neste diagrama, é possível adicionar várias atividades e conectá-las em ordem sequencial.

## Adicionar atividades {#add}

Nessa etapa da configuração, o diagrama é exibido com um ícone de início, representando o início do workflow. Para adicionar sua primeira atividade, clique no botão **+** conectado ao ícone de início.

Uma lista de atividades que podem ser adicionadas ao diagrama é exibida. As atividades disponíveis dependem da sua posição no diagrama de composição. Por exemplo, ao adicionar sua primeira atividade, você pode iniciar sua composição direcionando um público-alvo, dividindo o caminho do fluxo de trabalho, configurando um agendador para atrasar a execução do fluxo de trabalho ou configurando uma atividade **Wait** para atrasar a execução do fluxo de trabalho. Por outro lado, após uma atividade **Criar público-alvo**, você pode refinar seu público-alvo com atividades de direcionamento ou organizar o processo de composição com atividades de controle de fluxo.

Depois que uma atividade é adicionada ao diagrama, um painel direito é exibido, permitindo configurar a atividade recém-adicionada com configurações específicas. Informações detalhadas sobre como configurar cada atividade estão disponíveis em [esta seção](activities/about-activities.md).

![](assets/composition-create-add.png)

Repita esse processo para adicionar quantas atividades desejar, dependendo das tarefas que deseja que sua composição execute. Observe que você também pode inserir uma nova atividade entre duas atividades. Para fazer isso, clique no botão **+** na transição entre as atividades, selecione a atividade desejada e a configure no painel direito.

>[!TIP]
>
>Você tem a opção de personalizar o nome das transições entre cada atividade. Para fazer isso, selecione a transição e altere seu rótulo no painel direito.

## A barra de ferramentas da tela {#toolbar}

A barra de ferramentas localizada no canto superior direito da tela fornece opções para manipular facilmente as atividades e navegar na tela.

![](assets/canvas-toolbar.png)

As ações disponíveis são:

* **Seleção múltipla**: selecione várias atividades para excluí-las todas de uma vez ou copie-as e cole-as. Consulte [esta seção](#copy).
* **Girar**: Alternar a tela verticalmente.
* **Ajustar à tela**: adapte o nível de zoom da tela à sua tela.
* **Menos zoom** / **Menos zoom**: Menos zoom ou mais zoom na tela.
* **Exibir mapa**: abre um instantâneo da tela mostrando que você está localizado.

## Gerenciar atividades {#manage}

Ao adicionar atividades, os botões de ação ficam disponíveis no painel de propriedades, permitindo que você execute várias operações.

![](assets/activity-actions.png)

É possível:

* **Excluir** a atividade da tela.
* **Desabilitar/Habilitar** a atividade. Quando o workflow é executado, as atividades desativadas e as atividades a seguir no mesmo caminho não são executadas e o workflow é interrompido.
* **Pausar/Retomar** a atividade. Quando o workflow é executado, ele é pausado na atividade pausada. A tarefa correspondente, bem como todas as que a seguem no mesmo caminho, não são executadas.
* **Copie** a atividade para colá-la em outro local na composição. Para fazer isso, clique no botão **+** em uma transição e selecione &quot;Colar atividade X&quot;. <!-- cannot copy multiple activities ? cannot paste in another composition?-->
* Configure **Opções de execução** para a atividade selecionada. Expanda a seção abaixo para saber mais sobre as opções disponíveis.

  +++Opções de execução disponíveis

  A seção **Properties** permite definir configurações genéricas referentes à execução da atividade:

   * **Execução**: defina a ação a ser executada quando o for iniciado.
   * **Duração máxima da execução**: especifique uma duração como &quot;30s&quot; ou &quot;1h&quot;. Se a atividade não for concluída após o término da duração especificada, um alerta será acionado. Isso não afeta o funcionamento do fluxo de trabalho.
   * **Fuso horário**: selecione o fuso horário da atividade. A Composição de público-alvo federado permite gerenciar as diferenças de tempo entre vários países na mesma instância. A configuração aplicada é definida quando a instância é criada.
   * **Afinidade**: forçar a atividade de composição a ser executada em uma máquina específica. Para fazer isso, é necessário especificar uma ou várias afinidades para a atividade em questão.
   * **Comportamento**: defina o procedimento a ser seguido se tarefas assíncronas forem usadas.

  A seção **Gerenciamento de erros** permite que você especifique a ação a ser executada caso a atividade encontre um erro.

  A seção **Initialization script** permite inicializar variáveis ou modificar propriedades de atividades. Clique no botão **Editar código** e digite o trecho de código a ser executado. O script é chamado quando a atividade é executada.

+++

* Acesse os **Logs e tarefas** da atividade.
