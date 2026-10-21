---
audience: end-user
title: Introdução a composições
description: Saiba como começar a usar as composições
exl-id: 92142d16-3483-4f6e-afde-9f88d5d7d1c4
TQID: https://experienceleague.adobe.com/-SzMG0wJnEcqFJPJZqBWKD8y22d4Z525Obe5CnyhcfE
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: CX Enterprise
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
    internal-label: Governance
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
source-git-commit: 062f7f55aafbbe5999c1a0d31ddea542f9b4b75d
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 59%
---
# Visão geral das composições

>[!AVAILABILITY]
>
>Para acessar composições, você precisará de uma das seguintes permissões:
>
>-**Gerenciar Composições Federadas**
>-**Visualizar composições federadas**
>
>Para mais informações sobre as permissões exigidas, leia o [guia de controle de acesso](/help/governance-privacy-security/access-control.md).

A Composição de público-alvo federado permite criar composições, onde é possível aproveitar várias atividades em uma tela visual para criar públicos-alvo. Após criar a composição, os públicos-alvo resultantes são salvos na Adobe Experience Platform e podem ser aproveitados nos destinos da Experience Platform e no Adobe Journey Optimizer para o direcionamento de clientes.

![Um exemplo de fluxo de trabalho de composição é exibido na composição de público-alvo federado.](/help/compositions/assets/home/composition-example.png){zoomable="yes"}{width="70%"}

## Componentes de composição {#components}

Uma composição na Composição do Federated Audience é composta pelas seguintes partes:

- **[!UICONTROL Atividades]**: uma atividade é uma tarefa a ser executada, e são representadas na composição por ícones.
- **[!UICONTROL Transições]**: as transições vinculam uma atividade de origem a uma atividade de destino e definem sua sequência. As informações contidas nas transições são armazenadas em uma tabela de trabalho. Cada composição usa várias tabelas de trabalho. Os dados transmitidos nessas tabelas podem ser usados durante todo o ciclo de vida da composição.

## Acessar e gerenciar composições {#access}

>[!CONTEXTUALHELP]
>id="dc_composition_list"
>title="Composições"
>abstract="Nesta tela, é possível acessar a lista completa de composições, verificar o status atual, as datas da última/próxima execução e criar uma nova composição."

As composições podem ser acessadas a partir do menu **[!UICONTROL Públicos-alvo]** da Adobe Experience Platform, na guia **[!UICONTROL Composições federadas]** dentro da seção **[!UICONTROL Clientes]**.

![Os botões Federated compositions e Audiences estão destacados, mostrando como acessar a seção federated compositions.](/help/compositions/assets/home/access-fac-compositions.png){zoomable="yes"}{width="70%"}

Nessa tela, é possível exibir informações sobre as composições e criar novas composições.

![A lista de composições federadas é exibida.](/help/compositions/assets/home/composition-list.png){zoomable="yes"}{width="70%"}

| Campo | Descrição |
| ----- | ----------- |
| **[!UICONTROL Nome]** | O nome da composição. Se você selecionar a composição, poderá editá-la. Para obter mais informações sobre criação e edição de composições, leia o [criar um guia de composição](/help/compositions/create-composition.md). |
| **[!UICONTROL Status]** | O status da composição. Os valores possíveis incluem [!UICONTROL Rascunho], [!UICONTROL Em andamento], [!UICONTROL Parado], [!UICONTROL Pausado] e [!UICONTROL Incorreto]. <ul><li>**[!UICONTROL Rascunho]**: A composição foi criada e salva.</li><li>**[!UICONTROL Em andamento]**: a composição foi executada e está em execução no momento.</li><li>**[!UICONTROL Parado]**: a execução da composição foi concluída e interrompida.</li><li>**[!UICONTROL Pausado]**: a execução da composição foi pausada.</li><li>**[!UICONTROL Erro]**: a execução da composição encontrou um erro. Para exibir mais informações sobre o erro, abra a composição e acesse os logs.</li></ul> Para saber como iniciar ou parar uma composição, leia o [guia de criação de composição](./create-composition.md#monitor-logs). |
| **[!UICONTROL Criado por]** | O nome e o endereço de email da pessoa que criou a composição. |
| **[!UICONTROL Modificado]** | A data e a hora em que a composição foi atualizada pela última vez. |

Também é possível executar ações rápidas nas composições selecionando o botão ![reticências](/help/assets/icons/more.png) ao lado do nome.

| Ação | Descrição |
| ------ | ----------- |
| **[!UICONTROL Duplicar]** | Duplica a composição selecionada. |
| **[!UICONTROL Excluir]** | Exclui a composição selecionada. |
| **[!UICONTROL Adicionar ao pacote]** | Move a composição entre sandboxes. Para obter mais informações sobre este recurso, leia o [guia de ferramentas da sandbox](https://experienceleague.adobe.com/en/docs/experience-platform/sandbox/ui/sandbox-tooling). |

Para refinar a lista e encontrar a composição que está procurando, é possível pesquisar na lista e filtrar as composições por status ou data do último processamento.

Você também pode personalizar a lista adicionando ou removendo colunas. Para fazer isso, clique no botão **[!UICONTROL Configurar colunas]** e adicione ou remova as colunas de saída desejadas.

![É exibida uma lista das colunas disponíveis para adicionar à página de navegação das composições.](/help/compositions/assets/home/compositions-columns.png){zoomable="yes"}{width="70%"}

### Aplicar rótulos de acesso {#access-labels}

Para aplicar rótulos de acesso a uma composição específica, selecione a composição e depois escolha **[!UICONTROL Gerenciar acesso]**.

![O botão &quot;Gerenciar acesso&quot; está realçado na tela de composição.](/help/compositions/assets/home/select-manage-access.png){zoomable="yes"}{width="70%"}

O popover **[!UICONTROL Gerenciar acesso]** é exibido. Nessa página, é possível aplicar os rótulos de acesso e governança de dados compatíveis com a composição.

![O popover Gerenciar acesso é exibido. Isso mostra uma lista de todos os rótulos disponíveis aplicáveis à composição.](/help/compositions/assets/home/manage-access.png){zoomable="yes"}{width="70%"}

| Tipo de rótulo | Descrição |
| ---------- | ----------- |
| Rótulos de contrato | Os rótulos de contrato (&quot;C&quot;) são usados para categorizar dados que contêm obrigações contratuais ou que estão relacionados às políticas de governança de dados da sua organização. |
| Rótulos de identidade | Os rótulos de identidade (&quot;I&quot;) são usados para categorizar dados que podem ser usados para identificar ou entrar em contato com uma pessoa específica. |
| Rótulos de sensibilidade | Rótulos de sensibilidade (&quot;S&quot;) são usados para categorizar dados que você e/ou sua organização consideram confidenciais. |
| Rótulos de ecossistema de parceiros | Os rótulos de ecossistemas de parceiros são usados para categorizar dados de fontes externas à organização. |

Para obter mais informações sobre rótulos de acesso e governança de dados, leia o [glossário de rótulos de uso de dados](https://experienceleague.adobe.com/pt-br/docs/experience-platform/data-governance/labels/reference).

## Criar {#create}

Você pode criar uma composição para o Adobe Experience Platform usando a Composição de público-alvo. Para obter mais informações, leia o [criar um guia de composição](./create-composition.md).

## Próximas etapas

Depois de ler este guia, você aprendeu a acessar, gerenciar e criar rótulos de acesso para suas composições. Para obter mais informações sobre como trabalhar com públicos-alvo como um todo, leia o [guia de públicos-alvo](../start/audiences.md).
