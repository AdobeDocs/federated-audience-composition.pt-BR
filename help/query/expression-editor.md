---
audience: end-user
title: Visão geral do editor de expressão
description: Saiba como usar as funções no editor de expressão para criar uma consulta no modelador de consultas.
exl-id: abff07ef-2bc0-4e00-8957-4d59fc3bc938
TQID: https://experienceleague.adobe.com/CEu72QK6dqP1LCl8Ip1JSdZpZtubK0nyDJvj3QM75FU
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: CX Enterprise
source-git-commit: 6dc582548645bffd85b612256b79aefd613f9185
workflow-type: tm+mt
source-wordcount: '4215'
ht-degree: 9%
---
# Visão geral do editor de expressão {#expression}

A edição de uma expressão envolve a inserção manual de condições para formar uma regra. Esse modo permite usar funções avançadas, que permitem manipular os valores usados para realizar consultas específicas, como manipular datas, cadeias de caracteres, campos numéricos, classificação etc.

## Trabalhar com o editor de expressão {#edit}

O editor de expressão está disponível pelo botão **[!UICONTROL Editar expressão]** do modelador de consulta, disponível para os campos **[!UICONTROL Atributo]** e **[!UICONTROL Valor]** ao configurar uma condição personalizada.

| Acesso a partir do campo **[!UICONTROL Atributo]** | Acesso a partir do campo **[!UICONTROL Valor]** |
|  ---  |  ---  |
| ![](assets/expression-editor-attribute.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} | ![](assets/edit-expression.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |

O editor de expressão fornece:

* Um campo de entrada **(1)** no qual a expressão é definida.
* A lista de **campos (2)** disponíveis que podem ser usados na expressão e que correspondem ao esquema, também conhecido como targeting dimension, da consulta.
* **Funções auxiliares (3)**, ordenadas por categoria.

Para editar a expressão, insira uma expressão diretamente no campo de entrada. Para adicionar um campo ou uma função auxiliar, coloque o cursor na expressão em que deseja adicioná-lo e selecione o botão +.

![](assets/expression-editor.png){zoomable="yes"}

Quando a expressão estiver pronta, selecione **[!UICONTROL Confirmar]**. A expressão é exibida no campo selecionado. Para editá-lo, abra o editor de expressão e faça as alterações desejadas.

O exemplo abaixo mostra uma expressão configurada para o campo **[!UICONTROL Value]**. Para editá-lo, é necessário abrir o editor de expressão usando o botão **[!UICONTROL Editar expressão]**.

![](assets/edit-expression-value.png){zoomable="yes"}

## Funções de ajuda

A ferramenta de edição de consultas permite usar funções avançadas para fazer filtragens complexas, dependendo dos resultados desejados e dos tipos de dados manipulados. Os recursos abaixo estão disponíveis.

### Data

As funções de data são usadas para manipular valores de data ou hora.

>[!BEGINTABS]

>[!TAB Google BigQuery]

| Nome | Descrição | Sintaxe | Exemplo |
| ---- | ----------- | ------ | ------- |
| **AddYears** | Adiciona o número especificado de anos ao datetime fornecido. | AddYears(&lt;DATETIME>, &lt;NUMBER>) | AddYears(&quot;2019-12-25 15:30:00&quot;, 3) |
| **AddMonths** | Adiciona o número especificado de meses ao datetime fornecido. | AddMonths(&lt;DATETIME>, &lt;NUMBER>) | AddMonths(&quot;2019-12-25 15:30:00&quot;, 6) |
| **AddDays** | Adiciona o número especificado de dias ao datetime fornecido. | AddDays(&lt;DATETIME>, &lt;NUMBER>) | AddDays(&quot;2019-12-25 15:30:00&quot;, 10) |
| **AddHours** | Adiciona o número especificado de horas ao datetime fornecido. | AddHours(&lt;DATETIME>, &lt;NUMBER>) | AddHours(&quot;2019-12-25 15:30:00&quot;, 3) |
| **AddMinutes** | Adiciona o número especificado de minutos ao datetime fornecido. | AddMinutes(&lt;DATETIME>, &lt;NUMBER>) | AddMinutes(&quot;2019-12-25 15:30:00&quot;, 32) |
| **AddSeconds** | Adiciona o número especificado de segundos ao datetime fornecido. | AddSeconds(&lt;DATETIME>, &lt;NUMBER>) | AddSeconds(&quot;2019-12-25 15:30:00&quot;, 37) |
| **SubYears** | Subtrai o número de anos especificado para o datetime fornecido. | SubYears(&lt;DATETIME>, &lt;NUMBER>) | SubYears(&quot;2019-12-25 15:30:00&quot;, 3) |
| **SubMonths** | Subtrai o número de meses especificado para o datetime fornecido. | SubMonths(&lt;DATETIME>, &lt;NUMBER>) | SubMonths(&quot;2019-12-25 15:30:00&quot;, 6) |
| **SubDays** | Subtrai o número de dias especificado para a data e hora fornecida. | SubDays(&lt;DATETIME>, &lt;NUMBER>) | SubDays(&quot;2019-12-25 15:30:00&quot;, 10) |
| **SubHours** | Subtrai o número de horas especificado para o datetime fornecido. | SubHours(&lt;DATETIME>, &lt;NUMBER>) | SubHours(&quot;2019-12-25 15:30:00&quot;, 3) |
| **SubMinutes** | Subtrai o número especificado de minutos para o datetime fornecido. | SubMinutes(&lt;DATETIME>, &lt;NUMBER>) | SubMinutes(&quot;2019-12-25 15:30:00&quot;, 32) |
| **SubSeconds** | Subtrai o número especificado de segundos para o datetime fornecido. | SubSeconds(&lt;DATETIME>, &lt;NUMBER>) | SubSeconds(&quot;2019-12-25 15:30:00&quot;, 37) |
| **Year** | Extrai o ano do objeto datetime fornecido. | Year(&lt;DATETIME>) | Year(&quot;12-15-2019 15:30:00&quot;) |
| **Month** | Extrai o mês do objeto datetime fornecido. | Month(&lt;DATETIME>) | Month(&quot;12-15-2019 15:30:00&quot;) |
| **Day** | Extrai o dia do objeto datetime fornecido. | Day(&lt;DATETIME>) | Day(&quot;12-15-2019 15:30:00&quot;) |
| **DayOfYear** | Extrai o dia do ano do objeto datetime fornecido. Por exemplo, se o datetime fornecido for 2 de fevereiro, ele retornará 33. | DayOfYear(&lt;DATETIME>) | DayOfYear(&quot;12-15-2019 15:30:00&quot;) |
| **WeekDay** | Extrai o dia da semana do objeto datetime fornecido, como um número de 0 a 6, com 0 representando domingo. | Year(&lt;DATETIME>) | Year(&quot;12-15-2019 15:30:00&quot;) |
| **Hour** | Extrai o valor de hora do objeto datetime fornecido. | Year(&lt;DATETIME>) | Year(&quot;12-15-2019 15:30:00&quot;) |
| **Minute** | Extrai o valor de minuto do objeto datetime fornecido. | Year(&lt;DATETIME>) | Year(&quot;12-15-2019 15:30:00&quot;) |
| **Second** | Extrai o segundo valor do objeto datetime fornecido. | Year(&lt;DATETIME>) | Year(&quot;12-15-2019 15:30:00&quot;) |
| **YearsDiff** | Localiza a diferença entre os datetimes fornecidos, com uma granularidade de anos. | YearsDiff(&lt;DATETIME>, &lt;DATETIME>) | YearsDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **MonthsDiff** | Localiza a diferença entre os datetimes fornecidos, com uma granularidade de meses. | MonthsDiff(&lt;DATETIME>, &lt;DATETIME>) | MonthsDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **DaysDiff** | Localiza a diferença entre os datetimes fornecidos, com uma granularidade de dias. | DaysDiff(&lt;DATETIME>, &lt;DATETIME>) | DaysDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **HoursDiff** | Localiza a diferença entre os datetimes fornecidos, com uma granularidade de horas. | HoursDiff(&lt;DATETIME>, &lt;DATETIME>) | HoursDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **MinutesDiff** | Localiza a diferença entre os datetimes fornecidos, com uma granularidade de minutos. | MinutesDiff(&lt;DATETIME>, &lt;DATETIME>) | MinutesDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **SecondsDiff** | Localiza a diferença entre os datetimes fornecidos, com uma granularidade de segundos. | SecondsDiff(&lt;DATETIME>, &lt;DATETIME>) | SecondsDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **YearsOld** | Encontra a diferença entre o datetime fornecido e o presente, com uma granularidade de anos. | YearsOld(&lt;DATETIME>) | YearsOld(&quot;2019-12-25 15:30:00&quot;) |
| **MonthsOld** | Localiza a diferença entre o datetime fornecido e o presente, com uma granularidade de meses. | MonthsOld(&lt;DATETIME>) | MonthsOld(&quot;2019-12-25 15:30:00&quot;) |
| **DaysOld** | Localiza a diferença entre o datetime fornecido e o presente, com uma granularidade de dias. | DaysOld(&lt;DATETIME>) | DaysOld(&quot;2019-12-25 15:30:00&quot;) |
| **GetDate** | Obter a data atual do servidor. | GetDate() | GetDate() |
| **DateOnly** | Corta a data e hora somente para o ano, mês e dia. | DateOnly(&lt;DATETIME>) | DateOnly(&quot;2019-12-25 15:30:00&quot;) |
| **ToDate** | Converte o campo em um campo de data. | ToDate(&lt;DATETIME>) | ToDate(&quot;2019-12-25 15:30:00&quot;) |
| **ToDateTime** | Converte o campo em um campo de data e hora. | ToDateTime(&lt;DATE>) | ToDateTime(&quot;2019-12-25 15:30:00&quot;) |
| **ToTimestamp** | Converte o campo em um campo de carimbo de data e hora. | ToTimestamp(&lt;DATETIME>) | ToTimestamp(&quot;2019-12-25 15:30:00&quot;) |
| **Oldest** | Retorna a data mais antiga entre os dois fornecidos. | Oldest(&lt;DATETIME>, &lt;DATETIME>) | Oldest(&quot;2015-02-13 11:59:59&quot;, &quot;2016-04-13 19:28:14&quot;) |
| **TruncDate** | Corta o datetime para a unidade mais próxima, com base no valor numérico fornecido. Se o valor numérico for igual a 60, ele será truncado no minuto mais próximo. Se o valor numérico for igual a 3600, ele será truncado na hora mais próxima. Se o valor numérico for igual a 86400, ele será truncado no dia mais próximo. Caso contrário, ele será truncado no segundo mais próximo. | TruncDate(&lt;DATETIME>, &lt;NUMBER>) | TruncDate(&quot;13/04/2016 19:28:14&quot;, 3600) |
| **TruncDateTZ** | Corta o datetime para a unidade mais próxima, com base no valor numérico fornecido, e define o datetime para o fuso horário especificado. Se o valor numérico for igual a 60, ele será truncado no minuto mais próximo. Se o valor numérico for igual a 3600, ele será truncado na hora mais próxima. Se o valor numérico for igual a 86400, ele será truncado no dia mais próximo. | TruncDateTZ(&lt;DATETIME>, &lt;NUMBER>, &lt;TIMEZONE>) | TruncDateTZ(&quot;2016-04-13 19:28:14&quot;, 3600, &quot;América/Los_Angeles&quot;) |
| **TruncTime** | Define o datetime como 1º de janeiro de 2000 e arredonda o restante do datetime para a unidade mais próxima, com base no valor numérico fornecido.Se o valor numérico for igual a 60, ele será truncado no minuto mais próximo. Se o valor numérico for igual a 3600, ele será truncado na hora mais próxima. | TruncTime(&lt;DATETIME>, &lt;NUMBER>) | TruncTime(&quot;13/04/2016 19:28:14&quot;, 3600) |
| **TruncQuarter** | Corta o datetime para a primeira data do trimestre mais próximo. | TruncQuarter(&lt;DATETIME>) | TruncQuarter(&quot;13/04/2016 19:28:14&quot;) |
| **TruncYear** | Corta o datetime para a primeira data no ano mais próximo. | TruncYear(&lt;DATETIME>) | TruncYear(&quot;13/04/2016 19:28:14&quot;) |
| **TruncWeek** | Corta o datetime para o domingo da semana mais próxima. | TruncWeek(&lt;DATETIME>) | TruncWeek(&quot;13/04/2016 19:28:14&quot;) |

>[!TAB Snowflake]

| Nome | Descrição | Sintaxe | Exemplo |
| ---- | ----------- | ------ | ------- |
| **AddYears** | Adiciona o número especificado de anos ao datetime fornecido. | AddYears(&lt;DATETIME>, &lt;NUMBER>) | AddYears(&quot;2019-12-25 15:30:00&quot;, 3) |
| **AddMonths** | Adiciona o número especificado de meses ao datetime fornecido. | AddMonths(&lt;DATETIME>, &lt;NUMBER>) | AddMonths(&quot;2019-12-25 15:30:00&quot;, 6) |
| **AddDays** | Adiciona o número especificado de dias ao datetime fornecido. | AddDays(&lt;DATETIME>, &lt;NUMBER>) | AddDays(&quot;2019-12-25 15:30:00&quot;, 10) |
| **AddHours** | Adiciona o número especificado de horas ao datetime fornecido. | AddHours(&lt;DATETIME>, &lt;NUMBER>) | AddHours(&quot;2019-12-25 15:30:00&quot;, 3) |
| **AddMinutes** | Adiciona o número especificado de minutos ao datetime fornecido. | AddMinutes(&lt;DATETIME>, &lt;NUMBER>) | AddMinutes(&quot;2019-12-25 15:30:00&quot;, 32) |
| **AddSeconds** | Adiciona o número especificado de segundos ao datetime fornecido. | AddSeconds(&lt;DATETIME>, &lt;NUMBER>) | AddSeconds(&quot;2019-12-25 15:30:00&quot;, 37) |
| **SubYears** | Subtrai o número de anos especificado para o datetime fornecido. | SubYears(&lt;DATETIME>, &lt;NUMBER>) | SubYears(&quot;2019-12-25 15:30:00&quot;, 3) |
| **SubMonths** | Subtrai o número de meses especificado para o datetime fornecido. | SubMonths(&lt;DATETIME>, &lt;NUMBER>) | SubMonths(&quot;2019-12-25 15:30:00&quot;, 6) |
| **SubDays** | Subtrai o número de dias especificado para a data e hora fornecida. | SubDays(&lt;DATETIME>, &lt;NUMBER>) | SubDays(&quot;2019-12-25 15:30:00&quot;, 10) |
| **SubHours** | Subtrai o número de horas especificado para o datetime fornecido. | SubHours(&lt;DATETIME>, &lt;NUMBER>) | SubHours(&quot;2019-12-25 15:30:00&quot;, 3) |
| **SubMinutes** | Subtrai o número especificado de minutos para o datetime fornecido. | SubMinutes(&lt;DATETIME>, &lt;NUMBER>) | SubMinutes(&quot;2019-12-25 15:30:00&quot;, 32) |
| **SubSeconds** | AdSubtracta o número especificado de segundos para o datetime fornecido. | SubSeconds(&lt;DATETIME>, &lt;NUMBER>) | SubSeconds(&quot;2019-12-25 15:30:00&quot;, 37) |
| **Year** | Extrai o ano do objeto datetime fornecido. | Year(&lt;DATETIME>) | Year(&quot;12-15-2019 15:30:00&quot;) |
| **Month** | Extrai o mês do objeto datetime fornecido. | Month(&lt;DATETIME>) | Month(&quot;12-15-2019 15:30:00&quot;) |
| **Day** | Extrai o dia do objeto datetime fornecido. | Day(&lt;DATETIME>) | Day(&quot;12-15-2019 15:30:00&quot;) |
| **DayOfYear** | Extrai o dia do ano do objeto datetime fornecido. Por exemplo, se o datetime fornecido for 2 de fevereiro, ele retornará 33. | DayOfYear(&lt;DATETIME>) | DayOfYear(&quot;12-15-2019 15:30:00&quot;) |
| **WeekDay** | Extrai o dia da semana do objeto datetime fornecido, como um número de 1 a 7, com 1 representando domingo. | Year(&lt;DATETIME>) | Year(&quot;12-15-2019 15:30:00&quot;) |
| **Hour** | Extrai o valor de hora do objeto datetime fornecido. | Year(&lt;DATETIME>) | Year(&quot;12-15-2019 15:30:00&quot;) |
| **Minute** | Extrai o valor de minuto do objeto datetime fornecido. | Year(&lt;DATETIME>) | Year(&quot;12-15-2019 15:30:00&quot;) |
| **Second** | Extrai o segundo valor do objeto datetime fornecido. | Year(&lt;DATETIME>) | Year(&quot;12-15-2019 15:30:00&quot;) |
| **YearsDiff** | Localiza a diferença entre os datetimes fornecidos, com uma granularidade de anos. | YearsDiff(&lt;DATETIME>, &lt;DATETIME>) | YearsDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **MonthsDiff** | Localiza a diferença entre os datetimes fornecidos, com uma granularidade de meses. | MonthsDiff(&lt;DATETIME>, &lt;DATETIME>) | MonthsDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **DaysDiff** | Localiza a diferença entre os datetimes fornecidos, com uma granularidade de dias. | DaysDiff(&lt;DATETIME>, &lt;DATETIME>) | DaysDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **HoursDiff** | Localiza a diferença entre os datetimes fornecidos, com uma granularidade de horas. | HoursDiff(&lt;DATETIME>, &lt;DATETIME>) | HoursDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **MinutesDiff** | Localiza a diferença entre os datetimes fornecidos, com uma granularidade de minutos. | MinutesDiff(&lt;DATETIME>, &lt;DATETIME>) | MinutesDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **SecondsDiff** | Localiza a diferença entre os datetimes fornecidos, com uma granularidade de segundos. | SecondsDiff(&lt;DATETIME>, &lt;DATETIME>) | SecondsDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **MonthsOld** | Localiza a diferença entre o datetime fornecido e o presente, com uma granularidade de meses. | MonthsOld(&lt;DATETIME>) | MonthsOld(&quot;2019-12-25 15:30:00&quot;) |
| **DaysOld** | Localiza a diferença entre o datetime fornecido e o presente, com uma granularidade de dias. | DaysOld(&lt;DATETIME>) | DaysOld(&quot;2019-12-25 15:30:00&quot;) |
| **GetDate** | Obter a data atual do servidor. | GetDate() | GetDate() |
| **DateOnly** | Corta a data e hora somente para o ano, mês e dia. | DateOnly(&lt;DATETIME>) | DateOnly(&quot;2019-12-25 15:30:00&quot;) |
| **ToDate** | Converte o campo em um campo de data. | ToDate(&lt;DATETIME>) | ToDate(&quot;2019-12-25 15:30:00&quot;) |
| **ToDateTime** | Converte o campo em um campo de data e hora. | ToDateTime(&lt;DATE>) | ToDateTime(&quot;2019-12-25 15:30:00&quot;) |
| **ToTimestamp** | Converte o campo em um campo de carimbo de data e hora. | ToTimestamp(&lt;DATETIME>) | ToTimestamp(&quot;2019-12-25 15:30:00&quot;) |
| **Oldest** | Retorna a data mais antiga entre os dois fornecidos. | Oldest(&lt;DATETIME>, &lt;DATETIME>) | Oldest(&quot;2015-02-13 11:59:59&quot;, &quot;2016-04-13 19:28:14&quot;) |
| **TruncDate** | Corta o datetime para a unidade mais próxima, com base no valor numérico fornecido. Se o valor numérico for igual a 60, ele será truncado no minuto mais próximo. Se o valor numérico for igual a 3600, ele será truncado na hora mais próxima. Se o valor numérico for igual a 86400, ele será truncado no dia mais próximo. Caso contrário, ele será truncado no segundo mais próximo. | TruncDate(&lt;DATETIME>, &lt;NUMBER>) | TruncDate(&quot;13/04/2016 19:28:14&quot;, 3600) |
| **TruncDateTZ** | Corta o datetime para a unidade mais próxima, com base no valor numérico fornecido, e define o datetime para o fuso horário especificado. Se o valor numérico for igual a 60, ele será truncado no minuto mais próximo. Se o valor numérico for igual a 3600, ele será truncado na hora mais próxima. Se o valor numérico for igual a 86400, ele será truncado no dia mais próximo. | TruncDateTZ(&lt;DATETIME>, &lt;NUMBER>, &lt;TIMEZONE>) | TruncDateTZ(&quot;2016-04-13 19:28:14&quot;, 3600, &quot;América/Los_Angeles&quot;) |
| **TruncTime** | Define o datetime como 1º de janeiro de 2000 e arredonda o restante do datetime para a unidade mais próxima, com base no valor numérico fornecido.Se o valor numérico for igual a 60, ele será truncado no minuto mais próximo. Se o valor numérico for igual a 3600, ele será truncado na hora mais próxima. | TruncTime(&lt;DATETIME>, &lt;NUMBER>) | TruncTime(&quot;13/04/2016 19:28:14&quot;, 3600) |
| **TruncQuarter** | Corta o datetime para a primeira data do trimestre mais próximo. | TruncQuarter(&lt;DATETIME>) | TruncQuarter(&quot;13/04/2016 19:28:14&quot;) |
| **TruncYear** | Corta o datetime para a primeira data no ano mais próximo. | TruncYear(&lt;DATETIME>) | TruncYear(&quot;13/04/2016 19:28:14&quot;) |
| **TruncWeek** | Corta o datetime para o domingo da semana mais próxima. | TruncWeek(&lt;DATETIME>) | TruncWeek(&quot;13/04/2016 19:28:14&quot;) |
| **ConvertNTZ** | Converte um carimbo de data e hora sem fuso horário em um carimbo de data e hora com fuso horário. O fuso horário anexado será o fuso horário da conta externa. | ConvertNTZ(&lt;DATETIME>) | ConvertNTZ(&quot;24/06/2024 14:43:49&quot;) |

>[!ENDTABS]

>[!NOTE]
>
>Observe que a função **Dateonly** considera o fuso horário do servidor e não do operador.

### Geomarketing

As funções de geomarketing são usadas para manipular valores geográficos.

>[!BEGINTABS]

>[!TAB Google BigQuery]

| Nome | Descrição | Sintaxe | Exemplo |
| ---- | ----------- | ------ | ------- |
| **Distance** | Retorna a distância entre dois pontos definidos por sua longitude e latitude em graus, como um duplo. | Distance(&lt;NUMBER>, &lt;NUMBER>, &lt;NUMBER>, &lt;NUMBER>) | Distance(40,345, 39,2345, -35,5834, 34,599) |

>[!TAB Snowflake]

| Nome | Descrição | Sintaxe | Exemplo |
| ---- | ----------- | ------ | ------- |
| **Distance** | Retorna a distância entre dois pontos definidos por sua longitude e latitude em graus, como um duplo. | Distance(&lt;NUMBER>, &lt;NUMBER>, &lt;NUMBER>, &lt;NUMBER>) | Distance(40,345, 39,2345, -35,5834, 34,599) |

>[!ENDTABS]

### Numérico

As funções numéricas são usadas para converter textos em números.

>[!BEGINTABS]

>[!TAB Google BigQuery]

| Nome | Descrição | Sintaxe | Exemplo |
| ---- | ----------- | ------ | ------- |
| **Mod** | Retorna o restante do primeiro número dividido pelo segundo número. | Mod(&lt;NUMBER>, &lt;NUMBER>) | Mod (3, 2) |
| **Percent** | Calcula a porcentagem do primeiro número em relação ao segundo número. | Percent(&lt;NUMBER>, &lt;NUMBER>) | Percentual(1, 2) |
| **Random** | Retorna um número aleatório entre 0 (inclusivo) e 1 (exclusivo). | Random() | Aleatório () |
| **Round** | Retorna o número fornecido para a casa decimal solicitada mais próxima. | Round(&lt;NÚMERO>, &lt;NÚMERO>) | Round(4.5394, 2) |
| **ToDouble** | Converte o número fornecido em um duplo. | ToDouble(&lt;NUMBER>) | ToDouble(5) |
| **ToInteger** | Converte o número fornecido em um inteiro. | ToInteger(&lt;NUMBER>) | ToInteger(45) |
| **ToInt64** | Converte o número fornecido em um inteiro de 64 bits. | ToInt64(&lt;NUMBER>) | ToInt64(493) |
| **Trunc** | Trunca o número fornecido para o número solicitado de casas decimais. | Trunc(&lt;NUMBER>, &lt;NUMBER>) | Trunc(36.9348934, 3) |

>[!TAB Snowflake]

| Nome | Descrição | Sintaxe | Exemplo |
| ---- | ----------- | ------ | ------- |
| **Mod** | Retorna o restante do primeiro número dividido pelo segundo número. | Mod(&lt;NUMBER>, &lt;NUMBER>) | Mod (3, 2) |
| **Percent** | Calcula a porcentagem do primeiro número em relação ao segundo número. | Percent(&lt;NUMBER>, &lt;NUMBER>) | Percentual(1, 2) |
| **Random** | Retorna um número aleatório entre 0 (inclusivo) e 1 (exclusivo). | Random() | Aleatório () |
| **ToDouble** | Converte o número fornecido em um duplo. | ToDouble(&lt;NUMBER>) | ToDouble(5) |
| **ToInteger** | Converte o número fornecido em um inteiro. | ToInteger(&lt;NUMBER>) | ToInteger(45) |
| **ToInt64** | Converte o número fornecido em um inteiro de 64 bits. | ToInt64(&lt;NUMBER>) | ToInt64(493) |
| **Trunc** | Trunca o número fornecido para o número solicitado de casas decimais. | Trunc(&lt;NUMBER>, &lt;NUMBER>) | Trunc(36.9348934, 3) |

>[!ENDTABS]

### Outros

Esta tabela contém as demais funções disponíveis.

>[!BEGINTABS]

>[!TAB Google BigQuery]

| Nome | Descrição | Sintaxe | Exemplo |
| ---- | ----------- | ------ | ------- |
| **Case** | Retorna o primeiro valor se a expressão for verdadeira. Caso contrário, retorna o segundo valor. | Case(When(&lt;EXPRESSÃO> &lt;VALOR>), Else(&lt;VALOR>)) | Case(Quando(a > b, &quot;sim&quot;), Else(&quot;não&quot;)) |
| **When** | Usado como parte da função Case. Usado para verificar a expressão em maiúsculas e minúsculas. | When(&lt;EXPRESSÃO> &lt;VALOR>) | Quando(a > b, &quot;sim&quot;) |
| **Else** | Usado como parte da função Case. Usado para escolher a outra opção, se a expressão When for falsa. | Else(&lt;VALOR>) | Senão (&quot;não&quot;) |
| **Coalesce** | Retorna o primeiro valor não nulo. | Coalesce(&lt;VALUE>, &lt;VALUE>) | União (&quot;&quot;, &quot;string&quot;) |
| **Decode** | Retorna a primeira opção se os valores forem iguais. Retorna a segunda opção se os valores não forem iguais. | Decode(&lt;VALUE>, &lt;VALUE>, &lt;VALUE>, &lt;VALUE>) | Decode( 1, 2, &quot;verdadeiro&quot;, &quot;falso&quot;) |
| **GetEmailDomain** | Extrai o domínio do endereço de email fornecido. | GetEmailDomain(&lt;CADEIA DE CARACTERES>) | GetEmailDomain(&quot;`sample@example.com`&quot;) |
| **Iif** | Retorna a primeira opção se a condição for verdadeira e retorna a segunda opção se a condição for falsa. | Iif(&lt;CONDIÇÃO>, &lt;VALOR>, &lt;VALOR>) | Iif(10 &lt; 20, &quot;true&quot;, &quot;false&quot;) |
| **IsEmptyString** | Retorna a primeira opção se a cadeira de caracteres estiver vazia. Caso contrário, retorna a segunda opção. | IsEmptyString( &lt;CADEIA DE CARACTERES> ,&lt;VALOR>, &lt;VALOR>) | IsEmptyString(&quot;string&quot;, &quot;sim&quot;, &quot;não&quot;) |
| **NewUUID** | Gera um novo UUID exclusivo. | NewUUID() | NewUUID() |
| **NoNull** | Retorna a cadeia de caracteres fornecida, se não estiver vazia, e retorna uma cadeia de caracteres vazia, se a cadeia de caracteres fornecida estiver vazia. | NoNull(&lt;STRING>) | NoNull(&quot;teste&quot;) |
| **IsBitSet** | Executa um bit a bit e (&amp;) nos números fornecidos. Isso permite verificar se o bit dentro do primeiro parâmetro está definido na posição fornecida no segundo parâmetro. | IsBitSet(&lt;NUMBER>, &lt;NUMBER>) | IsBitSet(5, 3) |
| **ClearBit** | Isso permite que você limpe o bit dentro do primeiro parâmetro na posição fornecida no segundo parâmetro. | ClearBit(&lt;NUMBER>, &lt;NUMBER>) | |
| **SetBit** | Executa um bit a bit ou (\|) nos números fornecidos. Isso permite que você defina o bit dentro do primeiro parâmetro é definido na posição fornecida no segundo parâmetro. | SetBit(&lt;NUMBER>, &lt;NUMBER>) | SetBit(5, 3) |
| **RowId** | Retorna o número da linha. | RowId() | RowId() |
| **ToBoolean** | Converte o valor em um booleano. | ToBoolean(&lt;VALUE>) | ToBoolean(a=b) |

>[!TAB Snowflake]

| Nome | Descrição | Sintaxe | Exemplo |
| ---- | ----------- | ------ | ------- |
| **Case** | Retorna o primeiro valor se a expressão for verdadeira. Caso contrário, retorna o segundo valor. | Case(When(&lt;EXPRESSÃO> &lt;VALOR>), Else(&lt;VALOR>)) | Case(Quando(a > b, &quot;sim&quot;), Else(&quot;não&quot;)) |
| **When** | Usado como parte da função Case. Usado para verificar a expressão em maiúsculas e minúsculas. | When(&lt;EXPRESSÃO> &lt;VALOR>) | Quando(a > b, &quot;sim&quot;) |
| **Else** | Usado como parte da função Case. Usado para escolher a outra opção, se a expressão When for falsa. | Else(&lt;VALOR>) | Senão (&quot;não&quot;) |
| **GetEmailDomain** | Extrai o domínio do endereço de email fornecido. | GetEmailDomain(&lt;CADEIA DE CARACTERES>) | GetEmailDomain(&quot;`sample@example.com`&quot;) |
| **Iif** | Retorna a primeira opção se a condição for verdadeira e retorna a segunda opção se a condição for falsa. | Iif(&lt;CONDIÇÃO>, &lt;VALOR>, &lt;VALOR>) | Iif(10 &lt; 20, &quot;true&quot;, &quot;false&quot;) |
| **IsEmptyString** | Retorna a primeira opção se a cadeira de caracteres estiver vazia. Caso contrário, retorna a segunda opção. | IsEmptyString( &lt;CADEIA DE CARACTERES> ,&lt;VALOR>, &lt;VALOR>) | IsEmptyString(&quot;string&quot;, &quot;sim&quot;, &quot;não&quot;) |
| **ToBoolean** | Retorna 1 se o valor for verdadeiro. Retorna 0 se o valor for falso. | ToBoolean(&lt;VALUE>) | ToBoolean(a=b) |
| **ToBooleanType** | Converte o valor em um booleano. | ToBooleanType(&lt;VALUE>) | ToBooleanType(a=b) |
| **IsBitSet** | Executa um bit a bit e (&amp;) nos números fornecidos. Isso permite verificar se o bit dentro do primeiro parâmetro está definido na posição fornecida no segundo parâmetro. | IsBitSet(&lt;NUMBER>, &lt;NUMBER>) | IsBitSet(5, 3) |
| **ClearBit** | Isso permite que você limpe o bit dentro do primeiro parâmetro na posição fornecida no segundo parâmetro. | ClearBit(&lt;NUMBER>, &lt;NUMBER>) | |
| **SetBit** | Executa um bit a bit ou (\|) nos números fornecidos. Isso permite que você defina o bit dentro do primeiro parâmetro é definido na posição fornecida no segundo parâmetro. | SetBit(&lt;NUMBER>, &lt;NUMBER>) | SetBit(5, 3) |
| **RowId** | Retorna o número da linha. | RowId() | RowId() |
| **NewUUID** | Gera um novo UUID exclusivo. | NewUUID() | NewUUID() |
| **NoNull** | Retorna a cadeia de caracteres fornecida, se não estiver vazia, e retorna uma cadeia de caracteres vazia, se a cadeia de caracteres fornecida estiver vazia. | NoNull(&lt;STRING>) | NoNull(&quot;teste&quot;) |
| **AESEncrypt** | Criptografa a string fornecida com o tipo de criptografia AES. | AESEncrypt() | AESEncrypt(&quot;Olá&quot;) |
| **ConstrutorDeObjetos** | Cria um objeto com base nos pares de chave/valor fornecidos. | ObjectConstruct(&lt;STRING>, &lt;STRING>) | ObjectConstruct(&quot;chave&quot;, &quot;valor&quot;) |

>[!ENDTABS]

### String

As funções de string são usadas para manipular um conjunto de strings.

>[!BEGINTABS]

>[!TAB Google BigQuery]

| Nome | Descrição | Sintaxe | Exemplo |
| ---- | ----------- | ------ | ------- |
| **AllNonNull2** | Pega duas sequências de caracteres e verifica se todas elas não são nulas e não estão vazias. | AllNonNull2(&lt;STRING>, &lt;STRING>) | AllNonNull2(&quot;&quot;, &quot;string2&quot;) |
| **AllNonNull3** | Pega três strings e verifica se todas elas não são nulas nem estão vazias | AllNonNull3(&lt;STRING>, &lt;STRING>, &lt;STRING>) | AllNonNull3(&quot;&quot;, &quot;um&quot;, &quot;três&quot;) |
| **Ascii** | Pega uma string e retorna o resultado . | Ascii(&lt;CADEIA DE CARACTERES>) | Ascii (&quot;foo&quot;) |
| **Char** | Obtém uma matriz de pontos de código Unicode e retorna a cadeia de caracteres resultante. | Char(&lt;ARRAY>) | Char([65, 68, 79, 66, 69]) |
| **Charindex** | Localiza a primeira ocorrência da substring especificada dentro da string principal. | Charindex(&lt;STRING>, &lt;SUBSTRING>) | Charindex (&quot;bar@example.com&quot;, &quot;@&quot;) |
| **dataLength** | Retorna o número de bytes na string. | dataLength(&lt;STRING>) | dataLength(&quot;Minha cadeia de caracteres&quot;) |
| **GetLine** | Retorna a linha solicitada da cadeia de caracteres fornecida. | GetLine(&lt;STRING>, &lt;NUMBER>) | GetLine(multilinestring, 5) |
| **IfEquals** | Pega quatro cadeias de caracteres e retorna a terceira se as duas primeiras forem iguais, e retorna a quarta se as duas primeiras não forem iguais. | IfEquals(&lt;STRING>, &lt;STRING>, &lt;STRING>, &lt;STRING>) | IfEquals(&quot;a&quot;, &quot;a&quot;, &quot;yes&quot;, &quot;no&quot;) |
| **IsMemoNull** | Retorna 1 se a string for nula, caso contrário, retorna 0. | IsMemoNull(&lt;STRING>) | IsMemoNull(&quot;Olá&quot;) |
| **JuxtWords** | Pega duas cordas e as combina em uma única. Se necessário, os espaços entre as cadeias de caracteres são adicionados. | JuxtWords(&lt;STRING>, &lt;STRING>) | JuxtWords(&quot;Olá&quot;, &quot;Mundo&quot;) |
| **JuxtWords3** | Pega três strings e as combina em uma única string. Se necessário, os espaços entre as cadeias de caracteres são adicionados. | JuxtWords3(&lt;STRING>, &lt;STRING>, &lt;STRING>) | JuxtWords3(&quot;Olá&quot;, &quot;Novo&quot;, &quot;Mundo&quot;) |
| **Left** | Pega uma string e retorna os caracteres mais à esquerda, conforme especificado. | Left(&lt;STRING>, &lt;NUMBER>) | Left(&quot;Substring&quot;, 3) |
| **Length** | Retorna o comprimento da cadeira de caracteres. | Length(&lt;CADEIA DE CARACTERES>) | Length(&quot;MyString&quot;) |
| **Md5Digest** | Converte a string com hash MD5 em sua representação hexadecimal. | Md5Digest(&lt;CADEIA DE CARACTERES>) | Md5Digest(&quot;Cadeia De Caracteres&quot;) |
| **MemoContains** | Verifica se a cadeia de caracteres contém a subsequência fornecida. | MemoContains(&lt;STRING>, &lt;STRING>) | MemoContains(&quot;string&quot;, &quot;str&quot;) |
| **Right** | Pega uma sequência de caracteres e retorna os caracteres mais à direita, conforme especificado. | Right(&lt;STRING>, &lt;NUMBER>) | À Direita (&quot;Substring&quot;, 3) |
| **Smart** | Retorna a cadeira de caracteres com a primeira letra de cada palavra em maiúscula. | Smart(&lt;CADEIA DE CARACTERES>) | Smart(&quot;olá mundo&quot;) |
| **Substring** | Pega uma sequência de caracteres e retorna uma parte da sequência fornecida, com base nas posições fornecidas. | Substring(&lt;STRING>, &lt;LEFT_NUMBER>, RIGHT_NUMBER>) | Substring(&quot;Substring&quot;, 3, 5) |
| **Sha256Digest** | Converte a string com hash SHA256 em sua representação hexadecimal. | Sha256Digest(&lt;CADEIA DE CARACTERES>) | Sha256Digest(&quot;string&quot;) |
| **Sha512Digest** | Converte a string com hash SHA512 em sua representação hexadecimal. | Sha512Digest(&lt;CADEIA DE CARACTERES>) | Sha512Digest(&quot;string&quot;) |
| **ToString** | Retorna o valor como uma string. | ToString(&lt;VALOR>) | ToString(123) |

>[!TAB Snowflake]

| Nome | Descrição | Sintaxe | Exemplo |
| ---- | ----------- | ------ | ------- |
| **AllNonNull2** | Pega duas sequências de caracteres e verifica se todas elas não são nulas e não estão vazias. | AllNonNull2(&lt;STRING>, &lt;STRING>) | AllNonNull2(&quot;&quot;, &quot;string2&quot;) |
| **AllNonNull3** | Pega três strings e verifica se todas elas não são nulas nem estão vazias | AllNonNull3(&lt;STRING>, &lt;STRING>, &lt;STRING>) | AllNonNull3(&quot;&quot;, &quot;um&quot;, &quot;três&quot;) |
| **Char** | Obtém uma matriz de pontos de código Unicode e retorna a cadeia de caracteres resultante. | Char(&lt;ARRAY>) | Char([65, 68, 79, 66, 69]) |
| **Charindex** | Localiza a primeira ocorrência da substring especificada dentro da string principal. | Charindex(&lt;STRING>, &lt;SUBSTRING>) | Charindex (&quot;bar@example.com&quot;, &quot;@&quot;) |
| **dataLength** | Retorna o número de bytes na string. | dataLength(&lt;STRING>) | dataLength(&quot;Minha cadeia de caracteres&quot;) |
| **GetLine** | Retorna a linha solicitada da cadeia de caracteres fornecida. | GetLine(&lt;STRING>, &lt;NUMBER>) | GetLine(multilinestring, 5) |
| **IfEquals** | Pega quatro cadeias de caracteres e retorna a terceira se as duas primeiras forem iguais, e retorna a quarta se as duas primeiras não forem iguais. | IfEquals(&lt;STRING>, &lt;STRING>, &lt;STRING>, &lt;STRING>) | IfEquals(&quot;a&quot;, &quot;a&quot;, &quot;yes&quot;, &quot;no&quot;) |
| **IsMemoNull** | Retorna 1 se a string for nula, caso contrário, retorna 0. | IsMemoNull(&lt;STRING>) | IsMemoNull(&quot;Olá&quot;) |
| **JuxtWords** | Pega duas cordas e as combina em uma única. Se necessário, os espaços entre as cadeias de caracteres são adicionados. | JuxtWords(&lt;STRING>, &lt;STRING>) | JuxtWords(&quot;Olá&quot;, &quot;Mundo&quot;) |
| **JuxtWords3** | Pega três strings e as combina em uma única string. Se necessário, os espaços entre as cadeias de caracteres são adicionados. | JuxtWords3(&lt;STRING>, &lt;STRING>, &lt;STRING>) | JuxtWords3(&quot;Olá&quot;, &quot;Novo&quot;, &quot;Mundo&quot;) |
| **Left** | Pega uma string e retorna os caracteres mais à esquerda, conforme especificado. | Left(&lt;STRING>, &lt;NUMBER>) | Left(&quot;Substring&quot;, 3) |
| **Length** | Retorna o comprimento da cadeira de caracteres. | Length(&lt;CADEIA DE CARACTERES>) | Length(&quot;MyString&quot;) |
| **Linha** | Retorna a linha numerada especificada da cadeia de caracteres. | Line(&lt;STRING>, &lt;NUMBER>) | Linha (multilinestring, 5) |
| **Md5Digest** | Converte a string com hash MD5 em sua representação hexadecimal. | Md5Digest(&lt;CADEIA DE CARACTERES>) | Md5Digest(&quot;Cadeia De Caracteres&quot;) |
| **Replace** | Pega uma sequência de caracteres e substitui todas as instâncias da subsequência por uma subsequência de substituição. | Replace(&lt;STRING>, &lt;STRING&amp;gt, &lt;STRING&amp;gt) | Replace(&quot;Capitão Steve&quot;, &quot;Capitão&quot;, &quot;Engenheiro&quot;) |
| **Right** | Pega uma sequência de caracteres e retorna os caracteres mais à direita, conforme especificado. | Right(&lt;STRING>, &lt;NUMBER>) | À Direita (&quot;Substring&quot;, 3) |
| **Sha256Digest** | Converte a string com hash SHA256 em sua representação hexadecimal. | Sha256Digest(&lt;CADEIA DE CARACTERES>) | Sha256Digest(&quot;string&quot;) |
| **Sha512Digest** | Converte a string com hash SHA512 em sua representação hexadecimal. | Sha512Digest(&lt;CADEIA DE CARACTERES>) | Sha512Digest(&quot;string&quot;) |
| **Smart** | Retorna a cadeira de caracteres com a primeira letra de cada palavra em maiúscula. | Smart(&lt;CADEIA DE CARACTERES>) | Smart(&quot;olá mundo&quot;) |
| **ToString** | Retorna o valor como uma string. | ToString(&lt;VALOR>) | ToString(123) |

>[!ENDTABS]

### Janela

>[!BEGINTABS]

>[!TAB Google BigQuery]

| Nome | Descrição | Sintaxe | Exemplo |
| ---- | ----------- | ------ | ------- |
| **RowNum** | Retorna uma sequência de linhas com base na partição da tabela e na sequência de classificação. | RowNum(PartitionBy(&lt;EXPRESSION>), OrderBy(&lt;EXPRESSION>)) | RowNum(PartitionBy(division), OrderBy(time)) |
| **PartitionBy** | Separa as linhas de entrada em diferentes partições, com base na expressão fornecida. | PartitionBy(&lt;EXPRESSION>) | PartitionBy(divisão) |
| **OrderBy** | Classifica o resultado da partição. | OrderBy(&lt;EXPRESSION>) | OrderBy(age) |
| **Desc** | Permite que o OrderBy seja classificado por ordem decrescente, em vez de crescente. | Desc(OrderBy(&lt;EXPRESSION>)) | Desc(OrderBy(age)) |

>[!TAB Snowflake]

| Nome | Descrição | Sintaxe | Exemplo |
| ---- | ----------- | ------ | ------- |
| **RowNum** | Retorna uma sequência de linhas com base na partição da tabela e na sequência de classificação. | RowNum(PartitionBy(&lt;EXPRESSION>), OrderBy(&lt;EXPRESSION>)) | RowNum(PartitionBy(division), OrderBy(time)) |
| **PartitionBy** | Separa as linhas de entrada em diferentes partições, com base na expressão fornecida. | PartitionBy(&lt;EXPRESSION>) | PartitionBy(divisão) |
| **OrderBy** | Classifica o resultado da partição. | OrderBy(&lt;EXPRESSION>) | OrderBy(age) |
| **Desc** | Permite que o OrderBy seja classificado por ordem decrescente, em vez de crescente. | Desc(OrderBy(&lt;EXPRESSION>)) | Desc(OrderBy(age)) |

>[!ENDTABS]
