# elabapi_python.TeamsApi

All URIs are relative to *https://elab.local:3148/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**patch_team**](TeamsApi.md#patch_team) | **PATCH** /teams/{id} | Actions on a team. 
[**post_teams**](TeamsApi.md#post_teams) | **POST** /teams | Create a new team.
[**read_team**](TeamsApi.md#read_team) | **GET** /teams/{id} | Read a team. Requires Admin permissions.
[**read_teams**](TeamsApi.md#read_teams) | **GET** /teams | Read all teams. Requires Sysadmin permissions.

# **patch_team**
> Team patch_team(id, body=body)

Actions on a team. 

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
api_instance = elabapi_python.TeamsApi(elabapi_python.ApiClient(configuration))
id = elabapi_python.Id() # Id | ID of the team or `current`.
body = elabapi_python.Team() # Team | Parameters for modifying a team. (optional)

try:
    # Actions on a team. 
    api_response = api_instance.patch_team(id, body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling TeamsApi->patch_team: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | [**Id**](.md)| ID of the team or &#x60;current&#x60;. | 
 **body** | [**Team**](Team.md)| Parameters for modifying a team. | [optional] 

### Return type

[**Team**](Team.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **post_teams**
> post_teams(body=body)

Create a new team.

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
api_instance = elabapi_python.TeamsApi(elabapi_python.ApiClient(configuration))
body = elabapi_python.TeamsBody() # TeamsBody | Parameters for creating a new team. (optional)

try:
    # Create a new team.
    api_instance.post_teams(body=body)
except ApiException as e:
    print("Exception when calling TeamsApi->post_teams: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**TeamsBody**](TeamsBody.md)| Parameters for creating a new team. | [optional] 

### Return type

void (empty response body)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **read_team**
> Team read_team(id)

Read a team. Requires Admin permissions.

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
api_instance = elabapi_python.TeamsApi(elabapi_python.ApiClient(configuration))
id = elabapi_python.Id() # Id | ID of the team or `current`.

try:
    # Read a team. Requires Admin permissions.
    api_response = api_instance.read_team(id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling TeamsApi->read_team: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | [**Id**](.md)| ID of the team or &#x60;current&#x60;. | 

### Return type

[**Team**](Team.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **read_teams**
> list[Team] read_teams()

Read all teams. Requires Sysadmin permissions.

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
api_instance = elabapi_python.TeamsApi(elabapi_python.ApiClient(configuration))

try:
    # Read all teams. Requires Sysadmin permissions.
    api_response = api_instance.read_teams()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling TeamsApi->read_teams: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**list[Team]**](Team.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

