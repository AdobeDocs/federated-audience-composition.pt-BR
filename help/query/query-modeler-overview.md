---
audience: end-user
title: Trabalhar com o modelador de consultas
description: Saiba como trabalhar com o modelador de consultas.
source-git-commit: f6730819712ffcbe815517a4406dac7e8fb9779c
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 8%

---

# Trabalhar com o modelador de consultas {#segment-builder}

>[!CONTEXTUALHELP]
>id="dc_orchestration_querymodeler_querymessage"
>title="Modelador de consulta"
>abstract="Defina os critérios de filtragem para recipients ou qualquer outra targeting dimension do banco de dados."

O modelador de consultas simplifica o processo de filtragem do banco de dados com base em vários critérios. Além disso, o modelador de consultas pode gerenciar consultas muito complexas e longas com eficiência, oferecendo flexibilidade e precisão aprimoradas. Além disso, ele oferece suporte a filtros predefinidos em condições, permitindo que você refine suas consultas com facilidade enquanto usa expressões e operadores avançados para estratégias abrangentes de direcionamento e segmentação de público.

## Acessar o modelador de consultas

O modelador de consultas está disponível em todo contexto onde é preciso definir regras para filtrar dados.

| Uso | Exemplo |
|  ---  |  ---  |
| **Definir públicos**: especifique a população que deseja direcionar em suas composições e crie facilmente novos públicos-alvo adaptados às suas necessidades. | ![](assets/access-audience.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |
| **Personalizar atividades de fluxo de trabalho**: aplique regras em atividades de workflow, como **Split** e **Reconciliação**, para alinhar-se aos seus requisitos específicos. [Saiba mais sobre atividades de workflow](../compositions/activities/about-activities.md) | ![](assets/access-workflow.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |
| **Filtros predefinidos**: crie filtros predefinidos que servem como atalhos durante várias operações de filtragem, independentemente de você estar trabalhando com listas de dados ou formando o público para um delivery. | ![](assets/access-predefined-filter.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |
| **Personalizar listas**: crie regras personalizadas para filtrar os dados exibidos em listas como recipients, listas de deliveries, etc. | ![](assets/access-lists.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |

## Interface do modelador de consultas {#interface}

O modelador de consultas fornece uma tela central onde você cria a consulta e um painel direito fornecendo informações sobre a consulta.

![](assets/query-interface.png){zoomable="yes"}

### A tela central {#canvas}

A tela central do modelador de consultas é onde você adiciona e combina os diferentes componentes que constroem sua consulta. [Saiba como criar uma consulta](build-query.md)

A barra de ferramentas localizada no canto superior direito da tela fornece opções para manipular facilmente os componentes da consulta e navegar na tela:

* **Modo de seleção múltipla**: selecione vários componentes de filtragem para copiá-los e colá-los no local de sua escolha.
* **Girar**: Alterne a tela de desenho verticalmente.
* **Ajustar à tela**: adapte o nível de zoom da tela de desenho à sua tela.
* **Menos zoom** / **Mais zoom**: Reduza ou na tela de desenho.
* **Exibir mapa**: abre um instantâneo da tela mostrando que você está localizado.

### O painel de propriedades Regra {#rule-properties}

No lado direito, a variável **[!UICONTROL Propriedades da regra]** fornece informações sobre a consulta. Ela permite executar várias operações para verificar a consulta e garantir que ela atenda às suas necessidades. [Saiba como verificar e validar seu query](build-query.md#check-and-validate-your-query)
