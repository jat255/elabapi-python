# elabapi_python.ApiKeysApi

All URIs are relative to *https://elab.local:3148/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_apikey**](ApiKeysApi.md#delete_apikey) | **DELETE** /apikeys/{id} | Delete an API key.
[**get_apikeys**](ApiKeysApi.md#get_apikeys) | **GET** /apikeys | Read API keys
[**post_apikeys**](ApiKeysApi.md#post_apikeys) | **POST** /apikeys | Create an API key

# **delete_apikey**
> delete_apikey(id)

Delete an API key.

Delete an API key

### Example
```python
from __future__ import print_function
import time
import elabapi_python
from elabapi_python.rest import ApiException
from pprint import pprint

# Configure API key authorization: token
configuration = elabapi_python.Configuration()
configuration.api_key['Authorization'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['Authorization'] = 'Bearer'

# create an instance of the API class
api_instance = elabapi_python.ApiKeysApi(elabapi_python.ApiClient(configuration))
id = 56 # int | ID of the API key

try:
    # Delete an API key.
    api_instance.delete_apikey(id)
except ApiException as e:
    print("Exception when calling ApiKeysApi->delete_apikey: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the API key | 

### Return type

void (empty response body)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_apikeys**
> Apikey get_apikeys()

Read API keys

Get list of API keys for currently logged in user.

### Example
```python
from __future__ import print_function
import time
import elabapi_python
from elabapi_python.rest import ApiException
from pprint import pprint

# Configure API key authorization: token
configuration = elabapi_python.Configuration()
configuration.api_key['Authorization'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['Authorization'] = 'Bearer'

# create an instance of the API class
api_instance = elabapi_python.ApiKeysApi(elabapi_python.ApiClient(configuration))

try:
    # Read API keys
    api_response = api_instance.get_apikeys()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ApiKeysApi->get_apikeys: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**Apikey**](Apikey.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **post_apikeys**
> post_apikeys(body=body)

Create an API key

Create an API key. The cleartext key is sent back in the location header.

### Example
```python
from __future__ import print_function
import time
import elabapi_python
from elabapi_python.rest import ApiException
from pprint import pprint

# Configure API key authorization: token
configuration = elabapi_python.Configuration()
configuration.api_key['Authorization'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['Authorization'] = 'Bearer'

# create an instance of the API class
api_instance = elabapi_python.ApiKeysApi(elabapi_python.ApiClient(configuration))
body = elabapi_python.ApikeysBody() # ApikeysBody |  (optional)

try:
    # Create an API key
    api_instance.post_apikeys(body=body)
except ApiException as e:
    print("Exception when calling ApiKeysApi->post_apikeys: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**ApikeysBody**](ApikeysBody.md)|  | [optional] 

### Return type

void (empty response body)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

