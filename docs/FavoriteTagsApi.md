# elabapi_python.FavoriteTagsApi

All URIs are relative to *https://elab.local:3148/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_favtag**](FavoriteTagsApi.md#delete_favtag) | **DELETE** /favtags/{id} | Unfavorite a tag.
[**post_favtags**](FavoriteTagsApi.md#post_favtags) | **POST** /favtags | Add a tag as favorite.
[**read_favtags**](FavoriteTagsApi.md#read_favtags) | **GET** /favtags | Read all favorite tags for the user.

# **delete_favtag**
> delete_favtag(id)

Unfavorite a tag.

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
api_instance = elabapi_python.FavoriteTagsApi(elabapi_python.ApiClient(configuration))
id = 56 # int | ID of the tag.

try:
    # Unfavorite a tag.
    api_instance.delete_favtag(id)
except ApiException as e:
    print("Exception when calling FavoriteTagsApi->delete_favtag: %s\n" % e)
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

# **post_favtags**
> post_favtags(body=body)

Add a tag as favorite.

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
api_instance = elabapi_python.FavoriteTagsApi(elabapi_python.ApiClient(configuration))
body = elabapi_python.FavtagsBody() # FavtagsBody | Parameters for adding a favorite tag. (optional)

try:
    # Add a tag as favorite.
    api_instance.post_favtags(body=body)
except ApiException as e:
    print("Exception when calling FavoriteTagsApi->post_favtags: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**FavtagsBody**](FavtagsBody.md)| Parameters for adding a favorite tag. | [optional] 

### Return type

void (empty response body)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **read_favtags**
> InlineResponse200 read_favtags()

Read all favorite tags for the user.

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
api_instance = elabapi_python.FavoriteTagsApi(elabapi_python.ApiClient(configuration))

try:
    # Read all favorite tags for the user.
    api_response = api_instance.read_favtags()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling FavoriteTagsApi->read_favtags: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**InlineResponse200**](InlineResponse200.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

