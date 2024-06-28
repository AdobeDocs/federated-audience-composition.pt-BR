---
audience: end-user
title: Usar a atividade Save audience
description: Saiba como usar a atividade Bifurcação
source-git-commit: 05a023a7f7aab719f3771030a7ac8bba57e5bee3
workflow-type: tm+mt
source-wordcount: '405'
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

1. No **Modo** selecione a ação que deseja executar:

   * **Criar ou atualizar um público existente**: definir um **Rótulo de público**. Se o público-alvo já existir, ele será atualizado, caso contrário, um novo público-alvo será criado.

   * **Atualizar um público existente**: escolha a variável **Público** você deseja atualizar na lista de públicos-alvo existentes.

1. Selecione o **Modo de atualização** que se aplicarão aos públicos-alvo existentes:

   * **Substituir o conteúdo do público-alvo por novos dados**: todo o conteúdo do público-alvo é substituído. Os dados antigos são perdidos. Somente os dados da transição de entrada da atividade Save audience são mantidos. Essa opção apaga o tipo de público-alvo e o targeting dimension do público-alvo atualizado.

   * **Público-alvo completo com novos dados**: o conteúdo antigo do público-alvo é mantido e os dados da transição de entrada da atividade Save audience são adicionados a ele.

1. Verifique a **Gerar uma transição de saída** se desejar adicionar uma transição após a variável **Salvar público-alvo** atividade.

O conteúdo do público-alvo salvo ficará disponível na visualização detalhada do público-alvo, que pode ser acessada no **Públicos-alvo** menu. As colunas disponíveis nessa visualização correspondem às da transição de entrada do **Salvar público-alvo** atividade.

<!--

## Example{#save-audience-example}

The following example illustrates a simple audience update from targeting. A scheduler is added to run the workflow once a month. A query recovers all the profiles subscribed to the different application services available. The **Save audience** activity updates the audience by deleting profiles that have unsubscribed from the service since the last workflow execution and by adding the newly subscribed profiles.
-->
