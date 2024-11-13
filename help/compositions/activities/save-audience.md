---
audience: end-user
title: Usar a atividade Save audience
description: Saiba como usar a atividade Salvar público
exl-id: fa67b1ee-8de6-4a71-b597-ade3f5587a38
source-git-commit: 65052ffcd8c70817aa428bea7f8b6baa0a49a1b0
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 31%

---

# Salvar público-alvo {#save-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience"
>title="Salvar um público-alvo"
>abstract="Use esta atividade para criar um novo público-alvo a partir da população calculada upstream na composição. Os públicos-alvo criados são adicionados à lista de públicos-alvo e disponibilizados no menu **Públicos-alvo**."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_outbound"
>title="Gerar transição de saída"
>abstract="Use essa opção se quiser adicionar uma transição após a atividade **Salvar público-alvo**."

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience_primary_identity"
>title="Campo de identidade principal"
>abstract="Selecione a identidade principal a ser usada para perfis."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-platform/xdm/ui/fields/identity#define-a-identity-field" text="Saiba mais na documentação da Experience Platform"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_namespace"
>title="Namespace de identidade"
>abstract="Selecione o namespace a ser usado para perfis."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-platform/identity/features/namespaces" text="Saiba mais na documentação da Experience Platform"

A atividade **Salvar público-alvo** permite criar um novo público-alvo a partir da população computada upstream em uma composição. Os públicos-alvo criados são adicionados à lista de públicos-alvo da Adobe Experience Platform e disponibilizados pelo menu **Públicos-alvo**. [Saiba como trabalhar com públicos-alvo](../../start/audiences.md)

Essa atividade é usada essencialmente para manter os grupos de populações computados na mesma composição, convertendo-os em públicos-alvo reutilizáveis. Conecte-a a outras atividades de direcionamento, como uma atividade **Criar público** ou **Combinar**.

>[!IMPORTANT]
>
>A atividade **Salvar público-alvo** requer um esquema e um conjunto de dados habilitados para perfil. [Saiba mais](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#enable-profile){target="_blank"}.

## Configurar a atividade Save audience {#save-audience-configuration}

Siga estas etapas para configurar a atividade **Salvar público-alvo**:

1. Adicione uma atividade **Salvar público-alvo** à sua composição.

   ![](../assets/save-audience.png)

1. Especifique o rótulo do público-alvo a ser criado.

   >[!IMPORTANT]
   >
   >O rótulo do público-alvo deve ser exclusivo na sandbox atual. Ele não pode ser o mesmo rótulo de nenhum público existente.

1. Use a seção Mapeamentos de público-alvo para selecionar os campos que deseja trazer com o público-alvo recém-criado. Para fazer isso, clique em **Adicionar mapeamento de público-alvo** e escolha os campos de público-alvo de origem e de destino.

   Repita a operação para adicionar quantos mapeamentos de público-alvo forem necessários.

1. Selecione a identidade e o namespace principais a serem usados para identificar os perfis direcionados no banco de dados:

   * **Campo de identidade principal**: selecione o campo a ser usado para identificar os perfis. Por exemplo, seu endereço de email ou número de telefone.
   * **Namespace de identidade**: selecione o namespace a ser usado para identificar os perfis, ou seja, o tipo de dados a ser usado como chave de identificação. Por exemplo, se o endereço de email tiver sido selecionado como campo de identidade principal, o namespace de identidade **Email** deverá ser selecionado. Se o identificador exclusivo for o número de telefone, o namespace de identidade **Telefone** deverá ser selecionado.

## Acessar seu público-alvo na Adobe Experience Platform {#access-audience}

Depois de executar a composição, o público-alvo resultante é salvo como externo na Adobe Experience Platform e disponibilizado na Adobe Real-time Customer Data Platform e/ou no Adobe Journey Optimizer. Ele é disponibilizado no menu **Públicos-alvo**. [Saiba mais](https://experienceleague.adobe.com/pt-br/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}

O público-alvo criado inclui todos os campos selecionados na seção Mapeamentos de público-alvo. Você pode direcionar esse público-alvo no Journey Optimizer ou ativá-lo para qualquer destino compatível com o Adobe Experience Platform.

[Saiba mais na documentação do Adobe Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}

<!--

## Example{#save-audience-example}

The following example illustrates a simple audience update from targeting. A scheduler is added to run the workflow once a month. A query recovers all the profiles subscribed to the different application services available. The **Save audience** activity updates the audience by deleting profiles that have unsubscribed from the service since the last workflow execution and by adding the newly subscribed profiles.
-->
