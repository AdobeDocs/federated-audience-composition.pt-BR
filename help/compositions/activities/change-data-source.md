---
audience: end-user
title: Alterar atividade do Data Source
description: Saiba como você pode usar a atividade Alterar fonte de dados para alterar a fonte de dados usada por sua composição, fornecendo mais flexibilidade no gerenciamento de dados em uma composição.
exl-id: 8f8e627a-fef9-42b8-a42a-bfa1c421b202
source-git-commit: 59983bb7fd0f8886cc38bfcfc8d7005db4747ac0
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 3%

---

# Alterar fonte de dados

>[!IMPORTANT]
>
>As atividades **[!UICONTROL Alterar dimensão]** e **[!UICONTROL Alterar fonte de dados]** devem **não** ser adicionadas em uma linha. Se você precisar usar ambas as atividades consecutivamente, inclua uma atividade **[!UICONTROL Enriquecimento]** entre elas. Isso garante a execução adequada e evita possíveis conflitos ou erros.

A atividade **[!UICONTROL Alterar fonte de dados]** permite alterar a fonte de dados usada pela sua composição.

## Configurar  {#configure}

Depois de adicionar uma atividade **[!UICONTROL Alterar fonte de dados]** à tela, você pode definir a fonte de dados para o fluxo de trabalho.

![A opção de fonte de dados está realçada no espaço de trabalho de Composição de Público Federado.](/help/compositions/assets/change-data-source/configure.png){zoomable="yes"}{width="70%"}

| Fonte | Descrição |
| ------ | ----------- |
| Conta externa FDA | Um banco de dados de nuvem externo conectado à Federated Audience Composition. |

Depois de selecionar **[!UICONTROL FDA external account]**, você pode escolher com qual conta externa deseja se conectar.

![O popover que exibe as opções da conta externa é exibido.](/help/compositions/assets/change-data-source/fda-external-account.png){zoomable="yes"}{width="70%"}
