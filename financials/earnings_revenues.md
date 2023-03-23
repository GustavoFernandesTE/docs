---
title: Historical
description: Financials earnings revenues 
keywords: financials, earnings, revenues
---

The API also provides historical of stocks earnings and fundamental information. Category is always a required parameter.

## Default calendar

Get default earnings revenues calendar

[/earnings-revenues](https://api.tradingeconomics.com/earnings-revenues?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getEarnings()
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getEarnings().then(function(data){
  console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## By date

Get earnings revenues calendar filtering by date

[/earnings-revenues?d1=yyyy-mm-dd](https://api.tradingeconomics.com/earnings-revenues?c=guest:guest&d1=2017-01-01&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getEarnings(initDate='2016-01-01')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getEarnings(start_date = '2018-02-02').then(function(data){
  console.log(data)     
});
```
{% endtab %}

{% endtabs %}

[/earnings-revenues?d1=yyyy-mm-dd&d2=yyy-mm-dd](https://api.tradingeconomics.com/earnings-revenues?c=guest:guest&d1=2017-01-01&d2=2017-12-31&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getEarnings(initDate='2016-01-01', endDate='2017-12-31')
```
{% endtab %}

{% tab log node %}
```javascript
CHECKING
```
{% endtab %}

{% endtabs %}

## By symbol and date

Get earnings revenues calendar filtering by instrument symbol and date

[/earnings-revenues/symbol/{symbol}?d1=yyyy-mm-dd](https://api.tradingeconomics.com/earnings-revenues/symbol/aapl:us?c=guest:guest&d1=2017-01-01&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getEarnings(symbols = 'msft:us', initDate='2016-01-01')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getEarnings(symbol = 'CMCSA:US', start_date = '2018-02-02').then(function(data){
  console.log(data)     
});
```
{% endtab %}

{% endtabs %}

[/earnings-revenues/symbol/{symbol}?d1=yyyy-mm-dd&d2=yyyy-mm-dd](https://api.tradingeconomics.com/earnings-revenues/symbol/msft:us?c=guest:guest&d1=2016-01-01&d2=2017-12-31&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getEarnings(symbols = 'msft:us', initDate='2016-01-01', endDate='2017-12-31')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getEarnings(symbol = 'CMCSA:US', start_date = '2018-02-02', end_date = '2019-12-31').then(function(data){
  console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## By country

Get earnings revenues calendar filtering by country

[/earnings-revenues/country/{country}](https://api.tradingeconomics.com/earnings-revenues/country/mexico?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getEarnings(country = 'united states')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getEarnings(country = 'united states').then(function(data){
  console.log(data)     
});
```
{% endtab %}

{% endtabs %}

|                       |                                                           |
|-----------------------|-----------------------------------------------------------|
| **Date**              |	Release date in UTC                                       |
| **Symbol**            |	Unique symbol used by Trading Economics                   |
| **Name**              |	Company name                                              |
| **Actual**	          | Earnings per share                                        |
| **Forecast**	        | Average forecast among a representative group of analysts |
| **Previous**          | Previously released value                                 |
| **FiscalTag**	        | Fiscal year and quarter. E.g. "FY2022Q4"                  |
| **FiscalReference**	  | Fiscal year and quarter in different format. E.g. "Q3"    |
| **CalendarReference**	| Calendar quarter for the release                          |
| **Country**	          | Country name                                              |
| **Currency**	        | Currency                                                  |
| **Session**	          | Expected earnings release hour                            |
| **Importance**        |	Importance being 3 the highest                            |
| **LastUpdate**        |	Time when new data was inserted or changed                |
| **marketRelease**	    | Release type: after_close, before_open, by_day_end        |
| **MarketCapUSD**      |	Market cap in US dollar                                   |