---
title: Snapshots
description: Indicator snapshot data
keywords: indicators, snapshot
---

Trading Economics API provides Indicators data using a few and simple parameters. Trading Economics National Statistical database includes more than 15,000 
dataseries that come directly from official sources like central banks, national statistical agencies. It is a comprehensive database covering the most 
important macroeconomic data for each country from GDP growth rates to tax rates and population.

## List indicators and countries

List all indicators

[/indicators](https://api.tradingeconomics.com/indicators?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getIndicatorData(output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getIndicatorData().then(function(data){
  console.log(data)  
});
```
{% endtab %}

{% endtabs %}

List all available countries

[/country](https://api.tradingeconomics.com/country?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getAllCountries(output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getAllCountries().then(function(data){
  console.log(data)       
});
```
{% endtab %}

{% endtabs %}

## By country

Get indicator data by specific country or countries

[/country/{country}](https://api.tradingeconomics.com/country/mexico?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getIndicatorData(country='mexico', output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getIndicatorData(country = 'mexico').then(function(data){
  console.log(data)       
});
```
{% endtab %}

{% endtabs %}

[/country/{countries}](https://api.tradingeconomics.com/country/mexico?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getIndicatorData(country=['mexico', 'sweden'], output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getIndicatorData(country = ['mexico', 'sweden']).then(function(data){
  console.log(data)       
});
```
{% endtab %}

{% endtabs %}

## By country and group

Get indicator data by specific country and group

[/country/{country}?c=guest:guest&group={group}](http://api.tradingeconomics.com/country/mexico?c=guest:guest&group=gdp&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getIndicatorByCategoryGroup(country='mexico', category_group='gdp', output_type='df')
```
{% endtab %}

{% tab log node %}

```javascript
data = te.getIndicatorData(country = 'mexico', group = 'gdp' ).then(function(data){
  console.log(data)       
});
```
{% endtab %}

{% endtabs %}

## By ticker

Get indicator data by specific ticker

[/country/ticker/{ticker}](https://api.tradingeconomics.com/country/ticker/usurtot?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getIndicatorByTicker(ticker='usurtot', output_type='df')
```
{% endtab %}

{% tab log node %}

```javascript
data = te.getIndicatorData(ticker = 'usurtot').then(function(data){
  console.log(data)       
});
```
{% endtab %}

{% endtabs %}

## Countries by indicator

Get indicator data for all countries by specific indicator

[/country/all/{indicator}](https://api.tradingeconomics.com/country/all/gdp?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getIndicatorData(indicators='gdp' , output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getIndicatorData(country = 'mexico', group = 'gdp' ).then(function(data){
  console.log(data)       
});
```
{% endtab %}

{% endtabs %}

## Response Fields

|                          |                                                                            |
| ------------------------ | -------------------------------------------------------------------------- |
| **Country**              | Country name                                                               |
| **Category**             | Category name                                                              |
| **CategoryGroup**        | Category group name                                                        |
| **Title**                | Combination of country/category                                            |
| **LatestValueDate**      | Date of the last released value                                            |
| **LatestValue**          | Last released value                                                        |
| **Source**               | Source of data                                                             |
| **Unit**                 | Unit of the value                                                          |
| **URL**                  | Hyperlink at Trading Economics                                             |
| **Adjustment**           | Data description, for example: base period, price adjustement, seasonality |
| **Frequency**            | Frequency of the indicator                                                 |
| **HistoricalDataSymbol** | Unique symbol used by Trading Economics                                    |
| **CreateDate**           | Time when an indicator was inserted                                        |
| **FirstValueDate**       | Date of the first value in the historical series                           |
| **PreviousValue**        | Previously released value                                                  |
| **PreviousValueDate**    | Date of the previously released value                                      |
