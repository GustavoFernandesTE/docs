---
title: Historical
description: Financials historical data
keywords: financials, historical
---

The API also provides historical of stocks earnings and fundamental information. Category is always a required parameter.

## By symbol

Get financials historical data filtering by symbol

[/financials/historical/{symbol:category}](https://api.tradingeconomics.com/financials/historical/aapl:us:assets?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getFinancialsHistorical(symbol = 'aapl:us', category = 'assets', output_type = 'df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getFinancialsHistorical(symbol = 'aapl:us', category = 'assets' ).then(function(data){
  console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## By multiple symbols

Get financials historical data filtering by symbol

[/financials/historical/{symbol:category,symbol:category}](https://api.tradingeconomics.com/financials/historical/aapl:us:assets,msft:us:assets?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getFinancialsHistorical(['aapl:us' , 'tsla:us'], category =['assets', 'debt'], output_type = 'df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getFinancialsHistorical(symbol = ['aapl:us', 'msft:us'], category = 'assets' ).then(function(data){
  console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## By symbol and date

Get financials historical data filtering by symbol and a date interval

[/financials/historical/{symbol:category}?d1=yyyy-mm-dd&d2=yyyy-mm-dd](https://api.tradingeconomics.com/financials/historical/aapl:us:assets?f=json&d1=2022-01-01&d2=2023-01-01)

{% tabs log %}

{% tab log python %}
```python
te.getFinancialsHistorical(['aapl:us', 'tsla:us'], category =['assets', 'debt'], initDate = '2021-01-01', endDate ='2023-12-01', output_type = 'df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getFinancialsHistorical(symbol = ['aapl:us', 'msft:us'], start_date = '2015-01-01', end_date = '2023-01-01', category = 'assets' ).then(function(data){
  console.log(data)     
});
```
{% endtab %}

{% endtabs %}

|               |                                         |
|---------------|-----------------------------------------|
| **Symbol**    |	Unique symbol used by Trading Economics |
| **Category**  |	Financials historical category          |
| **Date**      |	Trading Economics date time in UTC      |
| **Value**     |	Value of the historical date            |
| **Report**    |	Date	Reporting date                    |
| **Reference** |	Fiscal reference date                   |