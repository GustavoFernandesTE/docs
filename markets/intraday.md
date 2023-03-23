---
title: Intraday
description: Markets intraday
keywords: markets, intraday
---

The API also provides minute-to-minute intraday data.

## By symbol

Get intraday data by a specific symbol or symbols (max of 5)

[/markets/intraday/{symbol}](https://api.tradingeconomics.com/markets/intraday/aapl:us?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getMarketsIntraday(symbols='aapl:us',output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getMarketsIntraday(symbol = 'aapl:us').then(function(data){
  console.log(data)     
});
```
{% endtab %}

{% endtabs %}

[/markets/intraday/{symbols}](https://api.tradingeconomics.com/markets/intraday/aapl:us,stx:us?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getMarketsIntraday(symbols=['aapl:us','stx:us'], output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getMarketsIntraday(symbol = ['aapl:us','stx:us']).then(function(data){
  console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## By symbol and date

Get intraday data by a specific symbol or symbols and date

[/markets/intraday/{symbol}?d1=yyyy-mm-dd hh:mm](https://api.tradingeconomics.com/markets/intraday/aapl:us?c=guest:guest&d1=2017-08-10%2015:30&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getMarketsIntraday(symbols='aapl:us', initDate='2018-03-13 15:30',output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getMarketsIntraday(symbol = 'aapl:us', start_date = '2018-03-03').then(function(data){
  console.log(data)     
});
```
{% endtab %}

{% endtabs %}

[/markets/intraday/{symbol}?d1=yyyy-mm-dd&d2=yyyy-mm-dd](https://api.tradingeconomics.com/markets/intraday/aapl:us?c=guest:guest&d1=2017-08-01&d2=2017-08-08&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getMarketsIntraday(symbols='aapl:us', initDate='2021-03-13', endDate='2021-03-17', output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getMarketsIntraday(symbol = 'aapl:us', start_date = '2018-03-03', end_date = '2019-04-04').then(function(data){
  console.log(data)     
});
```
{% endtab %}

{% endtabs %}

### By interval

An interval can be added to the date. Allowed intervals: 1m, 5m, 10m, 15m, 30m, 1h, 2h, 4h

[/markets/intraday/{symbol}?agr={interval}&d1=yyyy-mm-dd&d2=yyyy-mm-dd](http://api.tradingeconomics.com/markets/intraday/aapl:us?agr=5d&d1=2020-01-01%2000:00&d2=2020-12-01%2015:30&client=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getMarketsIntradayByInterval(symbol='aapl:us', initDate='2021-03-13', endDate='2021-03-17', interval='1m', output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getMarketsIntraday(symbol = 'aapl:us', start_date = '2018-03-03', end_date = '2019-04-04', agr = '5m').then(function(data){
  console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## Response Fields

|            |                                         |
| ---------- | --------------------------------------- |
| **Symbol** | Unique symbol used by Trading Economics |
| **Date**   | Release time and date in UTC            |
| **Open**   | Open value                              |
| **High**   | High value                              |
| **Low**    | Low value                               |
| **Close**  | Close value                             |