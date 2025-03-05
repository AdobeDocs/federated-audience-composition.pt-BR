---
audience: end-user
title: Enriqueça os públicos-alvo da Adobe Experience Platform com dados externos
description: Saiba como refinar e enriquecer públicos-alvo do Adobe Experience Platform com dados de seus bancos de dados federados usando o destino de composição do público-alvo Federado.
exl-id: 03c2f813-21c9-4570-a3ff-3011f164a55e
source-git-commit: 302bdfa32249e5efa420256ab4f3abda31bbdd50
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 9%

---

# Enriqueça os públicos-alvo da Adobe Experience Platform com dados externos {#connect-aep-fac}

>[!CONTEXTUALHELP]
>id="dc_new_destination"
>title="Criar um destino"
>abstract="Defina as configurações para se conectar ao novo banco de dados federado. Use o botão **[!UICONTROL Conectar ao destino]** para validar a configuração."

O Adobe Experience Platform permite a integração perfeita de públicos do Portal de público-alvo com seus bancos de dados externos usando o **destino do Adobe Federated Audience Composition**. Com essa integração, você pode aproveitar os públicos existentes em composições e enriquecê-los ou refiná-los usando dados de seus bancos de dados externos para criar novos públicos.

Para fazer isso, é necessário configurar uma nova conexão no Adobe Experience Platform para o destino do Adobe Federated Audience Composition. Você pode usar um scheduler para enviar um determinado público-alvo em frequências regulares, selecionar atributos específicos a serem incluídos, como IDs para reconciliação de dados. Se você tiver aplicado políticas de governança e privacidade ao público-alvo, elas serão mantidas e enviadas de volta ao portal de público-alvo depois que o público-alvo for atualizado.

Por exemplo, digamos que você esteja armazenando informações de compra em seu data warehouse e tenha um público do Adobe Experience Platform direcionado a clientes interessados em um produto específico nos últimos dois meses. Ao usar o destino da Composição de público-alvo federado, você pode:

* Refine o público com base nas informações de compra. Por exemplo, você pode filtrar o público-alvo para clientes do público-alvo que fizeram uma compra somente de mais de 150$.
* Enriqueça o público-alvo com campos relacionados às compras, como o nome do produto e a quantidade comprada.

As principais etapas para enviar públicos-alvo da Adobe Experience Platform para a Composição de público-alvo federado da Adobe são as seguintes:

1. Acesse o catálogo Destinos do Adobe Experience Platform e selecione o destino da Composição do Audience Federado.

   No painel direito, selecione **[!UICONTROL Configurar novo destino]**.

   ![](assets/destination-new.png)

1. Insira um nome para a nova conexão e selecione o **[!UICONTROL Tipo de Conexão]** entre as seguintes conexões disponíveis:

   * Amazon Redshift
   * Azure Synapse Analytics
   * Google Big Query
   * Snowflake
   * Vertica Analytics
   * Databricks
   * Microsoft Fabric

1. Selecione o **[!UICONTROL Banco de dados federado]** ao qual você deseja se conectar e clique em **[!UICONTROL Avançar]**.

   ![](assets/destination-configure.png)

1. Na seção **[!UICONTROL Alertas]**, você pode habilitar alertas para receber notificações sobre o status do fluxo de dados para o seu destino.

   Para obter mais informações sobre alertas, consulte a documentação do Adobe Experience Platform sobre [assinatura em alertas de destinos usando a interface](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/alerts){target="_blank"}

1. Na etapa **[!UICONTROL Política de governança e ações de aplicação]**, você pode definir suas políticas de governança de dados e garantir que os dados usados estejam em conformidade quando os públicos-alvo forem enviados e estiverem ativos.

   Quando você terminar de selecionar as ações de marketing desejadas para o destino, clique em **[!UICONTROL Criar]**.

1. A nova conexão com o destino é criada. Agora você pode ativar os públicos-alvo para enviá-los ao destino. Para fazer isso, selecione-o na lista e clique em **[!UICONTROL Avançar]**

   ![](assets/destination-activate.png)

1. Selecione os públicos desejados que você deseja enviar e clique em **[!UICONTROL Avançar]**.

1. Configure o nome do arquivo e um agendamento de exportação para o(s) público(s) selecionado(s).

   ![](assets/destination-schedule.png)

   >[!NOTE]
   >
   >Informações detalhadas sobre como configurar um agendamento e nomes de arquivo estão disponíveis nas seguintes seções da documentação do Adobe Experience Platform:
   >
   >* [Agendar exportação de público-alvo](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#scheduling){target="_blank"}
   >* [Configurar nomes de arquivo](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#configure-file-names){target="_blank"}

1. Na etapa **[!UICONTROL Mapping]**, selecione quais campos de atributo e identidade serão exportados para seu(s) público(s). Para obter mais informações, exiba a [etapa de mapeamento](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#mapping){target="_blank"} na documentação do Adobe Experience Platform.

   ![](assets/destination-attributes.png)

1. Revise a configuração de destino e as configurações de público e clique em **[!UICONTROL Concluir]**.

   ![](assets/destination-review.png)

Os públicos-alvo selecionados agora estão ativados para a nova conexão. Você pode adicionar mais públicos-alvo para enviar com esta conexão navegando de volta para a página **[!UICONTROL Ativar públicos-alvo]**. Não é possível remover públicos-alvo depois de ativados.
