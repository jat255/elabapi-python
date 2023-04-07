# elabapi_python.NotificationsApi

All URIs are relative to *https://elab.local:3148/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_notifications**](NotificationsApi.md#delete_notifications) | **DELETE** /users/{id}/notifications | Delete all notifications of the user.
[**patch_notification**](NotificationsApi.md#patch_notification) | **PATCH** /users/{id}/notifications/{subid} | Actions on a notification. Only changing &#x60;is_ack&#x60; column is possible. 
[**read_notification**](NotificationsApi.md#read_notification) | **GET** /users/{id}/notifications/{subid} | Read a notification.
[**read_notifications**](NotificationsApi.md#read_notifications) | **GET** /users/{id}/notifications | Read notifications of a user.

# **delete_notifications**
> delete_notifications(id)

Delete all notifications of the user.

All notifications for the user are deleted.

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
api_instance = elabapi_python.NotificationsApi(elabapi_python.ApiClient(configuration))
id = elabapi_python.Id2() # Id2 | ID of the user or `me`.

try:
    # Delete all notifications of the user.
    api_instance.delete_notifications(id)
except ApiException as e:
    print("Exception when calling NotificationsApi->delete_notifications: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | [**Id2**](.md)| ID of the user or &#x60;me&#x60;. | 

### Return type

void (empty response body)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **patch_notification**
> Notification patch_notification(id, subid)

Actions on a notification. Only changing `is_ack` column is possible. 

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
api_instance = elabapi_python.NotificationsApi(elabapi_python.ApiClient(configuration))
id = elabapi_python.Id3() # Id3 | ID of the user or `me`.
subid = 56 # int | ID of the notification.

try:
    # Actions on a notification. Only changing `is_ack` column is possible. 
    api_response = api_instance.patch_notification(id, subid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling NotificationsApi->patch_notification: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | [**Id3**](.md)| ID of the user or &#x60;me&#x60;. | 
 **subid** | **int**| ID of the notification. | 

### Return type

[**Notification**](Notification.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **read_notification**
> Notification read_notification(id, subid)

Read a notification.

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
api_instance = elabapi_python.NotificationsApi(elabapi_python.ApiClient(configuration))
id = elabapi_python.Id3() # Id3 | ID of the user or `me`.
subid = 56 # int | ID of the notification.

try:
    # Read a notification.
    api_response = api_instance.read_notification(id, subid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling NotificationsApi->read_notification: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | [**Id3**](.md)| ID of the user or &#x60;me&#x60;. | 
 **subid** | **int**| ID of the notification. | 

### Return type

[**Notification**](Notification.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **read_notifications**
> InlineResponse2003 read_notifications(id)

Read notifications of a user.

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
api_instance = elabapi_python.NotificationsApi(elabapi_python.ApiClient(configuration))
id = elabapi_python.Id2() # Id2 | ID of the user or `me`.

try:
    # Read notifications of a user.
    api_response = api_instance.read_notifications(id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling NotificationsApi->read_notifications: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | [**Id2**](.md)| ID of the user or &#x60;me&#x60;. | 

### Return type

[**InlineResponse2003**](InlineResponse2003.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

