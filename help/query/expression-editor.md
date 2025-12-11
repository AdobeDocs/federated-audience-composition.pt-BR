---
audience: end-user
title: Criar a primeira consulta usando o modelador de consultas
description: Saiba como criar sua primeira consulta no modelador de consultas.
exl-id: abff07ef-2bc0-4e00-8957-4d59fc3bc938
source-git-commit: fdf93fb3554d05057052aa7059e141817a883dcc
workflow-type: tm+mt
source-wordcount: '4107'
ht-degree: 10%

---

# Editar expressões {#expression}

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

Para editar a expressão, insira uma expressão diretamente no campo de entrada. Para adicionar um campo ou uma função auxiliar, coloque o cursor na expressão à qual deseja adicionar o campo e clique no botão +.

![](assets/expression-editor.png){zoomable="yes"}

Quando a expressão estiver pronta, clique no botão **[!UICONTROL Confirmar]**. A expressão é exibida no campo selecionado. Para editá-lo, abra o editor de expressão e faça as alterações desejadas.

O exemplo abaixo mostra uma expressão configurada para o campo **[!UICONTROL Value]**. Para editá-lo, é necessário abrir o editor de expressão usando o botão **[!UICONTROL Editar expressão]**.

![](assets/edit-expression-value.png){zoomable="yes"}

## Funções de ajuda

A ferramenta de edição de consultas permite usar funções avançadas para fazer filtragens complexas, dependendo dos resultados desejados e dos tipos de dados manipulados. Os recursos abaixo estão disponíveis.

<!-- ### Aggregate

The aggregate functions are used to perform calculations on a set of values.

>[!BEGINTABS]

>[!TAB Google BigQuery]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **StdDev** | Returns the standard deviation of the values given. | StdDev(&lt;VALUE&gt;) | StdDev([0,3,5]) | -->

<!-- 

>[!TAB Databricks]

Aggregate functions are not available.

>[!TAB Fabric]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **StringAgg** | Returns the concatenation of the values of a string type column, separated by the character in the second argument | StringAgg(&lt;Value&gt;, &lt;String&gt;) | StringAgg(column, ",") |

>[!TAB Redshift]

Aggregate functions are not available. -->

<!-- 

>[!TAB Snowflake]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **StringAgg** | Returns the concatenation of the values of a string type column, separated by the character in the second argument | StringAgg(&lt;Value&gt;, &lt;String&gt;) | StringAgg(column, ",") | -->

<!-- 
>[!TAB Vertica]

Aggregate functions are not available. -->

<!-- 
>[!ENDTABS] 
-->

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
| **TruncTime** | Define o datetime para 1º de janeiro de 2000 e arredonda o restante do datetime para a unidade mais próxima, com base no valor numérico fornecido. Se o valor numérico for igual a 60, ele será truncado para o minuto mais próximo. Se o valor numérico for igual a 3600, ele será truncado na hora mais próxima. | TruncTime(&lt;DATETIME>, &lt;NUMBER>) | TruncTime(&quot;13/04/2016 19:28:14&quot;, 3600) |
| **TruncQuarter** | Corta o datetime para a primeira data do trimestre mais próximo. | TruncQuarter(&lt;DATETIME>) | TruncQuarter(&quot;13/04/2016 19:28:14&quot;) |
| **TruncYear** | Corta o datetime para a primeira data no ano mais próximo. | TruncYear(&lt;DATETIME>) | TruncYear(&quot;13/04/2016 19:28:14&quot;) |
| **TruncWeek** | Corta o datetime para o domingo da semana mais próxima. | TruncWeek(&lt;DATETIME>) | TruncWeek(&quot;13/04/2016 19:28:14&quot;) |

<!-- 
| **YearAndMonth** | Truncates the datetime to just the year and month. | YearAndMonth(&lt;DATETIME&gt;) | YearAndMonth("2019-12-25 15:30:00") | 
-->

<!-- | **DaysAgo** | Calculates the number of days between the current date and the provided timestamp, and returns the value as a datetime. | DaysAgo(&lt;DATETIME&gt;) | DaysAgo("2024-06-24 14:43:49") |
| **DaysAgoInt** | Calculates the number of days between the current date and the provided timestamp, and returns the value as an integer. | DaysAgoInt(&lt;DATETIME&gt;) | DaysAgoInt("2024-06-24 14:43:49") |
| **MonthsAgo** | Calculates the number of months between the current date and the provided timestamp, and returns the value as a datetime. | MonthsAgo(&lt;DATETIME&gt;) | MonthsAgo("2024-06-24 14:43:49") |
| **YearsAgo** | Calculates the number of years between the current date and the provided timestamp, and returns the value as a datetime. | YearsAgo(&lt;DATETIME&gt;) | YearsAgo("2024-06-24 14:43:49") | -->


<!-- 
>[!TAB Databricks]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **AddYears** | Adds the specified number of years to the provided datetime. | AddYears(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddYears("2019-12-25 15:30:00", 3) |
| **AddMonths** | Adds the specified number of months to the provided datetime. | AddMonths(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddMonths("2019-12-25 15:30:00", 6) |
| **AddDays** | Adds the specified number of days to the provided datetime. | AddDays(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddDays("2019-12-25 15:30:00", 10) |
| **AddHours** | Adds the specified number of hours to the provided datetime. | AddHours(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddHours("2019-12-25 15:30:00", 3) |
| **AddMinutes** | Adds the specified number of minutes to the provided datetime. | AddMinutes(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddMinutes("2019-12-25 15:30:00", 32) |
| **AddSeconds** | Adds the specified number of seconds to the provided datetime. | AddSeconds(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddSeconds("2019-12-25 15:30:00", 37) |
| **SubYears** | Subtracts the specified number of years to the provided datetime. | SubYears(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubYears("2019-12-25 15:30:00", 3) |
| **SubMonths** | Adds the specified number of months to the provided datetime. | SubMonths(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubMonths("2019-12-25 15:30:00", 6) |
| **SubDays** | Adds the specified number of days to the provided datetime. | SubDays(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubDays("2019-12-25 15:30:00", 10) |
| **SubHours** | Adds the specified number of hours to the provided datetime. | SubHours(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubHours("2019-12-25 15:30:00", 3) |
| **SubMinutes** | Adds the specified number of minutes to the provided datetime. | SubMinutes(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubMinutes("2019-12-25 15:30:00", 32) |
| **SubSeconds** | Adds the specified number of seconds to the provided datetime. | SubSeconds(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubSeconds("2019-12-25 15:30:00", 37) |
| **Year** | Extracts the year from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Month** | Extracts the month from the given datetime object. | Month(&lt;DATETIME&gt;) | Month("2019-12-15 15:30:00") |
| **Day** | Extracts the day from the given datetime object. | Day(&lt;DATETIME&gt;) | Day("2019-12-15 15:30:00") |
| **DayOfYear** | Extracts the day of year from the given datetime object. For example, if the provided datetime is February 2nd, it would return 33. | DayOfYear(&lt;DATETIME&gt;) | DayOfYear("2019-12-15 15:30:00") |
| **WeekDay** | Extracts the day of the week from the given datetime object, as a number from 1 to 7, with 1 representing Sunday. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Hour** | Extracts the hour value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Minute** | Extracts the minute value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Second** | Extracts the second value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **YearsDiff** | Finds the difference between the given datetimes, with a granularity of years. | YearsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | YearsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **MonthsDiff** | Finds the difference between the given datetimes, with a granularity of months. | MonthsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | MonthsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **DaysDiff** | Finds the difference between the given datetimes, with a granularity of days. | DaysDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | DaysDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **HoursDiff** | Finds the difference between the given datetimes, with a granularity of hours. | HoursDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | HoursDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **MinutesDiff** | Finds the difference between the given datetimes, with a granularity of minutes. | MinutesDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | MinutesDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **SecondsDiff** | Finds the difference between the given datetimes, with a granularity of seconds. | SecondsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | SecondsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **YearsOld** | Finds the difference between the given datetime and the present, with a granularity of years. | YearsOld(&lt;DATETIME&gt;) | YearsOld("2019-12-25 15:30:00") |
| **MonthsOld** | Finds the difference between the given datetime and the present, with a granularity of months. | MonthsOld(&lt;DATETIME&gt;) | MonthsOld("2019-12-25 15:30:00") |
| **DaysOld** | Finds the difference between the given datetime and the present, with a granularity of days. | DaysOld(&lt;DATETIME&gt;) | DaysOld("2019-12-25 15:30:00") |
| **DaysAgo** | Calculates the number of days between the current date and the provided timestamp, and returns the value as a datetime. | DaysAgo(&lt;DATETIME&gt;) | DaysAgo("2024-06-24 14:43:49") |
| **DaysAgoInt** | Calculates the number of days between the current date and the provided timestamp, and returns the value as an integer. | DaysAgoInt(&lt;DATETIME&gt;) | DaysAgoInt("2024-06-24 14:43:49") |
| **MonthsAgo** | Calculates the number of months between the current date and the provided timestamp, and returns the value as a datetime. | MonthsAgo(&lt;DATETIME&gt;) | MonthsAgo("2024-06-24 14:43:49") |
| **ToDateTime** | Converts the field to a datetime field. | ToDateTime(&lt;DATE&gt;) | ToDateTime("2019-12-25 15:30:00") |
| **ToTimestamp** | Converts the field to a timestamp field. | ToTimestamp(&lt;DATETIME&gt;) | ToTimestamp("2019-12-25 15:30:00") |
| **GetDate** | Get the current date of the server. | GetDate() | GetDate() |
| **DateOnly** | Truncates the datetime to just the year, month, and day. | DateOnly(&lt;DATETIME&gt;) | DateOnly("2019-12-25 15:30:00") |
| **ToDate** | Converts the field to a date field. | ToDate(&lt;DATETIME&gt;) | ToDate("2019-12-25 15:30:00") |
| **YearAndMonth** | Truncates the datetime to just the year and month. | YearAndMonth(&lt;DATETIME&gt;) | YearAndMonth("2019-12-25 15:30:00") |
| **Oldest** | Returns the oldest date between the two provided. | Oldest(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | Oldest("2015-02-13 11:59:59", "2016-04-13 19:28:14") |
| **TruncDate** | Truncates the datetime to the nearest unit, based on the numerical value given. If the numeric value is equal to 60, it truncates to the nearest minute. If the numeric value is equal to 3600, it truncates to the nearest hour. If the numeric value is equal to 86400, it truncates to the nearest day. Otherwise, it truncates to the nearest second. | TruncDate(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | TruncDate("2016-04-13 19:28:14", 3600) |
| **TruncDateTZ** | Truncates the datetime to the nearest unit, based on the numerical value given, and sets the datetime to the specified timezone. If the numeric value is equal to 60, it truncates to the nearest minute. If the numeric value is equal to 3600, it truncates to the nearest hour. If the numeric value is equal to 86400, it truncates to the nearest day. | TruncDateTZ(&lt;DATETIME&gt;, &lt;NUMBER&gt;, &lt;TIMEZONE&gt;) | TruncDateTZ("2016-04-13 19:28:14", 3600, "America/Los_Angeles") |
| **TruncTime** | Sets the datetime to January 1st, 2000 and rounds the rest of the datetime to the nearest unit, based on the numerical value given.If the numeric value is equal to 60, it truncates to the nearest minute. If the numeric value is equal to 3600, it truncates to the nearest hour. | TruncTime(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | TruncTime("2016-04-13 19:28:14", 3600) |
| **TruncQuarter** | Truncates the datetime to the first date in the nearest quarter. | TruncQuarter(&lt;DATETIME&gt;) | TruncQuarter("2016-04-13 19:28:14") |
| **TruncYear** | Truncates the datetime to the first date in the nearest year. | TruncYear(&lt;DATETIME&gt;) | TruncYear("2016-04-13 19:28:14") |
| **TruncWeek** | Truncates the datetime to the Sunday of the nearest week. | TruncWeek(&lt;DATETIME&gt;) | TruncWeek("2016-04-13 19:28:14") |

>[!TAB Fabric]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **AddYears** | Adds the specified number of years to the provided datetime. | AddYears(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddYears("2019-12-25 15:30:00", 3) |
| **AddMonths** | Adds the specified number of months to the provided datetime. | AddMonths(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddMonths("2019-12-25 15:30:00", 6) |
| **AddDays** | Adds the specified number of days to the provided datetime. | AddDays(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddDays("2019-12-25 15:30:00", 10) |
| **AddHours** | Adds the specified number of hours to the provided datetime. | AddHours(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddHours("2019-12-25 15:30:00", 3) |
| **AddMinutes** | Adds the specified number of minutes to the provided datetime. | AddMinutes(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddMinutes("2019-12-25 15:30:00", 32) |
| **AddSeconds** | Adds the specified number of seconds to the provided datetime. | AddSeconds(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddSeconds("2019-12-25 15:30:00", 37) |
| **SubYears** | Subtracts the specified number of years to the provided datetime. | SubYears(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubYears("2019-12-25 15:30:00", 3) |
| **SubMonths** | Adds the specified number of months to the provided datetime. | SubMonths(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubMonths("2019-12-25 15:30:00", 6) |
| **SubDays** | Adds the specified number of days to the provided datetime. | SubDays(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubDays("2019-12-25 15:30:00", 10) |
| **SubHours** | Adds the specified number of hours to the provided datetime. | SubHours(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubHours("2019-12-25 15:30:00", 3) |
| **SubMinutes** | Adds the specified number of minutes to the provided datetime. | SubMinutes(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubMinutes("2019-12-25 15:30:00", 32) |
| **SubSeconds** | Adds the specified number of seconds to the provided datetime. | SubSeconds(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubSeconds("2019-12-25 15:30:00", 37) |
| **DayOfYear** | Extracts the day of year from the given datetime object. For example, if the provided datetime is February 2nd, it would return 33. | DayOfYear(&lt;DATETIME&gt;) | DayOfYear("2019-12-15 15:30:00") |
| **DateOnly** | Truncates the datetime to just the year, month, and day. | DateOnly(&lt;DATETIME&gt;) | DateOnly("2019-12-25 15:30:00") |
| **YearsOld** | Finds the difference between the given datetime and the present, with a granularity of years. | YearsOld(&lt;DATETIME&gt;) | YearsOld("2019-12-25 15:30:00") |
| **YearsDiff** | Finds the difference between the given datetimes, with a granularity of years. | YearsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | YearsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **MonthsDiff** | Finds the difference between the given datetimes, with a granularity of months. | MonthsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | MonthsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **DaysDiff** | Finds the difference between the given datetimes, with a granularity of days. | DaysDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | DaysDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **HoursDiff** | Finds the difference between the given datetimes, with a granularity of hours. | HoursDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | HoursDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **MinutesDiff** | Finds the difference between the given datetimes, with a granularity of minutes. | MinutesDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | MinutesDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **SecondsDiff** | Finds the difference between the given datetimes, with a granularity of seconds. | SecondsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | SecondsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **WeekDay** | Extracts the day of the week from the given datetime object, as a number from 1 to 7, with 1 representing Sunday. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Hour** | Extracts the hour value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Minute** | Extracts the minute value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Second** | Extracts the second value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Oldest** | Returns the oldest date between the two provided. | Oldest(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | Oldest("2015-02-13 11:59:59", "2016-04-13 19:28:14") |
| **YearAndMonth** | Truncates the datetime to just the year and month. | YearAndMonth(&lt;DATETIME&gt;) | YearAndMonth("2019-12-25 15:30:00") |
| **ToDate** | Converts the field to a date field. | ToDate(&lt;DATETIME&gt;) | ToDate("2019-12-25 15:30:00") |
| **TruncDate** | Truncates the datetime to the nearest unit, based on the numerical value given. If the numeric value is equal to 60, it truncates to the nearest minute. If the numeric value is equal to 3600, it truncates to the nearest hour. If the numeric value is equal to 86400, it truncates to the nearest day. Otherwise, it truncates to the nearest second. | TruncDate(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | TruncDate("2016-04-13 19:28:14", 3600) |
| **TruncTime** | Sets the datetime to January 1st, 2000 and rounds the rest of the datetime to the nearest unit, based on the numerical value given.If the numeric value is equal to 60, it truncates to the nearest minute. If the numeric value is equal to 3600, it truncates to the nearest hour. | TruncTime(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | TruncTime("2016-04-13 19:28:14", 3600) |
| **TruncQuarter** | Truncates the datetime to the first date in the nearest quarter. | TruncQuarter(&lt;DATETIME&gt;) | TruncQuarter("2016-04-13 19:28:14") |
| **TruncYear** | Truncates the datetime to the first date in the nearest year. | TruncYear(&lt;DATETIME&gt;) | TruncYear("2016-04-13 19:28:14") |
| **TruncWeek** | Truncates the datetime to the Sunday of the nearest week. | TruncWeek(&lt;DATETIME&gt;) | TruncWeek("2016-04-13 19:28:14") |
| **ToTimestamp** | Converts the field to a timestamp field. | ToTimestamp(&lt;DATETIME&gt;) | ToTimestamp("2019-12-25 15:30:00") |

>[!TAB Redshift]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **ConvertTimezone** | Converts the datetime from its timezone to the timezone of the external account. | ConvertTimezone(&lt;DATETIME&gt;) | ConvertTimezone("2019-12-25 15:30:00") |

 -->

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
| **TruncTime** | Define o datetime para 1º de janeiro de 2000 e arredonda o restante do datetime para a unidade mais próxima, com base no valor numérico fornecido. Se o valor numérico for igual a 60, ele será truncado para o minuto mais próximo. Se o valor numérico for igual a 3600, ele será truncado na hora mais próxima. | TruncTime(&lt;DATETIME>, &lt;NUMBER>) | TruncTime(&quot;13/04/2016 19:28:14&quot;, 3600) |
| **TruncQuarter** | Corta o datetime para a primeira data do trimestre mais próximo. | TruncQuarter(&lt;DATETIME>) | TruncQuarter(&quot;13/04/2016 19:28:14&quot;) |
| **TruncYear** | Corta o datetime para a primeira data no ano mais próximo. | TruncYear(&lt;DATETIME>) | TruncYear(&quot;13/04/2016 19:28:14&quot;) |
| **TruncWeek** | Corta o datetime para o domingo da semana mais próxima. | TruncWeek(&lt;DATETIME>) | TruncWeek(&quot;13/04/2016 19:28:14&quot;) |
| **ConvertNTZ** | Converte um carimbo de data e hora sem fuso horário em um carimbo de data e hora com fuso horário. O fuso horário anexado será o fuso horário da conta externa. | ConvertNTZ(&lt;DATETIME>) | ConvertNTZ(&quot;24/06/2024 14:43:49&quot;) |

<!-- 
| **YearAndMonth** | Truncates the datetime to just the year and month. | YearAndMonth(&lt;DATETIME&gt;) | YearAndMonth("2019-12-25 15:30:00") | 
-->

<!-- 
| **DaysAgo** | Calculates the number of days between the current date and the provided timestamp, and returns the value as a datetime. | DaysAgo(&lt;DATETIME&gt;) | DaysAgo("2024-06-24 14:43:49") |
| **DaysAgoInt** | Calculates the number of days between the current date and the provided timestamp, and returns the value as an integer. | DaysAgoInt(&lt;DATETIME&gt;) | DaysAgoInt("2024-06-24 14:43:49") |
| **MonthsAgo** | Calculates the number of months between the current date and the provided timestamp, and returns the value as a datetime. | MonthsAgo(&lt;DATETIME&gt;) | MonthsAgo("2024-06-24 14:43:49") |
| **YearsAgo** | Calculates the number of years between the current date and the provided timestamp, and returns the value as a datetime. | YearsAgo(&lt;DATETIME&gt;) | YearsAgo("2024-06-24 14:43:49") | 
-->

<!-- 

>[!TAB Vertica]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **AddYears** | Adds the specified number of years to the provided datetime. | AddYears(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddYears("2019-12-25 15:30:00", 3) |
| **AddMonths** | Adds the specified number of months to the provided datetime. | AddMonths(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddMonths("2019-12-25 15:30:00", 6) |
| **AddDays** | Adds the specified number of days to the provided datetime. | AddDays(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddDays("2019-12-25 15:30:00", 10) |
| **AddHours** | Adds the specified number of hours to the provided datetime. | AddHours(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddHours("2019-12-25 15:30:00", 3) |
| **AddMinutes** | Adds the specified number of minutes to the provided datetime. | AddMinutes(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddMinutes("2019-12-25 15:30:00", 32) |
| **AddSeconds** | Adds the specified number of seconds to the provided datetime. | AddSeconds(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddSeconds("2019-12-25 15:30:00", 37) |
| **SubYears** | Subtracts the specified number of years to the provided datetime. | SubYears(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubYears("2019-12-25 15:30:00", 3) |
| **SubMonths** | Adds the specified number of months to the provided datetime. | SubMonths(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubMonths("2019-12-25 15:30:00", 6) |
| **SubDays** | Adds the specified number of days to the provided datetime. | SubDays(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubDays("2019-12-25 15:30:00", 10) |
| **SubHours** | Adds the specified number of hours to the provided datetime. | SubHours(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubHours("2019-12-25 15:30:00", 3) |
| **SubMinutes** | Adds the specified number of minutes to the provided datetime. | SubMinutes(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubMinutes("2019-12-25 15:30:00", 32) |
| **SubSeconds** | Adds the specified number of seconds to the provided datetime. | SubSeconds(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubSeconds("2019-12-25 15:30:00", 37) |
| **Year** | Extracts the year from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Month** | Extracts the month from the given datetime object. | Month(&lt;DATETIME&gt;) | Month("2019-12-15 15:30:00") |
| **Day** | Extracts the day from the given datetime object. | Day(&lt;DATETIME&gt;) | Day("2019-12-15 15:30:00") |
| **DayOfYear** | Extracts the day of year from the given datetime object. For example, if the provided datetime is February 2nd, it would return 33. | DayOfYear(&lt;DATETIME&gt;) | DayOfYear("2019-12-15 15:30:00") |
| **WeekDay** | Extracts the day of the week from the given datetime object, as a number from 1 to 7, with 1 representing Sunday. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Hour** | Extracts the hour value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Minute** | Extracts the minute value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Second** | Extracts the second value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **YearsDiff** | Finds the difference between the given datetimes, with a granularity of years. | YearsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | YearsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **MonthsDiff** | Finds the difference between the given datetimes, with a granularity of months. | MonthsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | MonthsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **DaysDiff** | Finds the difference between the given datetimes, with a granularity of days. | DaysDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | DaysDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **HoursDiff** | Finds the difference between the given datetimes, with a granularity of hours. | HoursDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | HoursDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **MinutesDiff** | Finds the difference between the given datetimes, with a granularity of minutes. | MinutesDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | MinutesDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **SecondsDiff** | Finds the difference between the given datetimes, with a granularity of seconds. | SecondsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | SecondsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **YearsOld** | Finds the difference between the given datetime and the present, with a granularity of years. | YearsOld(&lt;DATETIME&gt;) | YearsOld("2019-12-25 15:30:00") |
| **MonthsOld** | Finds the difference between the given datetime and the present, with a granularity of months. | MonthsOld(&lt;DATETIME&gt;) | MonthsOld("2019-12-25 15:30:00") |
| **DaysOld** | Finds the difference between the given datetime and the present, with a granularity of days. | DaysOld(&lt;DATETIME&gt;) | DaysOld("2019-12-25 15:30:00") |
| **GetDate** | Get the current date of the server. | GetDate() | GetDate() |
| **DateOnly** | Truncates the datetime to just the year, month, and day. | DateOnly(&lt;DATETIME&gt;) | DateOnly("2019-12-25 15:30:00") |
| **ToDate** | Converts the field to a date field. | ToDate(&lt;DATETIME&gt;) | ToDate("2019-12-25 15:30:00") |
| **ToDateTime** | Converts the field to a datetime field. | ToDateTime(&lt;DATE&gt;) | ToDateTime("2019-12-25 15:30:00") |
| **ToTimestamp** | Converts the field to a timestamp field. | ToTimestamp(&lt;DATETIME&gt;) | ToTimestamp("2019-12-25 15:30:00") |
| **YearAndMonth** | Truncates the datetime to just the year and month. | YearAndMonth(&lt;DATETIME&gt;) | YearAndMonth("2019-12-25 15:30:00") |
| **Oldest** | Returns the oldest date between the two provided. | Oldest(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | Oldest("2015-02-13 11:59:59", "2016-04-13 19:28:14") |
| **TruncDate** | Truncates the datetime to the nearest unit, based on the numerical value given. If the numeric value is equal to 60, it truncates to the nearest minute. If the numeric value is equal to 3600, it truncates to the nearest hour. If the numeric value is equal to 86400, it truncates to the nearest day. Otherwise, it truncates to the nearest second. | TruncDate(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | TruncDate("2016-04-13 19:28:14", 3600) |
| **TruncTime** | Sets the datetime to January 1st, 2000 and rounds the rest of the datetime to the nearest unit, based on the numerical value given.If the numeric value is equal to 60, it truncates to the nearest minute. If the numeric value is equal to 3600, it truncates to the nearest hour. | TruncTime(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | TruncTime("2016-04-13 19:28:14", 3600) |
| **TruncQuarter** | Truncates the datetime to the first date in the nearest quarter. | TruncQuarter(&lt;DATETIME&gt;) | TruncQuarter("2016-04-13 19:28:14") |
| **TruncYear** | Truncates the datetime to the first date in the nearest year. | TruncYear(&lt;DATETIME&gt;) | TruncYear("2016-04-13 19:28:14") |
| **TruncWeek** | Truncates the datetime to the Sunday of the nearest week. | TruncWeek(&lt;DATETIME&gt;) | TruncWeek("2016-04-13 19:28:14") |
| **DaysAgo** | Calculates the number of days between the current date and the provided timestamp, and returns the value as a datetime. | DaysAgo(&lt;DATETIME&gt;) | DaysAgo("2024-06-24 14:43:49") |
| **MonthsAgo** | Calculates the number of months between the current date and the provided timestamp, and returns the value as a datetime. | MonthsAgo(&lt;DATETIME&gt;) | MonthsAgo("2024-06-24 14:43:49") |
| **YearsAgo** | Calculates the number of years between the current date and the provided timestamp, and returns the value as a datetime. | YearsAgo(&lt;DATETIME&gt;) | YearsAgo("2024-06-24 14:43:49") |
-->

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

<!-- 

>[!TAB Databricks]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Distance** | Returns the distance between two points defined by their longitude and latitude in degrees, as a double. | Distance(&lt;NUMBER&gt;, &lt;NUMBER&gt;, &lt;NUMBER&gt;, &lt;NUMBER&gt;) | Distance(40.345, 39.2345, -35.5834, 34.599) |

>[!TAB Fabric]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Distance** | Returns the distance between two points defined by their longitude and latitude in degrees, as a double. | Distance(&lt;NUMBER&gt;, &lt;NUMBER&gt;, &lt;NUMBER&gt;, &lt;NUMBER&gt;) | Distance(40.345, 39.2345, -35.5834, 34.599) |

>[!TAB Redshift]

Geomarketing functions are not available.

-->

>[!TAB Snowflake]

| Nome | Descrição | Sintaxe | Exemplo |
| ---- | ----------- | ------ | ------- |
| **Distance** | Retorna a distância entre dois pontos definidos por sua longitude e latitude em graus, como um duplo. | Distance(&lt;NUMBER>, &lt;NUMBER>, &lt;NUMBER>, &lt;NUMBER>) | Distance(40,345, 39,2345, -35,5834, 34,599) |

<!-- 

>[!TAB Vertica]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Distance** | Returns the distance between two points defined by their longitude and latitude in degrees, as a double. | Distance(&lt;NUMBER&gt;, &lt;NUMBER&gt;, &lt;NUMBER&gt;, &lt;NUMBER&gt;) | Distance(40.345, 39.2345, -35.5834, 34.599) |

-->

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

<!-- 
| **Ceil** | Rounds up the provided number to the nearest integer. For example, if the provided number is 2.3, it will return 3. | Ceil(&lt;NUMBER&gt;) | Ceil(2.3) |
| **Floor** | Rounds down the provided number to the nearest integer. For example, if the provided number is 3.8, it will return 3. | Floor(&lt;NUMBER&gt;) | Floor(3.8) |
| **Greatest** | Returns the larger number between the two provided numbers. | Greatest(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Greatest(1, 2) |
| **Least** | Returns the smaller number between the two provided numbers. | Least(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Least (1,2) |
 -->

<!-- 

>[!TAB Databricks]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Mod** | Returns the remainder of the first number divided by the second number. | Mod(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Mod (3, 2) |
| **Percent** | Calculates what percentage the first number is of the second number. | Percent(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Percent(1, 2) |
| **Random** | Returns a random number between 0 (inclusive) and 1 (exclusive). | Random() | Random () |
| **ToDouble** | Converts the provided number to a double. | ToDouble(&lt;NUMBER&gt;) | ToDouble(5) |
| **ToInteger** | Converts the provided number to an integer. | ToInteger(&lt;NUMBER&gt;) | ToInteger(45) |
| **ToInt64** | Converts the provided number to a 64-bit integer. | ToInt64(&lt;NUMBER&gt;) | ToInt64(493) |
| **Trunc** | Truncates the provided number to the requested number of decimal places. | Trunc(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Trunc(36.9348934, 3) |

>[!TAB Fabric]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Ceil** | Rounds up the provided number to the nearest integer. For example, if the provided number is 2.3, it will return 3. | Ceil(&lt;NUMBER&gt;) | Ceil(2.3) |
| **Mod** | Returns the remainder of the first number divided by the second number. | Mod(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Mod (3, 2) |
| **Percent** | Calculates what percentage the first number is of the second number. | Percent(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Percent(1, 2) |
| **ToDouble** | Converts the provided number to a double. | ToDouble(&lt;NUMBER&gt;) | ToDouble(5) |
| **ToInteger** | Converts the provided number to an integer. | ToInteger(&lt;NUMBER&gt;) | ToInteger(45) |
| **ToInt64** | Converts the provided number to a 64-bit integer. | ToInt64(&lt;NUMBER&gt;) | ToInt64(493) |
| **Trunc** | Truncates the provided number to the requested number of decimal places. | Trunc(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Trunc(36.9348934, 3) |

>[!TAB Redshift]

Numeric functions are not available.

--->

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

<!-- 

>[!TAB Vertica]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Mod** | Returns the remainder of the first number divided by the second number. | Mod(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Mod (3, 2) |
| **Percent** | Calculates what percentage the first number is of the second number. | Percent(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Percent(1, 2) |
| **Random** | Returns a random number between 0 (inclusive) and 1 (exclusive). | Random() | Random () |
| **ToDouble** | Converts the provided number to a double. | ToDouble(&lt;NUMBER&gt;) | ToDouble(5) |
| **ToInteger** | Converts the provided number to an integer. | ToInteger(&lt;NUMBER&gt;) | ToInteger(45) |
| **ToInt64** | Converts the provided number to a 64-bit integer. | ToInt64(&lt;NUMBER&gt;) | ToInt64(493) |
| **Trunc** | Truncates the provided number to the requested number of decimal places. | Trunc(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Trunc(36.9348934, 3) |

--->

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
| **GetEmailDomain** | Extrai o domínio do endereço de email fornecido. | GetEmailDomain(&lt;CADEIA DE CARACTERES>) | GetEmailDomain(&quot;sample@example.com&quot;) |
| **Iif** | Retorna a primeira opção se a condição for verdadeira e retorna a segunda opção se a condição for falsa. | Iif(&lt;CONDIÇÃO>, &lt;VALOR>, &lt;VALOR>) | Iif(10 &lt; 20, &quot;true&quot;, &quot;false&quot;) |
| **IsEmptyString** | Retorna a primeira opção se a cadeira de caracteres estiver vazia. Caso contrário, retorna a segunda opção. | IsEmptyString( &lt;CADEIA DE CARACTERES> ,&lt;VALOR>, &lt;VALOR>) | IsEmptyString(&quot;string&quot;, &quot;sim&quot;, &quot;não&quot;) |
| **NewUUID** | Gera um novo UUID exclusivo. | NewUUID() | NewUUID() |
| **NoNull** | Retorna a cadeia de caracteres fornecida, se não estiver vazia, e retorna uma cadeia de caracteres vazia, se a cadeia de caracteres fornecida estiver vazia. | NoNull(&lt;STRING>) | NoNull(&quot;teste&quot;) |
| **IsBitSet** | Executa um bit a bit e (&amp;) nos números fornecidos. Isso permite verificar se o bit dentro do primeiro parâmetro está definido na posição fornecida no segundo parâmetro. | IsBitSet(&lt;NUMBER>, &lt;NUMBER>) | IsBitSet(5, 3) |
| **ClearBit** | Isso permite que você limpe o bit dentro do primeiro parâmetro na posição fornecida no segundo parâmetro. | ClearBit(&lt;NUMBER>, &lt;NUMBER>) | |
| **SetBit** | Executa um bit a bit ou (\|) nos números fornecidos. Isso permite que você defina o bit dentro do primeiro parâmetro é definido na posição fornecida no segundo parâmetro. | SetBit(&lt;NUMBER>, &lt;NUMBER>) | SetBit(5, 3) |
| **RowId** | Retorna o número da linha. | RowId() | RowId() |
| **ToBoolean** | Converte o valor em um booleano. | ToBoolean(&lt;VALUE>) | ToBoolean(a=b) |

<!-- 

>[!TAB Databricks]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Case** | Returns the first value if the expression is true. Otherwise, returns the second value. | Case(When(&lt;EXPRESSION&gt; &lt;VALUE&gt;), Else(&lt;VALUE&gt;)) | Case(When(a > b, "yes"), Else("no")) |
| **When** | Used as part of the Case function. Used to check the expression within Case. | When(&lt;EXPRESSION&gt; &lt;VALUE&gt;) | When(a > b, "yes") |
| **Else** | Used as part of the Case function. Used to choose the other option, if the When expression is false. | Else(&lt;VALUE&gt;) | Else ("no") |
| **GetEmailDomain** | Extracts the domain from the provided email address. | GetEmailDomain(&lt;STRING&gt;) | GetEmailDomain("sample@example.com") |
| **Iif** | Returns the first option if the condition is true and returns the second option if the condition is false. | Iif(&lt;CONDITION&gt;, &lt;VALUE&gt;, &lt;VALUE&gt;) | Iif(10 < 20, "true", "false") |
| **IsBitSet** | Performs a bitwise and (&) on the provided numbers. This lets you check if the bit within the first parameter is set at the position provided in the second parameter. | IsBitSet(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | IsBitSet(5, 3) |
| **ClearBit** | This lets your clear the bit within the first parameter at the position provided in the second parameter. | ClearBit(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | |
| **SetBit** | Performs a bitwise or (\|) on the provided numbers. This lets you set the bit within the first parameter is set at the position provided in the second parameter. | SetBit(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | SetBit(5, 3) |
| **IsEmptyString** | Returns the first option if the string is empty. Otherwise, returns the second option. | IsEmptyString( &lt;STRING&gt; ,&lt;VALUE&gt;, &lt;VALUE&gt;) | IsEmptyString("string", "yes", "no") |
| **NewUUID** | Generates a new unique UUID. | NewUUID() | NewUUID() |
| **NoNull** | Returns the provided string if it's not empty, and returns an empty string if the provided string is empty. | NoNull(&lt;STRING&gt;) | NoNull("test") |
| **RowId** | Returns the line number. | RowId() | RowId() |
| **ToBoolean** | Converts the value to a boolean. | ToBool(&lt;VALUE&gt;) | ToBool(a=b) |

>[!TAB Fabric]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Case** | Returns the first value if the expression is true. Otherwise, returns the second value. | Case(When(&lt;EXPRESSION&gt; &lt;VALUE&gt;), Else(&lt;VALUE&gt;)) | Case(When(a > b, "yes"), Else("no")) |
| **When** | Used as part of the Case function. Used to check the expression within Case. | When(&lt;EXPRESSION&gt; &lt;VALUE&gt;) | When(a > b, "yes") |
| **Else** | Used as part of the Case function. Used to choose the other option, if the When expression is false. | Else(&lt;VALUE&gt;) | Else ("no") |
| **IsBitSet** | Performs a bitwise and (&) on the provided numbers. This lets you check if the bit within the first parameter is set at the position provided in the second parameter. | IsBitSet(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | IsBitSet(5, 3) |
| **ClearBit** | This lets your clear the bit within the first parameter at the position provided in the second parameter. | ClearBit(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | |
| **SetBit** | Performs a bitwise or (\|) on the provided numbers. This lets you set the bit within the first parameter is set at the position provided in the second parameter. | SetBit(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | SetBit(5, 3) |
| **IsEmptyString** | Returns the first option if the string is empty. Otherwise, returns the second option. | IsEmptyString( &lt;STRING&gt; ,&lt;VALUE&gt;, &lt;VALUE&gt;) | IsEmptyString("string", "yes", "no") |
| **NoNull** | Returns the provided string if it's not empty, and returns an empty string if the provided string is empty. | NoNull(&lt;STRING&gt;) | NoNull("test") |
| **RowId** | Returns the line number. | RowId() | RowId() |
| **GetEmailDomain** | Extracts the domain from the provided email address. | GetEmailDomain(&lt;STRING&gt;) | GetEmailDomain("sample@example.com") |

>[!TAB Redshift]

Other functions are not available.

--->

>[!TAB Snowflake]

| Nome | Descrição | Sintaxe | Exemplo |
| ---- | ----------- | ------ | ------- |
| **Case** | Retorna o primeiro valor se a expressão for verdadeira. Caso contrário, retorna o segundo valor. | Case(When(&lt;EXPRESSÃO> &lt;VALOR>), Else(&lt;VALOR>)) | Case(Quando(a > b, &quot;sim&quot;), Else(&quot;não&quot;)) |
| **When** | Usado como parte da função Case. Usado para verificar a expressão em maiúsculas e minúsculas. | When(&lt;EXPRESSÃO> &lt;VALOR>) | Quando(a > b, &quot;sim&quot;) |
| **Else** | Usado como parte da função Case. Usado para escolher a outra opção, se a expressão When for falsa. | Else(&lt;VALOR>) | Senão (&quot;não&quot;) |
| **GetEmailDomain** | Extrai o domínio do endereço de email fornecido. | GetEmailDomain(&lt;CADEIA DE CARACTERES>) | GetEmailDomain(&quot;sample@example.com&quot;) |
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

<!-- 

>[!TAB Vertica]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Case** | Returns the first value if the expression is true. Otherwise, returns the second value. | Case(When(&lt;EXPRESSION&gt; &lt;VALUE&gt;), Else(&lt;VALUE&gt;)) | Case(When(a > b, "yes"), Else("no")) |
| **When** | Used as part of the Case function. Used to check the expression within Case. | When(&lt;EXPRESSION&gt; &lt;VALUE&gt;) | When(a > b, "yes") |
| **Else** | Used as part of the Case function. Used to choose the other option, if the When expression is false. | Else(&lt;VALUE&gt;) | Else ("no") |
| **Coalesce** | Returns the first non-null value. | Coalesce(&lt;VALUE&gt;, &lt;VALUE&gt;) | Coalesce ("", "string") |
| **GetEmailDomain** | Extracts the domain from the provided email address. | GetEmailDomain(&lt;STRING&gt;) | GetEmailDomain("sample@example.com") |
| **Iif** | Returns the first option if the condition is true and returns the second option if the condition is false. | Iif(&lt;CONDITION&gt;, &lt;VALUE&gt;, &lt;VALUE&gt;) | Iif(10 < 20, "true", "false") |
| **IsBitSet** | Performs a bitwise and (&) on the provided numbers. This lets you check if the bit within the first parameter is set at the position provided in the second parameter. | IsBitSet(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | IsBitSet(5, 3) |
| **ClearBit** | This lets your clear the bit within the first parameter at the position provided in the second parameter. | ClearBit(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | |
| **SetBit** | Performs a bitwise or (\|) on the provided numbers. This lets you set the bit within the first parameter is set at the position provided in the second parameter. | SetBit(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | SetBit(5, 3) |
| **IsEmptyString** | Returns the first option if the string is empty. Otherwise, returns the second option. | IsEmptyString( &lt;STRING&gt; ,&lt;VALUE&gt;, &lt;VALUE&gt;) | IsEmptyString("string", "yes", "no") |
| **NewUUID** | Generates a new unique UUID. | NewUUID() | NewUUID() |
| **NoNull** | Returns the provided string if it's not empty, and returns an empty string if the provided string is empty. | NoNull(&lt;STRING&gt;) | NoNull("test") |
| **RowId** | Returns the line number. | RowId() | RowId() |
| **ToBoolean** | Converts the value to a boolean. | ToBoolean(&lt;VALUE&gt;) | ToBoolean(a=b) |

-->

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

<!-- 

>[!TAB Databricks]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **AllNonNull2** | Takes two strings and checks if all of them are not null and not empty. |  AllNonNull2(&lt;STRING&gt;, &lt;STRING&gt;) | AllNonNull2("", "string2") | 
| **AllNonNull3** | Takes three strings and checks if all of them are not null and not empty | AllNonNull3(&lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;) | AllNonNull3("", "one", "three") |
| **Char** | Takes an array of Unicode codepoints and returns the resulting string. | Char(&lt;ARRAY&gt;) | Char([65, 68, 79, 66, 69]) |
| **Charindex** | Finds the first occurrence of the specified substring within the main string. | Charindex(&lt;STRING&gt;, &lt;SUBSTRING&gt;) | Charindex ("bar@example.com", "@") |
| **dataLength** | Returns the number of bytes in the string. | dataLength(&lt;STRING&gt;) | dataLength("My string") |
| **IfEquals** | Takes four strings and returns the third string if the first two strings are equal and returns the fourth string if the first two strings are not equal. | IfEquals(&lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;) | IfEquals("a", "a", "yes", "no") |
| **JuxtWords** | Takes two strings and combines them into a single string. Spaces between the strings are added if required. | JuxtWords(&lt;STRING&gt;, &lt;STRING&gt;) | JuxtWords("Hello", "World") |
| **Left** | Takes a string and returns the leftmost characters as specified. | Left(&lt;STRING&gt;, &lt;NUMBER&gt;) | Left("Substring", 3) |
| **Length** | Returns the length of the string. | Length(&lt;STRING&gt;) | Length("MyString") |
| **Md5Digest** | Converts the MD5-hashed string into its hexadecimal representation. |  Md5Digest(&lt;STRING&gt;) | Md5Digest("String") |
| **Right** | Takes a string and returns the rightmost characteres as specified. | Right(&lt;STRING&gt;, &lt;NUMBER&gt;)  | Right ("Substring", 3) |
| **Smart** | Returns the string with the first letter of each word capitalized. | Smart(&lt;STRING&gt;) | Smart("hello world") |
| **ToString** | Returns the value as a string. | ToString(&lt;VALUE&gt;) | ToString(123) |
| **Sha256Digest** | Converts the SHA256-hashed string into its hexadecimal representation. | Sha256Digest(&lt;STRING&gt;)  | Sha256Digest("string") |
| **Sha512Digest** | Converts the SHA512-hashed string into its hexadecimal representation. | Sha512Digest(&lt;STRING&gt;)  | Sha512Digest("string") |

>[!TAB Fabric]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **AllNonNull2** | Takes two strings and checks if all of them are not null and not empty. |  AllNonNull2(&lt;STRING&gt;, &lt;STRING&gt;) | AllNonNull2("", "string2") | 
| **AllNonNull3** | Takes three strings and checks if all of them are not null and not empty | AllNonNull3(&lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;) | AllNonNull3("", "one", "three") |
| **Char** | Takes an array of Unicode codepoints and returns the resulting string. | Char(&lt;ARRAY&gt;) | Char([65, 68, 79, 66, 69]) |
| **Charindex** | Finds the first occurrence of the specified substring within the main string. | Charindex(&lt;STRING&gt;, &lt;SUBSTRING&gt;) | Charindex ("bar@example.com", "@") |
| **dataLength** | Returns the number of bytes in the string. | dataLength(&lt;STRING&gt;) | dataLength("My string") |
| **GetLine** | Return the requested line of the provided string. | GetLine(&lt;STRING&gt;, &lt;NUMBER&gt;) | GetLine(multilinestring, 5) |
| **IfEquals** | Takes four strings and returns the third string if the first two strings are equal and returns the fourth string if the first two strings are not equal. | IfEquals(&lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;) | IfEquals("a", "a", "yes", "no") |
| **IsMemoNull** |  Returns 1 if the string is null, otherwise it returns 0. | IsMemoNull(&lt;STRING&gt;) | IsMemoNull("hello") |
| **Left** | Takes a string and returns the leftmost characters as specified. | Left(&lt;STRING&gt;, &lt;NUMBER&gt;) | Left("Substring", 3) |
| **Md5Digest** | Converts the MD5-hashed string into its hexadecimal representation. |  Md5Digest(&lt;STRING&gt;) | Md5Digest("String") |
| **JuxtWords** | Takes two strings and combines them into a single string. Spaces between the strings are added if required. | JuxtWords(&lt;STRING&gt;, &lt;STRING&gt;) | JuxtWords("Hello", "World") |
| **JuxtWords3** | Takes three strings and combines them into a single string. Spaces between the strings are added if required. | JuxtWords3(&lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;) | JuxtWords3("Hello", "New", "World") |
| **LPad** | Pads the provided string on the left side with the padding string up to the length given. | LPad(&lt;STRING&gt;, &lt;NUMBER&gt;, &lt;STRING&gt;) | LPad("LongerString", 15, "ch") |
| **Length** | Returns the length of the string. | Length(&lt;STRING&gt;) | Length("MyString") |
| **Right** | Takes a string and returns the rightmost characteres as specified. | Right(&lt;STRING&gt;, &lt;NUMBER&gt;)  | Right ("Substring", 3) |
| **RPad** | Pads the provided string on the right side with the padding string up to the length given. | RPad(&lt;STRING&gt;, &lt;NUMBER&gt;, &lt;STRING&gt;) | RPad("LongerString", 15, "ch") |
| **Smart** | Returns the string with the first letter of each word capitalized. | Smart(&lt;STRING&gt;) | Smart("hello world") |
| **ToString** | Returns the value as a string. | ToString(&lt;VALUE&gt;) | ToString(123) |
| **Sha256Digest** | Converts the SHA256-hashed string into its hexadecimal representation. | Sha256Digest(&lt;STRING&gt;)  | Sha256Digest("string") |
| **Sha512Digest** | Converts the SHA512-hashed string into its hexadecimal representation. | Sha512Digest(&lt;STRING&gt;)  | Sha512Digest("string") |

>[!TAB Redshift]

String functions are not available.

-->

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

<!-- 

>[!TAB Vertica]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **AllNonNull2** | Takes two strings and checks if all of them are not null and not empty. |  AllNonNull2(&lt;STRING&gt;, &lt;STRING&gt;) | AllNonNull2("", "string2") | 
| **AllNonNull3** | Takes three strings and checks if all of them are not null and not empty | AllNonNull3(&lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;) | AllNonNull3("", "one", "three") |
| **Char** | Takes an array of Unicode codepoints and returns the resulting string. | Char(&lt;ARRAY&gt;) | Char([65, 68, 79, 66, 69]) |
| **Charindex** | Finds the first occurrence of the specified substring within the main string. | Charindex(&lt;STRING&gt;, &lt;SUBSTRING&gt;) | Charindex ("bar@example.com", "@") |
| **dataLength** | Returns the number of bytes in the string. | dataLength(&lt;STRING&gt;) | dataLength("My string") |
| **GetLine** | Return the requested line of the provided string. | GetLine(&lt;STRING&gt;, &lt;NUMBER&gt;) | GetLine(multilinestring, 5) |
| **IfEquals** | Takes four strings and returns the third string if the first two strings are equal and returns the fourth string if the first two strings are not equal. | IfEquals(&lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;) | IfEquals("a", "a", "yes", "no") |
| **JuxtWords** | Takes two strings and combines them into a single string. Spaces between the strings are added if required. | JuxtWords(&lt;STRING&gt;, &lt;STRING&gt;) | JuxtWords("Hello", "World") |
| **JuxtWords3** | Takes three strings and combines them into a single string. Spaces between the strings are added if required. | JuxtWords3(&lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;) | JuxtWords3("Hello", "New", "World") |
| **Left** | Takes a string and returns the leftmost characters as specified. | Left(&lt;STRING&gt;, &lt;NUMBER&gt;) | Left("Substring", 3) |
| **Length** | Returns the length of the string. | Length(&lt;STRING&gt;) | Length("MyString") |
| **LPad** | Pads the provided string on the left side with the padding string up to the length given. | LPad(&lt;STRING&gt;, &lt;NUMBER&gt;, &lt;STRING&gt;) | LPad("LongerString", 15, "ch") |
| **Md5Digest** | Converts the MD5-hashed string into its hexadecimal representation. |  Md5Digest(&lt;STRING&gt;) | Md5Digest("String") |
| **Right** | Takes a string and returns the rightmost characteres as specified. | Right(&lt;STRING&gt;, &lt;NUMBER&gt;)  | Right ("Substring", 3) |
| **RPad** | Pads the provided string on the right side with the padding string up to the length given. | RPad(&lt;STRING&gt;, &lt;NUMBER&gt;, &lt;STRING&gt;) | RPad("LongerString", 15, "ch") |
| **Sha256Digest** | Converts the SHA256-hashed string into its hexadecimal representation. | Sha256Digest(&lt;STRING&gt;)  | Sha256Digest("string") |
| **Sha512Digest** | Converts the SHA512-hashed string into its hexadecimal representation. | Sha512Digest(&lt;STRING&gt;)  | Sha512Digest("string") |
| **Smart** | Returns the string with the first letter of each word capitalized. | Smart(&lt;STRING&gt;) | Smart("hello world") |
| **ToString** | Returns the value as a string. | ToString(&lt;VALUE&gt;) | ToString(123) |

-->

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

<!-- 

>[!TAB Databricks]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **RowNum** | Returns a sequence of rows based on the table partition and the sorting sequence. | RowNum(PartitionBy(&lt;EXPRESSION&gt;), OrderBy(&lt;EXPRESSION&gt;)) | RowNum(PartitionBy(division), OrderBy(time)) |
| **PartitionBy** | Separates the input rows into different partitions, based on the expression given. | PartitionBy(&lt;EXPRESSION&gt;) | PartitionBy(division) |
| **OrderBy** | Sorts the result of the partition. | OrderBy(&lt;EXPRESSION&gt;) | OrderBy(age) |
| **Desc** | Lets your OrderBy sort by descending order, rather than ascending order. | Desc(OrderBy(&lt;EXPRESSION&gt;)) | Desc(OrderBy(age)) |

>[!TAB Fabric]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **RowNum** | Returns a sequence of rows based on the table partition and the sorting sequence. | RowNum(PartitionBy(&lt;EXPRESSION&gt;), OrderBy(&lt;EXPRESSION&gt;)) | RowNum(PartitionBy(division), OrderBy(time)) |
| **PartitionBy** | Separates the input rows into different partitions, based on the expression given. | PartitionBy(&lt;EXPRESSION&gt;) | PartitionBy(division) |
| **OrderBy** | Sorts the result of the partition. | OrderBy(&lt;EXPRESSION&gt;) | OrderBy(age) |
| **Desc** | Lets your OrderBy sort by descending order, rather than ascending order. | Desc(OrderBy(&lt;EXPRESSION&gt;)) | Desc(OrderBy(age)) |

>[!TAB Redshift]

Window functions are not available.

--->

>[!TAB Snowflake]

| Nome | Descrição | Sintaxe | Exemplo |
| ---- | ----------- | ------ | ------- |
| **RowNum** | Retorna uma sequência de linhas com base na partição da tabela e na sequência de classificação. | RowNum(PartitionBy(&lt;EXPRESSION>), OrderBy(&lt;EXPRESSION>)) | RowNum(PartitionBy(division), OrderBy(time)) |
| **PartitionBy** | Separa as linhas de entrada em diferentes partições, com base na expressão fornecida. | PartitionBy(&lt;EXPRESSION>) | PartitionBy(divisão) |
| **OrderBy** | Classifica o resultado da partição. | OrderBy(&lt;EXPRESSION>) | OrderBy(age) |
| **Desc** | Permite que o OrderBy seja classificado por ordem decrescente, em vez de crescente. | Desc(OrderBy(&lt;EXPRESSION>)) | Desc(OrderBy(age)) |

<!-- 

>[!TAB Vertica]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **RowNum** | Returns a sequence of rows based on the table partition and the sorting sequence. | RowNum(PartitionBy(&lt;EXPRESSION&gt;), OrderBy(&lt;EXPRESSION&gt;)) | RowNum(PartitionBy(division), OrderBy(time)) |
| **PartitionBy** | Separates the input rows into different partitions, based on the expression given. | PartitionBy(&lt;EXPRESSION&gt;) | PartitionBy(division) |
| **OrderBy** | Sorts the result of the partition. | OrderBy(&lt;EXPRESSION&gt;) | OrderBy(age) |
| **Desc** | Lets your OrderBy sort by descending order, rather than ascending order. | Desc(OrderBy(&lt;EXPRESSION&gt;)) | Desc(OrderBy(age)) |

-->

>[!ENDTABS]
