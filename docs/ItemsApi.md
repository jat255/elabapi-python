# elabapi_python.ItemsApi

All URIs are relative to *https://elab.local:3148/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_item**](ItemsApi.md#delete_item) | **DELETE** /items/{id} | Delete an item.
[**get_item**](ItemsApi.md#get_item) | **GET** /items/{id} | Read an item
[**patch_item**](ItemsApi.md#patch_item) | **PATCH** /items/{id} | Modify an item
[**post_item**](ItemsApi.md#post_item) | **POST** /items | Create an item
[**read_items**](ItemsApi.md#read_items) | **GET** /items | Read all items that are accessible

# **delete_item**
> delete_item(id)

Delete an item.

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
api_instance = elabapi_python.ItemsApi(elabapi_python.ApiClient(configuration))
id = 56 # int | ID of the item

try:
    # Delete an item.
    api_instance.delete_item(id)
except ApiException as e:
    print("Exception when calling ItemsApi->delete_item: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the item | 

### Return type

void (empty response body)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_item**
> Item get_item(id, format=format)

Read an item

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
api_instance = elabapi_python.ItemsApi(elabapi_python.ApiClient(configuration))
id = 56 # int | ID of the item
format = 'json' # str | Get the entity in a different format like csv, pdf, eln or zip. \"pdfa\" means archive pdf (PDF/A), same with \"zipa\".  (optional) (default to json)

try:
    # Read an item
    api_response = api_instance.get_item(id, format=format)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ItemsApi->get_item: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the item | 
 **format** | **str**| Get the entity in a different format like csv, pdf, eln or zip. \&quot;pdfa\&quot; means archive pdf (PDF/A), same with \&quot;zipa\&quot;.  | [optional] [default to json]

### Return type

[**Item**](Item.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **patch_item**
> Item patch_item(id, body=body)

Modify an item

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
api_instance = elabapi_python.ItemsApi(elabapi_python.ApiClient(configuration))
id = 56 # int | ID of the item
body = elabapi_python.ItemsIdBody() # ItemsIdBody | Parameters for patching an item (optional)

try:
    # Modify an item
    api_response = api_instance.patch_item(id, body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ItemsApi->patch_item: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the item | 
 **body** | [**ItemsIdBody**](ItemsIdBody.md)| Parameters for patching an item | [optional] 

### Return type

[**Item**](Item.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **post_item**
> post_item(body=body)

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
api_instance = elabapi_python.ItemsApi(elabapi_python.ApiClient(configuration))
body = elabapi_python.ItemsBody() # ItemsBody | Parameters for creating an item (optional)

try:
    # Create an item
    api_instance.post_item(body=body)
except ApiException as e:
    print("Exception when calling ItemsApi->post_item: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**ItemsBody**](ItemsBody.md)| Parameters for creating an item | [optional] 

### Return type

void (empty response body)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **read_items**
> list[Item] read_items(q=q, extended=extended, cat=cat, limit=limit, offset=offset, metakey=metakey, metavalue=metavalue)

Read all items that are accessible

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
api_instance = elabapi_python.ItemsApi(elabapi_python.ApiClient(configuration))
q = 'q_example' # str | Search for a term in title, body or elabid.  (optional)
extended = 'extended_example' # str | Extended search (advanced query).  (optional)
cat = 56 # int | The category id of the items.  (optional)
limit = 15 # int | Limit the number of results.  (optional) (default to 15)
offset = 0 # int | Skip a number of results. Use with limit to work the pagination.  (optional) (default to 0)
metakey = ['metakey_example'] # list[str] | Key search in metadata.  (optional)
metavalue = ['metavalue_example'] # list[str] | Value search in metadata.  (optional)

try:
    # Read all items that are accessible
    api_response = api_instance.read_items(q=q, extended=extended, cat=cat, limit=limit, offset=offset, metakey=metakey, metavalue=metavalue)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ItemsApi->read_items: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **q** | **str**| Search for a term in title, body or elabid.  | [optional] 
 **extended** | **str**| Extended search (advanced query).  | [optional] 
 **cat** | **int**| The category id of the items.  | [optional] 
 **limit** | **int**| Limit the number of results.  | [optional] [default to 15]
 **offset** | **int**| Skip a number of results. Use with limit to work the pagination.  | [optional] [default to 0]
 **metakey** | [**list[str]**](str.md)| Key search in metadata.  | [optional] 
 **metavalue** | [**list[str]**](str.md)| Value search in metadata.  | [optional] 

### Return type

[**list[Item]**](Item.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

