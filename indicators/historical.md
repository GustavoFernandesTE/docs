---
title: Historical
description: Indicatos Historical
keywords: indicators, historical
---

The API also provides historical data for Indicators, using the same parameters for Indicators snapshot data.

## By country and indicator
Get historical data by specific country and indicator

[/historical/country/{country}/indicator/{indicator}](https://api.tradingeconomics.com/historical/country/mexico/indicator/gdp?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getHistoricalData(country='mexico', indicator='gdp')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getHistoricalData(country = 'mexico', indicator = 'gdp').then(function(data){
  console.log(data)       
});
```
{% endtab %}

{% endtabs %}

[/historical/country/{countries}/indicator/{indicators/{yyyy-mm-dd}/{yyyy-mm-dd}}](https://api.tradingeconomics.com/historical/country/mexico,sweden/indicator/gdp,population/2015-01-01/2015-12-31?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getHistoricalData(country=['mexico', 'sweden'], indicator=['gdp','population'], initDate='1990-01-01', endDate='2015-01-01')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getHistoricalData(country = ['mexico','sweden'], indicator = ['gdp','population']).then(function(data){
  console.log(data)
});
```
{% endtab %}

{% endtabs %}

## By ticker
Get historical data by specific ticker

[/historical/ticker/{ticker}/{yyyy-mm-dd}](https://api.tradingeconomics.com/historical/ticker/USURTOT/2015-03-01?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getHistoricalByTicker(ticker = 'USURTOT', start_date = '2015-03-01')   
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getHistoricalData(ticker = 'usurtot', start_date = '2015-03-01' ).then(function(data){
  console.log(data)       
});
```
{% endtab %}

{% endtabs %}

## Latest updates
Get historical latest updates

[/historical/updates](https://api.tradingeconomics.com/historical/updates?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getHistoricalUpdates()
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getHistoricalUpdates().then(function(data){
  console.log(data)       
});
```
{% endtab %}

{% endtabs %}

## Response Fields

|                          |                                            |
|--------------------------|--------------------------------------------|
| **Country**              | Country name                               |
| **Category**             | Indicator category name                    |
| **Date Time**            | Release time and date in UTC               |
| **Close**                | Value *                                    |
| **Frequency**            | Frequency of the indicator                 |
| **HistoricalDataSymbol** | Unique symbol used by TradingEconomics     |
| **LastUpdate**           | Time when new data was inserted or changed |

*Python package response field returns **Value** instead of 'Close'.