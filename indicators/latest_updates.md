---
title: Latest Updates
description: Indicators latest updates
keywords: indicators, updates
---

Get the latest economic updates using different parameters.

## Latest
Get latest updates

[/updates](https://api.tradingeconomics.com/updates?client=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getLatestUpdates(output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getLatestUpdates().then(function(data){
  console.log(data)       
});
```
{% endtab %}

{% endtabs %}

## By date
Get latest updates by specific date

[/updates/{date}](https://api.tradingeconomics.com/updates/2018-01-01?client=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getLatestUpdates(init_date='2018-08-15')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getLatestUpdates(start_date = '2018-02-02').then(function(data){
  console.log(data)       
});
```
{% endtab %}

{% endtabs %}

[/updates/{date}?time={hh:mm}](https://api.tradingeconomics.com/updates/2021-10-18?client=guest:guest&time=15:20&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getLatestUpdates(init_date='2021-10-18', time='15:20')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getLatestUpdates(start_date = '2021-10-18', time = '15:20').then(function(data){
  console.log(data)       
});
```
{% endtab %}

{% endtabs %}

## By country
Get latest updates by specific country

[/updates/country/{country}](https://api.tradingeconomics.com/updates/country/portugal?client=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getLatestUpdates(country='portugal')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getLatestUpdates(country = 'sweden').then(function(data){
  console.log(data)       
});
```
{% endtab %}

{% endtabs %}


[/updates/country/{country}/{date}](https://api.tradingeconomics.com/updates/country/portugal/2018-01-01?client=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getLatestUpdates(country='portugal', init_date='2018-08-15')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getLatestUpdates(start_date = '2018-02-02', country = 'sweden').then(function(data){
  console.log(data)       
});
```
{% endtab %}

{% endtabs %}

## Response Fields

|                          |                                            |
|--------------------------|--------------------------------------------|
| **Country**              | Country name                               |
| **Category**             | Category name                              |
| **HistoricalDataSymbol** | Unique symbol used by Trading Economics    |
| **LastUpdate**           | Time when new data was inserted or changed |