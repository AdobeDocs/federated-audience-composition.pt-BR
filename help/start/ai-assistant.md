---
title: Visão geral do Assistente de IA
description: Saiba como usar o Assistente de IA, incluindo conhecimento do produto, insights operacionais e criação de composições de público-alvo federado.
exl-id: f7493a57-e42d-43f9-b20a-1b9b90477a74
TQID: https://experienceleague.adobe.com/j-KXucjaZa4dNSjg5POqxh7KOSUHG5CnBkBLFA6rPVs
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: d095671a-1355-40aa-8b5f-06c33c68080bid: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: fda4d9d7b45833d7e080ae80f42b7ca5ce36b3ad
workflow-type: ht
source-wordcount: 642
ht-degree: 100%

---

# Visão geral do Assistente de IA {#ai-assistant}

O Assistente de IA é um recurso da interface projetado para ajudar você a navegar e entender os conceitos da Adobe. Você pode usar o Assistente de IA para entender melhor os casos de uso de conhecimento do produto em diversos produtos da Adobe Experience Cloud, incluindo a Composição de público-alvo federado.

>[!CAUTION]
>
>É preciso concordar com as diretrizes do usuário para IA generativa da Adobe Experience Cloud antes de usar o Assistente de IA. Saiba mais sobre o contrato na [visão geral do Assistente de IA (legado)](https://experienceleague.adobe.com/pt-br/docs/experience-platform/ai-assistant/home){target="_blank"}.

Na composição de público-alvo federado, é possível acessar o conhecimento do produto para aprender sobre conceitos da Adobe relacionados a diferentes partes do processo. O Assistente de IA oferece suporte a quatro tipos de casos de uso: **Descoberta aberta** (explore conceitos de produto com base na documentação da Experience League), **Aprendizagem e solução de problemas direcionadas** (faça perguntas sobre recursos ou funcionalidades específicos), **Insights operacionais** (faça perguntas sobre seus objetos na Composição de público-alvo federado) e **Criação de composições de público-alvo federado**.

## Acesso {#access}

Para acessar o Assistente de IA, clique no ![ícone do Assistente de IA](/help/start/assets/ai-assistant/icon.png) na barra superior. O Assistente de IA será exibido na seção direita da tela. Você pode clicar no ![Texto alternativo da imagem](assets/do-not-localize/Smock_FullScreen_18_N.svg "ícone Expandir") para abrir a janela do Assistente de IA.

![O ícone do Assistente de IA está realçado, mostrando como acessar o Assistente de IA.](/help/start/assets/ai-assistant/access.png)

## Uso do Assistente de IA {#using}

Após abrir o Assistente de IA, digite sua pergunta no campo na parte inferior da tela e pressione Enter. A resposta à sua pergunta agora é exibida. Você pode usar polegares para cima ou para baixo para classificar sua resposta.

![Um exemplo de pergunta e resposta no Assistente de IA é exibido.](/help/start/assets/ai-assistant/sample-question-answer.png)

## Exemplos de perguntas {#sample-questions}

As seguintes consultas mostram os tipos disponíveis de perguntas que você pode fazer ao Assistente de IA:

| Tipo de consulta | Exemplo de pergunta |
| ---------- | --------------- |
| Descoberta aberta | <ul><li>O que é a composição de público-alvo federado?</li></ul> |
| Aprendizado direcionado | <ul><li>Como posso configurar uma conta de banco de dados federado do Snowflake?</li><li>Como posso criar uma composição federada?</li></ul> |
| Insights operacionais | <ul><li>Quantos bancos de dados federados tenho na minha sandbox?</li><li>Quantos esquemas criei nos últimos 30 dias?</li></ul> |
| Criação de uma composição de público-alvo federado | <ul><li>Crie um público-alvo federado de clientes que moram no Reino Unido.</li></ul> |

Além disso, você pode usar o Assistente de IA para criar de forma autônoma uma composição de público-alvo federado.

## Criar um público-alvo {#create-audience}

Você pode usar o Assistente de IA para criar uma composição de público-alvo federado usando prompts em linguagem natural. Ao usar o Assistente de IA para criar um público-alvo, ele apresenta um plano com base em seu prompt e o executa no navegador usando a automação habilitada por IA.

Por exemplo, se você pedir ao Assistente de IA para “Criar um público-alvo federado de clientes que residem no Reino Unido usando o esquema CUSTOMERS_Table”, o Assistente de IA apresentará o plano que seguirá para criar o público-alvo, incluindo etapas como a navegação até a página Composições federadas, como o agente criará a composição e como salvará o público-alvo depois de concluída.

![Uma pergunta e uma resposta de exemplo são exibidas.](/help/start/assets/ai-assistant/ask-create.png)

Se o plano parecer preciso, você pode selecionar **[!UICONTROL Executar]** para permitir que o agente realize a automação. O agente, no navegador, executa autonomamente as etapas de criação da composição solicitada na interface de Composição de público-alvo federado. Se, a qualquer momento, você quiser parar a automação, selecione **[!UICONTROL Parar]**.

![O plano foi executado e o agente está executando o plano de forma autônoma.](/help/start/assets/ai-assistant/execute-plan.png)

Atualmente, a habilidade de criação de público-alvo aceita os seguintes recursos adicionais:

- Scheduler
   - Você pode criar composições federadas que são executadas em uma programação recorrente. Os valores aceitos incluem **Uma vez** e **Diariamente**.
- Desduplicação
   - Você pode desduplicar os registros de dados federados durante a reconciliação de dados

## Próximas etapas

Para obter mais informações sobre o Assistente de IA, incluindo exemplos de objetivos que você pode alcançar com ele e aprender como ele funciona, leia a [visão geral do Assistente de IA](https://experienceleague.adobe.com/pt-br/docs/experience-platform/ai-assistant/home){target="_blank"}.

Para obter uma lista completa das perguntas de Insights operacionais que você pode fazer para a Composição de público-alvo federado, leia a [seção de insights operacionais ](https://experienceleague.adobe.com/pt-br/docs/experience-platform/ai-assistant/home#operational-insights){target="_blank"}.
