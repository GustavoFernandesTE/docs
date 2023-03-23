---
title: Peers
description: Indicators peers
keywords: indicators, peer
---

It's also possible get Indicators related tickers with API.

## By ticker

Get peers data by specific ticker

[/peers/(ticker)](https://api.tradingeconomics.com/peers/CPI%20YOY?c=guest\:guest\&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getPeers(ticker='CPI YOY', output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getPeers(ticker = 'CPI YOY').then(function(data){
  console.log(data)       
});
```
{% endtab %}

{% endtabs %}

## By country

Get peers data by specific country

[/peers/country/(country)](https://api.tradingeconomics.com/peers/country/mexico?c=guest\:guest\&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getPeers(country='mexico', output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getPeers(country = 'mexico').then(function(data){
  console.log(data)       
});
```
{% endtab %}

{% endtabs %}

## By country and category

Get peers data by specific country and category

[/peers/country/(country)/(category)](https://api.tradingeconomics.com/peers/country/mexico/money?c=guest\:guest\&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getPeers(country='mexico', category='money', output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getPeers(country = 'mexico', category = 'money').then(function(data){
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
| **CreateDate**           | Date of the first value in the historical series                           |
| **PreviousValue**        | Previously released value                                                  |
| **PreviousValueDate**    | Date of the previously released value                                      |
| **Peer**                 | Related ticker                                                             |
| **Relationship**         | 0 related, 1 component, 2 parent, 3 derivative                             |