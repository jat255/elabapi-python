# elabapi_python.ItemsTypesApi

All URIs are relative to *https://elab.local:3148/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_items_type**](ItemsTypesApi.md#delete_items_type) | **DELETE** /items_types/{id} | Delete an item type.
[**get_items_type**](ItemsTypesApi.md#get_items_type) | **GET** /items_types/{id} | Read an items type
[**patch_items_type**](ItemsTypesApi.md#patch_items_type) | **PATCH** /items_types/{id} | Modify an item type
[**post_items_types**](ItemsTypesApi.md#post_items_types) | **POST** /items_types | Create an item
[**read_items_types**](ItemsTypesApi.md#read_items_types) | **GET** /items_types | Read all items_types that are accessible.

# **delete_items_type**
> delete_items_type(id)

Delete an item type.

The item gets soft-deleted.

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
api_instance = elabapi_python.ItemsTypesApi(elabapi_python.ApiClient(configuration))
id = 56 # int | ID of the items type.

try:
    # Delete an item type.
    api_instance.delete_items_type(id)
except ApiException as e:
    print("Exception when calling ItemsTypesApi->delete_items_type: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the items type. | 

### Return type

void (empty response body)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_items_type**
> ItemsType get_items_type(id)

Read an items type

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
api_instance = elabapi_python.ItemsTypesApi(elabapi_python.ApiClient(configuration))
id = 56 # int | ID of the items type.

try:
    # Read an items type
    api_response = api_instance.get_items_type(id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ItemsTypesApi->get_items_type: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the items type. | 

### Return type

[**ItemsType**](ItemsType.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **patch_items_type**
> ItemsType patch_items_type(id)

Modify an item type

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
api_instance = elabapi_python.ItemsTypesApi(elabapi_python.ApiClient(configuration))
id = 56 # int | ID of the items type.

try:
    # Modify an item type
    api_response = api_instance.patch_items_type(id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ItemsTypesApi->patch_items_type: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the items type. | 

### Return type

[**ItemsType**](ItemsType.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **post_items_types**
> post_items_types(body=body)

Create an item

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
api_instance = elabapi_python.ItemsTypesApi(elabapi_python.ApiClient(configuration))
body = elabapi_python.ItemsTypesBody() # ItemsTypesBody | Parameters for creating an item (optional)

try:
    # Create an item
    api_instance.post_items_types(body=body)
except ApiException as e:
    print("Exception when calling ItemsTypesApi->post_items_types: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**ItemsTypesBody**](ItemsTypesBody.md)| Parameters for creating an item | [optional] 

### Return type

void (empty response body)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **read_items_types**
> list[Item] read_items_types()

Read all items_types that are accessible.

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
api_instance = elabapi_python.ItemsTypesApi(elabapi_python.ApiClient(configuration))

try:
    # Read all items_types that are accessible.
    api_response = api_instance.read_items_types()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ItemsTypesApi->read_items_types: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**list[Item]**](Item.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

