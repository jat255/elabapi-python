# elabapi_python.TagsApi

All URIs are relative to *https://elab.local:3148/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_tag**](TagsApi.md#delete_tag) | **DELETE** /{entity_type}/{id}/tags/{subid} | Delete all tags.
[**patch_tag**](TagsApi.md#patch_tag) | **PATCH** /{entity_type}/{id}/tags/{subid} | Actions on a tag (like removing it from the entity). 
[**post_tag**](TagsApi.md#post_tag) | **POST** /{entity_type}/{id}/tags | Create a tag.
[**read_tag**](TagsApi.md#read_tag) | **GET** /{entity_type}/{id}/tags/{subid} | Read a tag.
[**read_tags**](TagsApi.md#read_tags) | **GET** /{entity_type}/{id}/tags | Read all tags of that entity.

# **delete_tag**
> delete_tag(entity_type, id, subid)

Delete all tags.

All the tags from that entity get removed.

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
api_instance = elabapi_python.TagsApi(elabapi_python.ApiClient(configuration))
entity_type = 'entity_type_example' # str | Entity type
id = 56 # int | ID of the entity
subid = 56 # int | ID of the tag

try:
    # Delete all tags.
    api_instance.delete_tag(entity_type, id, subid)
except ApiException as e:
    print("Exception when calling TagsApi->delete_tag: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **entity_type** | **str**| Entity type | 
 **id** | **int**| ID of the entity | 
 **subid** | **int**| ID of the tag | 

### Return type

void (empty response body)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **patch_tag**
> Tag patch_tag(entity_type, id, subid, body=body)

Actions on a tag (like removing it from the entity). 

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
api_instance = elabapi_python.TagsApi(elabapi_python.ApiClient(configuration))
entity_type = 'entity_type_example' # str | Entity type
id = 56 # int | ID of the entity
subid = 56 # int | ID of the tag
body = elabapi_python.TagsSubidBody() # TagsSubidBody | Parameters for modifying a tag (optional)

try:
    # Actions on a tag (like removing it from the entity). 
    api_response = api_instance.patch_tag(entity_type, id, subid, body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling TagsApi->patch_tag: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **entity_type** | **str**| Entity type | 
 **id** | **int**| ID of the entity | 
 **subid** | **int**| ID of the tag | 
 **body** | [**TagsSubidBody**](TagsSubidBody.md)| Parameters for modifying a tag | [optional] 

### Return type

[**Tag**](Tag.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **post_tag**
> post_tag(entity_type, id, body=body)

Create a tag.

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
api_instance = elabapi_python.TagsApi(elabapi_python.ApiClient(configuration))
entity_type = 'entity_type_example' # str | Entity type
id = 56 # int | ID of the entity
body = elabapi_python.IdTagsBody() # IdTagsBody | Parameters for creating a tag. (optional)

try:
    # Create a tag.
    api_instance.post_tag(entity_type, id, body=body)
except ApiException as e:
    print("Exception when calling TagsApi->post_tag: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **entity_type** | **str**| Entity type | 
 **id** | **int**| ID of the entity | 
 **body** | [**IdTagsBody**](IdTagsBody.md)| Parameters for creating a tag. | [optional] 

### Return type

void (empty response body)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **read_tag**
> Tag read_tag(entity_type, id, subid)

Read a tag.

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
api_instance = elabapi_python.TagsApi(elabapi_python.ApiClient(configuration))
entity_type = 'entity_type_example' # str | Entity type
id = 56 # int | ID of the entity
subid = 56 # int | ID of the tag

try:
    # Read a tag.
    api_response = api_instance.read_tag(entity_type, id, subid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling TagsApi->read_tag: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **entity_type** | **str**| Entity type | 
 **id** | **int**| ID of the entity | 
 **subid** | **int**| ID of the tag | 

### Return type

[**Tag**](Tag.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **read_tags**
> list[Tag] read_tags(entity_type, id)

Read all tags of that entity.

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
api_instance = elabapi_python.TagsApi(elabapi_python.ApiClient(configuration))
entity_type = 'entity_type_example' # str | Entity type
id = 56 # int | ID of the entity

try:
    # Read all tags of that entity.
    api_response = api_instance.read_tags(entity_type, id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling TagsApi->read_tags: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **entity_type** | **str**| Entity type | 
 **id** | **int**| ID of the entity | 

### Return type

[**list[Tag]**](Tag.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

