---
title: "Get started"
description: The Trading Economics Application Programming Interface (API) presentation
keywords: start using, authentication, packages, data types, status code, rate limits
redirect_from:
- /engine/getstarted-voting-app/
- /engine/getstarted-voting-app/cleanup/
- /engine/getstarted-voting-app/create-swarm/
- /engine/getstarted-voting-app/customize-app/
- /engine/getstarted-voting-app/deploy-app/
- /engine/getstarted-voting-app/node-setup/
- /engine/getstarted-voting-app/test-drive/
- /engine/getstarted/
- /engine/getstarted/last_page/
- /engine/getstarted/step_five/
- /engine/getstarted/step_four/
- /engine/getstarted/step_one/
- /engine/getstarted/step_six/
- /engine/getstarted/step_three/
- /engine/getstarted/step_two/
- /engine/quickstart/
- /engine/tutorials/
- /engine/tutorials/dockerimages/
- /engine/tutorials/dockerizing/
- /engine/tutorials/usingdocker/
- /engine/userguide/containers/dockerimages/
- /engine/userguide/dockerimages/
- /engine/userguide/intro/
- /get-started/part1/
- /get-started/part5/
- /get-started/part6/
- /getstarted/
- /getting-started/
- /learn/
- /linux/last_page/
- /linux/started/
- /linux/step_four/
- /linux/step_one/
- /linux/step_six/
- /linux/step_three/
- /linux/step_two/
- /mac/last_page/
- /mac/started/
- /mac/step_four/
- /mac/step_one/
- /mac/step_six/
- /mac/step_three/
- /mac/step_two/
- /userguide/dockerimages/
- /userguide/dockerrepos/
- /windows/last_page/
- /windows/started/
- /windows/step_four/
- /windows/step_one/
- /windows/step_six/
- /windows/step_three/
- /windows/step_two/
---

The basics steps to start using Trading Economics API. There is two ways of using the API: endpoints or packages. Endpoint is a URL wich, with the right parameters, returns a specific data. Trading Economics API uses differents endpoints to provide several data. Users can also download Trading Economics API packages to easily integrate it to its projects. The packages are available for Python and Node.js.

## The Documentation

Trading Economics API Documentation provides a sample of data for a specific topic, using endpoints and code line from the packages.
Each section (menu on the left) has its related endpoints and code to make it easier to find. Some sections also has a Response Fields table.<br>
The endpoint shows how parameters are passed. Clicking in the endpoint will redirect to a sample of the data.
The code line is displayed on the selected language and is ready to use. Simply copy and paste it in your project.

## Authentication

The API provides different methods of authorization. Each request made against API must be supplied with authentication credentials.

Note: without an API key all requests will return the default sample data.

### Endpoint

Authorization parameters must be provided in the URL query or in the Request Reader.

```curl -i "https://api.tradingeconomics.com/country/mexico/?client=guest:guest"```

Using Headers auth:

```curl -i "https://api.tradingeconomics.com/country/mexico/" -H "Authorization: Client guest:guest"```

### Packages 

{% tabs log %}

{% tab log python %}
You can get Python from: <a href="https://www.python.org/downloads/" target="_blank">python.org/downloads <i class='fa-solid fa-up-right-from-square'></i></a>.
Then you need to install the <b>tradingeconomics package</b>.<br>
Install the tradingeconomics package using pip, a package management system used to install and manage software packages written in Python. In Windows Command Prompt or Linux bash type:

```python
pip3 install tradingeconomics
```

To start using the Trading Economics Python package, open the python command line, and type:

```python
import tradingeconomics as te
te.login('Your_Key:Your_Secret')
```

If you don’t have an APIkey and just want to try a demo of our API:

```python
te.login()
```

{% endtab %}

{% tab log node %}
You can get Node.js from: <a href="https://nodejs.org/en/download/" target="_blank">nodejs.org/en/download <i class='fa-solid fa-up-right-from-square'></i></a>.
Then you need to install the <b>tradingeconomics package</b>.<br>
In Windows Command Prompt or Linux bash type:

```javascript
npm install tradingeconomics
```

To start using the Trading Economics Node package:

```javascript
const te = require('tradingeconomics');
te.login('client_key');
```

If you don’t have an APIkey and just want to try a demo of our API:

```javascript
te.login()
```
{% endtab %}

{% endtabs %}

You can get a test key at [User dashboard](http://developer.tradingeconomics.com).

## GitHub

You can look for other examples on how to use our API in different programming languages, in our [Github](https://github.com/tradingeconomics/tradingeconomics) repository.

## Data Types

You can request data in several formats:

- json

    https://api.tradingeconomics.com/historical/country/mexico/indicator/gdp?c=guest:guest&f=json

- xml

    https://api.tradingeconomics.com/historical/country/mexico/indicator/gdp?c=guest:guest&f=xml

- csv

    https://api.tradingeconomics.com/historical/country/mexico/indicator/gdp?c=guest:guest&f=csv

## Status codes

- 200 - OK
- 401 - Unauthorized (The user doesn’t have an access, client key missing or wrong)
- 403 - Forbidden (The user hit the maximum limit of downloads or was blocked)
- 400 - Bad Request (Some error with a request, like a typo, wrong parameter, etc.)
- 409 - Conflict (Throttle, to many requests per second, beyond the API limit - 1 request per second)

## Rate Limits

- API calls for historical data have a maximum limitation of 10000 rows.
- PI calls for the Economic Calendar have a maximum limitation of 2500 rows.
- One API call is limited to 260 characters.
- There is a general limitation of 1 request per second.


