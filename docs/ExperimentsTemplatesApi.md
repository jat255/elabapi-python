# elabapi_python.ExperimentsTemplatesApi

All URIs are relative to *https://elab.local:3148/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_experiment_template**](ExperimentsTemplatesApi.md#delete_experiment_template) | **DELETE** /experiments_templates/{id} | Delete an experiment template.
[**get_experiment_template**](ExperimentsTemplatesApi.md#get_experiment_template) | **GET** /experiments_templates/{id} | Read an experiment template
[**patch_experiment_template**](ExperimentsTemplatesApi.md#patch_experiment_template) | **PATCH** /experiments_templates/{id} | Modify an experiment template
[**post_experiment_template**](ExperimentsTemplatesApi.md#post_experiment_template) | **POST** /experiments_templates | Create an experiment template
[**read_experiments_templates**](ExperimentsTemplatesApi.md#read_experiments_templates) | **GET** /experiments_templates | Read all experiments_templates that are accessible

# **delete_experiment_template**
> delete_experiment_template(id)

Delete an experiment template.

The experiment template gets soft-deleted.

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
api_instance = elabapi_python.ExperimentsTemplatesApi(elabapi_python.ApiClient(configuration))
id = 56 # int | ID of the experiment template

try:
    # Delete an experiment template.
    api_instance.delete_experiment_template(id)
except ApiException as e:
    print("Exception when calling ExperimentsTemplatesApi->delete_experiment_template: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the experiment template | 

### Return type

void (empty response body)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_experiment_template**
> ExperimentTemplate get_experiment_template(id)

Read an experiment template

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
api_instance = elabapi_python.ExperimentsTemplatesApi(elabapi_python.ApiClient(configuration))
id = 56 # int | ID of the experiment template

try:
    # Read an experiment template
    api_response = api_instance.get_experiment_template(id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ExperimentsTemplatesApi->get_experiment_template: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the experiment template | 

### Return type

[**ExperimentTemplate**](ExperimentTemplate.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **patch_experiment_template**
> ExperimentTemplate patch_experiment_template(id, body=body)

Modify an experiment template

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
api_instance = elabapi_python.ExperimentsTemplatesApi(elabapi_python.ApiClient(configuration))
id = 56 # int | ID of the experiment template
body = elabapi_python.ExperimentsTemplatesIdBody() # ExperimentsTemplatesIdBody | Parameters for modifying an experiment template (optional)

try:
    # Modify an experiment template
    api_response = api_instance.patch_experiment_template(id, body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ExperimentsTemplatesApi->patch_experiment_template: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of the experiment template | 
 **body** | [**ExperimentsTemplatesIdBody**](ExperimentsTemplatesIdBody.md)| Parameters for modifying an experiment template | [optional] 

### Return type

[**ExperimentTemplate**](ExperimentTemplate.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **post_experiment_template**
> post_experiment_template(body=body)

Create an experiment template

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
api_instance = elabapi_python.ExperimentsTemplatesApi(elabapi_python.ApiClient(configuration))
body = elabapi_python.ExperimentsTemplatesBody() # ExperimentsTemplatesBody | Parameters for creating an experiment template (optional)

try:
    # Create an experiment template
    api_instance.post_experiment_template(body=body)
except ApiException as e:
    print("Exception when calling ExperimentsTemplatesApi->post_experiment_template: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**ExperimentsTemplatesBody**](ExperimentsTemplatesBody.md)| Parameters for creating an experiment template | [optional] 

### Return type

void (empty response body)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **read_experiments_templates**
> list[ExperimentTemplate] read_experiments_templates()

Read all experiments_templates that are accessible

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
api_instance = elabapi_python.ExperimentsTemplatesApi(elabapi_python.ApiClient(configuration))

try:
    # Read all experiments_templates that are accessible
    api_response = api_instance.read_experiments_templates()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ExperimentsTemplatesApi->read_experiments_templates: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**list[ExperimentTemplate]**](ExperimentTemplate.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

