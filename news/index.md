---
title: Get news
description: Get news
keywords: news, get
---

News are short summaries, usually three to five sentences covering a specific release/event related to the data, providing an explanation of what was behind growth/contraction, increase/decrease in the specific dataseries.

## Latest

Get latest news

[/news](https://api.tradingeconomics.com/news?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getNews(output_type = 'df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getNews().then(function(data){
    console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## By date

Get news by a date range

[/news?c=guest:guest&d1={date}&d2={date}](https://api.tradingeconomics.com/news?c=guest:guest&d1=2021-02-02&d2=2021-03-03&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getNews(start_date = '2021-02-02', end_date = '2021-03-03', output_type = 'df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getNews('2021-02-02', end_date = '2021-03-03').then(function(data){
    console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## By country

Get news by country

[/news/country/{countries}](https://api.tradingeconomics.com/news/country/mexico?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getNews(country = 'mexico', output_type = 'df')
```

```python
te.getNews(country = ['mexico', 'sweden'], output_type = 'df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getNews(country = 'mexico').then(function(data){
    console.log(data)     
});
```

```javascript
data = te.getNews(country = ['mexico', 'sweden']).then(function(data){
    console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## By country and date

Get news by country and date range

[/news/country/{countries}?c=guest:guest&d1={date}&d2={date}](https://api.tradingeconomics.com/news/country/mexico?c=guest:guest&d1=2021-02-02&d2=2021-03-03&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getNews(country = 'mexico', start_date = '2021-02-02', end_date = '2021-03-03', output_type = 'df')
```

```python
te.getNews(country = ['mexico', 'sweden'], start_date = '2021-02-02', end_date = '2021-03-03', output_type = 'df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getNews(country = 'mexico', start_date = '2021-02-02', end_date = '2021-03-03').then(function(data){
    console.log(data)     
});
```

```javascript
data = te.getNews(country = ['mexico', 'sweden'], start_date = '2021-02-02', end_date = '2021-03-03').then(function(data){
    console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## By indicator

Get news by indicators

[/news/indicator/{indicators}](https://api.tradingeconomics.com/news/indicator/inflation%20rate?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getNews(indicator = 'inflation rate', output_type = 'df')
```

```python
te.getNews(indicator = ['inflation rate','gdp'], output_type = 'df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getNews(indicator = 'imports').then(function(data){
    console.log(data)     
});
```

```javascript
data = te.getNews(indicator = ['imports','gdp']).then(function(data){
    console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## By indicator and date

Get news by indicators and date range

[/news/indicator/{indicators}?c=guest:guest&d1={date}&d2={date}](https://api.tradingeconomics.com/news/indicator/inflation%20rate?c=guest:guest&d1=2021-02-02&d2=2021-03-03&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getNews(indicator = 'inflation rate', start_date = '2021-02-02', end_date = '2021-03-03', output_type = 'df')
```

```python
te.getNews(indicator = ['inflation rate', 'imports'], start_date = '2021-02-02', end_date = '2021-03-03', output_type = 'df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getNews(indicator = 'imports', start_date = '2021-01-01', end_date = '2021-02-02').then(function(data){
    console.log(data)     
});
```

```javascript
data = te.getNews(indicator = ['inflation rate', 'imports'], start_date = '2021-01-01', end_date = '2021-02-02').then(function(data){
    console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## By country and indicator

Get news by country and indicators

[/news/country/{countries}/{indicators}](https://api.tradingeconomics.com/news/country/mexico/inflation%20rate?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getNews(country = 'mexico', indicator = 'inflation rate', output_type = 'df')  
```

```python
te.getNews(country = ['mexico', 'sweden'], indicator = ['inflation rate', 'imports'], output_type = 'df')  
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getNews(country = 'mexico', indicator = 'inflation rate').then(function(data){
    console.log(data)     
});
```

```javascript
data = te.getNews(country = ['mexico', 'sweden'], indicator = ['inflation rate', 'imports']).then(function(data){
    console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## By country, indicator and date

Get news by country, indicators and date range

[/news/country/{countries}/{indicators}?c=guest:guest&d1={date}&d2={date}](https://api.tradingeconomics.com/news/country/mexico/inflation%20rate?c=guest:guest&d1=2021-02-02&d2=2021-03-03&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getNews(country = 'mexico', indicator = 'inflation rate', start_date = '2021-02-02', end_date = '2021-03-03', output_type = 'df')  
```

```python
te.getNews(country = ['mexico', 'sweden'], indicator = ['inflation rate', 'imports'], start_date = '2021-02-02', end_date = '2021-03-03', output_type = 'df')  
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getNews(country = 'mexico', indicator = 'inflation rate', start_date = '2021-01-01', end_date = '2021-02-02').then(function(data){
    console.log(data)     
});
```

```javascript
data = te.getNews(country = ['mexico', 'sweden'], indicator = ['inflation rate', 'imports'], start_date = '2021-01-01', end_date = '2021-02-02').then(function(data){
    console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## Pagination

Paginate news list specifying start index and list limit size

[/news?c=guest:guest&limit={list_size}&start={start_index}](https://api.tradingeconomics.com/news?c=guest:guest&limit=5&start=150&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getNews(start=10, limit=5)
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getNews(start = '2', limit = '4').then(function(data){
    console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## Response Fields

|                 |                                         |
|-----------------|-----------------------------------------|
| **ID**          |	Unique ID                               |
| **Title**       |	Title of the event                      |
| **Description** |	Description of the event                |
| **Date**        |	Release time and date in UTC            |
| **Country**     |	Country name                            |
| **Category**    |	Category name                           |
| **Symbol**      |	Unique symbol used by Trading Economics |
| **Url**         |	Hyperlink at Trading Economics          |
| **Importance**  |	Lowest 0 to 3 highest                   |