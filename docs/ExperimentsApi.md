# elabapi_python.ExperimentsApi

All URIs are relative to *https://elab.local:3148/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_experiment**](ExperimentsApi.md#delete_experiment) | **DELETE** /experiments/{id} | Delete an experiment.
[**get_experiment**](ExperimentsApi.md#get_experiment) | **GET** /experiments/{id} | Read an experiment
[**patch_experiment**](ExperimentsApi.md#patch_experiment) | **PATCH** /experiments/{id} | Modify an experiment
[**post_experiment**](ExperimentsApi.md#post_experiment) | **POST** /experiments | Create an experiment
[**read_experiments**](ExperimentsApi.md#read_experiments) | **GET** /experiments | Read all experiments that are accessible

# **delete_experiment**
> delete_experiment(id)

Delete an experiment.

The experiment gets soft-deleted.

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
api_instance = elabapi_python.ExperimentsApi(elabapi_python.ApiClient(configuration))
id = 56 # int | ID of the experiment

try:
    # Delete an experiment.
    api_instance.delete_experiment(id)
except ApiException as e:
    print("Exception when calling ExperimentsApi->delete_experiment: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the experiment | 

### Return type

void (empty response body)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_experiment**
> Experiment get_experiment(id, format=format)

Read an experiment

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
api_instance = elabapi_python.ExperimentsApi(elabapi_python.ApiClient(configuration))
id = 56 # int | ID of the experiment
format = 'json' # str | Get the entity in a different format like csv, pdf, eln or zip. \"pdfa\" means archive pdf (PDF/A), same with \"zipa\".  (optional) (default to json)

try:
    # Read an experiment
    api_response = api_instance.get_experiment(id, format=format)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ExperimentsApi->get_experiment: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the experiment | 
 **format** | **str**| Get the entity in a different format like csv, pdf, eln or zip. \&quot;pdfa\&quot; means archive pdf (PDF/A), same with \&quot;zipa\&quot;.  | [optional] [default to json]

### Return type

[**Experiment**](Experiment.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **patch_experiment**
> Experiment patch_experiment(id, body=body)

Modify an experiment

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
api_instance = elabapi_python.ExperimentsApi(elabapi_python.ApiClient(configuration))
id = 56 # int | ID of the experiment
body = elabapi_python.ExperimentsIdBody() # ExperimentsIdBody | Parameters for patching an item (optional)

try:
    # Modify an experiment
    api_response = api_instance.patch_experiment(id, body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ExperimentsApi->patch_experiment: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the experiment | 
 **body** | [**ExperimentsIdBody**](ExperimentsIdBody.md)| Parameters for patching an item | [optional] 

### Return type

[**Experiment**](Experiment.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **post_experiment**
> post_experiment(body=body)

Create an experiment

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
api_instance = elabapi_python.ExperimentsApi(elabapi_python.ApiClient(configuration))
body = elabapi_python.ExperimentsBody() # ExperimentsBody | Parameters for creating an experiment (optional)

try:
    # Create an experiment
    api_instance.post_experiment(body=body)
except ApiException as e:
    print("Exception when calling ExperimentsApi->post_experiment: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**ExperimentsBody**](ExperimentsBody.md)| Parameters for creating an experiment | [optional] 

### Return type

void (empty response body)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **read_experiments**
> list[Experiment] read_experiments(q=q, extended=extended, related=related, cat=cat, limit=limit, offset=offset, metakey=metakey, metavalue=metavalue)

Read all experiments that are accessible

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
api_instance = elabapi_python.ExperimentsApi(elabapi_python.ApiClient(configuration))
q = 'q_example' # str | Search for a term in title, body or elabid.  (optional)
extended = 'extended_example' # str | Extended search (advanced query).  (optional)
related = 56 # int | Look only for entries linked to this item id.  (optional)
cat = 56 # int | The status id of the experiments.  (optional)
limit = 15 # int | Limit the number of results.  (optional) (default to 15)
offset = 0 # int | Skip a number of results. Use with limit to work the pagination.  (optional) (default to 0)
metakey = ['metakey_example'] # list[str] | Key search in metadata.  (optional)
metavalue = ['metavalue_example'] # list[str] | Value search in metadata.  (optional)

try:
    # Read all experiments that are accessible
    api_response = api_instance.read_experiments(q=q, extended=extended, related=related, cat=cat, limit=limit, offset=offset, metakey=metakey, metavalue=metavalue)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ExperimentsApi->read_experiments: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **q** | **str**| Search for a term in title, body or elabid.  | [optional] 
 **extended** | **str**| Extended search (advanced query).  | [optional] 
 **related** | **int**| Look only for entries linked to this item id.  | [optional] 
 **cat** | **int**| The status id of the experiments.  | [optional] 
 **limit** | **int**| Limit the number of results.  | [optional] [default to 15]
 **offset** | **int**| Skip a number of results. Use with limit to work the pagination.  | [optional] [default to 0]
 **metakey** | [**list[str]**](str.md)| Key search in metadata.  | [optional] 
 **metavalue** | [**list[str]**](str.md)| Value search in metadata.  | [optional] 

### Return type

[**list[Experiment]**](Experiment.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

