---
audience: end-user
title: Trabalhar com o modelador de consultas
description: Aprenda a trabalhar com o query modelador.
source-git-commit: 5d4bdbbb9c903e839b21d22455d870396ac1df7d
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 9%

---

# Trabalhar com o modelador de consultas {#segment-builder}

>[!CONTEXTUALHELP]
>id="dc_orchestration_querymodeler_querymessage"
>title="Modelador de consulta"
>abstract="Defina os critérios de filtragem para recipients ou qualquer outra schema, também conhecida como targeting dimension, no banco de dados."

O modelador de query simplifica o processo de filtrar o banco de dados com base em vários critérios. Além disso, o modelador query pode gerenciar consultas muito complexas e longas com eficiência, oferecendo flexibilidade e precisão aprimoradas. Além disso, oferece suporte à filtros predefinidos em condições, potencializando-o a refinar suas consultas com facilidade ao utilizar expressões e operadores avançados para estratégias abrangentes de público-alvo direcionamento e segmentação.

## Acessar o modelador query

O modelador de consultas está disponível em todo contexto onde é preciso definir regras para filtrar dados.

| Uso | Exemplo |
|  ---  |  ---  |
| **Definir públicos-alvo: especifique** a população que deseja Direcionamento em suas composição e crie novos públicos sem esforço adaptados às suas necessidades. | ![](assets/access-audience.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |
| **Personalize fluxo de Trabalho atividades**: aplique regras dentro de atividades de composição, como **Split** e **Reconciliação**, para se alinhar aos seus requisitos específicos. [Saiba mais sobre atividades de composição](../compositions/activities/about-activities.md) | ![](assets/access-composition.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |

## Interface do modelador de consulta {#interface}

O modelador query fornece uma tela central onde você build seu query e um painel direito fornecendo informações sobre seu query.

![](assets/query-interface.png){zoomable="yes"}

### A tela central {#canvas}

A query tela central do modelador é onde você adiciona e combina os diferentes componentes que constrói suas query. [Aprenda a build um query](build-query.md)

A barra de ferramentas localizada no canto superior direito da tela fornece opções para manipular facilmente os componentes query e navegar na tela:

* **Várias modo de seleção**: selecione vários componentes de filtragem para copiar e colar no local de sua escolha.
* **Girar: alterne** a tela verticalmente.
* **Ajustar à tela**: adapte o nível de zoom da tela.
* **Zoom para fora** / **Zoom em**: Zoom para fora ou para a tela.
* **** Mapa de exibição: abre um instantâneo da tela que mostra sua localização.

### O painel de propriedades da regra {#rule-properties}

No lado direito, o painel de propriedades de **[!UICONTROL Regras]** fornece informações sobre sua query. Ele permite que você realize várias operações para verificar a query e garantir que ela atenda às suas necessidades. [Aprenda a verificar e validar suas query](build-query.md#check-and-validate-your-query)
