---
title: Events
description: Economic Calendar events data
keywords: calendar, events, economic
---

The economic calendar covers around 1600 events for more than 150 countries a month.

## All events

List all calendar events

[/calendar](https://api.tradingeconomics.com/calendar?c=guest\:guest\&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getCalendarData(output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getCalendar().then(function (data) {
  console.log(data)
});
```
{% endtab %}

{% endtabs %}

## By importance

List all calendar events by importance (1-Low, 2-Medium, 3-High)

[/calendar?importance=2](https://api.tradingeconomics.com/calendar?c=guest:guest&importance=2&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getCalendarData(importance='1', output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getCalendar(importance = '1').then(function(data){
    console.log(data)       
});
```
{% endtab %}

{% endtabs %}

## By date

List all calendar events by date

[/calendar/country/All/{yyyy-mm-dd}/{yyyy-mm-dd}](https://api.tradingeconomics.com/calendar/country/All/2016-12-02/2016-12-03?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getCalendarData(initDate='2016-02-01', endDate='2016-02-02', output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getCalendar(start_date = '2016-02-01', end_date = '2016-02-10'  ).then(function(data){
    console.log(data)     
});
```
{% endtab %}

{% endtabs %}

[/calendar/country/All/{yyyy-mm-dd}/{yyyy-mm-dd}?importance=3](https://api.tradingeconomics.com/calendar/country/All/2016-12-02/2016-12-03?c=guest:guest&importance=3&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getCalendarData(initDate='2016-02-01', endDate='2016-02-02', importance='3', output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getCalendar(start_date = '2016-02-01', end_date = '2016-02-10',importance = '3').then(function(data){
    console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## By country

List all calendar events by country

[/calendar/country/{country}](https://api.tradingeconomics.com/calendar/country/united%20states?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getCalendarData(country='united states', output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getCalendar(country = 'united states').then(function(data){
    console.log(data)     
});
```
{% endtab %}

{% endtabs %}

[/calendar/country/{countries}](https://api.tradingeconomics.com/calendar/country/united%20states,china?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getCalendarData(country=['united states','united kingdom'],output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getCalendar(country = ['united states', 'united kingdom']).then(function(data){
    console.log(data)     
});
```
{% endtab %}

{% endtabs %}

[/calendar/country/{countries}/{yyyy-mm-dd}/{yyyy-mm-dd}?importance=2](https://api.tradingeconomics.com/calendar/country/united%20states,china/2016-02-10/2016-02-11?c=guest:guest&importance=2&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getCalendarData(country=['united states','united kingdom'], initDate='2022-02-10', endDate='2022-03-15', importance='1' output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getCalendar(country = ['united states','united kingdom'], start_date = '2022-02-10', end_date = '2022-03-15', importance = '1').then(function(data){
  console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## By indicator

List all calendar events by indicator

[/calendar/indicator/{indicators}](https://api.tradingeconomics.com/calendar/indicator/inflation%20rate?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getCalendarData(category='inflation rate', output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getCalendar(indicator = 'inflation rate').then(function(data){
    console.log(data)     
});
```
{% endtab %}

{% endtabs %}

[/calendar/country/{countries}/indicator/{indicators}/{yyyy-mm-dd}/{yyyy-mm-dd}](https://api.tradingeconomics.com/calendar/country/united%20states/indicator/initial%20jobless%20claims/2016-12-01/2017-02-25?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getCalendarData(category='initial jobless claims', country='united states', initDate='2017-06-07', endDate='2017-12-31', output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getCalendar(indicator = 'inflation rate', country = ['united states','united kingdom'], start_date = '2017-06-07', end_date = '2017-12-31').then(function(data){
    console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## By group.

List all calendar events by group (interest rate, inflation, bonds, consumer, gdp, government, housing, labour, markets, money, prices, trade, business)

[/calendar/group/{group}](https://api.tradingeconomics.com/calendar/group/bonds?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getCalendarEventsByGroup(group='bonds', output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getCalendarEventsByGroup(group = 'bonds').then(function(data){
    console.log(data)     
});
```
{% endtab %}

{% endtabs %}

[/calendar/country/{country}/group/{group}/{yyy-mm-dd}/{yyy-mm-dd}](https://api.tradingeconomics.com/calendar/country/united%20states/group/bonds/2016-03-01/2018-03-03?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getCalendarEventsByGroup(group='inflation', country='united states', initDate='2023-01-01', endDate='2023-02-01', output_type='df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getCalendarEventsByGroup(group = 'inflation', country = 'china', start_date = '2018-01-01',end_date = '2023-12-01').then(function(data){
    console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## By ID

List all calendar events by calendar ID 

[/calendar/calendarid/{calendarids}](https://api.tradingeconomics.com/calendar/calendarid/174108,160025,160030?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getCalendarId(id = '174108', output_type=  'df')
```
```python
te.getCalendarId(id = ['160025',  '174108',  '160030'], output_type=  'df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getCalendar(id = '174108').then(function(data){
  console.log(data)     
});
```
```javascript
data = te.getCalendar(id = ['174108','160025','160030']).then(function(data){
    console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## By ticker

List all calendar events by calendar ticker 

[/calendar/ticker/{ticker}](https://api.tradingeconomics.com/calendar/ticker/IJCUSA,SPAINFACORD,BAHRAININFNRATE?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getCalendarData(ticker = 'IJCUSA', output_type =  'df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getCalendar(ticker = 'IJCUSA').then(function(data){
    console.log(data)     
});
```

{% endtab %}

{% endtabs %}

[/calendar/ticker/{ticker}/{yyyy-mm-dd}/{yyyy-mm-dd}](https://api.tradingeconomics.com/calendar/ticker/IJCUSA,SPAINFACORD,BAHRAININFNRATE/2018-01-01/2018-03-01?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getCalendarData(ticker = ['IJCUSA',  'SPAINFACORD',  'BAHRAININFNRATE'],  initDate='2017-06-07', endDate='2017-12-31', output_type =  'df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getCalendar(ticker = ['IJCUSA','SPAINFACORD','BAHRAININFNRATE'], start_date = '2017-06-07',end_date = '2017-12-31').then(function(data){
    console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## Updates

Get calendar latest updates (for events with a released Actual)

[/calendar/updates?c=guest:guest](https://api.tradingeconomics.com/calendar/updates?c=guest:guest&f=json)

{% tabs log %}

{% tab log python %}
```python
te.getCalendarUpdates(output_type =  'df')
```
{% endtab %}

{% tab log node %}
```javascript
data = te.getCalendarUpdates().then(function(data){
    console.log(data)     
});
```
{% endtab %}

{% endtabs %}

## Response Fields

|                 |                                                                                                                                         |
| --------------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| **Date**        |	Release time and date in UTC                                                                                                            |
| **Country**     |	Country name                                                                                                                            |
| **Category**    |	Indicator category name                                                                                                                 |
| **Event**       |	Specific event name in the calendar                                                                                                     |
| **Reference**   |	The period for which released data refers to                                                                                            |
| **Source**      |	Source of data                                                                                                                          |
| **Actual**      |	Latest released value                                                                                                                   |
| **Previous**    |	Value for the previous period after the revision (if revision is applicable)                                                            |
| **Forecast**    |	Average forecast among a representative group of economists                                                                             |
| **TEForecast**  |	TE own projections                                                                                                                      |
| **URL**         |	Hyperlink at Trading Economics                                                                                                          |
| **DateSpan**    |	0 Indicates that the time of the event is known, 1 indicates that we only know the date of event, the exact time of event is unknown    |
| **Importance**  |	1 = low, 2 = medium, 3 = high                                                                                                           |
| **LastUpdate**  |	Time when new data was inserted or changed                                                                                              |
| **Revised**     |	Value reported in the previous period after revision (if there is no revision field remains empty)                                      |
| **Ticker**      |	Unique ticker used by Trading Economics                                                                                                 |
| **Symbol**      |	Unique symbol used by Trading Economics                                                                                                 |
| **CalendarID**  |	Unique calendar ID used by Trading Economics                                                                                            |
| **OCountry***   |	Country’s original name                                                                                                                 |
| **OCategory***  |	Category’s original name                                                                                                                |
| **OEvent***     |	Event’s original name                                                                                                                   |

***Response fields only used on translated calendar queries.**