# elabapi_python.EventsApi

All URIs are relative to *https://elab.local:3148/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_event**](EventsApi.md#delete_event) | **DELETE** /event/{id} | Delete a booking slot.
[**patch_event**](EventsApi.md#patch_event) | **PATCH** /events/{id} | Modify a booking slot. Warning: only one value (target) can be edited at a time. 
[**post_events**](EventsApi.md#post_events) | **POST** /events/{id} | Create an event for the item specified as id.
[**read_events**](EventsApi.md#read_events) | **GET** /events | Read all events in the team.

# **delete_event**
> delete_event(id)

Delete a booking slot.

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
api_instance = elabapi_python.EventsApi(elabapi_python.ApiClient(configuration))
id = 56 # int | ID of the event to modify.

try:
    # Delete a booking slot.
    api_instance.delete_event(id)
except ApiException as e:
    print("Exception when calling EventsApi->delete_event: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the event to modify. | 

### Return type

void (empty response body)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **patch_event**
> Event patch_event(id, body=body)

Modify a booking slot. Warning: only one value (target) can be edited at a time. 

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
api_instance = elabapi_python.EventsApi(elabapi_python.ApiClient(configuration))
id = 56 # int | ID of the item to book.
body = elabapi_python.EventsIdBody1() # EventsIdBody1 | Parameters for modifying an event. (optional)

try:
    # Modify a booking slot. Warning: only one value (target) can be edited at a time. 
    api_response = api_instance.patch_event(id, body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling EventsApi->patch_event: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the item to book. | 
 **body** | [**EventsIdBody1**](EventsIdBody1.md)| Parameters for modifying an event. | [optional] 

### Return type

[**Event**](Event.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **post_events**
> post_events(id, body=body)

Create an event for the item specified as id.

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
api_instance = elabapi_python.EventsApi(elabapi_python.ApiClient(configuration))
id = 56 # int | ID of the item to book.
body = elabapi_python.EventsIdBody() # EventsIdBody | Parameters for creating an event. (optional)

try:
    # Create an event for the item specified as id.
    api_instance.post_events(id, body=body)
except ApiException as e:
    print("Exception when calling EventsApi->post_events: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the item to book. | 
 **body** | [**EventsIdBody**](EventsIdBody.md)| Parameters for creating an event. | [optional] 

### Return type

void (empty response body)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **read_events**
> list[Event] read_events()

Read all events in the team.

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
api_instance = elabapi_python.EventsApi(elabapi_python.ApiClient(configuration))

try:
    # Read all events in the team.
    api_response = api_instance.read_events()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling EventsApi->read_events: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**list[Event]**](Event.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

