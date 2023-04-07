# elabapi_python.LinksToExperimentsApi

All URIs are relative to *https://elab.local:3148/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_entity_experiments_link**](LinksToExperimentsApi.md#delete_entity_experiments_link) | **DELETE** /{entity_type}/{id}/experiments_links/{subid} | Delete an experiment link.
[**post_entity_experiments_links**](LinksToExperimentsApi.md#post_entity_experiments_links) | **POST** /{entity_type}/{id}/experiments_links/{subid} | Create or import a link.
[**read_entity_experiments_links**](LinksToExperimentsApi.md#read_entity_experiments_links) | **GET** /{entity_type}/{id}/experiments_links | Read all experiments links of that entity.

# **delete_entity_experiments_link**
> delete_entity_experiments_link(entity_type, id, subid)

Delete an experiment link.

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
api_instance = elabapi_python.LinksToExperimentsApi(elabapi_python.ApiClient(configuration))
entity_type = 'entity_type_example' # str | Entity type
id = 56 # int | ID of the entity
subid = 56 # int | ID of the experiment linked

try:
    # Delete an experiment link.
    api_instance.delete_entity_experiments_link(entity_type, id, subid)
except ApiException as e:
    print("Exception when calling LinksToExperimentsApi->delete_entity_experiments_link: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **entity_type** | **str**| Entity type | 
 **id** | **int**| ID of the entity | 
 **subid** | **int**| ID of the experiment linked | 

### Return type

void (empty response body)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **post_entity_experiments_links**
> post_entity_experiments_links(entity_type, id, subid, body=body)

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
api_instance = elabapi_python.LinksToExperimentsApi(elabapi_python.ApiClient(configuration))
entity_type = 'entity_type_example' # str | Entity type
id = 56 # int | ID of the entity
subid = 56 # int | ID of the experiment linked
body = elabapi_python.ExperimentsLinksSubidBody() # ExperimentsLinksSubidBody | Parameters for creating or importing a link. (optional)

try:
    # Create or import a link.
    api_instance.post_entity_experiments_links(entity_type, id, subid, body=body)
except ApiException as e:
    print("Exception when calling LinksToExperimentsApi->post_entity_experiments_links: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **entity_type** | **str**| Entity type | 
 **id** | **int**| ID of the entity | 
 **subid** | **int**| ID of the experiment linked | 
 **body** | [**ExperimentsLinksSubidBody**](ExperimentsLinksSubidBody.md)| Parameters for creating or importing a link. | [optional] 

### Return type

void (empty response body)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **read_entity_experiments_links**
> list[Link] read_entity_experiments_links(entity_type, id)

Read all experiments links of that entity.

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
api_instance = elabapi_python.LinksToExperimentsApi(elabapi_python.ApiClient(configuration))
entity_type = 'entity_type_example' # str | Entity type
id = 56 # int | ID of the entity

try:
    # Read all experiments links of that entity.
    api_response = api_instance.read_entity_experiments_links(entity_type, id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling LinksToExperimentsApi->read_entity_experiments_links: %s\n" % e)
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

