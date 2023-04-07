# elabapi_python.TeamTagsApi

All URIs are relative to *https://elab.local:3148/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_team_tag**](TeamTagsApi.md#delete_team_tag) | **DELETE** /team_tags/{id} | Delete a tag.
[**patch_tags**](TeamTagsApi.md#patch_tags) | **PATCH** /team_tags | Actions on tags. 
[**patch_team_tag**](TeamTagsApi.md#patch_team_tag) | **PATCH** /team_tags/{id} | Actions on a tag. 
[**post_team_tag**](TeamTagsApi.md#post_team_tag) | **POST** /team_tags | Create a tag in the team.
[**read_team_tag**](TeamTagsApi.md#read_team_tag) | **GET** /team_tags/{id} | Read a tag.
[**read_team_tags**](TeamTagsApi.md#read_team_tags) | **GET** /team_tags | Read all tags for the team.

# **delete_team_tag**
> delete_team_tag(id)

Delete a tag.

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
api_instance = elabapi_python.TeamTagsApi(elabapi_python.ApiClient(configuration))
id = 56 # int | ID of the tag.

try:
    # Delete a tag.
    api_instance.delete_team_tag(id)
except ApiException as e:
    print("Exception when calling TeamTagsApi->delete_team_tag: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the tag. | 

### Return type

void (empty response body)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **patch_tags**
> list[Tag] patch_tags(body=body)

Actions on tags. 

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
api_instance = elabapi_python.TeamTagsApi(elabapi_python.ApiClient(configuration))
body = elabapi_python.TeamTagsBody1() # TeamTagsBody1 | Parameters for modifying team tags. (optional)

try:
    # Actions on tags. 
    api_response = api_instance.patch_tags(body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling TeamTagsApi->patch_tags: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**TeamTagsBody1**](TeamTagsBody1.md)| Parameters for modifying team tags. | [optional] 

### Return type

[**list[Tag]**](Tag.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **patch_team_tag**
> Tag patch_team_tag(id, body=body)

Actions on a tag. 

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
api_instance = elabapi_python.TeamTagsApi(elabapi_python.ApiClient(configuration))
id = 56 # int | ID of the tag.
body = elabapi_python.TeamTagsIdBody() # TeamTagsIdBody | Parameters for modifying a tag. (optional)

try:
    # Actions on a tag. 
    api_response = api_instance.patch_team_tag(id, body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling TeamTagsApi->patch_team_tag: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the tag. | 
 **body** | [**TeamTagsIdBody**](TeamTagsIdBody.md)| Parameters for modifying a tag. | [optional] 

### Return type

[**Tag**](Tag.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **post_team_tag**
> post_team_tag(body=body)

Create a tag in the team.

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
api_instance = elabapi_python.TeamTagsApi(elabapi_python.ApiClient(configuration))
body = elabapi_python.TeamTagsBody() # TeamTagsBody | Parameters for adding a tag in the team. (optional)

try:
    # Create a tag in the team.
    api_instance.post_team_tag(body=body)
except ApiException as e:
    print("Exception when calling TeamTagsApi->post_team_tag: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**TeamTagsBody**](TeamTagsBody.md)| Parameters for adding a tag in the team. | [optional] 

### Return type

void (empty response body)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **read_team_tag**
> InlineResponse2001 read_team_tag(id)

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
api_instance = elabapi_python.TeamTagsApi(elabapi_python.ApiClient(configuration))
id = 56 # int | ID of the tag.

try:
    # Read a tag.
    api_response = api_instance.read_team_tag(id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling TeamTagsApi->read_team_tag: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the tag. | 

### Return type

[**InlineResponse2001**](InlineResponse2001.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **read_team_tags**
> InlineResponse2001 read_team_tags()

Read all tags for the team.

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
api_instance = elabapi_python.TeamTagsApi(elabapi_python.ApiClient(configuration))

try:
    # Read all tags for the team.
    api_response = api_instance.read_team_tags()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling TeamTagsApi->read_team_tags: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**InlineResponse2001**](InlineResponse2001.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

