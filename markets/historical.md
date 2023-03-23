---
title: Historical
description: Markets historical
keywords: markets, historical
---

Markets historical is also provided by the API.

## By symbol

Get market historical data by a specific symbol

[/markets/historical/{symbol}](https://api.tradingeconomics.com/markets/historical/aapl:us?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getHistorical(symbol='aapl:us',output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getHistoricalMarkets(symbol = 'aapl:us').then(function(data){
  console.log(data)     
});
```
{% endtab %}

{% endtabs %}

[/markets/historical/{symbols}](https://api.tradingeconomics.com/markets/historical/aapl:us,gac:com?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getHistorical(symbol=['aapl:us','gac:com'],output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getHistoricalMarkets(symbol = ['aapl:us','gac:com']).then(function(data){
  console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## By symbol and date

Get market historical data by a specific symbol and date interval. You can pass only a start date.

[/markets/historical/{symbol}?d1=yyyy-mm-dd&d2=yyyy-mm-dd](https://api.tradingeconomics.com/markets/historical/aapl:us?c=guest:guest&d1=2017-08-01&d2=2017-08-08&f=json)

{% tabs log %}

{% tab log python %}
```python
te.fetchMarkets(symbol='aapl:us', initDate='2017-01-01', endDate='2017-06-15')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getHistoricalMarkets(symbol = 'aapl:us', start_date = '2018-02-02', end_date = '2019-02-02').then(function(data){
  console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## Response Field

|            |                                         |
| ---------- | --------------------------------------- |
| **Symbol** | Unique symbol used by Trading Economics |
| **Date**   | Release time and date in UTC            |
| **Open**   | Open value                              |
| **High**   | High value                              |
| **Low**    | Low value                               |
| **Close**  | Close value                             |