---
audience: end-user
title: Introdução a composições
description: Saiba como começar a usar as composições
exl-id: 92142d16-3483-4f6e-afde-9f88d5d7d1c4
source-git-commit: 5c16e22587cbbbe5bc87cfa4f22210aa8108341c
workflow-type: ht
source-wordcount: '551'
ht-degree: 100%

---

# Introdução a composições {#compositions}

>[!AVAILABILITY]
>
>Para acessar composições, você precisará de uma das seguintes permissões:
>
>-**Gerenciar composições federadas**
>>-**Visualizar composições federadas**
>
>Para mais informações sobre as permissões exigidas, leia o [guia de controle de acesso](/help/governance-privacy-security/access-control.md).

A Composição de público-alvo federado permite criar composições, onde é possível aproveitar várias atividades em uma tela visual para criar públicos-alvo. Após criar a composição, os públicos-alvo resultantes são salvos na Adobe Experience Platform e podem ser aproveitados nos destinos da Experience Platform e no Adobe Journey Optimizer para o direcionamento de clientes.

![Um exemplo de fluxo de trabalho de composição é exibido na composição de público-alvo federado.](assets/gs-compositions/composition-example.png){zoomable="yes"}{width="70%"}

## Acessar e gerenciar composições  {#access}

>[!CONTEXTUALHELP]
>id="dc_composition_list"
>title="Composições"
>abstract="Nesta tela, é possível acessar a lista completa de composições, verificar o status atual, as datas da última/próxima execução e criar uma nova composição."

As composições podem ser acessadas a partir do menu **[!UICONTROL Públicos-alvo]** da Adobe Experience Platform, na guia **[!UICONTROL Composições federadas]** dentro da seção **[!UICONTROL Clientes]**.

Nessa tela, é possível criar novas composições e acessar as já existentes. Também é possível duplicar ou excluir uma composição existente clicando no botão de ![reticências](/help/assets/icons/more.png) ao lado do nome.

Você também pode exibir informações sobre as composições, incluindo o nome, o status, o criador e a última data de modificação.

| Status | Descrição |
| ------ | ----------- |
| **[!UICONTROL Rascunho]** | A composição foi criada e salva. |
| **[!UICONTROL Em andamento]** | A composição foi iniciada e está em execução no momento. |
| **[!UICONTROL Interrompida]** | A execução da composição foi concluída e interrompida. |
| **[!UICONTROL Em pausa]** | A execução da composição foi pausada. |
| **[!UICONTROL Incorreta]** | A execução da composição encontrou um erro. Para exibir mais informações sobre o erro, abra a composição e acesse os logs. |

Você pode aprender como iniciar ou parar uma composição no [guia de início e monitoramento de composição](./start-monitor-composition.md).

![Uma lista de composições disponíveis é exibida.](assets/gs-compositions/compositions-list.png){zoomable="yes"}{width="70%"}{align="center"}

Para refinar a lista e encontrar a composição que está procurando, é possível pesquisar na lista e filtrar as composições por status ou data do último processamento.

Você também pode personalizar a lista adicionando ou removendo colunas. Para fazer isso, clique no botão **[!UICONTROL Configurar colunas]** e adicione ou remova as colunas de saída desejadas.

![É exibida uma lista das colunas disponíveis para adicionar à página de navegação das composições.](assets/gs-compositions/compositions-columns.png){zoomable="yes"}{width="70%"}{align="center"}

### Aplicar rótulos de acesso {#access-labels}

Para aplicar rótulos de acesso a uma composição específica, selecione a composição e depois escolha **[!UICONTROL Gerenciar acesso]**.

![O botão &quot;Gerenciar acesso&quot; está realçado na tela de composição.](assets/gs-compositions/select-manage-access.png){zoomable="yes"}{width="70%"}{align="center"}

O popover **[!UICONTROL Gerenciar acesso]** é exibido. Nessa página, é possível aplicar os rótulos de acesso e governança de dados compatíveis com a composição.

![O popover Gerenciar acesso é exibido. Isso mostra uma lista de todos os rótulos disponíveis aplicáveis à composição.](assets/gs-compositions/manage-access.png){zoomable="yes"}{width="70%"}{align="center"}

| Tipo de rótulo | Descrição |
| ---------- | ----------- |
| Rótulos de contrato | Os rótulos de contrato (&quot;C&quot;) são usados para categorizar dados que contêm obrigações contratuais ou que estão relacionados às políticas de governança de dados da sua organização. |
| Rótulos de identidade | Os rótulos de identidade (&quot;I&quot;) são usados para categorizar dados que podem ser usados para identificar ou entrar em contato com uma pessoa específica. |
| Rótulos de sensibilidade | Rótulos de sensibilidade (&quot;S&quot;) são usados para categorizar dados que você e/ou sua organização consideram confidenciais. |
| Rótulos de ecossistema de parceiros | Os rótulos de ecossistemas de parceiros são usados para categorizar dados de fontes externas à organização. |

Para obter mais informações sobre rótulos de acesso e governança de dados, leia o [glossário de rótulos de uso de dados](https://experienceleague.adobe.com/pt-br/docs/experience-platform/data-governance/labels/reference).

## Próximas etapas

Depois de ler este guia, você aprendeu a acessar, gerenciar e criar rótulos de acesso para suas composições. Para obter mais informações sobre como trabalhar com públicos-alvo como um todo, leia o [guia de públicos-alvo](../start/audiences.md).
