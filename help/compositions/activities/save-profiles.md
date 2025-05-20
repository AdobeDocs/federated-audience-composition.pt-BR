---
audience: end-user
title: Usar a atividade Salvar perfis
description: Saiba como usar a atividade Salvar perfis
exl-id: 1c840838-32d5-4ceb-8430-835a235b7436
source-git-commit: fae57356b8e9f5358a39d31cad4883171a310fb6
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 29%

---

# Salvar perfis {#save-profile}

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile"
>title="Salvar perfis"
>abstract="A atividade Salvar perfis permite enriquecer perfis da Experience Platform federando dados de depósitos externos, permitindo aprimorar os perfis do cliente com atributos adicionais. "

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_aepschemalist"
>title="Selecionar esquema da AEP"
>abstract="Escolha o esquema da Experience Platform para os perfis."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_primaryidentitynamespace"
>title="Selecione o campo de identificação principal"
>abstract="Selecione a Identidade principal a ser usada para identificar os perfis direcionados no banco de dados."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_selectaepschema"
>title="Selecionar esquema da AEP"
>abstract="Escolha o esquema da Experience Platform para os perfis."

A atividade **Salvar perfis** permite enriquecer perfis do Adobe Experience Platform com dados federados de depósitos externos.

Normalmente, essa atividade é usada para aprimorar os perfis do cliente, trazendo atributos e insights adicionais sem mover fisicamente ou duplicar os dados na plataforma

## Configurar a atividade Salvar perfis {#save-profile-configuration}

Siga estas etapas para configurar a atividade **Salvar perfis**:

1. Adicione uma atividade **Salvar perfis** à sua composição.

   ![](../assets/save-profile.png)

1. Especifique o rótulo dos perfis que serão criados.

   >[!IMPORTANT]
   >
   >O rótulo do público-alvo deve ser exclusivo na sandbox atual. Ele não pode ser o mesmo rótulo de nenhum público existente.

1. Selecione o esquema do Adobe Experience Platform que deseja usar.

   ![](../assets/save-profile-2.png)

1. Escolha o campo de identidade principal que será usado para identificar perfis no banco de dados.

1. Para reconciliar atributos de dados adicionais, clique em **Adicionar atributos**.

   Em seguida, especifique o campo **Source** (dados externos) e o campo **Destination** (campo de esquema) para cada atributo que deseja mapear.

   ![](../assets/save-profile-3.png)

1. Depois de configurado, clique em **Iniciar**.
