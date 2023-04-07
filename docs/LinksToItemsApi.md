# elabapi_python.LinksToItemsApi

All URIs are relative to *https://elab.local:3148/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_entitiy_items_link**](LinksToItemsApi.md#delete_entitiy_items_link) | **DELETE** /{entity_type}/{id}/items_links/{subid} | Delete an item link.
[**post_entity_items_links**](LinksToItemsApi.md#post_entity_items_links) | **POST** /{entity_type}/{id}/items_links/{subid} | Create or import a link.
[**read_entity_items_links**](LinksToItemsApi.md#read_entity_items_links) | **GET** /{entity_type}/{id}/items_links | Read all items links of that entity.

# **delete_entitiy_items_link**
> delete_entitiy_items_link(entity_type, id, subid)

Delete an item link.

The link gets deleted.

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
api_instance = elabapi_python.LinksToItemsApi(elabapi_python.ApiClient(configuration))
entity_type = 'entity_type_example' # str | Entity type
id = 56 # int | ID of the entity
subid = 56 # int | ID of the item (link)

try:
    # Delete an item link.
    api_instance.delete_entitiy_items_link(entity_type, id, subid)
except ApiException as e:
    print("Exception when calling LinksToItemsApi->delete_entitiy_items_link: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **entity_type** | **str**| Entity type | 
 **id** | **int**| ID of the entity | 
 **subid** | **int**| ID of the item (link) | 

### Return type

void (empty response body)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **post_entity_items_links**
> post_entity_items_links(entity_type, id, subid, body=body)

Create or import a link.

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
api_instance = elabapi_python.LinksToItemsApi(elabapi_python.ApiClient(configuration))
entity_type = 'entity_type_example' # str | Entity type
id = 56 # int | ID of the entity
subid = 56 # int | ID of the item (link)
body = elabapi_python.ItemsLinksSubidBody() # ItemsLinksSubidBody | Parameters for creating or importing a link. (optional)

try:
    # Create or import a link.
    api_instance.post_entity_items_links(entity_type, id, subid, body=body)
except ApiException as e:
    print("Exception when calling LinksToItemsApi->post_entity_items_links: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **entity_type** | **str**| Entity type | 
 **id** | **int**| ID of the entity | 
 **subid** | **int**| ID of the item (link) | 
 **body** | [**ItemsLinksSubidBody**](ItemsLinksSubidBody.md)| Parameters for creating or importing a link. | [optional] 

### Return type

void (empty response body)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **read_entity_items_links**
> list[Link] read_entity_items_links(entity_type, id)

Read all items links of that entity.

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
api_instance = elabapi_python.LinksToItemsApi(elabapi_python.ApiClient(configuration))
entity_type = 'entity_type_example' # str | Entity type
id = 56 # int | ID of the entity

try:
    # Read all items links of that entity.
    api_response = api_instance.read_entity_items_links(entity_type, id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling LinksToItemsApi->read_entity_items_links: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **entity_type** | **str**| Entity type | 
 **id** | **int**| ID of the entity | 

### Return type

[**list[Link]**](Link.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

