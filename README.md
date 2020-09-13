# cloudmersive_currency_api_client
The currency APIs help you retrieve exchange rates and convert prices between currencies easily.

This Python package provides a native API client for [Cloudmersive Currency API](https://www.cloudmersive.com/currency-api)

- API version: v1
- Package version: 3.0.1
- Build package: io.swagger.codegen.languages.PythonClientCodegen

## Requirements.

Python 2.7 and 3.4+

## Installation & Usage
### pip install

If the python package is hosted on Github, you can install directly from Github

```sh
pip install git+https://github.com/GIT_USER_ID/GIT_REPO_ID.git
```
(you may need to run `pip` with root permission: `sudo pip install git+https://github.com/GIT_USER_ID/GIT_REPO_ID.git`)

Then import the package:
```python
import cloudmersive_currency_api_client 
```

### Setuptools

Install via [Setuptools](http://pypi.python.org/pypi/setuptools).

```sh
python setup.py install --user
```
(or `sudo python setup.py install` to install the package for all users)

Then import the package:
```python
import cloudmersive_currency_api_client
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```python
from __future__ import print_function
import time
import cloudmersive_currency_api_client
from cloudmersive_currency_api_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: Apikey
configuration = cloudmersive_currency_api_client.Configuration()
configuration.api_key['Apikey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['Apikey'] = 'Bearer'

# create an instance of the API class
api_instance = cloudmersive_currency_api_client.CurrencyExchangeApi(cloudmersive_currency_api_client.ApiClient(configuration))
source = 'source_example' # str | Source currency three-digit code (ISO 4217), e.g. USD, EUR, etc.
destination = 'destination_example' # str | Destination currency three-digit code (ISO 4217), e.g. USD, EUR, etc.
source_price = 1.2 # float | Input price, such as 19.99 in source currency

try:
    # Converts a price from the source currency into the destination currency
    api_response = api_instance.currency_exchange_convert_currency(source, destination, source_price)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling CurrencyExchangeApi->currency_exchange_convert_currency: %s\n" % e)

```

## Documentation for API Endpoints

All URIs are relative to *https://api.cloudmersive.com*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*CurrencyExchangeApi* | [**currency_exchange_convert_currency**](docs/CurrencyExchangeApi.md#currency_exchange_convert_currency) | **POST** /currency/exchange-rates/convert/{source}/to/{destination} | Converts a price from the source currency into the destination currency
*CurrencyExchangeApi* | [**currency_exchange_get_available_currencies**](docs/CurrencyExchangeApi.md#currency_exchange_get_available_currencies) | **POST** /currency/exchange-rates/list-available | Get a list of available currencies and corresponding countries
*CurrencyExchangeApi* | [**currency_exchange_get_exchange_rate**](docs/CurrencyExchangeApi.md#currency_exchange_get_exchange_rate) | **POST** /currency/exchange-rates/get/{source}/to/{destination} | Gets the exchange rate from the source currency into the destination currency


## Documentation For Models

 - [AvailableCurrency](docs/AvailableCurrency.md)
 - [AvailableCurrencyResponse](docs/AvailableCurrencyResponse.md)
 - [ConvertedCurrencyResult](docs/ConvertedCurrencyResult.md)
 - [ExchangeRateResult](docs/ExchangeRateResult.md)


## Documentation For Authorization


## Apikey

- **Type**: API key
- **API key parameter name**: Apikey
- **Location**: HTTP header


## Author



