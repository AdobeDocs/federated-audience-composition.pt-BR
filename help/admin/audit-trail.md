---
audience: end-user
title: Introdução à Trilha de auditoria
description: Saiba como monitorar seus bancos de dados com a trilha de auditoria
badge: label="Disponibilidade limitada" type="Informative"
source-git-commit: bdef7049ee78c512857adcf7d587066eaf80046e
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 12%

---

# Introdução à Trilha de auditoria {#audit-trail}

>[!CONTEXTUALHELP]
>id="dc_audit_trail"
>title="Trilha de auditoria"
>abstract="O recurso Trilha de auditoria fornece um registro detalhado e cronológico de todas as ações e eventos que ocorreram no ambiente em tempo real."

O recurso de trilha de auditoria fornece um registro detalhado e cronológico de todas as ações e eventos que foram realizados em seu ambiente em tempo real

O recurso **[!UICONTROL Trilha de auditoria]** registra constantemente um log detalhado de ações e eventos que ocorrem na instância da Composição de dados Adobe em tempo real. Ele oferece um método conveniente para acessar um registro cronológico de dados, abordando queries como: o status dos workflows, os indivíduos mais recentes para modificá-los ou as atividades executadas pelos usuários na instância.

+++ Saiba mais sobre entidades disponíveis da Trilha de auditoria

* **A trilha de auditoria do esquema do Source** permite monitorar atividades e modificações recentes feitas em seus esquemas na instância de composição de dados Adobe.

  Para obter informações detalhadas sobre esquemas, consulte esta [página](../customer/schemas.md).

* A **trilha de auditoria do fluxo de trabalho** permite acompanhar atividades e alterações recentes feitas nos fluxos de trabalho, incluindo seus estados atuais, como:

   * Start
   * Pause
   * Stop
   * Restart
   * Limpeza que é igual ao histórico de Expurgação da ação
   * Simular qual é igual ao Início da ação no modo de simulação
   * Ativar que é igual à ação Executar tarefas pendentes agora
   * Unconditional Stop

  Para obter mais informações sobre fluxos de trabalho, consulte esta [página](../compositions/gs-compositions.md).

* **Conta Externa** permite verificar as modificações feitas em contas externas na instância da Composição de Dados do Adobe.

  Para obter mais informações sobre a conta externa, consulte esta [página](../connections/federated-db.md).

+++

## Acessando a Trilha de auditoria {#accessing-audit-trail}

Para acessar a **[!UICONTROL Trilha de auditoria]** da sua instância:

1. No menu **[!UICONTROL Dados federados]**, selecione **[!UICONTROL Trilha de auditoria]**.

1. A janela **[!UICONTROL Trilha de auditoria]** é aberta com a lista de suas entidades. A Interface do usuário da Web do Adobe Campaign audita a criação, edição e exclusão de ações para workflows, opções, deliveries e esquemas.

   ![](assets/audit_trail.png)

1. A janela **[!UICONTROL Entidade de auditoria]** fornece informações mais detalhadas sobre a entidade escolhida, como:

   * **[!UICONTROL Tipo]**: Fluxo de Trabalho, Opções, Entregas ou Esquemas.
   * **[!UICONTROL Entidade]** : nome interno de suas atividades.
   * **[!UICONTROL Modificado por]**: nome de usuário da última pessoa que modificou esta entidade pela última vez.
   * **[!UICONTROL Ação]**: última ação executada nesta entidade, Criada, Modificada ou Excluída.
   * **[!UICONTROL Data de modificação]**: data da última ação executada nesta entidade.
