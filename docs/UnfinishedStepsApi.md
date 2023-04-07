# elabapi_python.UnfinishedStepsApi

All URIs are relative to *https://elab.local:3148/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**read_unfinished_steps**](UnfinishedStepsApi.md#read_unfinished_steps) | **GET** /unfinished_steps | Read all unfinished steps.

# **read_unfinished_steps**
> list[UnfinishedSteps] read_unfinished_steps(scope=scope)

Read all unfinished steps.

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
api_instance = elabapi_python.UnfinishedStepsApi(elabapi_python.ApiClient(configuration))
scope = 'user' # str | Set to \"team\" to extend the list to other members.  (optional) (default to user)

try:
    # Read all unfinished steps.
    api_response = api_instance.read_unfinished_steps(scope=scope)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling UnfinishedStepsApi->read_unfinished_steps: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **scope** | **str**| Set to \&quot;team\&quot; to extend the list to other members.  | [optional] [default to user]

### Return type

[**list[UnfinishedSteps]**](UnfinishedSteps.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

