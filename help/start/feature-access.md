---
title: Acessar a composição de público-alvo federado
description: Saiba mais sobre as permissões necessárias para a composição de público-alvo federado
exl-id: 84138456-218b-4beb-ae7b-146213b03cc2
source-git-commit: 62bbed4818caf06539234f97d4c0d1cf9c9a52d1
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 46%

---

# Acessar a composição de público-alvo federado {#feature-access}

## Gerenciar o acesso a sandboxes {#access-sandboxes}

Ao adquirir a composição de público-alvo federado da Adobe Experience Platform, um perfil do produto é criado para cada sandbox ativa no momento. Esse perfil de produto é criado no Admin Console sob o cartão de produto **Adobe Experience Platform** e segue a seguinte convenção de nomeação: `ACP_FAC - <<SandboxName>> - admin.` Para acessar a Composição de público-alvo federado de uma sandbox específica, os usuários devem ser adicionados ao perfil de produto criado para essa sandbox.

Por exemplo, se uma nova sandbox chamada “fac-test” for ativada, um perfil de produto correspondente “ACP_FAC - fac-test - admin” será criado. Para acessar a Composição de público-alvo federado com esta sandbox, os usuários precisam ser adicionados a este perfil de produto.

## Gerenciar o acesso à composição de público-alvo federado

Para acessar a **Composição de Público-Alvo Federado**, primeiro certifique-se de atribuir as permissões necessárias para acessar diferentes aspectos da Composição de Público-Alvo Federado. Essas funções devem ser atribuídas aos usuários que precisam de acesso à **Federated Audience Composition**.

Observe que somente administradores têm a capacidade de atribuir permissões.

1. Navegue até o menu **[!UICONTROL Permissões]**.

1. No menu **[!UICONTROL Funções]**, selecione a **[!UICONTROL Função]** que deseja atualizar.

   ![](assets/access_fda_1.png)

1. Selecione **[!UICONTROL Editar]** para modificar as permissões de sua função.

   ![](assets/access_fda_2.png)

1. Adicione as permissões necessárias para o usuário. Você pode adicionar as seguintes permissões para acessar a Composição de público-alvo federado:

   | Permissão | Descrição |
   | ---------- | ----------- |
   | Gerenciar Dados Federados | Use essa permissão para gerenciar todos os aspectos da Composição de público-alvo federado. Essa permissão engloba Gerenciar Banco de Dados Federado, Gerenciar Esquema Federado, Gerenciar Modelo de Dados Federado e Gerenciar Composições Federadas. |
   | Gerenciar Banco de Dados Federado | Use esta permissão para adicionar, exibir, atualizar e excluir suas conexões com bancos de dados federados. |
   | Exibir Banco de Dados Federado | Use esta permissão para exibir suas conexões com bancos de dados federados. |
   | Gerenciar Esquema Federado | Use esta permissão para criar, exibir, atualizar, excluir e atualizar esquemas. |
   | Exibir Dados do Esquema Federado | Use essa permissão para exibir a guia de dados na seção schema. |
   | Exibir Esquema Federado | Use essa permissão para exibir as tabelas do esquema. |
   | Gerenciar Modelo de Dados Federados | Use esta permissão para criar, exibir, atualizar e excluir modelos de dados. |
   | Exibir Modelo de Dados Federados | Use essa permissão para exibir os modelos de dados. |
   | Exibir trilha de auditoria da federação | Use essa permissão para exibir a trilha de auditoria da Composição de público-alvo federado. |
   | Gerenciar composições federadas | Use esta permissão para criar, exibir, atualizar e excluir composições federadas. |
   | Exibir Composições Federadas | Use essa permissão para exibir composições federadas. |

   ![](assets/permissions.png)

1. Depois de fazer as alterações necessárias, selecione **[!UICONTROL Salvar]**.

Todos os usuários já atribuídos a essa função terão suas permissões automaticamente atualizadas e acesso à composição de público-alvo federado.

Para atribuir esta função a novos usuários:

1. Navegue até a guia **[!UICONTROL Usuários]** no painel Função e selecione **[!UICONTROL Adicionar usuários]**.

   ![](assets/access_fda_4.png)

1. Insira o nome ou endereço de email do usuário, ou selecione-o na lista disponível. Depois de concluído, selecione **[!UICONTROL Salvar]**.

<!-- Alternatively, you can assign one of the pre-existing roles to the users, depending on what permissions they need. For more information on assigning pre-existing roles to a user, please read the [guide on managing users for a product profile](https://experienceleague.adobe.com/pt-br/docs/experience-platform/access-control/ui/users).

| Role name | Permissions |
| --------- | ----------- |
| FAC Data Managers | <ul><li>Manage Federated Compositions</li><li>View Federated Databases</li><li>View Federated Schemas</li><li>View Federated Schema Data</li><li>View Federated Data Models</li></ul> |
| FAC Composition Managers | <ul><li>Manage Federated Compositions</li></ul> |
| FAC Administrators | <ul><li>Manage Federated Data</li></ul> | -->

O usuário receberá um email com instruções para acessar a sua instância. Se o usuário não tiver sido criado anteriormente, consulte [esta documentação](https://experienceleague.adobe.com/pt-br/docs/experience-platform/access-control/abac/permissions-ui/users).
