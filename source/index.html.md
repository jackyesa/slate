---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - php
  - shell
  - ruby
  - python
  - javascript

toc_footers:
    - <a href='https://www.paystore.asia'>Documentation Powered by Paystore</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the Paystore API. You can use our api to access Paystore API endpoints which can perform merely fetching and manipulating the data.

Currently we only support PHP language. You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.

```php

```

```ruby

```

```python

```

```shell

```

```javascript

```


# Authentication

## Login 

```php
  #Request details
 <?php 

  $retailer_id = 'demo';
  $retailer_user_id = 'demo123';
  $password = '12345678';
  $location = '6.437690,100.445460';
  $signature_key = md5($retailer_id.$retailer_user_id.$password.$secret_key);

  #Prepare data for POST request
  $data = array(
  'rid'=>$retailer_id,
  'ruid'=>$retailer_user_id,
  'password'=>$password,
  'location'=>$location,
  'signaturekey' => $signature_key
  );

  #Send the POST request with cURL
  $ch = curl_init('http://www.paystore.asia/api/retailer/api.php/v1/login/');
  curl_setopt($ch, CURLOPT_POST, true);
  curl_setopt($ch, CURLOPT_POSTFIELDS, $data);
  curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);
  $response = curl_exec($ch);
  curl_close($ch);

  #Process your response here
  echo $response;
  ?>
```

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
```

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
```

>  The above command returns JSON structured like this: 

```json
{
    "code": 200,
    "status": true,
    "message": "Logged in successfully",
    "data": {
        "token": "utqMdJMHUn_1539260710"
    }
}
```

This endpoint authenticate user and generate token upon sucess.

### HTTP Request

`POST http://www.paystore.asia/api/retailer/api.php/v1/login/`

### Query Parameters

Parameter | Mandatory | Example | Description
--------- | ------- | ------- | -----------
rid | yes | demo | Retailer id
ruid | yes | demo123 | Retailer user id
password | yes | 12345678 | password of the retailer user
location | yes | 6.437690,100.445460 | latitude and longitude of your location
signaturekey | yes | 9dd664963a537601f44433b561adb76a | unique key generated



# Account Management

## Check credit balance

```php

```

```ruby

```

```python

```

```shell

```

```javascript

```

>  The above command returns JSON structured like this: 

```json

```

This endpoint retrieves account balance for user.

### HTTP Request

`POST http://www.paystore.asia/api/retailer/api.php/v1/creditbalance/`

### Query Parameters

Parameter | Mandatory | Example | Description
--------- | ------- | ------- | -----------
token | yes | utqMdJMHUn_1539260710 | unique token key

# Product

## Retreive product list

```php

```

```ruby

```

```python

```

```shell

```

```javascript

```

>  The above command returns JSON structured like this: 

```json

```

This endpoint retrieves account balance for user.

### HTTP Request

`POST http://www.paystore.asia/api/retailer/api.php/v1/productlist/`

### Query Parameters

Parameter | Mandatory | Example | Description
--------- | ------- | ------- | -----------
token | yes | utqMdJMHUn_1539260710 | unique token key
product | no | DIGI05 | product code
page | no | 1 | starting number for pagination


# Order

## Make An Order 

```php

```

```ruby

```

```python

```

```shell

```

```javascript

```

>  The above command returns JSON structured like this: 

```json

```

This endpoint order physical product.

### HTTP Request

`POST http://www.paystore.asia/api/retailer/api.php/v1/order/`

### Query Parameters

Parameter | Mandatory | Example | Description
--------- | ------- | ------- | -----------
token | yes | utqMdJMHUn_1539260710 | unique token key
product | yes | DIGI05 | product code
quantity | yes | 1 | number of unit to purchase, If telco reload or bill payment service will be as default value
name | depend on product | Jacky | It require when some telco reload or bill payment service for validation purpose
mobilenumber | depend on product | 60126357416 | It require when some telco reload or bill payment service for validation purpose





