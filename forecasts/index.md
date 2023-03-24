---
title: Indicators
description: Forecasts indicators data
keywords: forecasts, indicators, snapshot
---

Trading Economics forecasts are built using a proprietary global macro model that takes into account our analysts’ expectations, correlations between countries, and a set of logical relationships between different indicators.

## By country

Get forecast indicator data by country

[/forecast/country/{country}](https://api.tradingeconomics.com/forecast/country/mexico?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getForecastData(country='mexico', output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getForecasts(country = 'mexico').then(function(data){
    console.log(data)     
});
```
{% endtab %}

{% endtabs %}

[/forecast/country/{countries}](https://api.tradingeconomics.com/forecast/country/mexico,sweden?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getForecastData(country= ['mexico', 'sweden' ], output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getForecasts(country = ['mexico','sweden']).then(function(data){
    console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## By indicator

Get forecast indicator data by indicator

[/forecast/indicator/{indicator}](https://api.tradingeconomics.com/forecast/indicator/gdp?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getForecastData(indicator= 'gdp', output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getForecasts(indicator = 'gdp').then(function(data){
    console.log(data)     
});
```
{% endtab %}

{% endtabs %}

[/forecast/indicator/{indicators}](https://api.tradingeconomics.com/forecast/indicator/gdp,population?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getForecastData(indicator= ['gdp', 'population'], output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getForecasts(indicator = ['gdp','population']).then(function(data){
    console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## By country and indicator

Get forecast indicator data by country and indicator

[/forecast/country/{country}/indicator/{indicator}](https://api.tradingeconomics.com/forecast/country/mexico/indicator/gdp?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getForecastData(country='mexico', indicator='gdp', output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getForecasts(country = 'mexico', indicator = 'gdp').then(function(data){
    console.log(data)     
});
```
{% endtab %}

{% endtabs %}

[/forecast/country/{countries}/indicator/{indicators}](https://api.tradingeconomics.com/forecast/country/mexico,sweden/indicator/gdp,population?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
data = te.getForecastData(country= ['mexico','sweden'], indicator= ['gdp','population'], output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getForecasts(country = ['mexico','sweden'], indicator = ['gdp','population']).then(function(data){
    console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## By ticker

Get forecast indicator data by ticker

[/forecast/ticker/{ticker}](https://api.tradingeconomics.com//forecast/ticker/usurtot?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getForecastByTicker(ticker= 'usurtot', output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getForecasts(ticker = 'usurtot').then(function(data){
    console.log(data)     
});
```
{% endtab %}

{% endtabs %}

[/forecast/ticker/{tickers}](https://api.tradingeconomics.com//forecast/ticker/usurtot,wgdpchin?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getForecastByTicker(ticker= ['usurtot', 'wgdpchin'], output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getForecasts(ticker = ['usurtot','wgdpchin']).then(function(data){
    console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## Response Fields

|                          |                                                          |
|--------------------------|----------------------------------------------------------|
| **Category**             | Name of the indicator                                    |
| **Title**	               | Combination of country and indicator name                |
| **LatestValue**	       | Last released value                                      |
| **LatestValueDate**      | Date of the last released value                          |
| **ForecastValue1Q***     | Forecast value for the next quarter                      |
| **ForecastValue2Q***     | Forecast value for the quarter following ForecastValue1Q |
| **ForecastValue3Q***     | Forecast value for the quarter following ForecastValue2Q |
| **ForecastValue4Q***     | Forecast value for the quarter following ForecastValue3Q |
| **ForecastValue1***      | Forecast value for the year end                          |
| **ForecastValue2***      | Forecast value for the year end following ForecastValue1 |
| **ForecastValue3***      | Forecast value for the year end following ForecastValue2 |
| **q1_date**              | Date for ForecastValue1Q                                 |
| **q2_date**              | Date for ForecastValue2Q                                 |
| **q3_date**              | Date for ForecastValue3Q                                 |
| **q4_date**              | Date for ForecastValue4Q                                 |
| **Frequency**            | Frequency of the indicator                               |
| **Unit**                 | Unit of the forecasted values                            |
| **HistoricalDataSymbol** | Unique symbol used by Trading Economics                  |

***Forecast response fields can be diferent from Html response fields.**

|  Python  | HTML            |
|----------|-----------------|                 
| yearend  | ForecastValue1  |
| yearend2 | ForecastValue2  |
| yearend3 | ForecastValue3  |
| q1       | ForecastValue1Q |
| q2       | ForecastValue2Q |
| q3       | ForecastValue3Q |
| q4       | ForecastValue4Q | 