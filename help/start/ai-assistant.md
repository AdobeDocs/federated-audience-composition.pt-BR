---
title: Visão geral do assistente de IA
description: Saiba como usar o Assistente de IA, incluindo conhecimento do produto, insights operacionais e criação de composições de público federado.
exl-id: f7493a57-e42d-43f9-b20a-1b9b90477a74
source-git-commit: 226679a38d0ad17726fd743f5df3b74879a2dd32
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 16%

---

# Visão geral do Assistente de IA {#ai-assistant}

O Assistente de IA é um recurso da interface projetado para ajudar você a navegar e entender os conceitos da Adobe. Você pode usar o AI Assistant para entender melhor os casos de uso de conhecimento do produto em vários produtos do Adobe Experience Cloud, incluindo a Federated Audience Composition.

>[!CAUTION]
>
>É preciso concordar com as diretrizes do usuário para IA generativa da Adobe Experience Cloud antes de usar o Assistente de IA. Saiba mais sobre o contrato na [visão geral do Assistente de IA (herdado)](https://experienceleague.adobe.com/pt-br/docs/experience-platform/ai-assistant/home){target="_blank"}.

Na composição de público-alvo federado, é possível acessar o conhecimento do produto para aprender sobre conceitos da Adobe relacionados a diferentes partes do processo. O Assistente de IA oferece suporte a quatro tipos de casos de uso: **Descoberta aberta** (explore conceitos de produto com base na documentação do Experience League), **Aprendizagem e solução de problemas direcionadas** (faça perguntas sobre recursos ou funcionalidades específicos), **Insights operacionais** (faça perguntas sobre seus objetos no Federated Audience Composition) e **Criação de composições de público federado**.

## Acesso {#access}

Para acessar o Assistente de IA, selecione ![o ícone do Assistente de IA](/help/start/assets/ai-assistant/icon.png) na barra superior. O Assistente de IA será exibido na seção direita da tela. Você pode selecionar ![Dividir texto alternativo da imagem](assets/do-not-localize/Smock_FullScreen_18_N.svg "o ícone Expandir") para expandir a janela do Assistente de IA.

![O ícone do Assistente de IA está realçado, mostrando como acessar o Assistente de IA.](/help/start/assets/ai-assistant/access.png)

## Usar o Assistente de IA {#using}

Depois de abrir o Assistente de IA, insira a pergunta no campo na parte inferior da tela e pressione Enter. A resposta à sua pergunta agora é exibida. Você pode usar polegares para cima ou para baixo para classificar sua resposta.

![Um exemplo de pergunta e resposta no Assistente de IA é exibido.](/help/start/assets/ai-assistant/sample-question-answer.png)

## Exemplos de perguntas {#sample-questions}

As seguintes consultas mostram os tipos disponíveis de perguntas que você pode fazer ao Assistente de IA:

| Tipo de consulta | Exemplo de pergunta |
| ---------- | --------------- |
| Abrir descoberta | <ul><li>O que é a composição de público-alvo federado?</li></ul> |
| Aprendizado direcionado | <ul><li>Como posso configurar uma conta do Snowflake Federated database?</li><li>Como posso criar uma composição federada?</li></ul> |
| Insights operacionais | <ul><li>Quantos bancos de dados federados eu tenho na minha sandbox?</li><li>Quantos esquemas eu criei nos últimos 30 dias?</li></ul> |
| Criação de uma composição de público-alvo federado | <ul><li>Crie um público-alvo federado de clientes que moram no Reino Unido.</li></ul> |

Além disso, você pode usar o Assistente de IA para criar autonomamente uma composição de público-alvo federado.

## Criar um público-alvo {#create-audience}

Você pode usar o AI Assistant para criar uma composição de público-alvo federado usando prompts em linguagem natural. Quando você usa o AI Assistant para criar um público-alvo, o AI Assistant apresenta um plano com base em seu prompt e o executa em seu navegador usando a automação habilitada por IA.

Por exemplo, se você pedir ao Assistente de IA para &quot;Criar um público-alvo federado de clientes que vivem no Reino Unido usando o esquema CUSTOMERS_Table&quot;, o Assistente de IA apresentará o plano que seguirá para criar o público-alvo, incluindo etapas como navegar até a página Composições federadas, como o agente criará a composição e salvará o público-alvo depois de concluída.

![Uma pergunta e uma resposta de exemplo são exibidas.](/help/start/assets/ai-assistant/ask-create.png)

Se o plano parecer preciso, você pode selecionar **[!UICONTROL Executar]** para permitir que o agente passe pela automação. O agente, no navegador, percorrerá autonomamente as etapas de criação da composição solicitada na interface do usuário da Composição de público-alvo federado. Se, a qualquer momento, você quiser parar a automação, selecione **[!UICONTROL Parar]**.

![O plano foi executado e o agente está executando o plano de forma autônoma.](/help/start/assets/ai-assistant/execute-plan.png)

Atualmente, a habilidade de criação de público-alvo suporta os seguintes recursos adicionais:

- Scheduler
   - Você pode criar composições federadas que são executadas em uma programação recorrente. Os valores suportados incluem **Uma vez** e **Diariamente**.
- Desduplicação
   - Você pode desduplicar os registros de dados federados durante a reconciliação de dados

## Próximas etapas

Para obter mais informações sobre o Assistente de IA, incluindo exemplos de objetivos que você pode realizar com o Assistente de IA e saber como o Assistente de IA funciona, leia a [Visão geral do Assistente de IA](https://experienceleague.adobe.com/pt-br/docs/experience-platform/ai-assistant/home){target="_blank"}.

Para obter uma lista completa das perguntas sobre o Operational Insight que você pode fazer para a Federated Audience Composition, leia a [seção de insights operacionais](https://experienceleague.adobe.com/pt-br/docs/experience-platform/ai-assistant/home#operational-insights){target="_blank"}.
