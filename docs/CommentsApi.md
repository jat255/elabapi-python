# elabapi_python.CommentsApi

All URIs are relative to *https://elab.local:3148/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_entity_comment**](CommentsApi.md#delete_entity_comment) | **DELETE** /{entity_type}/{id}/comments/{subid} | Delete an entity comment.
[**patch_entity_comment**](CommentsApi.md#patch_entity_comment) | **PATCH** /{entity_type}/{id}/comments/{subid} | Modify an entity comment.
[**post_entity_comments**](CommentsApi.md#post_entity_comments) | **POST** /{entity_type}/{id}/comments | Create a comment.
[**read_entity_comment**](CommentsApi.md#read_entity_comment) | **GET** /{entity_type}/{id}/comments/{subid} | Read a comment of that entity.
[**read_entity_comments**](CommentsApi.md#read_entity_comments) | **GET** /{entity_type}/{id}/comments | Read all comments of that entity.

# **delete_entity_comment**
> delete_entity_comment(entity_type, id, subid)

Delete an entity comment.

The comment gets deleted.

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
api_instance = elabapi_python.CommentsApi(elabapi_python.ApiClient(configuration))
entity_type = 'entity_type_example' # str | Entity type
id = 56 # int | ID of the entity
subid = 56 # int | ID of the comment

try:
    # Delete an entity comment.
    api_instance.delete_entity_comment(entity_type, id, subid)
except ApiException as e:
    print("Exception when calling CommentsApi->delete_entity_comment: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **entity_type** | **str**| Entity type | 
 **id** | **int**| ID of the entity | 
 **subid** | **int**| ID of the comment | 

### Return type

void (empty response body)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **patch_entity_comment**
> Comment patch_entity_comment(entity_type, id, subid, body=body)

Modify an entity comment.

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
api_instance = elabapi_python.CommentsApi(elabapi_python.ApiClient(configuration))
entity_type = 'entity_type_example' # str | Entity type
id = 56 # int | ID of the entity
subid = 56 # int | ID of the comment
body = elabapi_python.Comment() # Comment | Parameters for patching an entity comment. (optional)

try:
    # Modify an entity comment.
    api_response = api_instance.patch_entity_comment(entity_type, id, subid, body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling CommentsApi->patch_entity_comment: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **entity_type** | **str**| Entity type | 
 **id** | **int**| ID of the entity | 
 **subid** | **int**| ID of the comment | 
 **body** | [**Comment**](Comment.md)| Parameters for patching an entity comment. | [optional] 

### Return type

[**Comment**](Comment.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **post_entity_comments**
> post_entity_comments(entity_type, id, body=body)

Create a comment.

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
api_instance = elabapi_python.CommentsApi(elabapi_python.ApiClient(configuration))
entity_type = 'entity_type_example' # str | Entity type
id = 56 # int | ID of the entity
body = elabapi_python.IdCommentsBody() # IdCommentsBody | Parameters for creating a comment (optional)

try:
    # Create a comment.
    api_instance.post_entity_comments(entity_type, id, body=body)
except ApiException as e:
    print("Exception when calling CommentsApi->post_entity_comments: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **entity_type** | **str**| Entity type | 
 **id** | **int**| ID of the entity | 
 **body** | [**IdCommentsBody**](IdCommentsBody.md)| Parameters for creating a comment | [optional] 

### Return type

void (empty response body)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **read_entity_comment**
> Comment read_entity_comment(entity_type, id, subid)

Read a comment of that entity.

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
api_instance = elabapi_python.CommentsApi(elabapi_python.ApiClient(configuration))
entity_type = 'entity_type_example' # str | Entity type
id = 56 # int | ID of the entity
subid = 56 # int | ID of the comment

try:
    # Read a comment of that entity.
    api_response = api_instance.read_entity_comment(entity_type, id, subid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling CommentsApi->read_entity_comment: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **entity_type** | **str**| Entity type | 
 **id** | **int**| ID of the entity | 
 **subid** | **int**| ID of the comment | 

### Return type

[**Comment**](Comment.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **read_entity_comments**
> list[Comment] read_entity_comments(entity_type, id)

Read all comments of that entity.

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
api_instance = elabapi_python.CommentsApi(elabapi_python.ApiClient(configuration))
entity_type = 'entity_type_example' # str | Entity type
id = 56 # int | ID of the entity

try:
    # Read all comments of that entity.
    api_response = api_instance.read_entity_comments(entity_type, id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling CommentsApi->read_entity_comments: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **entity_type** | **str**| Entity type | 
 **id** | **int**| ID of the entity | 

### Return type

[**list[Comment]**](Comment.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

