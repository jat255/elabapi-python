# elabapi_python.UploadsApi

All URIs are relative to *https://elab.local:3148/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_upload**](UploadsApi.md#delete_upload) | **DELETE** /{entity_type}/{id}/uploads/{subid} | Delete an upload.
[**patch_upload**](UploadsApi.md#patch_upload) | **PATCH** /{entity_type}/{id}/uploads/{subid} | Actions on an upload. 
[**post_upload**](UploadsApi.md#post_upload) | **POST** /{entity_type}/{id}/uploads | Create an upload.
[**post_upload_replace**](UploadsApi.md#post_upload_replace) | **POST** /{entity_type}/{id}/uploads/{subid} | Replace an existing uploaded file. The existing file will be archived and the new one will be added.
[**read_upload**](UploadsApi.md#read_upload) | **GET** /{entity_type}/{id}/uploads/{subid} | Read an upload.
[**read_uploads**](UploadsApi.md#read_uploads) | **GET** /{entity_type}/{id}/uploads | Read attached files of that entity.

# **delete_upload**
> delete_upload(entity_type, id, subid)

Delete an upload.

The upload gets deleted.

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
api_instance = elabapi_python.UploadsApi(elabapi_python.ApiClient(configuration))
entity_type = 'entity_type_example' # str | Entity type
id = 56 # int | ID of the entity
subid = 56 # int | ID of the upload

try:
    # Delete an upload.
    api_instance.delete_upload(entity_type, id, subid)
except ApiException as e:
    print("Exception when calling UploadsApi->delete_upload: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **entity_type** | **str**| Entity type | 
 **id** | **int**| ID of the entity | 
 **subid** | **int**| ID of the upload | 

### Return type

void (empty response body)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **patch_upload**
> Upload patch_upload(entity_type, id, subid, body=body)

Actions on an upload. 

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
api_instance = elabapi_python.UploadsApi(elabapi_python.ApiClient(configuration))
entity_type = 'entity_type_example' # str | Entity type
id = 56 # int | ID of the entity
subid = 56 # int | ID of the upload
body = elabapi_python.UploadsSubidBody() # UploadsSubidBody | Parameters for modifying an upload. (optional)

try:
    # Actions on an upload. 
    api_response = api_instance.patch_upload(entity_type, id, subid, body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling UploadsApi->patch_upload: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **entity_type** | **str**| Entity type | 
 **id** | **int**| ID of the entity | 
 **subid** | **int**| ID of the upload | 
 **body** | [**UploadsSubidBody**](UploadsSubidBody.md)| Parameters for modifying an upload. | [optional] 

### Return type

[**Upload**](Upload.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **post_upload**
> post_upload(entity_type, id, file=file, comment=comment)

Create an upload.

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
api_instance = elabapi_python.UploadsApi(elabapi_python.ApiClient(configuration))
entity_type = 'entity_type_example' # str | Entity type
id = 56 # int | ID of the entity
file = 'file_example' # str |  (optional)
comment = 'comment_example' # str |  (optional)

try:
    # Create an upload.
    api_instance.post_upload(entity_type, id, file=file, comment=comment)
except ApiException as e:
    print("Exception when calling UploadsApi->post_upload: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **entity_type** | **str**| Entity type | 
 **id** | **int**| ID of the entity | 
 **file** | **str**|  | [optional] 
 **comment** | **str**|  | [optional] 

### Return type

void (empty response body)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **post_upload_replace**
> post_upload_replace(entity_type, id, subid, body=body)

Replace an existing uploaded file. The existing file will be archived and the new one will be added.

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
api_instance = elabapi_python.UploadsApi(elabapi_python.ApiClient(configuration))
entity_type = 'entity_type_example' # str | Entity type
id = 56 # int | ID of the entity
subid = 56 # int | ID of the upload
body = elabapi_python.Object() # Object | Parameters for replacing an upload. (optional)

try:
    # Replace an existing uploaded file. The existing file will be archived and the new one will be added.
    api_instance.post_upload_replace(entity_type, id, subid, body=body)
except ApiException as e:
    print("Exception when calling UploadsApi->post_upload_replace: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **entity_type** | **str**| Entity type | 
 **id** | **int**| ID of the entity | 
 **subid** | **int**| ID of the upload | 
 **body** | **Object**| Parameters for replacing an upload. | [optional] 

### Return type

void (empty response body)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/octet-stream
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **read_upload**
> Upload read_upload(entity_type, id, subid, format=format)

Read an upload.

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
api_instance = elabapi_python.UploadsApi(elabapi_python.ApiClient(configuration))
entity_type = 'entity_type_example' # str | Entity type
id = 56 # int | ID of the entity
subid = 56 # int | ID of the upload
format = 'json' # str | To download the file itself, use `binary` format parameter. In python library, when downloading a file content, make sure to add ` _preload_content=False` into the call to `read_upload()`.  (optional) (default to json)

try:
    # Read an upload.
    api_response = api_instance.read_upload(entity_type, id, subid, format=format)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling UploadsApi->read_upload: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **entity_type** | **str**| Entity type | 
 **id** | **int**| ID of the entity | 
 **subid** | **int**| ID of the upload | 
 **format** | **str**| To download the file itself, use &#x60;binary&#x60; format parameter. In python library, when downloading a file content, make sure to add &#x60; _preload_content&#x3D;False&#x60; into the call to &#x60;read_upload()&#x60;.  | [optional] [default to json]

### Return type

[**Upload**](Upload.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **read_uploads**
> list[Upload] read_uploads(entity_type, id)

Read attached files of that entity.

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
api_instance = elabapi_python.UploadsApi(elabapi_python.ApiClient(configuration))
entity_type = 'entity_type_example' # str | Entity type
id = 56 # int | ID of the entity

try:
    # Read attached files of that entity.
    api_response = api_instance.read_uploads(entity_type, id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling UploadsApi->read_uploads: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **entity_type** | **str**| Entity type | 
 **id** | **int**| ID of the entity | 

### Return type

[**list[Upload]**](Upload.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

