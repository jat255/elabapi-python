# elabapi_python.UsersApi

All URIs are relative to *https://elab.local:3148/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**patch_user**](UsersApi.md#patch_user) | **PATCH** /users/{id} | Modify a user.
[**post_user**](UsersApi.md#post_user) | **POST** /users | Create a new user.
[**read_user**](UsersApi.md#read_user) | **GET** /users/{id} | Read information of a user.
[**read_users**](UsersApi.md#read_users) | **GET** /users | Read users from instance.

# **patch_user**
> Users patch_user(id, body=body)

Modify a user.

Note: it is possible to use \"me\" instead of the userid to access the user of the API key. 

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
api_instance = elabapi_python.UsersApi(elabapi_python.ApiClient(configuration))
id = elabapi_python.Id1() # Id1 | ID of the user or `me`.
body = elabapi_python.UsersIdBody() # UsersIdBody | Parameters for modifying a user. (optional)

try:
    # Modify a user.
    api_response = api_instance.patch_user(id, body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling UsersApi->patch_user: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | [**Id1**](.md)| ID of the user or &#x60;me&#x60;. | 
 **body** | [**UsersIdBody**](UsersIdBody.md)| Parameters for modifying a user. | [optional] 

### Return type

[**Users**](Users.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **post_user**
> post_user(body=body)

Create a new user.

An Admin can create a user in its own team only. A sysadmin can specify the team. 

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
api_instance = elabapi_python.UsersApi(elabapi_python.ApiClient(configuration))
body = elabapi_python.UsersBody() # UsersBody | Parameters for creating a user. (optional)

try:
    # Create a new user.
    api_instance.post_user(body=body)
except ApiException as e:
    print("Exception when calling UsersApi->post_user: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**UsersBody**](UsersBody.md)| Parameters for creating a user. | [optional] 

### Return type

void (empty response body)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **read_user**
> Users read_user(id)

Read information of a user.

Note: it is possible to use \"me\" instead of the userid to access the user of the API key. 

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
api_instance = elabapi_python.UsersApi(elabapi_python.ApiClient(configuration))
id = elabapi_python.Id1() # Id1 | ID of the user or `me`.

try:
    # Read information of a user.
    api_response = api_instance.read_user(id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling UsersApi->read_user: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | [**Id1**](.md)| ID of the user or &#x60;me&#x60;. | 

### Return type

[**Users**](Users.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **read_users**
> list[Users] read_users()

Read users from instance.

If Sysadmin all users will be shown. If Admin only the users from the team. Normal users will be shown an error.

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
api_instance = elabapi_python.UsersApi(elabapi_python.ApiClient(configuration))

try:
    # Read users from instance.
    api_response = api_instance.read_users()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling UsersApi->read_users: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**list[Users]**](Users.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

