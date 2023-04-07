# elabapi_python.IdpsApi

All URIs are relative to *https://elab.local:3148/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_idp**](IdpsApi.md#delete_idp) | **DELETE** /idps/{id} | Delete an idp.
[**patch_idp**](IdpsApi.md#patch_idp) | **PATCH** /idps/{id} | Actions on an idp.
[**post_idp**](IdpsApi.md#post_idp) | **POST** /idps | Create an idp.
[**read_idp**](IdpsApi.md#read_idp) | **GET** /idps/{id} | Read an idp.
[**read_idps**](IdpsApi.md#read_idps) | **GET** /idps | Read all IDPs.

# **delete_idp**
> delete_idp(id)

Delete an idp.

The idp gets deleted.

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
api_instance = elabapi_python.IdpsApi(elabapi_python.ApiClient(configuration))
id = 56 # int | ID of the idp

try:
    # Delete an idp.
    api_instance.delete_idp(id)
except ApiException as e:
    print("Exception when calling IdpsApi->delete_idp: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the idp | 

### Return type

void (empty response body)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **patch_idp**
> Idp patch_idp(id, body=body)

Actions on an idp.

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
api_instance = elabapi_python.IdpsApi(elabapi_python.ApiClient(configuration))
id = 56 # int | ID of the idp
body = elabapi_python.IdpsIdBody() # IdpsIdBody | Parameters for modifying an idp. (optional)

try:
    # Actions on an idp.
    api_response = api_instance.patch_idp(id, body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling IdpsApi->patch_idp: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the idp | 
 **body** | [**IdpsIdBody**](IdpsIdBody.md)| Parameters for modifying an idp. | [optional] 

### Return type

[**Idp**](Idp.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **post_idp**
> post_idp(body=body)

Create an idp.

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
api_instance = elabapi_python.IdpsApi(elabapi_python.ApiClient(configuration))
body = elabapi_python.IdpsBody() # IdpsBody | Parameters for creating an idp. (optional)

try:
    # Create an idp.
    api_instance.post_idp(body=body)
except ApiException as e:
    print("Exception when calling IdpsApi->post_idp: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**IdpsBody**](IdpsBody.md)| Parameters for creating an idp. | [optional] 

### Return type

void (empty response body)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **read_idp**
> Idp read_idp(id)

Read an idp.

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
api_instance = elabapi_python.IdpsApi(elabapi_python.ApiClient(configuration))
id = 56 # int | ID of the idp

try:
    # Read an idp.
    api_response = api_instance.read_idp(id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling IdpsApi->read_idp: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the idp | 

### Return type

[**Idp**](Idp.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **read_idps**
> list[Idp] read_idps()

Read all IDPs.

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
api_instance = elabapi_python.IdpsApi(elabapi_python.ApiClient(configuration))

try:
    # Read all IDPs.
    api_response = api_instance.read_idps()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling IdpsApi->read_idps: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**list[Idp]**](Idp.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

