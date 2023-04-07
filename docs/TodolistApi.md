# elabapi_python.TodolistApi

All URIs are relative to *https://elab.local:3148/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_todoitem**](TodolistApi.md#delete_todoitem) | **DELETE** /todolist/{id} | Delete a todoitem.
[**patch_todoitem**](TodolistApi.md#patch_todoitem) | **PATCH** /todolist/{id} | Actions on a todoitem. 
[**post_todolist**](TodolistApi.md#post_todolist) | **POST** /todolist | Create a todo item
[**read_todoitem**](TodolistApi.md#read_todoitem) | **GET** /todolist/{id} | Read a todo entry.
[**read_todolist**](TodolistApi.md#read_todolist) | **GET** /todolist | Read all todoitems.

# **delete_todoitem**
> delete_todoitem(id)

Delete a todoitem.

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
api_instance = elabapi_python.TodolistApi(elabapi_python.ApiClient(configuration))
id = 56 # int | ID of the todoitem.

try:
    # Delete a todoitem.
    api_instance.delete_todoitem(id)
except ApiException as e:
    print("Exception when calling TodolistApi->delete_todoitem: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the todoitem. | 

### Return type

void (empty response body)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **patch_todoitem**
> Todoitem patch_todoitem(id, body=body)

Actions on a todoitem. 

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
api_instance = elabapi_python.TodolistApi(elabapi_python.ApiClient(configuration))
id = 56 # int | ID of the todoitem.
body = elabapi_python.TodolistIdBody() # TodolistIdBody | Parameters for modifying a todoitem. (optional)

try:
    # Actions on a todoitem. 
    api_response = api_instance.patch_todoitem(id, body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling TodolistApi->patch_todoitem: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the todoitem. | 
 **body** | [**TodolistIdBody**](TodolistIdBody.md)| Parameters for modifying a todoitem. | [optional] 

### Return type

[**Todoitem**](Todoitem.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **post_todolist**
> post_todolist(body=body)

Create a todo item

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
api_instance = elabapi_python.TodolistApi(elabapi_python.ApiClient(configuration))
body = elabapi_python.TodolistBody() # TodolistBody | Parameters for creating a todoitem. (optional)

try:
    # Create a todo item
    api_instance.post_todolist(body=body)
except ApiException as e:
    print("Exception when calling TodolistApi->post_todolist: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**TodolistBody**](TodolistBody.md)| Parameters for creating a todoitem. | [optional] 

### Return type

void (empty response body)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **read_todoitem**
> Todoitem read_todoitem(id)

Read a todo entry.

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
api_instance = elabapi_python.TodolistApi(elabapi_python.ApiClient(configuration))
id = 56 # int | ID of the todoitem.

try:
    # Read a todo entry.
    api_response = api_instance.read_todoitem(id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling TodolistApi->read_todoitem: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the todoitem. | 

### Return type

[**Todoitem**](Todoitem.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **read_todolist**
> list[Todoitem] read_todolist()

Read all todoitems.

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
api_instance = elabapi_python.TodolistApi(elabapi_python.ApiClient(configuration))

try:
    # Read all todoitems.
    api_response = api_instance.read_todolist()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling TodolistApi->read_todolist: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**list[Todoitem]**](Todoitem.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

