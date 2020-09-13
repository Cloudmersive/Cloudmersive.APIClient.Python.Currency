# cloudmersive_currency_api_client.CurrencyExchangeApi

All URIs are relative to *https://api.cloudmersive.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**currency_exchange_convert_currency**](CurrencyExchangeApi.md#currency_exchange_convert_currency) | **POST** /currency/exchange-rates/convert/{source}/to/{destination} | Converts a price from the source currency into the destination currency
[**currency_exchange_get_available_currencies**](CurrencyExchangeApi.md#currency_exchange_get_available_currencies) | **POST** /currency/exchange-rates/list-available | Get a list of available currencies and corresponding countries
[**currency_exchange_get_exchange_rate**](CurrencyExchangeApi.md#currency_exchange_get_exchange_rate) | **POST** /currency/exchange-rates/get/{source}/to/{destination} | Gets the exchange rate from the source currency into the destination currency


# **currency_exchange_convert_currency**
> ConvertedCurrencyResult currency_exchange_convert_currency(source, destination, source_price)

Converts a price from the source currency into the destination currency

Automatically converts the price in the source currency into the destination currency using the latest available currency exchange rate data.

### Example
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

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **source** | **str**| Source currency three-digit code (ISO 4217), e.g. USD, EUR, etc. | 
 **destination** | **str**| Destination currency three-digit code (ISO 4217), e.g. USD, EUR, etc. | 
 **source_price** | **float**| Input price, such as 19.99 in source currency | 

### Return type

[**ConvertedCurrencyResult**](ConvertedCurrencyResult.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json
 - **Accept**: application/json, text/json, application/xml, text/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **currency_exchange_get_available_currencies**
> AvailableCurrencyResponse currency_exchange_get_available_currencies()

Get a list of available currencies and corresponding countries

Enumerates available currencies and the countries that correspond to these currencies.

### Example
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

try:
    # Get a list of available currencies and corresponding countries
    api_response = api_instance.currency_exchange_get_available_currencies()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling CurrencyExchangeApi->currency_exchange_get_available_currencies: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**AvailableCurrencyResponse**](AvailableCurrencyResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/json, application/xml, text/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **currency_exchange_get_exchange_rate**
> ExchangeRateResult currency_exchange_get_exchange_rate(source, destination)

Gets the exchange rate from the source currency into the destination currency

Automatically gets the exchange rate from the source currency into the destination currency using the latest available currency exchange rate data.

### Example
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

try:
    # Gets the exchange rate from the source currency into the destination currency
    api_response = api_instance.currency_exchange_get_exchange_rate(source, destination)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling CurrencyExchangeApi->currency_exchange_get_exchange_rate: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **source** | **str**| Source currency three-digit code (ISO 4217), e.g. USD, EUR, etc. | 
 **destination** | **str**| Destination currency three-digit code (ISO 4217), e.g. USD, EUR, etc. | 

### Return type

[**ExchangeRateResult**](ExchangeRateResult.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/json, application/xml, text/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

