---
title: Acessar composição de público-alvo federado
description: Saiba mais sobre as permissões necessárias para a Composição de público federado
exl-id: 84138456-218b-4beb-ae7b-146213b03cc2
hide: true
hidefromtoc: true
source-git-commit: e9cc50cbcbd076f784c924bd941e4396c14190ce
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 36%

---

# Acessar composição de público-alvo federado {#feature-access}

## Gerenciar acesso a sandboxes {#access-sandboxes}

Ao comprar o complemento Composição de público-alvo federado, um perfil de produto é criado para cada sandbox ativa nesse momento. Esse perfil de produto é criado no Admin Console sob o cartão de produto **Adobe Experience Platform** e segue a seguinte convenção de nomeação: `ACP_FAC - <<SandboxName>> - admin.` Para acessar a Composição de público-alvo federado de uma sandbox específica, os usuários devem ser adicionados ao perfil de produto criado para essa sandbox.

Por exemplo, se uma nova sandbox chamada “fac-test” for ativada, um perfil de produto correspondente “ACP_FAC - fac-test - admin” será criado. Para acessar a Composição de público-alvo federado com esta sandbox, os usuários precisam ser adicionados a este perfil de produto.

## Gerenciar acesso à Composição de Público-Alvo Federado

>[!AVAILABILITY]
>
>As permissões do estão disponíveis como parte da versão de março.

Para acessar a **Federated Audience Composition**, primeiro verifique se a permissão **Gerenciar Dados Federados** está atribuída às funções apropriadas. Essas funções devem ser atribuídas aos usuários que precisam de acesso à **Federated Audience Composition**.

Observe que somente os administradores têm a capacidade de atribuir permissões.

1. Navegue até o menu **[!UICONTROL Permissões]**.

1. No menu **[!UICONTROL Funções]**, selecione a **[!UICONTROL Função]** que deseja atualizar.

   ![](assets/access_fda_1.png)

1. Clique em **[!UICONTROL Editar]** para modificar as permissões de sua função.

   ![](assets/access_fda_2.png)

1. Adicione o recurso **Dados Federados** e selecione **[!UICONTROL Gerenciar Dados Federados]** no menu suspenso.

   ![](assets/access_fda_3.png)

1. Depois de fazer as alterações necessárias, clique em **[!UICONTROL Salvar]**.

Todos os usuários já atribuídos a essa função terão suas permissões automaticamente atualizadas e acesso à Federated Audience Composition.

Para atribuir esta função a novos usuários:

1. Navegue até a guia **[!UICONTROL Usuários]** no painel Função e clique em **[!UICONTROL Adicionar usuários]**.

   ![](assets/access_fda_4.png)

1. Insira o nome do usuário ou endereço de email, ou selecione na lista disponível. Depois de concluído, clique em **[!UICONTROL Salvar]**.

O usuário receberá um email com instruções para acessar sua instância. Se o usuário não tiver sido criado anteriormente, consulte [esta documentação](https://experienceleague.adobe.com/pt-br/docs/experience-platform/access-control/abac/permissions-ui/users).
