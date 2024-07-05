---
audience: end-user
title: Usar a atividade Save audience
description: Saiba como usar a atividade Salvar público
source-git-commit: 6b7a0ae164bdb09b1f5fc067a13e304eec9c5201
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 12%

---


# Salvar público-alvo {#save-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience"
>title="Salvar um público-alvo"
>abstract="Use esta atividade para atualizar um público-alvo ou criar um novo público-alvo a partir da população computada upstream na composição. Os públicos-alvo criados são adicionados à lista de públicos-alvo e disponibilizados no menu **Públicos-alvo**."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_outbound"
>title="Gerar transição de saída"
>abstract="Use essa opção se quiser adicionar uma transição após a atividade **Salvar público-alvo**."

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience_primary_identity"
>title="Campo de identidade principal"
>abstract="Selecione a identidade principal a ser usada para perfis."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/fields/identity#define-a-identity-field" text="Saiba mais na documentação do Experience Platform"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_namespace"
>title="Namespace de identidade"
>abstract="Selecione o namespace a ser usado para perfis."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-platform/identity/features/namespaces" text="Saiba mais na documentação do Experience Platform"

A variável **Salvar público-alvo** A atividade permite atualizar um público-alvo ou criar um novo público-alvo a partir da população computada upstream em uma composição. Os públicos-alvo criados são adicionados à lista de públicos-alvo do aplicativo e disponibilizados por meio do **Públicos-alvo** menu.

Essa atividade é usada essencialmente para manter os grupos de populações computados na mesma composição, convertendo-os em públicos-alvo reutilizáveis. Conecte-a a outras atividades de direcionamento, como uma **Criar público-alvo** ou um **Combinar** atividade.

## Configurar a atividade Save audience {#save-audience-configuration}

Siga estas etapas para configurar o **Salvar público-alvo** atividade:

1. Adicionar um **Salvar público-alvo** atividade para sua composição.

   ![](../assets/save-audience.png)

1. Especifique o rótulo do público-alvo a ser criado.

1. Clique em **Adicionar mapeamento de público-alvo** em seguida, escolha os campos de público-alvo de origem e destino:

   * **Campo de público-alvo do Source**:
   * **Campo de público-alvo**:

   Repita a operação para adicionar quantos mapeamentos de público-alvo forem necessários.

1. Selecione a identidade e o namespace principais a serem usados para identificar os perfis direcionados no banco de dados:

   * **Campo de identidade principal**: selecione o campo que será usado para identificar os perfis. Por exemplo, seu endereço de email ou número de telefone.
   * **Namespace de identidade**: selecione o namespace que será usado para identificar os perfis, ou seja, o tipo de dados a ser usado como chave de identificação. Por exemplo, se o endereço de email tiver sido selecionado como o campo de identidade principal, o namespace de identidade **E-mail** deve ser selecionado. Se o identificador exclusivo for o número de telefone, o namespace de identidade **Telefone** deve ser selecionado.

Depois de executar a composição, o público-alvo resultante é salvo no Adobe Experience Platform <!-- to check-->e acessíveis no **Públicos-alvo** menu.

<!--

## Example{#save-audience-example}

The following example illustrates a simple audience update from targeting. A scheduler is added to run the workflow once a month. A query recovers all the profiles subscribed to the different application services available. The **Save audience** activity updates the audience by deleting profiles that have unsubscribed from the service since the last workflow execution and by adding the newly subscribed profiles.
-->
