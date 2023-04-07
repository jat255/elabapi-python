# elabapi_python.StatusApi

All URIs are relative to *https://elab.local:3148/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_status**](StatusApi.md#delete_status) | **DELETE** /teams/{id}/status/{subid} | Delete a status.
[**patch_status**](StatusApi.md#patch_status) | **PATCH** /teams/{id}/status/{subid} | Modify a status.
[**post_team_one_status**](StatusApi.md#post_team_one_status) | **POST** /teams/{id}/status | Create a new status.
[**read_team_one_status**](StatusApi.md#read_team_one_status) | **GET** /teams/{id}/status/{subid} | Read a status.
[**read_team_status**](StatusApi.md#read_team_status) | **GET** /teams/{id}/status | Read status of a team.

# **delete_status**
> delete_status(id, subid)

Delete a status.

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
api_instance = elabapi_python.StatusApi(elabapi_python.ApiClient(configuration))
id = 56 # int | ID of the team.
subid = 56 # int | ID of the status

try:
    # Delete a status.
    api_instance.delete_status(id, subid)
except ApiException as e:
    print("Exception when calling StatusApi->delete_status: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the team. | 
 **subid** | **int**| ID of the status | 

### Return type

void (empty response body)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **patch_status**
> Status patch_status(id, subid, body=body)

Modify a status.

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
api_instance = elabapi_python.StatusApi(elabapi_python.ApiClient(configuration))
id = 56 # int | ID of the team.
subid = 56 # int | ID of the status
body = elabapi_python.Status() # Status | Parameters for modifying a status. (optional)

try:
    # Modify a status.
    api_response = api_instance.patch_status(id, subid, body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling StatusApi->patch_status: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the team. | 
 **subid** | **int**| ID of the status | 
 **body** | [**Status**](Status.md)| Parameters for modifying a status. | [optional] 

### Return type

[**Status**](Status.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **post_team_one_status**
> post_team_one_status(id, body=body)

Create a new status.

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
api_instance = elabapi_python.StatusApi(elabapi_python.ApiClient(configuration))
id = 56 # int | ID of the team.
body = elabapi_python.IdStatusBody() # IdStatusBody | Parameters for creating a status. (optional)

try:
    # Create a new status.
    api_instance.post_team_one_status(id, body=body)
except ApiException as e:
    print("Exception when calling StatusApi->post_team_one_status: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the team. | 
 **body** | [**IdStatusBody**](IdStatusBody.md)| Parameters for creating a status. | [optional] 

### Return type

void (empty response body)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **read_team_one_status**
> Status read_team_one_status(id, subid)

Read a status.

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
api_instance = elabapi_python.StatusApi(elabapi_python.ApiClient(configuration))
id = 56 # int | ID of the team.
subid = 56 # int | ID of the status

try:
    # Read a status.
    api_response = api_instance.read_team_one_status(id, subid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling StatusApi->read_team_one_status: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the team. | 
 **subid** | **int**| ID of the status | 

### Return type

[**Status**](Status.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **read_team_status**
> list[Status] read_team_status(id)

Read status of a team.

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
api_instance = elabapi_python.StatusApi(elabapi_python.ApiClient(configuration))
id = 56 # int | ID of the team.

try:
    # Read status of a team.
    api_response = api_instance.read_team_status(id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling StatusApi->read_team_status: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the team. | 

### Return type

[**list[Status]**](Status.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

