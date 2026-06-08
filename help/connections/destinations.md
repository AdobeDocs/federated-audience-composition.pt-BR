---
audience: end-user
title: Enriqueça os públicos-alvo da Adobe Experience Platform com dados externos
description: Saiba como refinar e enriquecer públicos-alvo do Adobe Experience Platform com dados de seus bancos de dados federados usando o destino de composição do público-alvo Federado.
exl-id: 03c2f813-21c9-4570-a3ff-3011f164a55e
TQID: https://experienceleague.adobe.com/g32ycFuhXFq68NmBJjunWZT3m4JpmL108bhMSs-4EYc
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: ce79e1b9216ca69020155978ac84f29577c5ff8d
workflow-type: tm+mt
source-wordcount: 774
ht-degree: 5%

---

# Enriqueça os públicos-alvo da Adobe Experience Platform com dados externos {#connect-aep-fac}

>[!CONTEXTUALHELP]
>id="dc_new_destination"
>title="Criar um destino"
>abstract="Defina as configurações para se conectar ao novo banco de dados federado. Use o botão **[!UICONTROL Conectar ao destino]** para validar a configuração."

O Adobe Experience Platform permite a integração perfeita de públicos do Portal de público-alvo com seus bancos de dados externos usando o **destino do Adobe Federated Audience Composition**. Com essa integração, você pode aproveitar os públicos existentes em composições e enriquecê-los ou refiná-los usando dados de seus bancos de dados externos para criar novos públicos.

Para fazer isso, é necessário configurar uma nova conexão no Adobe Experience Platform para o destino do Adobe Federated Audience Composition. Você pode usar um scheduler para enviar um determinado público-alvo em frequências regulares, selecionar atributos específicos a serem incluídos, como IDs para reconciliação de dados. Se você tiver aplicado políticas de governança e privacidade ao público-alvo, elas serão mantidas e enviadas de volta ao portal de público-alvo depois que o público-alvo for atualizado.

Por exemplo, digamos que você esteja armazenando informações de compra em seu data warehouse e tenha um público do Adobe Experience Platform direcionado a clientes interessados em um produto específico nos últimos dois meses. Ao usar o destino da Composição de público-alvo federado, você pode:

* Refine o público com base nas informações de compra. Por exemplo, você pode filtrar o público-alvo para clientes do público-alvo que fizeram uma compra de apenas mais de US$ 150.
* Enriqueça o público-alvo com campos relacionados às compras, como o nome do produto e a quantidade comprada.

## Ativar público para destino {#activate}

No catálogo de Destinos do Adobe Experience Platform, selecione o destino da Composição de público federado. No painel direito, selecione **[!UICONTROL Configurar novo destino]**.

![O botão Configurar novo destino está realçado no catálogo de destinos.](assets/destinations/new.png)

A página **[!UICONTROL Configurar novo destino]** é exibida. Nesta página, você pode configurar detalhes do seu destino, incluindo o nome, a descrição, o tipo de conexão e o banco de dados federado.

![A página Configurar novo destino é exibida, mostrando quais detalhes precisam ser adicionados para criar o destino.](assets/destinations/configure.png)

Na seção **[!UICONTROL Alertas]**, você pode habilitar alertas para receber notificações sobre o status do fluxo de dados para o seu destino. Isso inclui alertas de atrasos de execução de fluxo de dados, falhas de execução, sucessos de execução, inicializações de execução e ignoramentos de ativação.

Para obter mais informações sobre alertas, leia a documentação do Adobe Experience Platform sobre [assinatura em alertas de destinos usando a interface](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/alerts){target="_blank"}.

![Os alertas disponíveis para o destino são exibidos.](assets/destinations/alerts.png)

Após concluir a configuração dos detalhes do seu destino, selecione **[!UICONTROL Avançar]**. A etapa **[!UICONTROL Política de governança e ações de aplicação]** é exibida. Nesta página, você pode definir suas políticas de governança de dados e garantir que os dados usados estejam em conformidade quando os públicos-alvo forem enviados e estiverem ativos.

Quando terminar de selecionar as ações de marketing desejadas para o destino, selecione **[!UICONTROL Criar]**.

A nova conexão com o destino é criada. Agora você pode ativar os públicos-alvo para enviá-los ao destino. Escolha o destino para o qual deseja ativar os públicos-alvo, seguido por **[!UICONTROL Próximo]**.

![O botão de ativação está realçado.](assets/destinations/activate.png)

A etapa **[!UICONTROL Agendando]** é exibida. Você pode selecionar os públicos-alvo desejados que deseja ativar para o destino. Para configurar um agendamento, selecione ![ícone de lápis](assets/do-not-localize/Smock_Edit_18_N.svg) para editar seu agendamento de exportação.

![A página Ativar destino é exibida.](assets/destinations/schedule.png)

O popover **[!UICONTROL Agendando]** é exibido. Nesse popover, você pode definir as opções de exportação de arquivo, a frequência e configurar o cronograma.

![O popover de agendamento é exibido.](assets/destinations/schedule-2.png)

>[!NOTE]
>
>Para ativar os públicos-alvo mais rapidamente, selecione a opção **[!UICONTROL Após a avaliação do segmento]** para acionar o trabalho de ativação imediatamente após a conclusão diária do trabalho de segmentação em lote do Platform.
>
>Para obter informações detalhadas sobre como configurar um agendamento e nomes de arquivo, leia as seguintes seções da documentação do Adobe Experience Platform:
>
>* [Agendar exportação de público-alvo](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#scheduling){target="_blank"}
>* [Configurar nomes de arquivo](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#configure-file-names){target="_blank"}

Na etapa **[!UICONTROL Mapping]**, selecione quais campos de atributo e identidade serão exportados para seu(s) público(s).

>[!IMPORTANT]
>
>Você **não pode** usar colunas geradas pelo sistema ao ativar para destinos. Selecionar uma coluna gerada pelo sistema causará um erro.

Para obter mais informações, leia a [seção de mapeamento](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#mapping){target="_blank"} na documentação do Adobe Experience Platform.

![A página de atributos de mapeamento é exibida.](assets/destinations/attributes.png)

Revise a configuração de destino e as configurações de público e selecione **[!UICONTROL Concluir]**.

![A página de destino da revisão é exibida.](assets/destinations/review.png)

Os públicos-alvo selecionados agora estão ativados para a nova conexão. Você pode adicionar mais públicos-alvo para enviar com esta conexão navegando de volta para a página **[!UICONTROL Ativar públicos-alvo]**. Não é possível remover públicos-alvo depois de ativados.
