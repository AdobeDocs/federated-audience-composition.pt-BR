---
audience: end-user
title: Direcionamento De Várias Entidades Com Públicos-Alvo Federados De Composição No Adobe Journey Optimizer
description: Saiba como direcionar perfis de públicos-alvo de Composição de público-alvo federado no Adobe Journey Optimizer jornada.
source-git-commit: 79f05c5a1b025b522a1b88615973d9fe383e3720
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 3%

---


# Direcionamento de várias entidades com públicos-alvo de composição de público-alvo federado no Adobe Journey Optimizer

Com o direcionamento de várias entidades, você pode usar os atributos de público-alvo da Federated Audience Composition como identificadores complementares no Adobe Journey Optimizer jornada. Esses atributos permitem ativar públicos-alvo em várias entidades, como contas ou nível de assinatura.

## Criar seu público na Composição de público federado {#create}

Para começar com o direcionamento de várias entidades, primeiro será necessário criar e salvar seu público na Composição de público-alvo federado.

Na interface de Composição de público-alvo, adicione a atividade **Criar público-alvo** para criar o público-alvo na tela de composição federada e adicione a atividade **Salvar público-alvo** para configurar os mapeamentos do público-alvo, a identidade principal e a expiração dos dados.

![A interface do usuário da Composição de Público-Alvo Federado é exibida, mostrando o público-alvo.](/help/connections/assets/multi-entity-targeting/build-activity.png)

Depois de concluir as configurações do público-alvo, selecione **Iniciar** para iniciar a execução da composição. Esse público-alvo e seu conjunto de dados correspondente estarão disponíveis para uso no Experience Platform.

Para obter mais detalhes sobre como criar uma composição na Composição de Público-Alvo Federado, leia o [criar um guia de composição](/help/compositions/create-composition.md).

## Ativar público no Adobe Journey Optimizer {#activate}

Após a conclusão da execução da composição, é possível ativar o público no Journey Optimizer. Na seção **Gerenciamento de Jornadas** do Adobe Journey Optimizer, selecione **Jornadas** seguido por **Criar jornada** para abrir a interface de usuário do jornada.

![O botão Criar jornada no Adobe Journey Optimizer está realçado.](/help/connections/assets/multi-entity-targeting/select-create-journey.png)

Na interface do jornada, adicione um nó **Read audience**. Você pode configurar esse nó fornecendo um rótulo e selecionando o público-alvo criado anteriormente.

![O nó Ler público-alvo é exibido na interface do usuário do Journey Optimizer.](/help/connections/assets/multi-entity-targeting/read-journey.png)

Depois de escolher o público criado anteriormente, habilite **Usar identificador complementar**.

![A caixa de seleção Usar identificador complementar está realçada.](/help/connections/assets/multi-entity-targeting/enable-use-supplemental-identifier.png)

Agora você pode escolher um identificador complementar. Na tela do seletor, selecione **Modo Avançado** e navegue até **Experience Platform**. Nesta página, selecione o nome do público-alvo criado anteriormente e escolha o identificador complementar que deseja usar para o público-alvo.

![O editor de expressão é exibido.](/help/connections/assets/multi-entity-targeting/add-expression.png)

## Configurar condições de jornada {#configure-journey}

Agora que ativou e definiu as configurações do público-alvo, você pode continuar a definir o restante das condições da jornada. Neste caso de uso, adicione um nó **Otimizer** após o nó **Read audience**, seguido de um nó **Action**.

Depois de configurar os nós restantes, selecione **Publicar** para concluir a criação da jornada.

![O botão Publicar está realçado.](/help/connections/assets/multi-entity-targeting/select-publish.png)

Sua jornada agora segmentará os perfis de público-alvo com base no **identificador complementar** em vez do identificador principal. Usando esse recurso, agora é possível direcionar várias entidades, como ID de assinatura, ID de conta ou ID de pedido, e ativar para o canal desejado.

## Próximas etapas {#next-steps}

Depois de ler este guia, agora você sabe como usar identificadores complementares dos públicos-alvo do Federated Audience Composition no Journey Optimizer jornada. Para obter mais informações sobre como usar jornadas complementares, leia o [usar identificadores complementares no guia do jornada](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/orchestrate-journeys/manage-journey/supplemental-identifier).

