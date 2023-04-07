# elabapi_python.TeamgroupsApi

All URIs are relative to *https://elab.local:3148/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_teamgroup**](TeamgroupsApi.md#delete_teamgroup) | **DELETE** /teams/{id}/teamgroups/{subid} | Delete a teamgroup.
[**patch_teamgroup**](TeamgroupsApi.md#patch_teamgroup) | **PATCH** /teams/{id}/teamgroups/{subid} | Modify a teamgroup.
[**post_teamgroups**](TeamgroupsApi.md#post_teamgroups) | **POST** /teams/{id}/teamgroups | Create a new teamgroup.
[**read_team_teamgroups**](TeamgroupsApi.md#read_team_teamgroups) | **GET** /teams/{id}/teamgroups | Read teamgroups of a team.
[**read_teamgroup**](TeamgroupsApi.md#read_teamgroup) | **GET** /teams/{id}/teamgroups/{subid} | Read a teamgroup.

# **delete_teamgroup**
> delete_teamgroup(id, subid)

Delete a teamgroup.

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
api_instance = elabapi_python.TeamgroupsApi(elabapi_python.ApiClient(configuration))
id = 56 # int | ID of the team.
subid = 56 # int | ID of the teamgroup.

try:
    # Delete a teamgroup.
    api_instance.delete_teamgroup(id, subid)
except ApiException as e:
    print("Exception when calling TeamgroupsApi->delete_teamgroup: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the team. | 
 **subid** | **int**| ID of the teamgroup. | 

### Return type

void (empty response body)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **patch_teamgroup**
> Teamgroup patch_teamgroup(id, subid, body=body)

Modify a teamgroup.

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
api_instance = elabapi_python.TeamgroupsApi(elabapi_python.ApiClient(configuration))
id = 56 # int | ID of the team.
subid = 56 # int | ID of the teamgroup.
body = elabapi_python.TeamgroupsSubidBody() # TeamgroupsSubidBody | Parameters for modifying a teamgroup. (optional)

try:
    # Modify a teamgroup.
    api_response = api_instance.patch_teamgroup(id, subid, body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling TeamgroupsApi->patch_teamgroup: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the team. | 
 **subid** | **int**| ID of the teamgroup. | 
 **body** | [**TeamgroupsSubidBody**](TeamgroupsSubidBody.md)| Parameters for modifying a teamgroup. | [optional] 

### Return type

[**Teamgroup**](Teamgroup.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **post_teamgroups**
> post_teamgroups(id, body=body)

Create a new teamgroup.

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
api_instance = elabapi_python.TeamgroupsApi(elabapi_python.ApiClient(configuration))
id = 56 # int | ID of the team.
body = elabapi_python.IdTeamgroupsBody() # IdTeamgroupsBody | Parameters for creating a teamgroup. (optional)

try:
    # Create a new teamgroup.
    api_instance.post_teamgroups(id, body=body)
except ApiException as e:
    print("Exception when calling TeamgroupsApi->post_teamgroups: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the team. | 
 **body** | [**IdTeamgroupsBody**](IdTeamgroupsBody.md)| Parameters for creating a teamgroup. | [optional] 

### Return type

void (empty response body)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **read_team_teamgroups**
> list[Teamgroup] read_team_teamgroups(id)

Read teamgroups of a team.

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
api_instance = elabapi_python.TeamgroupsApi(elabapi_python.ApiClient(configuration))
id = 56 # int | ID of the team.

try:
    # Read teamgroups of a team.
    api_response = api_instance.read_team_teamgroups(id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling TeamgroupsApi->read_team_teamgroups: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the team. | 

### Return type

[**list[Teamgroup]**](Teamgroup.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **read_teamgroup**
> InlineResponse2002 read_teamgroup(id, subid)

Read a teamgroup.

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
api_instance = elabapi_python.TeamgroupsApi(elabapi_python.ApiClient(configuration))
id = 56 # int | ID of the team.
subid = 56 # int | ID of the teamgroup.

try:
    # Read a teamgroup.
    api_response = api_instance.read_teamgroup(id, subid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling TeamgroupsApi->read_teamgroup: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the team. | 
 **subid** | **int**| ID of the teamgroup. | 

### Return type

[**InlineResponse2002**](InlineResponse2002.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

