---
audience: end-user
title: Visão geral das atividades
description: Saiba mais sobre as diferentes atividades e transições disponíveis para uso na Composição de público-alvo federado.
source-git-commit: 93f4a16d00c71059672c4c6a51ff36debb6c9cee
workflow-type: tm+mt
source-wordcount: '4619'
ht-degree: 33%

---

# Visão geral das atividades

Na Composição de público-alvo federado, você pode adicionar atividades e transições que ajudam a definir seu público-alvo.

## Atividades {#activities}

As atividades permitem definir os componentes dentro do público-alvo.

Há **dois** tipos diferentes de atividades para usar na Federated Audience Composition: atividades de direcionamento e atividades de controle de fluxo.

### Atividades de direcionamento {#targeting}

As atividades de direcionamento permitem definir quais componentes do seu público-alvo para a composição.

#### Criar público-alvo

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience_audienceselector"
>title="Público-alvo"
>abstract="Selecione o público-alvo."

A atividade **Criar público-alvo** permite que você defina sua população alvo para a composição. Você pode selecionar um público-alvo já existente ou usar o modelador de consultas para definir a sua própria consulta.

+++ Detalhes de configuração

Depois de adicionar a atividade **Criar público-alvo** à tela de composição, nomeie o público-alvo. Agora você pode especificar se deseja criar um público ou usar um existente.

>[!BEGINTABS]

>[!TAB Criar novo público-alvo]

Depois de selecionar **Criar público-alvo**, escolha o **Esquema** para o público-alvo. O schema permite definir o público alvo da operação, como recipients, beneficiários de contrato, operadores ou assinantes. Por padrão, o schema é selecionado dos recipients.

![](./assets/activities/build-audience-create.png)

Depois de escolher um esquema, selecione **Continuar**. Agora, você pode definir a definição do seu público-alvo na Modeler de consulta. Para obter mais informações sobre como usar a Modeler de consulta, leia a [Visão geral da Modeler de consulta](../query/home.md).

>[!TAB Usar público existente]

Depois de selecionar **Ler público-alvo**, escolha **Continuar**.

![](./assets/activities/build-audience-read.png)

Agora você pode selecionar qual público-alvo deseja usar para a composição.

>[!ENDTABS]

Após selecionar suas opções, você pode optar por **Gerar uma transição de saída**. Selecionar essa opção permite adicionar uma transição de saída que será ativada no final da execução da atividade se a população do público-alvo estiver vazia.

+++

#### Alterar fonte de dados

A atividade **Alterar fonte de dados** permite alterar qual fonte de dados está sendo usada pela sua composição.

+++ Detalhes de configuração

Depois de adicionar a atividade **Alterar fonte de dados** à tela de composição, você pode definir a fonte de dados que será usada para a composição.

![A opção de fonte de dados está realçada no espaço de trabalho de Composição de Público Federado.](./assets/activities/configure.png){zoomable="yes"}{width="70%"}

| Fonte | Descrição |
| ------ | ----------- |
| Conta externa FDA | Um banco de dados de nuvem externo conectado à Federated Audience Composition. |

Depois de selecionar **[!UICONTROL FDA external account]**, você pode escolher com qual conta externa deseja se conectar.

![O popover que exibe as opções da conta externa é exibido.](./assets/activities/fda-external-account.png){zoomable="yes"}{width="70%"}

+++

#### Mudar dimensão

>[!CONTEXTUALHELP]
>id="dc_orchestration_dimension_complement"
>title="Gerar um complemento"
>abstract="É possível gerar uma transição de saída adicional com a população restante, que foi excluída como uma duplicata. Para fazer isso, ative a opção **[!UICONTROL Gerar complemento]**"

>[!CONTEXTUALHELP]
>id="dc_orchestration_change_dimension"
>title="Atividade Mudar dimensão"
>abstract="Esta atividade permite alterar o esquema, também conhecido como dimensão de direcionamento, à medida que você constrói um público-alvo. Ela desloca o eixo dependendo do modelo de dados e do esquema de entrada. Por exemplo, você pode mudar do esquema “contratos” para o esquema “clientes”."

A atividade **Change dimension** permite alterar o esquema (também conhecido como targeting dimension) da sua composição.

+++ Detalhes de configuração

Depois de adicionar a atividade **Alterar dimensão** à tela de composição, você pode definir um novo esquema para substituir o esquema anterior. Durante essa alteração de esquema, todos os registros serão mantidos.

![](./assets/activities/change-dimension.png)

Após executar a composição, os resultados serão atualizados.

+++

#### Combinar

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine"
>title="Atividade de combinar"
>abstract="A atividade **Combinar** permite executar a segmentação na população de entrada. Dessa forma, é possível combinar várias populações, excluir uma parte delas ou manter apenas dados comuns a vários públicos-alvo."

>[!CONTEXTUALHELP]
>id="dc_orchestration_intersection_merging_options"
>title="Opções de mesclagem de interseção"
>abstract="A **interseção** permite manter somente os elementos comuns às diferentes populações de entrada na atividade. Na seção **Conjuntos para unir**, marque todas as atividades anteriores que deseja unir."

>[!CONTEXTUALHELP]
>id="dc_orchestration_exclusion_merging_options"
>title="Opções de mesclagem de exclusão"
>abstract="A **Exclusão** permite excluir elementos de uma população de acordo com determinados critérios. Na seção **Conjuntos para unir**, marque todas as atividades anteriores que deseja unir."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_options"
>title="Selecione o tipo de segmentação"
>abstract="Selecione como combinar públicos: união, interseção ou exclusão."

>[!CONTEXTUALHELP]
>id="dc_orchestration_intersection_reconciliation_options"
>title="Opções de reconciliação de interseção"
>abstract="Selecione o tipo de reconciliação para definir como as duplicatas são tratadas."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_reconciliation"
>title="Opções de reconciliação"
>abstract="Selecione o **Tipo de reconciliação** para definir como lidar com duplicatas."

>[!CONTEXTUALHELP]
>id="dc_orchestration_exclusion_options"
>title="Regras de exclusão"
>abstract="Quando necessário, é possível manipular tabelas de entrada. De fato, para excluir um público-alvo de outro esquema, também conhecido como dimensão de direcionamento, esse público-alvo deve ser retornado ao mesmo esquema que o público-alvo principal. Para fazer isso, selecione **Adicionar uma regra** na seção E **regras de exclusão** e especifique as condições de alteração do esquema. A reconciliação de dados é realizada por meio de um atributo ou de uma união."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_sets"
>title="Selecionar conjuntos a serem combinados"
>abstract="Na seção **Conjuntos para unir**, selecione o **Conjunto principal** das transições de entrada. Esse é o conjunto a partir do qual os elementos são excluídos. Os outros conjuntos correspondem a elementos antes de serem excluídos do conjunto principal."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_exclusion"
>title="Regras de exclusão"
>abstract="Quando necessário, é possível manipular tabelas de entrada. De fato, para excluir um público-alvo de outro esquema, também conhecido como dimensão de direcionamento, esse público-alvo deve ser retornado ao mesmo esquema que o público-alvo principal. Para fazer isso, selecione **Adicionar uma regra** na seção **Regras de exclusão** e especifique as condições de alteração do esquema. A reconciliação de dados é realizada por meio de um atributo ou de uma união."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_complement"
>title="Combinar e gerar complemento"
>abstract="Ative a opção **Gerar complemento** para processar a população restante em uma transição adicional."

>[!NOTE]
>
>A atividade **Combinar** **deve** ser colocada após outra atividade e **não pode** ser colocada no início da composição.

A atividade **Combinar** permite que você agrupe vários públicos de várias maneiras: uma união, interseção ou exclusão.

- **União**: uma união combina os diferentes públicos em um único público. É equivalente a uma operação OR.
- **Interseção**: uma interseção combina os diferentes públicos em um único público com apenas o conteúdo **compartilhado** sendo preservado. É equivalente a uma operação AND.
- **Exclusão**: uma exclusão combina os diferentes públicos-alvo em um único público-alvo sem as regras de exclusão especificadas. É equivalente a uma operação XOR.

+++ Detalhes de configuração

Depois de adicionar várias atividades para formar pelo menos **duas** ramificações diferentes, adicione a atividade **Combinar** ao final de uma das ramificações. Agora você pode escolher uma das opções combinadas - União, Interseção ou Exclusão.

![](./assets/activities/combine.png)

>[!BEGINTABS]

>[!TAB União]

![](./assets/activities/combine-union.png)

Se você selecionar **União**, precisará escolher o **Tipo de reconciliação** para a atividade de combinação. O tipo de reconciliação permite definir como as entradas duplicadas são tratadas.

- **Somente chaves**: selecionar **Somente chaves** mantém o elemento **one** quando vários elementos têm a mesma chave. Você só poderá usar essa opção se as populações recebidas forem homogêneas.
- **Uma seleção de colunas**: selecionar **Uma seleção de colunas** permite definir uma lista de colunas em que a reconciliação de dados é aplicada. Você pode selecionar o conjunto principal de dados que contém os dados de origem, seguido pelas colunas a serem usadas para a associação.

>[!TAB Interseção]

![](./assets/activities/combine-intersection.png)

Se você selecionar **Interseção**, precisará escolher o **Tipo de reconciliação** para a atividade de combinação. O tipo de reconciliação permite definir como as entradas duplicadas são tratadas.

- **Somente chaves**: selecionar **Somente chaves** mantém o elemento **one** quando vários elementos têm a mesma chave. Você só poderá usar essa opção se as populações recebidas forem homogêneas.
- **Uma seleção de colunas**: selecionar **Uma seleção de colunas** permite definir uma lista de colunas em que a reconciliação de dados é aplicada.

Após configurar seu tipo de reconciliação, você também pode selecionar a opção **Gerar complemento**. A geração de um complemento processa a população restante e contém os dados **não** incluídos como parte da interseção. Uma transição de saída adicional será adicionada à atividade.

>[!TAB Exclusão]

![](./assets/activities/combine-exclusion.png)

Se você selecionar **Exclusão**, precisará selecionar o **Conjunto principal** das transições de entrada. Representa os conjuntos dos quais os elementos serão excluídos.

Depois de escolher o conjunto principal, você pode configurar as **Regras de exclusão**. Você pode selecionar **Corresponder por atributo** ou **Ingressar**.

Depois de configurar as regras de exclusão, você também pode selecionar a opção **Gerar complemento**. A geração de um complemento processa a população restante e contém os dados **não** incluídos como parte da exclusão. Uma transição de saída adicional será adicionada à atividade.

+++

#### Desduplicação

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_fields"
>title="Campos para identificar duplicatas"
>abstract="Na seção **[!UICONTROL Fields to identify duplicates]**, selecione o botão **[!UICONTROL Add attribute]** para especificar os campos para os quais os valores idênticos permitem a identificação das duplicatas, como: endereço de email, nome, sobrenome etc. A ordem dos campos permite especificar os que devem ser processados primeiro."

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication"
>title="Atividade de desduplicação"
>abstract="A atividade **Desduplicação** permite excluir duplicatas nos resultados das atividades de entrada. Ela é usada principalmente após atividades de direcionamento e antes de atividades que permitem o uso de dados direcionados."

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_complement"
>title="Gerar um complemento"
>abstract="É possível gerar uma transição de saída adicional com a população restante, que foi excluída como uma duplicata. Para fazer isso, ative a opção **[!UICONTROL Gerar complemento]**"

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_settings"
>title="Configurações de desduplicação"
>abstract="Para excluir duplicatas nos dados recebidos, defina o método de desduplicação nos campos abaixo. Por padrão, somente um registro é mantido. Também é necessário selecionar o modo de desduplicação com base em uma expressão ou um atributo. Por padrão, o registro a ser mantido fora das duplicatas é selecionado aleatoriamente."

A atividade **Deduplication** remove todos os resultados duplicados no público.

+++ Detalhes de configuração

>[!NOTE]
>
>Se você tiver várias transições de entrada, primeiro precisará selecionar o **Conjunto principal** na lista suspensa.

Depois de adicionar uma atividade **Desduplicação**, você pode escolher os campos para identificar duplicatas. Selecione **Adicionar atributo** para identificar os campos em que podem ocorrer duplicatas.

![](./assets/activities/deduplication.png)

Depois de identificar os campos, é possível definir as configurações de desduplicação.

| Configuração | Descrição |
| ------- | ----------- |
| Duplicatas a serem mantidas | O número de registros duplicados a serem mantidos. Se o valor for definido como 0, **todos** os registros duplicados serão mantidos. |
| Método de desduplicação | O método para remover os registros duplicados. <ul><li>**Seleção aleatória**: o registro removido é escolhido aleatoriamente.</li><li>**Usando uma expressão**: o registro removido é baseado na expressão enviada. Você pode classificar em ordem crescente ou decrescente, dependendo de quais valores deseja remover.</li><li>**Valores não vazios**: o registro removido é baseado na expressão enviada. Os registros nos quais a expressão não tiver um valor serão removidos.</li><li>**Seguindo uma lista de valores**: o registro removido é baseado no campo ou na expressão enviada. Você pode classificar os valores restantes aleatoriamente, em ordem crescente ou decrescente.</li></ul> |

Além disso, você pode selecionar a opção **Gerar complemento**. A geração de um complemento processa a população restante e contém os dados **não** incluídos como parte da desduplicação. Uma transição de saída adicional será adicionada à atividade.

+++

#### Enriquecimento

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment"
>title="Atividade enriquecimento"
>abstract="A atividade **Enriquecimento** permite aprimorar os dados direcionados com informações adicionais do banco de dados. Normalmente, ela é usada em uma composição após atividades de segmentação."

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_data"
>title="Atividade enriquecimento"
>abstract="Após a sua adição na composição, os dados de enriquecimento podem ser usados nas atividades adicionadas posteriormente à atividade **Enriquecimento** para segmentar perfis em grupos distintos com base em seus comportamentos, preferências e escolhas."

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_simplejoin"
>title="Definição de link"
>abstract="Crie um link entre os dados da tabela de trabalho e o banco de dados federado."

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_reconciliation"
>title="Reconciliação de enriquecimento"
>abstract="Defina os parâmetros de reconciliação."

>[!CONTEXTUALHELP]
>id="dc_targetdata_personalization_enrichmentdata"
>title="Dados de enriquecimento"
>abstract="Selecione os dados a serem usados para enriquecer a sua composição. Você pode selecionar dois tipos de dados de enriquecimento: um único atributo de enriquecimento do esquema, também conhecido como dimensão de direcionamento, ou um link de coleção, que é um link com cardinalidade 1-N entre tabelas."

A atividade **Enrichment** permite aprimorar sua composição adicionando dados adicionais do banco de dados federado.

Se você tiver configurado uma conexão com o destino Federated Audience Composition, poderá usar a atividade Enrichment para enriquecer dados que vêm do Adobe Experience Platform com atributos do banco de dados externo. [Saiba como enriquecer públicos do Adobe Experience Platform com dados externos](../connections/destinations.md)

+++ Detalhes de configuração

>[!NOTE]
>
>Se você tiver várias transições de entrada, primeiro precisará selecionar o **Conjunto principal** na lista suspensa.

Depois de adicionar a atividade **Enriquecimento** à sua composição, você pode selecionar **Adicionar dados de enriquecimento** para escolher qual atributo deseja usar para enriquecer sua composição. Você pode selecionar **Editar expressão** para criar uma expressão avançada para selecionar o atributo.

![](./assets/activities/enrichment.png)

+++

#### Reconciliação

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation"
>title="Atividade de reconciliação"
>abstract="A atividade **Reconciliação** permite definir o vínculo entre os dados no banco de dados os dados em uma tabela de trabalho."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_field"
>title="Campo de seleção de reconciliação"
>abstract="Campo de seleção de reconciliação"

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_condition"
>title="Condição de criação de reconciliação"
>abstract="Condição de criação de reconciliação"

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_complement"
>title="Complemento de geração de reconciliação"
>abstract="Complemento de geração de reconciliação"

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_targeting"
>title="Esquema"
>abstract="Selecione o novo esquema a ser aplicado aos dados. Um esquema, também conhecido como dimensão de direcionamento, permite definir a população direcionada: destinatários, assinantes de aplicativos, operadores, assinantes etc. Por padrão, o esquema atual da composição está selecionado."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_rules"
>title="Regras de reconciliação"
>abstract="Selecione as regras de reconciliação a serem usadas para a desduplicação. Para usar atributos, selecione a opção **Atributos simples** e escolha os campos origem e destino. Para criar sua própria condição de reconciliação usando o modelador de consultas, selecione a opção **Condições de reconciliação avançadas**."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_targeting_selection"
>title="Selecione a dimensão de direcionamento"
>abstract="Selecione o esquema, também conhecido como dimensão de direcionamento, com o qual seus dados de entrada serão reconciliados."

>[!CONTEXTUALHELP]
>id="dc_orchestration_keep_unreconciled_data"
>title="Manter dados não reconciliados"
>abstract="Por padrão, os dados não reconciliados são mantidos na transição de saída e disponibilizados na tabela de trabalho para uso futuro. Para remover dados não reconciliados, desative a opção **Manter dados não reconciliados**."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_attribute"
>title="Atributo de reconciliação"
>abstract="Selecione o atributo a ser usado para reconciliar dados e confirme."

>[!NOTE]
>
>Por padrão, os dados não reconciliados são mantidos na transição de saída e ficam disponíveis na tabela de trabalho para uso futuro. Se você **não** deseja que os dados reconciliados sejam usados, desative a opção **Manter dados não reconciliados**.

A atividade **Reconciliation** permite definir o vínculo entre os dados do banco de dados federado e os dados de uma tabela de trabalho.

+++ Detalhes de configuração

Depois de adicionar a atividade **Reconciliação** à sua composição, você pode escolher qual esquema usar para a reconciliação.

Depois de escolher o esquema, você precisará configurar suas regras de reconciliação. Você pode escolher entre **Atributos simples** ou **Condições avançadas de reconciliação**.

>[!BEGINTABS]

>[!TAB Atributos simples]

Depois de escolher **Atributos simples**, selecione **Adicionar regra**. Agora você pode configurar a reconciliação adicionando os campos **Source** e **Destino**. O campo **Destination** corresponde aos campos do esquema selecionado.

![](./assets/activities/reconciliation-rules.png)

Os dados são reconciliados quando a origem e o destino são iguais. Você pode adicionar mais critérios de reconciliação selecionando **Adicionar regra**. Se várias condições de associação forem especificadas, **todas** delas deverão ser verificadas para que os dados possam ser vinculados.

>[!TAB Condições avançadas de reconciliação]

Depois de escolher **Condições de reconciliação avançadas**, selecione **Criar condições**. Agora você pode criar sua própria condição de reconciliação usando o modelador de consultas. Para obter mais informações sobre como usar a Modeler de consulta, leia a [Visão geral da Modeler de consulta](../query/home.md)

![](./assets/activities/reconciliation-advanced.png)

>[!ENDTABS]

Também é possível filtrar os dados reconciliados. Selecione **Criar filtro** para criar uma condição personalizada usando o Query Modeler. Para obter mais informações sobre como usar a Modeler de consulta, leia a [Visão geral da Modeler de consulta](../query/home.md)

+++

#### Salvar público-alvo

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

>[!IMPORTANT]
>
>Se sua sandbox usa uma política de mesclagem de **precedência de conjunto de dados**, entre em contato com o atendimento ao cliente da Adobe para adicionar o conjunto de dados `Halos UPS` à política de mesclagem.
>
>Para obter mais informações sobre políticas de mesclagem, leia a [visão geral das políticas de mesclagem](https://experienceleague.adobe.com/pt-br/docs/experience-platform/profile/merge-policies/overview).

A atividade **Salvar público-alvo** permite criar um público-alvo com base na composição. Depois que o público-alvo é criado, é possível usá-los no Audience Portal no Adobe Experience Platform. Para obter mais informações sobre como usar os públicos-alvo com a Composição de público federado, leia a [visão geral dos públicos-alvo](../start/audiences.md). Para obter mais informações sobre públicos no Experience Platform, leia a [Visão geral do Portal de público-alvo](https://experienceleague.adobe.com/pt-br/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}.

+++ Detalhes de configuração

>[!IMPORTANT]
>
>O nome do público-alvo **deve** ser exclusivo na sandbox atual e não pode ter o mesmo nome que qualquer público-alvo existente.

Depois de adicionar a atividade **Salvar público-alvo** à sua composição, você pode especificar o nome do público recém-criado.

![](./assets/activities/save-audience.png)

Agora você pode especificar os mapeamentos para selecionar quais campos deseja transferir para o público-alvo recém-criado. Selecione **Adicionar mapeamento de público-alvo** e escolha os campos de público-alvo de origem e de destino, repetindo quantas vezes forem necessárias.

Depois de adicionar os mapeamentos, é possível selecionar a identidade e o namespace principais para identificar os perfis direcionados no banco de dados. O campo de identidade principal é usado para identificar os perfis, enquanto o namespace de identidade atua como uma chave para identificar a identidade.

+++

#### Divisão

>[!CONTEXTUALHELP]
>id="dc_orchestration_split"
>title="Atividade Divisão"
>abstract="A atividade **Divisão** permite segmentar as populações recebidas em vários subconjuntos com base em diferentes critérios de seleção, como regras de filtragem ou tamanho da população."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_segments"
>title="Segmentos para atividade de divisão"
>abstract="Adicione quantos subconjuntos desejar para segmentar a população recebida.<br/></br>Quando a atividade **Divisão** é executada, a população é segmentada nos diferentes subconjuntos na ordem em que são adicionados à atividade. Antes de iniciar a sua composição, certifique-se de ter ordenado os subconjuntos na ordem que atenda às suas necessidades usando os botões de seta."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_filter"
>title="Filtro da atividade de divisão"
>abstract="Para aplicar uma condição de filtragem ao subconjunto, selecione **[!UICONTROL Criar filtro]** e configure a regra de filtragem desejada usando o modelador de consultas. Por exemplo, inclua perfis da população recebida cujo endereço de email já exista no banco de dados."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_limit"
>title="Limite da atividade de divisão"
>abstract="Para limitar o número de perfis selecionados pelo subconjunto, ative a opção **[!UICONTROL Habilitar limite]**, e especifique o número ou as porcentagens da população a serem incluídas."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_sorting"
>title="Classificação da atividade de divisão"
>abstract="Ao definir um limite de população para um subconjunto, é possível classificar os perfis selecionados com base em um atributo de perfil específico, em ordem crescente ou decrescente. Para fazer isso, ative a opção **Habilitar classificação**. Por exemplo, é possível restringir um subconjunto para incluir apenas os 50 perfis com o valor de compra mais alto."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_complement"
>title="Divisão e geração de complemento"
>abstract="Após configurar todos os subconjuntos, é possível selecionar a população restante que não correspondeu a nenhum dos subconjuntos e incluí-la em uma transição de saída adicional. Para isso, ative a opção **Gerar complemento.**"

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_generatesubsets"
>title="Gerar todos os subconjuntos na mesma tabela"
>abstract="Ative essa opção para agrupar todos os subconjuntos em uma única transição de saída."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_emptytransition"
>title="Ignorar transição vazia"
>abstract="Ative a opção **[!UICONTROL Ignorar transição vazia]** para desabilitar a transição de saída para este subconjunto se a população de entrada estiver vazia."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_enable_overlapping"
>title="Habilitar sobreposição de populações de saída"
>abstract="A opção **[!UICONTROL Habilitar sobreposição de populações de saída]** permite gerenciar populações pertencentes a vários subconjuntos. Quando a caixa não está marcada, a atividade Divisão garante que um destinatário não possa estar presente em diversas transições de saída, mesmo que atenda aos critérios de vários subconjuntos. Eles estarão no público-alvo da primeira guia com critérios correspondentes. Quando a caixa for marcada, os destinatários poderão ser encontrados em vários subconjuntos se atenderem aos critérios de filtro.  "

A atividade **Split** separa a população de entrada em várias partes, dependendo dos critérios fornecidos.

+++ Detalhes de configuração

>[!IMPORTANT]
>
>Quando a atividade **Split** é executada, a população é separada entre os diferentes subconjuntos na **ordem em que são adicionados**. Por exemplo, se o primeiro subconjunto dividir 70% da população inicial, o próximo subconjunto aplicará seus critérios de seleção aos 30% restantes.
>
>Antes de executar a composição, certifique-se de ter ordenado os subconjuntos na ordem em que deseja que as divisões sejam executadas.

Depois de adicionar a atividade **Split** à sua composição, você pode determinar como subdefinir seu público. Selecione **Adicionar segmento** para criar seus diferentes caminhos de ramificação.

Agora você pode fornecer detalhes para cada um desses subcaminhos. Você pode dar um nome ao subcaminho, bem como às condições de filtro. Para criar uma condição de filtragem, selecione **Criar filtro** e configure a regra de filtragem usando o Query Modeler. Para obter mais informações sobre como usar a Modeler de consulta, leia a [Visão geral da Modeler de consulta](../query/home.md).

Depois de criar a condição de filtragem, você pode aplicar as seguintes regras adicionais:

- **Habilitar limite**: limita o número de perfis que podem ser divididos no subconjunto. Você pode definir isso como um número ou uma porcentagem da população.
   - Se você ativar um limite, também poderá classificar os perfis selecionados com base em um atributo de perfil específico. Ative **Habilitar classificação** e você poderá classificar os atributos em ordem crescente ou decrescente.
- **Ignorar transição vazia**: desabilita a transição se a população de entrada estiver vazia.

Agora que os subconjuntos foram configurados, há mais algumas opções adicionais que você pode definir.

| Opções | Descrição |
| ------- | ----------- |
| **Gerar complemento** | Cria uma transição de saída que contém a população restante. |
| **Habilitar sobreposição de populações de saída** | Se habilitado, o destinatário **não pode** estar presente em várias transições de saída e estará **somente** presente na primeira transição de saída. Se desabilitado, o destinatário **pode** aparecer em várias transições de saída. |
| **Gerar todos os subconjuntos na mesma tabela** | Agrupa todos os subconjuntos em uma única transição de saída. |

+++

### Atividades de controle do fluxo {#flow-control}

As atividades de controle de fluxo permitem definir a organização e a coordenação de sua composição.

#### E se juntar

>[!CONTEXTUALHELP]
>id="dc_orchestration_and-join"
>title="Atividade AND-join"
>abstract="A atividade **And-join** permite sincronizar várias ramificações de execução de uma composição. Ela é acionada quando todas as atividades anteriores forem concluídas. Isso permite que você se certifique de que determinadas atividades foram concluídas antes de continuar a execução da composição."

A atividade **AND-join** permite combinar várias ramificações de uma composição. Esta atividade só será disparada depois que **todas** as transições de entrada forem ativadas.

+++ Detalhes de configuração

Depois de adicionar várias atividades para formar pelo menos duas ramificações diferentes, você pode adicionar a atividade **AND-join** ao final de qualquer ramificação.

![](./assets/activities/and-join.png)

Na seção **Opções de mesclagem**, você pode selecionar todas as atividades que deseja sincronizar. Além disso, você pode escolher qual transição de entrada manter na lista suspensa **Conjunto principal**.

+++

#### Fim

A atividade **End** marca graficamente o fim da composição e não tem impacto funcional.

#### Bifurcação

>[!CONTEXTUALHELP]
>id="dc_orchestration_fork"
>title="Atividade Bifurcação"
>abstract="A atividade **Bifurcação** permite criar transições de saída para iniciar várias atividades ao mesmo tempo."

>[!CONTEXTUALHELP]
>id="dc_orchestration_fork_transitions"
>title="Transições da atividade bifurcação"
>abstract="Por padrão, duas transições são criadas com uma atividade **Bifurcação**. Selecione o botão **Adicionar transição** para definir uma transição de saída adicional e insira seu rótulo."

A atividade **Fork** permite criar várias transições de saída que iniciam várias atividades simultaneamente.

+++ Detalhes de configuração

Depois de adicionar a atividade **Bifurcação** à sua composição, duas transições de saída são geradas automaticamente. Você pode dar um nome a essas transições de saída. Além disso, você pode selecionar **Adicionar transição** para adicionar outra transição de saída.

![](./assets/activities/fork.png)

+++

#### Scheduler

>[!CONTEXTUALHELP]
>id="dc_orchestration_scheduler"
>title="Atividade scheduler"
>abstract="A atividade **Scheduler** permite programar quando a composição de público-alvo será iniciada. Esta atividade deve ser considerada como um início agendado. Ela só pode ser usada como a primeira atividade de uma composição."

>[!CONTEXTUALHELP]
>id="dc_orchestration_schedule_validity"
>title="Validade do Scheduler"
>abstract="É possível definir um período de validade para o Scheduler. Pode ser permanente (padrão) ou pode ser válido até uma data específica."

>[!CONTEXTUALHELP]
>id="dc_orchestration_schedule_options"
>title="Opções do Scheduler"
>abstract="Defina a frequência do scheduler. Pode ser executado em um momento específico, uma ou várias vezes por dia, semana ou mês."

A atividade **Scheduler** permite agendar quando iniciar a execução da composição. Você **deve** usá-la como a primeira atividade da composição.

+++ Detalhes de configuração

Depois de adicionar a atividade **Scheduler** à sua composição, você pode definir a **Frequência de execução** para a composição. As opções incluem **Uma Vez**, **Diariamente**, **Várias vezes por dia**, **Semanalmente** e **Mensalmente**.

>[!BEGINTABS]

>[!TAB Uma vez]

>[!NOTE]
>
>A hora é definida como UTC.

Se você selecionar **Uma Vez**, a composição será executada somente uma vez. Você pode selecionar a data e a hora em que a composição será executada.

>[!TAB Diariamente]

Se você selecionar **Diariamente**, a composição será executada uma vez por dia. No entanto, você pode definir em qual dia do mês a composição será executada na seção **Dia do mês**. Os valores possíveis incluem **Todos os dias**, **Nos dias da semana**, **Até um período selecionado** e **Dias da semana selecionados**.

| Dia do mês | Descrição |
| ---------------- | ----------- |
| Todos os dias | A composição é executada todos os dias. |
| Nos dias da semana | A composição é executada todos os dias da semana. |
| Por um período selecionado | A composição é executada todos os dias durante todo o período selecionado. Você pode definir a duração do período de recorrência, bem como a data em que o período começa. |
| Dias da semana selecionados | A composição é executada todos os dias da semana selecionada. |

Após escolher o dia do mês em que a programação será executada, você pode selecionar **Visualizar horários de inicialização** para verificar a programação das próximas dez execuções da sua composição.

>[!TAB Várias vezes ao dia]

Se você selecionar **Várias vezes por dia**, a composição será executada várias vezes por dia. Você pode escolher se a composição será executada em horários específicos por dia ou periodicamente em horários definidos.

Se você selecionar **Horas selecionadas**, poderá escolher as horas específicas em que a composição será executada. Se você selecionar **Periódico**, poderá escolher com que frequência a composição será executada em horas ou minutos e entre que horas será executada. Todos os horários estão em UTC.

Após selecionar as horas, você pode escolher com que frequência a execução é executada na seção **Dia do mês**.

| Dia do mês | Descrição |
| ---------------- | ----------- |
| Todos os dias da semana | A composição é executada todos os dias. |
| Em determinados dias da semana | A composição é executada todos os dias da semana selecionada. |

Após escolher o dia do mês em que a programação será executada, você pode selecionar **Visualizar horários de inicialização** para verificar a programação das próximas dez execuções da sua composição.

>[!TAB Semanalmente]

Se você selecionar **Semanalmente**, a composição será executada na frequência semanal definida. Se você definir a frequência semanal como um número maior que 1, também poderá escolher a data a partir da qual a execução começa.

Após escolher a frequência de avaliação, você pode escolher a frequência com que a execução é executada na seção **Dia do mês**.

| Dia do mês | Descrição |
| ---------------- | ----------- |
| Todos os dias da semana | A composição é executada todos os dias. |
| Em determinados dias da semana | A composição é executada todos os dias da semana selecionada. |

Após escolher o dia do mês em que a programação será executada, você pode selecionar **Visualizar horários de inicialização** para verificar a programação das próximas dez execuções da sua composição.

>[!TAB Mensal]

Se você selecionar **Mensalmente**, a composição será executada na frequência mensal definida. Você pode defini-lo para ser todo mês ou em determinados meses.

Após escolher a frequência mensal, você pode escolher o **Dia do mês** em que a execução é executada.

| Dia do mês | Descrição |
| ---------------- | ----------- |
| Todos os dias | A composição é executada todos os dias. |
| Nos dias da semana | A composição é executada todos os dias da semana. |
| Por um período selecionado | A composição é executada todos os dias durante todo o período selecionado. Você pode definir a duração do período de recorrência, bem como a data em que o período começa. |
| Dias da semana selecionados | A composição é executada todos os dias da semana selecionada. |

Depois de definir o **Dia do mês**, você pode escolher a hora de início. Todos os horários estão em UTC.

>[!ENDTABS]

Depois de selecionar a frequência de execução, você pode escolher o **Período de validade** do agendamento.

| Período de validade | Descrição |
| --------------- | ----------- |
| **Permanente (nunca expira)** | A composição nunca expirará. |
| **Período de validade** | A composição será executada entre as datas especificadas. |

+++

#### Aguardar

>[!CONTEXTUALHELP]
>id="dc_orchestration_wait"
>title="Atividade aguardar"
>abstract="A atividade **Aguardar** é usada para atrasar a transição de uma atividade para outra."

A atividade **Wait** pausa a execução da composição pelo período de tempo especificado.

+++ Detalhes de configuração

Depois de adicionar a atividade **Aguardar** à sua composição, você pode torná-la uma **Duração** ou uma **Tempo fixo** de espera.

![](./assets/activities/wait.png)

Se você selecionar duração, poderá definir o período de tempo de espera. Esse período pode ser em segundos, minutos, horas ou dias.

Se você selecionar tempo fixo, poderá definir a composição para aguardar até a data e hora especificadas. A hora está definida para o seu **fuso horário local**.

+++

## Transições {#transitions}

Em composições, as transições mostram como os dados são transportados de uma atividade para outra. As transições armazenam os dados em uma tabela de trabalho temporária. Se você selecionar a transição, poderá exibir as seguintes informações:

- **Visualizar esquema**: você pode selecionar esta opção para visualizar o esquema da tabela de trabalho.
- **Visualizar resultados**: você pode selecionar esta opção para visualizar os dados transportados na transição selecionada. Esta opção só estará disponível se **Manter o resultado de populações interinas entre duas execuções** estiver habilitada.

![](assets/transition-preview.png)

## Próximas etapas {#next-steps}

Depois de ler este guia, você terá uma melhor compreensão das atividades e transições que podem ser usadas em uma composição. Para obter mais informações sobre composições em geral, leia a [visão geral da composição](./create-composition.md).
