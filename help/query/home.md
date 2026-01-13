---
audience: end-user
title: Visão geral do Query Modeler
description: Saiba como usar o modelador de consultas para definir regras para filtrar seu banco de dados.
exl-id: b77b9d1c-61d5-4d6d-9d82-3c72bc9c932a
source-git-commit: 93f4a16d00c71059672c4c6a51ff36debb6c9cee
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 17%

---

# Visão geral do modelador de consulta {#query-modeler}

>[!CONTEXTUALHELP]
>id="dc_orchestration_querymodeler_querymessage"
>title="Modelador de consultas"
>abstract="Defina critérios de filtragem para destinatários ou qualquer outro esquema, também conhecido como dimensão de direcionamento, do banco de dados."

O modelador de consultas simplifica o processo de filtragem do banco de dados com base em vários critérios. Além disso, o modelador de consultas pode gerenciar consultas muito complexas e longas com eficiência, oferecendo flexibilidade e precisão aprimoradas. Além disso, ele oferece suporte a filtros predefinidos em condições, permitindo que você refine suas consultas com facilidade enquanto usa expressões e operadores avançados para estratégias abrangentes de direcionamento e segmentação de público.

## Acessar o modelador de consultas

O modelador de consultas está disponível em todo contexto onde é preciso definir regras para filtrar dados.

| Uso | Exemplo |
|  ---  |  ---  |
| **Definir públicos-alvo**: especifique a população que deseja direcionar em suas composições e crie facilmente novos públicos-alvo adaptados às suas necessidades. | ![](assets/access-audience.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |
| **Personalizar atividades**: aplique regras em atividades de composição, como **Divisão** e **Reconciliação**, para alinhar-se aos seus requisitos específicos. [Saiba mais sobre atividades de composição](../compositions/activities.md) | ![](assets/access-composition.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |

## Interface do modelador de consulta {#interface}

O modelador de consultas fornece uma tela central onde você cria a consulta e um painel direito fornecendo informações sobre a consulta.

![](assets/query-interface.png){zoomable="yes"}

### A tela central {#canvas}

A tela central do modelador de consultas é onde você adiciona e combina os diferentes componentes que constroem sua consulta. [Saiba como criar uma consulta](build-query.md)

A barra de ferramentas localizada no canto superior direito da tela fornece opções para manipular facilmente os componentes da consulta e navegar na tela:

* **[!UICONTROL Modo de seleção múltipla]**: selecione vários componentes de filtragem para copiá-los e colá-los no local de sua escolha.
* **[!UICONTROL Girar]**: Alternar a tela verticalmente.
* **[!UICONTROL Ajustar à tela]**: adapte o nível de zoom da tela à sua tela.
* **[!UICONTROL Menos zoom]** / **[!UICONTROL Menos zoom]**: Menos zoom ou mais zoom na tela.
* **[!UICONTROL Exibir mapa]**: abre um instantâneo da tela mostrando que você está localizado.

### O painel de propriedades Regra {#rule-properties}

No lado direito, o painel **[!UICONTROL Propriedades da regra]** fornece informações sobre a consulta. Ela permite executar várias operações para verificar a consulta e garantir que ela atenda às suas necessidades. Esse painel é exibido ao construir uma consulta para criar um público-alvo. [Saiba como verificar e validar a sua consulta](build-query.md#check-and-validate-your-query)
