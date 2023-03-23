---
title: Snapshots
description: Markets snapshot data
keywords: markets, snapshot
---

Here you can get a list of available commodities, currencies, indexes or bonds and their latest values. **Please consider that all market-related methods are beta and under heavy development.**

## Commodities

List all commodities available

[/markets/commodities](https://api.tradingeconomics.com/markets/commodities?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getMarketsData(marketsField = 'commodities', output_type = 'df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getMarketSnap(marketsField = 'commodities').then(function(data){
  console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## Currencies

List all major currencies

[/markets/currency](https://api.tradingeconomics.com/markets/currency?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
data = te.getMarketsData(marketsField = 'currency', output_type = 'df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getMarketSnap(marketsField = 'currency').then(function(data){
  console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## Crosses

List all currency crosses

[/markets/currency?cross=eur](https://api.tradingeconomics.com/markets/currency?c=guest:guest&cross=EUR&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getCurrencyCross(cross = 'EUR', output_type = 'df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getMarketSnap(cross = 'eur').then(function(data){
  console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## Crypto

List all crypto currencies

[/markets/crypto](https://api.tradingeconomics.com/markets/crypto?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getMarketsData(marketsField = 'crypto', output_type = 'df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getMarketSnap(marketsField = 'crypto').then(function(data){
  console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## Stock Market

List all stock market indexes

[/markets/index](https://api.tradingeconomics.com/markets/index?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getMarketsData(marketsField = 'index', output_type = 'df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getMarketSnap(marketsField = 'index').then(function(data){
  console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## Bonds

List all government bonds

[/markets/bond](https://api.tradingeconomics.com/markets/bond?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getMarketsData(marketsField = 'bond', output_type = 'df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getMarketSnap(marketsField = 'bond').then(function(data){
  console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## Markets

List all individual markets (stock, index, currency, crypto, commodity or bond) by a specific symbol or symbols

[/markets/symbol/{symbol}](https://api.tradingeconomics.com/markets/symbol/aapl:us?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getMarketsBySymbol(symbols='aapl:us', output_type = 'df') 
```

```python
te.getMarketsBySymbol(symbols=['aapl:us', 'gac:com'], output_type = 'df')  
```

{% endtab %}

{% tab log node %}
```javascript
data = te.getMarketSnap(symbol = 'aapl:us').then(function(data){
  console.log(data)     
});
```

```javascript
data = te.getMarketSnap(symbol = ['aapl:us', 'gac:com']).then(function(data){
  console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## Country stocks

List all stocks by a specific country

[/markets/country/{country}](https://api.tradingeconomics.com/markets/country/united%20states?client=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getStocksByCountry(country='united states', output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getMarketSnap(country = 'japan').then(function(data){
  console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## Peers

List all stock peers by a specific symbol

[/markets/peers/{symbol}](https://api.tradingeconomics.com/markets/peers/aapl:us?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getMarketsPeers(symbols='aapl:us', output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getMarketSnap(peers_symbol = 'aapl:us').then(function(data){
  console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## Components

List all components by a specific index symbol

[/markets/components/{symbol}](https://api.tradingeconomics.com/markets/components/psi20:ind?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getMarketsComponents(symbols='psi20:ind', output_type='df')
```

```python
te.getMarketsComponents(symbols=['indu:ind', 'psi20:ind'], output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getMarketSnap(components_symbol = 'psi20:ind').then(function(data){
  console.log(data)     
});
```

```javascript
data = te.getMarketSnap(components_symbol = ['indu:ind', 'psi20:ind']).then(function(data){
  console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## Description by symbol

List stock descriptions by company symbol

[/markets/stockdescriptions/symbol/{symbols}](https://api.tradingeconomics.com/markets/stockdescriptions/symbol/aapl:us,fb:us?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getMarketsStockDescriptions(symbol='aapl:us', output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getMarketStockDescriptions(symbol = 'aapl:us').then(function(data){
  console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## Description by country

List all stocks description by country

[/markets/stockdescriptions/country/{country}](https://api.tradingeconomics.com/markets/stockdescriptions/country/france?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getMarketsStockDescriptions(country='japan', output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getMarketStockDescriptions(country = 'china').then(function(data){
  console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## Symbologies by symbol

Get detailed symbology fields by company symbol

[markets/symbology/symbol/{symbol}](https://api.tradingeconomics.com/markets/symbology/symbol/aapl:us?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getMarketsSymbology(symbol = 'aapl:us', output_type = 'df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getSymbology(symbol = 'aapl:us').then(function(data){
  console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## Symbologies by ticker

Get detailed symbology fields by a specific ticker

[/markets/symbology/ticker/{ticker}](https://api.tradingeconomics.com/markets/symbology/ticker/aapl?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getMarketsSymbology(ticker = 'aapl', output_type = 'df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getSymbology(ticker = 'aapl').then(function(data){
  console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## Symbologies by ISIN

Get detailed symbology fields by a specific ISIN

[/markets/symbology/isin/{isin}](https://api.tradingeconomics.com/markets/symbology/isin/US0378331005?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getMarketsSymbology(isin = 'US0378331005', output_type = 'df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getSymbology(isin = 'US0378331005').then(function(data){
  console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## Response Fields

|                             |                                                                         |
| --------------------------- | ----------------------------------------------------------------------- |
| **Symbol**                  | Unique symbol used by Trading Economics                                 |
| **Ticker**                  | Unique ticker used by Trading Economics                                 |
| **Name**                    | Indicator full name                                                     |
| **Country**                 | Country name                                                            |
| **Date**                    | Release time and date in UTC                                            |
| **Group***                  | Group name                                                              |
| **Type\*\***                | Market type                                                             |
| **MarketCap\*\***           | Market Capitalization                                                   |
| **Decimals**                | Number of decimal places                                                |
| **Last**                    | Latest released value                                                   |
| **Unit**                    | Unit of the value                                                       |
| **URL**                     | Hyperlink at Trading Economics                                          |
| **Importance**              | Indicator importance from 0 (lowest) to 1000 (highest)                  |
| **DailyChange**             | Difference between last close and current price                         |
| **DailyPercentualChange**   | Difference in percentage between last close and current price           |
| **WeeklyChange**            | Difference between last week close and current price price              |
| **WeeklyPercentualChange**  | Difference in percentage between last week close and current price      |
| **MonthlyChange**           | Difference between last month close and current price                   |
| **MonthlyPercentualChange** | Difference in percentage between last month close and current price     |
| **YearlyChange**            | Difference between last year close and current price                    |
| **YearlyPercentualChange**  | Difference in percentage between last year close and current price      |
| **YTDChange**               | Difference between last year last close and current price               |
| **YTDPercentualChange**     | Difference in percentage between last year last close and current price |
| **Yesterday**               | Yesterday close                                                         |
| **LastWeek**                | Last week close                                                         |
| **LastMonth**               | Last month close                                                        |
| **LastYear**                | Last year close                                                         |
| **StartYear**               | Start year close                                                        |
| **LastUpdate**              | Time when new data was inserted or changed                              |
| **Frequency**               | Market frequency                                                        |

### N﻿otes

**\*Group available only in:**

* /markets/commodities
* /markets/index
* /markets/currency
* /markets/bond
* /markets/currency?cross=eur.

**\*\*Type and MarketCap NOT available in:**

* /markets/commodities
* /markets/index
* /markets/currency
* /markets/bond
* /markets/currency?cross=eur.