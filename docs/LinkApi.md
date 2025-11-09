# comicbagi_openapi.LinkApi

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_link**](LinkApi.md#add_link) | **POST** /rest/links | Add link.
[**delete_link**](LinkApi.md#delete_link) | **DELETE** /rest/links/{href} | Delete link.
[**get_link**](LinkApi.md#get_link) | **GET** /rest/links/{href} | Get link.
[**list_link**](LinkApi.md#list_link) | **GET** /rest/links | List link.
[**update_link**](LinkApi.md#update_link) | **PATCH** /rest/links/{href} | Update link.


# **add_link**
> Link add_link(new_link)

Add link.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import comicbagi_openapi
from comicbagi_openapi.models.link import Link
from comicbagi_openapi.models.new_link import NewLink
from comicbagi_openapi.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to /api
# See configuration.py for a list of all supported configuration parameters.
configuration = comicbagi_openapi.Configuration(
    host = "/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT): BearerAuth
configuration = comicbagi_openapi.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with comicbagi_openapi.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = comicbagi_openapi.LinkApi(api_client)
    new_link = comicbagi_openapi.NewLink() # NewLink | 

    try:
        # Add link.
        api_response = api_instance.add_link(new_link)
        print("The response of LinkApi->add_link:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LinkApi->add_link: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **new_link** | [**NewLink**](NewLink.md)|  | 

### Return type

[**Link**](Link.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Link added. |  * Location -  <br>  |
**0** | Unexpected error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_link**
> delete_link(href)

Delete link.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import comicbagi_openapi
from comicbagi_openapi.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to /api
# See configuration.py for a list of all supported configuration parameters.
configuration = comicbagi_openapi.Configuration(
    host = "/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT): BearerAuth
configuration = comicbagi_openapi.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with comicbagi_openapi.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = comicbagi_openapi.LinkApi(api_client)
    href = 'href_example' # str | 

    try:
        # Delete link.
        api_instance.delete_link(href)
    except Exception as e:
        print("Exception when calling LinkApi->delete_link: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **href** | **str**|  | 

### Return type

void (empty response body)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Link deleted. |  -  |
**0** | Unexpected error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_link**
> Link get_link(href)

Get link.

### Example


```python
import comicbagi_openapi
from comicbagi_openapi.models.link import Link
from comicbagi_openapi.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to /api
# See configuration.py for a list of all supported configuration parameters.
configuration = comicbagi_openapi.Configuration(
    host = "/api"
)


# Enter a context with an instance of the API client
with comicbagi_openapi.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = comicbagi_openapi.LinkApi(api_client)
    href = 'href_example' # str | 

    try:
        # Get link.
        api_response = api_instance.get_link(href)
        print("The response of LinkApi->get_link:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LinkApi->get_link: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **href** | **str**|  | 

### Return type

[**Link**](Link.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Link gets. |  -  |
**0** | Unexpected error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_link**
> List[Link] list_link(page=page, limit=limit, order=order, order_by=order_by, website_host=website_host, relative_reference=relative_reference, href=href, unredact=unredact)

List link.

### Example


```python
import comicbagi_openapi
from comicbagi_openapi.models.link import Link
from comicbagi_openapi.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to /api
# See configuration.py for a list of all supported configuration parameters.
configuration = comicbagi_openapi.Configuration(
    host = "/api"
)


# Enter a context with an instance of the API client
with comicbagi_openapi.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = comicbagi_openapi.LinkApi(api_client)
    page = 56 # int |  (optional)
    limit = 56 # int |  (optional)
    order = 'order_example' # str |  (optional)
    order_by = ['order_by_example'] # List[str] |  (optional)
    website_host = ['website_host_example'] # List[str] |  (optional)
    relative_reference = ['relative_reference_example'] # List[str] |  (optional)
    href = ['href_example'] # List[str] |  (optional)
    unredact = ['unredact_example'] # List[str] |  (optional)

    try:
        # List link.
        api_response = api_instance.list_link(page=page, limit=limit, order=order, order_by=order_by, website_host=website_host, relative_reference=relative_reference, href=href, unredact=unredact)
        print("The response of LinkApi->list_link:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LinkApi->list_link: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **limit** | **int**|  | [optional] 
 **order** | **str**|  | [optional] 
 **order_by** | [**List[str]**](str.md)|  | [optional] 
 **website_host** | [**List[str]**](str.md)|  | [optional] 
 **relative_reference** | [**List[str]**](str.md)|  | [optional] 
 **href** | [**List[str]**](str.md)|  | [optional] 
 **unredact** | [**List[str]**](str.md)|  | [optional] 

### Return type

[**List[Link]**](Link.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Link list. |  * X-Total-Count -  <br>  * X-Pagination-Limit -  <br>  |
**0** | Unexpected error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_link**
> Link update_link(href, set_link)

Update link.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import comicbagi_openapi
from comicbagi_openapi.models.link import Link
from comicbagi_openapi.models.set_link import SetLink
from comicbagi_openapi.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to /api
# See configuration.py for a list of all supported configuration parameters.
configuration = comicbagi_openapi.Configuration(
    host = "/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT): BearerAuth
configuration = comicbagi_openapi.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with comicbagi_openapi.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = comicbagi_openapi.LinkApi(api_client)
    href = 'href_example' # str | 
    set_link = comicbagi_openapi.SetLink() # SetLink | 

    try:
        # Update link.
        api_response = api_instance.update_link(href, set_link)
        print("The response of LinkApi->update_link:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LinkApi->update_link: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **href** | **str**|  | 
 **set_link** | [**SetLink**](SetLink.md)|  | 

### Return type

[**Link**](Link.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Link updated. |  * Location -  <br>  |
**204** | Link unmodified. |  -  |
**0** | Unexpected error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

