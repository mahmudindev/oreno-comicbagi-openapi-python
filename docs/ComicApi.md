# comicbagi_openapi.ComicApi

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_comic**](ComicApi.md#add_comic) | **POST** /rest/comics | Add comic.
[**add_comic_provider**](ComicApi.md#add_comic_provider) | **POST** /rest/comics/{comicCode}/providers | Add comic provider.
[**delete_comic**](ComicApi.md#delete_comic) | **DELETE** /rest/comics/{code} | Delete comic.
[**delete_comic_provider**](ComicApi.md#delete_comic_provider) | **DELETE** /rest/comics/{comicCode}/providers/{ulid} | Delete comic provider.
[**get_comic**](ComicApi.md#get_comic) | **GET** /rest/comics/{code} | Get comic.
[**get_comic_provider**](ComicApi.md#get_comic_provider) | **GET** /rest/comics/{comicCode}/providers/{ulid} | Get comic provider.
[**list_comic**](ComicApi.md#list_comic) | **GET** /rest/comics | List comic.
[**list_comic_provider**](ComicApi.md#list_comic_provider) | **GET** /rest/comics/{comicCode}/providers | List comic provider.
[**update_comic**](ComicApi.md#update_comic) | **PATCH** /rest/comics/{code} | Update comic.
[**update_comic_provider**](ComicApi.md#update_comic_provider) | **PATCH** /rest/comics/{comicCode}/providers/{ulid} | Update comic provider.


# **add_comic**
> Comic add_comic(new_comic)

Add comic.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import comicbagi_openapi
from comicbagi_openapi.models.comic import Comic
from comicbagi_openapi.models.new_comic import NewComic
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
    api_instance = comicbagi_openapi.ComicApi(api_client)
    new_comic = comicbagi_openapi.NewComic() # NewComic | 

    try:
        # Add comic.
        api_response = api_instance.add_comic(new_comic)
        print("The response of ComicApi->add_comic:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ComicApi->add_comic: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **new_comic** | [**NewComic**](NewComic.md)|  | 

### Return type

[**Comic**](Comic.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Comic added. |  * Location -  <br>  |
**0** | Unexpected error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **add_comic_provider**
> ComicProvider add_comic_provider(comic_code, new_comic_provider)

Add comic provider.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import comicbagi_openapi
from comicbagi_openapi.models.comic_provider import ComicProvider
from comicbagi_openapi.models.new_comic_provider import NewComicProvider
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
    api_instance = comicbagi_openapi.ComicApi(api_client)
    comic_code = 'comic_code_example' # str | 
    new_comic_provider = comicbagi_openapi.NewComicProvider() # NewComicProvider | 

    try:
        # Add comic provider.
        api_response = api_instance.add_comic_provider(comic_code, new_comic_provider)
        print("The response of ComicApi->add_comic_provider:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ComicApi->add_comic_provider: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **comic_code** | **str**|  | 
 **new_comic_provider** | [**NewComicProvider**](NewComicProvider.md)|  | 

### Return type

[**ComicProvider**](ComicProvider.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Comic provider added. |  * Location -  <br>  |
**0** | Unexpected error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_comic**
> delete_comic(code)

Delete comic.

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
    api_instance = comicbagi_openapi.ComicApi(api_client)
    code = 'code_example' # str | 

    try:
        # Delete comic.
        api_instance.delete_comic(code)
    except Exception as e:
        print("Exception when calling ComicApi->delete_comic: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **code** | **str**|  | 

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
**204** | Comic deleted. |  -  |
**0** | Unexpected error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_comic_provider**
> delete_comic_provider(comic_code, ulid)

Delete comic provider.

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
    api_instance = comicbagi_openapi.ComicApi(api_client)
    comic_code = 'comic_code_example' # str | 
    ulid = 'ulid_example' # str | 

    try:
        # Delete comic provider.
        api_instance.delete_comic_provider(comic_code, ulid)
    except Exception as e:
        print("Exception when calling ComicApi->delete_comic_provider: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **comic_code** | **str**|  | 
 **ulid** | **str**|  | 

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
**204** | Comic provider deleted. |  -  |
**0** | Unexpected error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_comic**
> Comic get_comic(code)

Get comic.

### Example


```python
import comicbagi_openapi
from comicbagi_openapi.models.comic import Comic
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
    api_instance = comicbagi_openapi.ComicApi(api_client)
    code = 'code_example' # str | 

    try:
        # Get comic.
        api_response = api_instance.get_comic(code)
        print("The response of ComicApi->get_comic:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ComicApi->get_comic: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **code** | **str**|  | 

### Return type

[**Comic**](Comic.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Comic gets. |  -  |
**0** | Unexpected error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_comic_provider**
> ComicProvider get_comic_provider(comic_code, ulid)

Get comic provider.

### Example


```python
import comicbagi_openapi
from comicbagi_openapi.models.comic_provider import ComicProvider
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
    api_instance = comicbagi_openapi.ComicApi(api_client)
    comic_code = 'comic_code_example' # str | 
    ulid = 'ulid_example' # str | 

    try:
        # Get comic provider.
        api_response = api_instance.get_comic_provider(comic_code, ulid)
        print("The response of ComicApi->get_comic_provider:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ComicApi->get_comic_provider: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **comic_code** | **str**|  | 
 **ulid** | **str**|  | 

### Return type

[**ComicProvider**](ComicProvider.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Comic provider gets. |  -  |
**0** | Unexpected error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_comic**
> List[Comic] list_comic(page=page, limit=limit, order=order, order_by=order_by, provider_link_website_host=provider_link_website_host, provider_link_relative_reference=provider_link_relative_reference, provider_link_href=provider_link_href, provider_language_lang=provider_language_lang)

List comic.

### Example


```python
import comicbagi_openapi
from comicbagi_openapi.models.comic import Comic
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
    api_instance = comicbagi_openapi.ComicApi(api_client)
    page = 56 # int |  (optional)
    limit = 56 # int |  (optional)
    order = 'order_example' # str |  (optional)
    order_by = ['order_by_example'] # List[str] |  (optional)
    provider_link_website_host = ['provider_link_website_host_example'] # List[str] |  (optional)
    provider_link_relative_reference = ['provider_link_relative_reference_example'] # List[str] |  (optional)
    provider_link_href = ['provider_link_href_example'] # List[str] |  (optional)
    provider_language_lang = ['provider_language_lang_example'] # List[str] |  (optional)

    try:
        # List comic.
        api_response = api_instance.list_comic(page=page, limit=limit, order=order, order_by=order_by, provider_link_website_host=provider_link_website_host, provider_link_relative_reference=provider_link_relative_reference, provider_link_href=provider_link_href, provider_language_lang=provider_language_lang)
        print("The response of ComicApi->list_comic:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ComicApi->list_comic: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **limit** | **int**|  | [optional] 
 **order** | **str**|  | [optional] 
 **order_by** | [**List[str]**](str.md)|  | [optional] 
 **provider_link_website_host** | [**List[str]**](str.md)|  | [optional] 
 **provider_link_relative_reference** | [**List[str]**](str.md)|  | [optional] 
 **provider_link_href** | [**List[str]**](str.md)|  | [optional] 
 **provider_language_lang** | [**List[str]**](str.md)|  | [optional] 

### Return type

[**List[Comic]**](Comic.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Comic list. |  * X-Total-Count -  <br>  * X-Pagination-Limit -  <br>  |
**0** | Unexpected error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_comic_provider**
> List[ComicProvider] list_comic_provider(comic_code, page=page, limit=limit, order=order, order_by=order_by, link_website_host=link_website_host, link_relative_reference=link_relative_reference, link_href=link_href, language_lang=language_lang, unredact=unredact)

List comic provider.

### Example


```python
import comicbagi_openapi
from comicbagi_openapi.models.comic_provider import ComicProvider
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
    api_instance = comicbagi_openapi.ComicApi(api_client)
    comic_code = 'comic_code_example' # str | 
    page = 56 # int |  (optional)
    limit = 56 # int |  (optional)
    order = 'order_example' # str |  (optional)
    order_by = ['order_by_example'] # List[str] |  (optional)
    link_website_host = ['link_website_host_example'] # List[str] |  (optional)
    link_relative_reference = ['link_relative_reference_example'] # List[str] |  (optional)
    link_href = ['link_href_example'] # List[str] |  (optional)
    language_lang = ['language_lang_example'] # List[str] |  (optional)
    unredact = ['unredact_example'] # List[str] |  (optional)

    try:
        # List comic provider.
        api_response = api_instance.list_comic_provider(comic_code, page=page, limit=limit, order=order, order_by=order_by, link_website_host=link_website_host, link_relative_reference=link_relative_reference, link_href=link_href, language_lang=language_lang, unredact=unredact)
        print("The response of ComicApi->list_comic_provider:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ComicApi->list_comic_provider: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **comic_code** | **str**|  | 
 **page** | **int**|  | [optional] 
 **limit** | **int**|  | [optional] 
 **order** | **str**|  | [optional] 
 **order_by** | [**List[str]**](str.md)|  | [optional] 
 **link_website_host** | [**List[str]**](str.md)|  | [optional] 
 **link_relative_reference** | [**List[str]**](str.md)|  | [optional] 
 **link_href** | [**List[str]**](str.md)|  | [optional] 
 **language_lang** | [**List[str]**](str.md)|  | [optional] 
 **unredact** | [**List[str]**](str.md)|  | [optional] 

### Return type

[**List[ComicProvider]**](ComicProvider.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Comic provider list. |  * X-Total-Count -  <br>  * X-Pagination-Limit -  <br>  |
**0** | Unexpected error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_comic**
> Comic update_comic(code, set_comic)

Update comic.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import comicbagi_openapi
from comicbagi_openapi.models.comic import Comic
from comicbagi_openapi.models.set_comic import SetComic
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
    api_instance = comicbagi_openapi.ComicApi(api_client)
    code = 'code_example' # str | 
    set_comic = comicbagi_openapi.SetComic() # SetComic | 

    try:
        # Update comic.
        api_response = api_instance.update_comic(code, set_comic)
        print("The response of ComicApi->update_comic:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ComicApi->update_comic: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **code** | **str**|  | 
 **set_comic** | [**SetComic**](SetComic.md)|  | 

### Return type

[**Comic**](Comic.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Comic updated. |  * Location -  <br>  |
**204** | Comic unmodified. |  -  |
**0** | Unexpected error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_comic_provider**
> ComicProvider update_comic_provider(comic_code, ulid, set_comic_provider)

Update comic provider.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import comicbagi_openapi
from comicbagi_openapi.models.comic_provider import ComicProvider
from comicbagi_openapi.models.set_comic_provider import SetComicProvider
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
    api_instance = comicbagi_openapi.ComicApi(api_client)
    comic_code = 'comic_code_example' # str | 
    ulid = 'ulid_example' # str | 
    set_comic_provider = comicbagi_openapi.SetComicProvider() # SetComicProvider | 

    try:
        # Update comic provider.
        api_response = api_instance.update_comic_provider(comic_code, ulid, set_comic_provider)
        print("The response of ComicApi->update_comic_provider:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ComicApi->update_comic_provider: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **comic_code** | **str**|  | 
 **ulid** | **str**|  | 
 **set_comic_provider** | [**SetComicProvider**](SetComicProvider.md)|  | 

### Return type

[**ComicProvider**](ComicProvider.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Comic provider updated. |  * Location -  <br>  |
**204** | Comic provider unmodified. |  -  |
**0** | Unexpected error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

