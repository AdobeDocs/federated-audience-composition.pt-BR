---
audience: end-user
title: Criar composições
description: Saiba como criar composições
source-git-commit: b946f8821d965fb00f79f6f5557adcfff1ee2387
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 0%

---


# Iniciar e monitorar sua composição {#start-monitor}

Depois de criar sua composição e projetar as tarefas a serem executadas na tela, você poderá iniciá-la e monitorar como ela está sendo executada.

## Iniciar a composição {#start}

Para iniciar a composição, navegue até a **[!UICONTROL Composições]** ou na campanha associada e clique no link **[!UICONTROL Início]** no canto superior direito da tela.

Quando a composição estiver em execução, cada atividade na tela de desenho será executada em ordem sequencial, até que o final da composição seja atingido.

Você pode acompanhar o progresso de perfis direcionados em tempo real usando um fluxo visual. Isso permite identificar rapidamente o status de cada atividade e o número de perfis em transição entre elas.

## Transições de composição {#transitions}

Em composições, os dados transportados de uma atividade para outra por meio de transições são armazenados em uma tabela de trabalho temporária. Esses dados podem ser exibidos para cada transição. Para fazer isso, selecione uma transição para abrir as propriedades no lado direito da tela.

* Clique em **[!UICONTROL Visualizar esquema]** para exibir o schema da tabela de trabalho.
* Clique em **[!UICONTROL Visualizar resultados]** para visualizar os dados transportados na transição selecionada.

## Monitorar execução da atividade {#activities}

Os indicadores visuais no canto superior direito de cada caixa de atividade permitem verificar a execução:

| Indicador visual | Descrição |
|-----|------------|
|  | A atividade está sendo executada no momento. |
|  | A atividade requer sua atenção. Isso pode envolver a confirmação do envio de um delivery ou a tomada de uma ação necessária. |
|  | A atividade encontrou um erro. Para resolver o problema, abra os logs de composição para obter mais informações. |
|  | A atividade foi executada com sucesso. |

## Monitorar logs e tarefas {#logs-tasks}

O monitoramento de logs e tarefas de composição é uma etapa essencial para analisar suas composições e garantir que elas estejam sendo executadas corretamente. Elas podem ser acessados pelo **[!UICONTROL Logs]** ícone que está disponível na barra de ferramentas da ação e no painel de propriedades de cada atividade.

A variável **[!UICONTROL Logs e tarefas]** O menu fornece um histórico da execução da composição, registrando todas as ações do usuário e encontrando erros. Esse histórico é salvo pela duração especificada na composição [opções de execução](composition-settings.md). Durante essa duração, todas as mensagens são salvas, mesmo após uma reinicialização da composição. Se não quiser salvar as mensagens de uma execução anterior, clique no link **[!UICONTROL Purge history]** botão.

Dois tipos de informações estão disponíveis:

* A variável **[!UICONTROL Log]** contém o histórico de execução de todas as atividades de composição. Ele indexa as operações realizadas e os erros de execução por ordem cronológica.
* A variável **[!UICONTROL Tarefas]** A guia detalha a sequência de execução das atividades.

Em ambas as guias, você pode escolher as colunas exibidas e sua ordem, aplicar filtros e usar o campo de pesquisa para localizar rapidamente as informações desejadas.

## Comandos de execução de composição {#execution-commands}

A barra de ação no canto superior direito fornece comandos que permitem gerenciar a execução da composição. É possível:

* **[!UICONTROL Início]** / **[!UICONTROL Retomar]** a execução da composição, que assume o status In progress. Se a composição tiver sido pausada, ela será retomada, caso contrário, ela será iniciada e as atividades iniciais serão ativadas.

* **[!UICONTROL Pausar]** a execução da composição, que assume o status Paused. Nenhuma nova atividade será ativada até que seja retomada, mas as operações em andamento não são suspensas.

* **[!UICONTROL Parar]** uma composição que está sendo executada, que assumirá o status Concluído. Se possível, as operações em andamento são interrompidas. Não é possível retomar da composição no mesmo local em que ela foi interrompida.
