---
audience: end-user
title: Usar a atividade Salvar perfis
description: Saiba como usar a atividade Salvar perfis
exl-id: 1c840838-32d5-4ceb-8430-835a235b7436
source-git-commit: c76ef4b64a58d3d43e78b489a1efe1a97a8c09f7
workflow-type: tm+mt
source-wordcount: '563'
ht-degree: 12%

---

# Salvar perfis {#save-profile}

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile"
>title="Salvar perfis"
>abstract="A atividade Salvar perfis permite enriquecer perfis da Experience Platform federando dados de depósitos externos, permitindo aprimorar os perfis do cliente com atributos adicionais. "

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_aepschemalist"
>title="Selecionar esquema do Experience Platform"
>abstract="Escolha o esquema da Experience Platform para os perfis."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_primaryidentitynamespace"
>title="Selecione o campo de identificação principal"
>abstract="Selecione a Identidade principal a ser usada para identificar os perfis direcionados no banco de dados."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_selectaepschema"
>title="Selecionar esquema do Experience Platform"
>abstract="Escolha o esquema da Experience Platform para os perfis."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_updatemode"
>title="Salvar modo de atualização do perfil"
>abstract="Os modos de atualização disponíveis para a atividade Salvar perfil incluem Atualização completa e Atualização incremental."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_updatemode_full"
>title="Atualização completa"
>abstract="O modo de atualização completa atualiza o conjunto completo de perfis para enriquecimento."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_updatemode_incremental"
>title="Atualização incremental"
>abstract="O modo de atualização incremental atualiza os perfis que foram modificados desde a última execução do enriquecimento."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_primaryidentityfield"
>title="Campo de identidade principal"
>abstract="O campo de identidade principal indica a fonte da verdade ao mesclar perfis para o enriquecimento."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_requiredfieldscheck"
>title="Critérios de campos obrigatórios"
>abstract="Um campo obrigatório é um atributo que deve ser preenchido para cada perfil ou registro ao exportar dados. Se um campo obrigatório estiver ausente, a exportação não será concluída ou válida."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_primaryidentitycheck"
>title="Critérios do campo de identidade principal"
>abstract="O identificador exclusivo de cada perfil ou registro. Isso garante que cada registro possa ser distintamente reconhecido e correspondido, evitando a duplicação de dados."

A atividade **[!UICONTROL Salvar Perfis]** permite enriquecer perfis do Adobe Experience Platform com dados federados de depósitos externos.

Normalmente, essa atividade é usada para aprimorar os perfis do cliente, trazendo atributos e insights adicionais sem mover fisicamente ou duplicar os dados na plataforma.

## Configurar a atividade [!UICONTROL Salvar Perfis] {#save-profile-configuration}

>[!IMPORTANT]
>
>A atividade **Salvar Perfis** requer um esquema e um conjunto de dados habilitados para perfil. Para saber como habilitar seu conjunto de dados para ser habilitado para perfil, leia o [guia do usuário do conjunto de dados](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#enable-profile){target="_blank"}.
>
>Além disso, se o conjunto de dados selecionado **não** tiver a substituição habilitada, os dados dos perfis serão **substituídos**. Para saber como habilitar a substituição para seus conjuntos de dados, leia o [guia de habilitação de substituição](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/enable-upsert).

Siga estas etapas para configurar a atividade **[!UICONTROL Salvar Perfis]**:

1. Adicione uma atividade **[!UICONTROL Salvar Perfis]** à sua composição.

   ![O botão Salvar Perfis está realçado dentro das atividades.](../assets/save-profiles/save-profiles.png){width="1500" zoomable="yes"}

1. Especifique o rótulo dos perfis que serão criados.

   >[!IMPORTANT]
   >
   >O rótulo do público-alvo deve ser exclusivo na sandbox atual. Ele não pode ser o mesmo rótulo de nenhum público existente.

1. Selecione o esquema do Adobe Experience Platform que deseja usar.

   ![Os esquemas disponíveis são exibidos.](../assets/save-profiles/select-schema.png){width="1500" zoomable="yes"}

1. Selecione o conjunto de dados no qual deseja salvar o enriquecimento.

   ![A lista suspensa de conjunto de dados está realçada.](../assets/save-profiles/select-dataset.png){width="300" zoomable="yes"}

1. Após selecionar o conjunto de dados, você pode ver o campo de identidade principal que será usado para identificar perfis no banco de dados.

1. Selecione **[!UICONTROL Adicionar campos]** para adicionar os campos de identidade principal e obrigatório.

   ![O botão Adicionar Campos está realçado.](../assets/save-profiles/add-fields.png){width="300" zoomable="yes"}

   Você pode especificar o campo **Source** (dados externos) e o campo **Destination** (campo de esquema) para cada atributo que deseja mapear.

   ![Os campos Source e Destino são realçados, mostrando onde criar o mapeamento entre os campos](../assets/save-profiles/specify-mapping.png){width="300" zoomable="yes"}

1. Você também pode especificar o modo de atualização para o enriquecimento.

   ![Os tipos de modo de atualização são exibidos.](../assets/save-profiles/select-update-mode.png){width="300" zoomable="yes"}

   | Modo de atualização | Descrição |
   | ----------- | ----------- |
   | Atualizações completas | O conjunto completo de perfis é atualizado para enriquecimento. |
   | Atualizações incrementais | Somente os perfis modificados desde a última execução do enriquecimento são atualizados para o enriquecimento. |

   Se você selecionar [!UICONTROL Atualizações incrementais], também precisará escolher a data da última modificação para determinar quais dados serão enviados.

1. Após a configuração, selecione **Iniciar**.
