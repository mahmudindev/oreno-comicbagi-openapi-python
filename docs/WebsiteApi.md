# comicbagi_openapi.WebsiteApi

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_website**](WebsiteApi.md#add_website) | **POST** /rest/websites | Add website.
[**delete_website**](WebsiteApi.md#delete_website) | **DELETE** /rest/websites/{host} | Delete website.
[**get_website**](WebsiteApi.md#get_website) | **GET** /rest/websites/{host} | Get website.
[**list_website**](WebsiteApi.md#list_website) | **GET** /rest/websites | List website.
[**update_website**](WebsiteApi.md#update_website) | **PATCH** /rest/websites/{host} | Update website.


# **add_website**
> Website add_website(new_website)

Add website.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import comicbagi_openapi
from comicbagi_openapi.models.new_website import NewWebsite
from comicbagi_openapi.models.website import Website
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
    api_instance = comicbagi_openapi.WebsiteApi(api_client)
    new_website = comicbagi_openapi.NewWebsite() # NewWebsite | 

    try:
        # Add website.
        api_response = api_instance.add_website(new_website)
        print("The response of WebsiteApi->add_website:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsiteApi->add_website: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **new_website** | [**NewWebsite**](NewWebsite.md)|  | 

### Return type

[**Website**](Website.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Website added. |  * Location -  <br>  |
**0** | Unexpected error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_website**
> delete_website(host)

Delete website.

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
    api_instance = comicbagi_openapi.WebsiteApi(api_client)
    host = 'host_example' # str | 

    try:
        # Delete website.
        api_instance.delete_website(host)
    except Exception as e:
        print("Exception when calling WebsiteApi->delete_website: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **host** | **str**|  | 

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
**204** | Website deleted. |  -  |
**0** | Unexpected error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_website**
> Website get_website(host)

Get website.

### Example


```python
import comicbagi_openapi
from comicbagi_openapi.models.website import Website
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
    api_instance = comicbagi_openapi.WebsiteApi(api_client)
    host = 'host_example' # str | 

    try:
        # Get website.
        api_response = api_instance.get_website(host)
        print("The response of WebsiteApi->get_website:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsiteApi->get_website: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **host** | **str**|  | 

### Return type

[**Website**](Website.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Website gets. |  -  |
**0** | Unexpected error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_website**
> List[Website] list_website(page=page, limit=limit, order=order, order_by=order_by, unredact=unredact)

List website.

### Example


```python
import comicbagi_openapi
from comicbagi_openapi.models.website import Website
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
    api_instance = comicbagi_openapi.WebsiteApi(api_client)
    page = 56 # int |  (optional)
    limit = 56 # int |  (optional)
    order = 'order_example' # str |  (optional)
    order_by = ['order_by_example'] # List[str] |  (optional)
    unredact = ['unredact_example'] # List[str] |  (optional)

    try:
        # List website.
        api_response = api_instance.list_website(page=page, limit=limit, order=order, order_by=order_by, unredact=unredact)
        print("The response of WebsiteApi->list_website:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsiteApi->list_website: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **limit** | **int**|  | [optional] 
 **order** | **str**|  | [optional] 
 **order_by** | [**List[str]**](str.md)|  | [optional] 
 **unredact** | [**List[str]**](str.md)|  | [optional] 

### Return type

[**List[Website]**](Website.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Website list. |  * X-Total-Count -  <br>  * X-Pagination-Limit -  <br>  |
**0** | Unexpected error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_website**
> Website update_website(host, set_website)

Update website.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import comicbagi_openapi
from comicbagi_openapi.models.set_website import SetWebsite
from comicbagi_openapi.models.website import Website
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
    api_instance = comicbagi_openapi.WebsiteApi(api_client)
    host = 'host_example' # str | 
    set_website = comicbagi_openapi.SetWebsite() # SetWebsite | 

    try:
        # Update website.
        api_response = api_instance.update_website(host, set_website)
        print("The response of WebsiteApi->update_website:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebsiteApi->update_website: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **host** | **str**|  | 
 **set_website** | [**SetWebsite**](SetWebsite.md)|  | 

### Return type

[**Website**](Website.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Website updated. |  * Location -  <br>  |
**204** | Website unmodified. |  -  |
**0** | Unexpected error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

