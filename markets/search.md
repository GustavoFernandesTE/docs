---
title: Search
description: Market search
keywords: markets, search
---

The API provides search functionality for Markets. By Default, the search will look into the categories: Indexes, markets (stocks), bonds, and commodities.

## By country

Search for market data by a specific country

[/markets/search/{country}](https://api.tradingeconomics.com/markets/search/united%20states?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getMarketsSearch(country='japan')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getMarketSnap(search_term = 'united states').then(function(data){
  console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## By country and category

Search for market data by a specific country and category (or categories)

[/markets/search/{country}?category={category}](https://api.tradingeconomics.com/markets/search/united%20states?c=guest:guest&category=index,markets&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getMarketsSearch(country='japan', category = 'index')
```

```python
te.getMarketsSearch(country='japan', category = ['index', 'markets'])
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getMarketSnap(search_term = 'united states', category = 'index').then(function(data){
  console.log(data)     
});
```

```javascript
data = te.getMarketSnap(search_term = 'united states', category = ['index', 'markets']).then(function(data){
  console.log(data)     
});
```
{% endtab %}

{% endtabs %}

**Categories available: index, markets, forex, bond and commodity.**

## By term

Search for market data by a specific term

[/markets/search/{term}](https://api.tradingeconomics.com/markets/search/msft:?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getMarketsSearch(country ='msft', output_type = 'df')
```

```python
te.getMarketsSearch(country ='msft', category = ['index', 'markets'], output_type = 'df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getMarketSnap(search_term = 'msft').then(function(data){
  console.log(data)     
});
```

```javascript
data = te.getMarketSnap(search_term = 'msft', category = ['index', 'markets']).then(function(data){
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
| **Type****                  | Market type                                                             |
| **MarketCap****             | Market Capitalization                                                   |
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

### Notes

***Group available only in:**

* /markets/commodities
* /markets/index
* /markets/currency
* /markets/bond
* /markets/currency?cross=eur.

****Type and MarketCap NOT available in:**

* /markets/commodities
* /markets/index
* /markets/currency
* /markets/bond
* /markets/currency?cross=eur.