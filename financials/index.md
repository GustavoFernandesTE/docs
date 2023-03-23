---
title: Snapshots
description: Financials snapshot data
keywords: financials, snapshot
---

Here you can get stocks earnings and fundamental information.

## Companies list

List all companies available

[/financials/companies](https://api.tradingeconomics.com/financials/companies?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getFinancialsData()
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getFinancialsData().then(function(data){
  console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## By country

List all financials data filtering by country (maximum of 5)

[/financials/companies?country={country}](https://api.tradingeconomics.com/financials/companies?country=united%20states&c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getFinancialsData(country = 'united states', output_type = 'df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getFinancialsData(country = 'china').then(function(data){
  console.log(data)     
});
```
{% endtab %}

{% endtabs %}

[/financials/companies?country={countries}](https://api.tradingeconomics.com/financials/companies?country=spain,germany&c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getFinancialsData(country = ['united states', 'china'], output_type = 'df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getFinancialsData(country = ['china', 'united states'] ).then(function(data){
  console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## Categories list

List all categories available

[/financials/categories](https://api.tradingeconomics.com/financials/categories?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getFinancialsCategoryList(output_type = 'df')
```
{% endtab %}

{% tab log node %}
```javascript
CHECKING
```
{% endtab %}

{% endtabs %}

## By categories

List all financials data filtering by category

[/financials/category/{category}](https://api.tradingeconomics.com/financials/category/assets?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
CHECKING
```
{% endtab %}

{% tab log node %}
```javascript
CHECKING
```
{% endtab %}

{% endtabs %}

## By symbol

List all financials data filtering by stock symbol

[/financials/symbol/{symbol}](https://api.tradingeconomics.com/financials/symbol/aapl:us?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getFinancialsData(symbol = 'aapl:us', output_type = 'df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getFinancialsData(symbol = 'aapl:us').then(function(data){
  console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## Response Fields

|                     |                                               |
|---------------------|-----------------------------------------------|
| **Symbol**          |	Unique symbol used by Trading Economics       |
| **Name**            |	Name of the company                           |
| **Country**         |	Company Country                               |
| **Date**            |	Trading Economics date time in UTC            |
| **Last**            |	Lastest value                                 |
| **Value1**          |	Value for the current quarter                 |
| **Date1**           |	Date for the current quarter                  |
| **Value2**          |	Value for the quarter prior to Value1         |
| **Date2**           |	Date for the quarter prior to Date1           |
| **Value3**          |	Value for the quarter prior to Value2         |
| **Date3**           |	Date for the quarter prior to Date2           |
| **Value4**          |	Value for the quarter prior to Value3         |
| **Date4**           |	Date for the quarter prior to Date3           |
| **Unit**            |	Unit                                          |
| **Currency**        |	Currency                                      |
| **Frequency**       |	Frequency of the financial                    |
| **Stock**           |	Stock unique symbol used by Trading Economics |
| **FinancialSymbol** |	Financials category                           |
| **Category**        |	Financials category                           |
| **Value**           |	Close price value                             |
| **Report**          |	Date	Reporting date                          |
| **Reference**       |	Fiscal reference date                         |