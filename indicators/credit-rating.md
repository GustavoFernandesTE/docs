---
title: Credit Ratings
description: Indicators Credit Ratings
keywords: indicators, credit, rating, agency
---

Trading Economics API provides Credit Rating data from many Agencies.

## Latest
Get latest credit ratings

[/ratings](https://api.tradingeconomics.com/ratings?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getRatings( output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getRatings().then(function(data){
  console.log(data)       
});
```
{% endtab %}

{% endtabs %}

## By country
Get credit rating data by specific country

[/ratings/{country}](https://api.tradingeconomics.com/ratings/mexico?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getRatings(country= 'mexico', output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getRatings(country = 'mexico').then(function(data){
  console.log(data)       
});
```
{% endtab %}

{% endtabs %}

[/ratings/{countries}](https://api.tradingeconomics.com/ratings/mexico,sweden?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getRatings(country=['mexico','sweden'], output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getRatings(country = ['mexico', 'sweden']).then(function(data){
  console.log(data)       
});
```
{% endtab %}

{% endtabs %}

## Historical
Get credit rating historical data

[/ratings/historical/{country}](https://api.tradingeconomics.com/ratings/historical/mexicos?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getHistoricalRatings(country= 'mexico', output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getRatings(historical = 'mexico').then(function(data){
  console.log(data)       
});
```
{% endtab %}

{% endtabs %}

[/ratings/historical/{countries}](https://api.tradingeconomics.com/ratings/historical/mexico,sweden?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getHistoricalRatings(country=['mexico','sweden'])
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getRatings(historical = ['mexico', 'sweden']).then(function(data){
  console.log(data)       
});
```
{% endtab %}

{% endtabs %}

[/ratings/historical/{country}/{yyyy-mm-dd}/{yyyy-mm-dd}](https://api.tradingeconomics.com/ratings/historical/mexico/2013-01-01/2014-01-01?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getHistoricalRatings(country= 'mexico',initDate= '2011-01-01',  endDate= '2012-01-01',output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getRatings(historical = 'mexico', start_date = '2011-01-01', end_date = '2015-01-01').then(function(data){
  console.log(data)       
});
```
{% endtab %}

{% endtabs %}

## Response Fields

|                          |                              |
|--------------------------|-------------------------------
| **Country**              | Country name                 |
| **TE**                   | Trading Economics rating     |
| **TE_Outlook**           | Trading Economics outlook    |
| **SP**                   | Standard & Poor’s rating     |
| **SP_Outlook**           | Standard & Poor’s outlook    |
| **Moodys**               | Moody’s rating               |
| **Moodys_Outlook**       | Moody’s outlook              |
| **Fitch**                | Fitch rating                 |
| **Fitch_outlook**        | Fitch outlook                |
| **DBRS**                 | DBRS rating                  |
| **DBRS_Outlook**         | DBRS outlook                 |
| **Date**                 | Release time and date in UTC |
| **Agency**               | Rating agency                |
| **Rating**               | Rating score                 |
| **Outlook**              | Rating outlook               |

