---
title: Markets
description: Forecasts markets data
keywords: forecasts, markets
---

Here you can get market forecast data from the API.

## By category

Get market forecast for major indexes by category

### Index

[/markets/forecasts/index](http://api.tradingeconomics.com/markets/forecasts/index?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getMarketsForecasts(category='index', output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getMarketsForecast(category = 'index').then(function(data){
    console.log(data)     
});
```
{% endtab %}

{% endtabs %}

### Currency

[/markets/forecasts/currency](http://api.tradingeconomics.com/markets/forecasts/currency?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getMarketsForecasts(category='currency', output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getMarketsForecast(category = 'currency').then(function(data){
    console.log(data)     
});
```
{% endtab %}

{% endtabs %}

### Crypto

[/markets/forecasts/crypto](http://api.tradingeconomics.com/markets/forecasts/crypto?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getMarketsForecasts(category='crypto', output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getMarketsForecast(category = 'crypto').then(function(data){
    console.log(data)     
});
```
{% endtab %}

{% endtabs %}

### Commodity

[/markets/forecasts/commodity](http://api.tradingeconomics.com/markets/forecasts/commodity?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getMarketsForecasts(category='commodity', output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getMarketsForecast(category = 'commodity').then(function(data){
    console.log(data)     
});
```
{% endtab %}

{% endtabs %}

### Bond

[/markets/forecasts/bond](http://api.tradingeconomics.com/markets/forecasts/bond?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getMarketsForecasts(category='bond', output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getMarketsForecast(category = 'bond').then(function(data){
    console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## By symbol

[/markets/forecasts/symbol/{symbols}](http://api.tradingeconomics.com/markets/forecasts/symbol/BULGARIAGOVB10Y:GOV,LITHUANIAGOVBON10Y:GOV,GBGB10YR:GOV?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getMarketsForecasts(symbol='aapl:us', output_type='df')
```
{% endtab %}

{% tab log python %}
```python
te.getMarketsForecasts(symbol=['psi20:ind', 'indu:ind'], output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getMarketsForecast(symbol = 'aapl:us').then(function(data){
    console.log(data)     
});
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getMarketsForecast(symbol = ['aapl:us', 'gac:com']).then(function(data){
    console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## Response Fields

|                 |                                                               |
|-----------------|---------------------------------------------------------------|
| **Symbol**      | Unique symbol used by Trading Economics                       |
| **Country**	  | Country name                                                  |
| **Date**	      | Release time and date in UTC                                  |
| **Type**        | Market category can be: index, commodities, currency and bond |
| **Last***       | Latest released value                                         |
| **URL***        | Hyperlink at Trading Economics                                |
| **Importance*** | Indicator importance from 0(lowest) to 1000(highest)          |
| **Forecast1***  | Forecast value for the next quarter                           |
| **Forecast2***  | Forecast value for the next quarter following Forecast1       |
| **Forecast3***  | Forecast value for the next quarter following Forecast2       |
| **Forecast4***  | Forecast value for the next quarter following Forecast3       |