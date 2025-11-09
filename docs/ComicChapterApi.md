# comicbagi_openapi.ComicChapterApi

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_comic_chapter**](ComicChapterApi.md#add_comic_chapter) | **POST** /rest/comics/{comicCode}/chapters | Add comic chapter.
[**add_comic_chapter_provider**](ComicChapterApi.md#add_comic_chapter_provider) | **POST** /rest/comics/{comicCode}/chapters/{chapterNV}/providers | Add comic chapter provider.
[**delete_comic_chapter**](ComicChapterApi.md#delete_comic_chapter) | **DELETE** /rest/comics/{comicCode}/chapters/{nv} | Delete comic chapter.
[**delete_comic_chapter_provider**](ComicChapterApi.md#delete_comic_chapter_provider) | **DELETE** /rest/comics/{comicCode}/chapters/{chapterNV}/providers/{ulid} | Delete comic chapter provider.
[**get_comic_chapter**](ComicChapterApi.md#get_comic_chapter) | **GET** /rest/comics/{comicCode}/chapters/{nv} | Get comic chapter.
[**get_comic_chapter_provider**](ComicChapterApi.md#get_comic_chapter_provider) | **GET** /rest/comics/{comicCode}/chapters/{chapterNV}/providers/{ulid} | Get comic chapter provider.
[**list_comic_chapter**](ComicChapterApi.md#list_comic_chapter) | **GET** /rest/comics/{comicCode}/chapters | List comic chapter.
[**list_comic_chapter_provider**](ComicChapterApi.md#list_comic_chapter_provider) | **GET** /rest/comics/{comicCode}/chapters/{chapterNV}/providers | List comic chapter properties.
[**update_comic_chapter**](ComicChapterApi.md#update_comic_chapter) | **PATCH** /rest/comics/{comicCode}/chapters/{nv} | Update comic chapter.
[**update_comic_chapter_provider**](ComicChapterApi.md#update_comic_chapter_provider) | **PATCH** /rest/comics/{comicCode}/chapters/{chapterNV}/providers/{ulid} | Update comic chapter provider.


# **add_comic_chapter**
> ComicChapter add_comic_chapter(comic_code, new_comic_chapter)

Add comic chapter.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import comicbagi_openapi
from comicbagi_openapi.models.comic_chapter import ComicChapter
from comicbagi_openapi.models.new_comic_chapter import NewComicChapter
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
    api_instance = comicbagi_openapi.ComicChapterApi(api_client)
    comic_code = 'comic_code_example' # str | 
    new_comic_chapter = comicbagi_openapi.NewComicChapter() # NewComicChapter | 

    try:
        # Add comic chapter.
        api_response = api_instance.add_comic_chapter(comic_code, new_comic_chapter)
        print("The response of ComicChapterApi->add_comic_chapter:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ComicChapterApi->add_comic_chapter: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **comic_code** | **str**|  | 
 **new_comic_chapter** | [**NewComicChapter**](NewComicChapter.md)|  | 

### Return type

[**ComicChapter**](ComicChapter.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Comic chapter added. |  * Location -  <br>  |
**0** | Unexpected error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **add_comic_chapter_provider**
> ComicChapterProvider add_comic_chapter_provider(comic_code, chapter_nv, new_comic_chapter_provider)

Add comic chapter provider.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import comicbagi_openapi
from comicbagi_openapi.models.comic_chapter_provider import ComicChapterProvider
from comicbagi_openapi.models.new_comic_chapter_provider import NewComicChapterProvider
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
    api_instance = comicbagi_openapi.ComicChapterApi(api_client)
    comic_code = 'comic_code_example' # str | 
    chapter_nv = 'chapter_nv_example' # str | Number[+Version]
    new_comic_chapter_provider = comicbagi_openapi.NewComicChapterProvider() # NewComicChapterProvider | 

    try:
        # Add comic chapter provider.
        api_response = api_instance.add_comic_chapter_provider(comic_code, chapter_nv, new_comic_chapter_provider)
        print("The response of ComicChapterApi->add_comic_chapter_provider:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ComicChapterApi->add_comic_chapter_provider: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **comic_code** | **str**|  | 
 **chapter_nv** | **str**| Number[+Version] | 
 **new_comic_chapter_provider** | [**NewComicChapterProvider**](NewComicChapterProvider.md)|  | 

### Return type

[**ComicChapterProvider**](ComicChapterProvider.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Comic chapter provider added. |  * Location -  <br>  |
**0** | Unexpected error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_comic_chapter**
> delete_comic_chapter(comic_code, nv)

Delete comic chapter.

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
    api_instance = comicbagi_openapi.ComicChapterApi(api_client)
    comic_code = 'comic_code_example' # str | 
    nv = 'nv_example' # str | Number[+Version]

    try:
        # Delete comic chapter.
        api_instance.delete_comic_chapter(comic_code, nv)
    except Exception as e:
        print("Exception when calling ComicChapterApi->delete_comic_chapter: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **comic_code** | **str**|  | 
 **nv** | **str**| Number[+Version] | 

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
**204** | Comic chapter deleted. |  -  |
**0** | Unexpected error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_comic_chapter_provider**
> delete_comic_chapter_provider(comic_code, chapter_nv, ulid)

Delete comic chapter provider.

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
    api_instance = comicbagi_openapi.ComicChapterApi(api_client)
    comic_code = 'comic_code_example' # str | 
    chapter_nv = 'chapter_nv_example' # str | Number[+Version]
    ulid = 'ulid_example' # str | 

    try:
        # Delete comic chapter provider.
        api_instance.delete_comic_chapter_provider(comic_code, chapter_nv, ulid)
    except Exception as e:
        print("Exception when calling ComicChapterApi->delete_comic_chapter_provider: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **comic_code** | **str**|  | 
 **chapter_nv** | **str**| Number[+Version] | 
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
**204** | Comic chapter provider deleted. |  -  |
**0** | Unexpected error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_comic_chapter**
> ComicChapter get_comic_chapter(comic_code, nv)

Get comic chapter.

### Example


```python
import comicbagi_openapi
from comicbagi_openapi.models.comic_chapter import ComicChapter
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
    api_instance = comicbagi_openapi.ComicChapterApi(api_client)
    comic_code = 'comic_code_example' # str | 
    nv = 'nv_example' # str | Number[+Version]

    try:
        # Get comic chapter.
        api_response = api_instance.get_comic_chapter(comic_code, nv)
        print("The response of ComicChapterApi->get_comic_chapter:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ComicChapterApi->get_comic_chapter: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **comic_code** | **str**|  | 
 **nv** | **str**| Number[+Version] | 

### Return type

[**ComicChapter**](ComicChapter.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Comic chapter gets. |  -  |
**0** | Unexpected error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_comic_chapter_provider**
> ComicChapterProvider get_comic_chapter_provider(comic_code, chapter_nv, ulid)

Get comic chapter provider.

### Example


```python
import comicbagi_openapi
from comicbagi_openapi.models.comic_chapter_provider import ComicChapterProvider
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
    api_instance = comicbagi_openapi.ComicChapterApi(api_client)
    comic_code = 'comic_code_example' # str | 
    chapter_nv = 'chapter_nv_example' # str | Number[+Version]
    ulid = 'ulid_example' # str | 

    try:
        # Get comic chapter provider.
        api_response = api_instance.get_comic_chapter_provider(comic_code, chapter_nv, ulid)
        print("The response of ComicChapterApi->get_comic_chapter_provider:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ComicChapterApi->get_comic_chapter_provider: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **comic_code** | **str**|  | 
 **chapter_nv** | **str**| Number[+Version] | 
 **ulid** | **str**|  | 

### Return type

[**ComicChapterProvider**](ComicChapterProvider.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Comic chapter provider gets. |  -  |
**0** | Unexpected error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_comic_chapter**
> List[ComicChapter] list_comic_chapter(comic_code, page=page, limit=limit, order=order, order_by=order_by, provider_link_website_host=provider_link_website_host, provider_link_relative_reference=provider_link_relative_reference, provider_link_href=provider_link_href, provider_language_lang=provider_language_lang)

List comic chapter.

### Example


```python
import comicbagi_openapi
from comicbagi_openapi.models.comic_chapter import ComicChapter
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
    api_instance = comicbagi_openapi.ComicChapterApi(api_client)
    comic_code = 'comic_code_example' # str | 
    page = 56 # int |  (optional)
    limit = 56 # int |  (optional)
    order = 'order_example' # str |  (optional)
    order_by = ['order_by_example'] # List[str] |  (optional)
    provider_link_website_host = ['provider_link_website_host_example'] # List[str] |  (optional)
    provider_link_relative_reference = ['provider_link_relative_reference_example'] # List[str] |  (optional)
    provider_link_href = ['provider_link_href_example'] # List[str] |  (optional)
    provider_language_lang = ['provider_language_lang_example'] # List[str] |  (optional)

    try:
        # List comic chapter.
        api_response = api_instance.list_comic_chapter(comic_code, page=page, limit=limit, order=order, order_by=order_by, provider_link_website_host=provider_link_website_host, provider_link_relative_reference=provider_link_relative_reference, provider_link_href=provider_link_href, provider_language_lang=provider_language_lang)
        print("The response of ComicChapterApi->list_comic_chapter:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ComicChapterApi->list_comic_chapter: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **comic_code** | **str**|  | 
 **page** | **int**|  | [optional] 
 **limit** | **int**|  | [optional] 
 **order** | **str**|  | [optional] 
 **order_by** | [**List[str]**](str.md)|  | [optional] 
 **provider_link_website_host** | [**List[str]**](str.md)|  | [optional] 
 **provider_link_relative_reference** | [**List[str]**](str.md)|  | [optional] 
 **provider_link_href** | [**List[str]**](str.md)|  | [optional] 
 **provider_language_lang** | [**List[str]**](str.md)|  | [optional] 

### Return type

[**List[ComicChapter]**](ComicChapter.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Comic chapter list. |  * X-Total-Count -  <br>  * X-Pagination-Limit -  <br>  |
**0** | Unexpected error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_comic_chapter_provider**
> List[ComicChapterProvider] list_comic_chapter_provider(comic_code, chapter_nv, page=page, limit=limit, order=order, order_by=order_by, link_website_host=link_website_host, link_relative_reference=link_relative_reference, link_href=link_href, language_lang=language_lang, unredact=unredact)

List comic chapter properties.

### Example


```python
import comicbagi_openapi
from comicbagi_openapi.models.comic_chapter_provider import ComicChapterProvider
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
    api_instance = comicbagi_openapi.ComicChapterApi(api_client)
    comic_code = 'comic_code_example' # str | 
    chapter_nv = 'chapter_nv_example' # str | Number[+Version]
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
        # List comic chapter properties.
        api_response = api_instance.list_comic_chapter_provider(comic_code, chapter_nv, page=page, limit=limit, order=order, order_by=order_by, link_website_host=link_website_host, link_relative_reference=link_relative_reference, link_href=link_href, language_lang=language_lang, unredact=unredact)
        print("The response of ComicChapterApi->list_comic_chapter_provider:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ComicChapterApi->list_comic_chapter_provider: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **comic_code** | **str**|  | 
 **chapter_nv** | **str**| Number[+Version] | 
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

[**List[ComicChapterProvider]**](ComicChapterProvider.md)

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

# **update_comic_chapter**
> ComicChapter update_comic_chapter(comic_code, nv, set_comic_chapter)

Update comic chapter.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import comicbagi_openapi
from comicbagi_openapi.models.comic_chapter import ComicChapter
from comicbagi_openapi.models.set_comic_chapter import SetComicChapter
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
    api_instance = comicbagi_openapi.ComicChapterApi(api_client)
    comic_code = 'comic_code_example' # str | 
    nv = 'nv_example' # str | Number[+Version]
    set_comic_chapter = comicbagi_openapi.SetComicChapter() # SetComicChapter | 

    try:
        # Update comic chapter.
        api_response = api_instance.update_comic_chapter(comic_code, nv, set_comic_chapter)
        print("The response of ComicChapterApi->update_comic_chapter:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ComicChapterApi->update_comic_chapter: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **comic_code** | **str**|  | 
 **nv** | **str**| Number[+Version] | 
 **set_comic_chapter** | [**SetComicChapter**](SetComicChapter.md)|  | 

### Return type

[**ComicChapter**](ComicChapter.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Comic chapter updated. |  * Location -  <br>  |
**204** | Comic chapter unmodified. |  -  |
**0** | Unexpected error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_comic_chapter_provider**
> ComicChapterProvider update_comic_chapter_provider(comic_code, chapter_nv, ulid, set_comic_chapter_provider)

Update comic chapter provider.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import comicbagi_openapi
from comicbagi_openapi.models.comic_chapter_provider import ComicChapterProvider
from comicbagi_openapi.models.set_comic_chapter_provider import SetComicChapterProvider
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
    api_instance = comicbagi_openapi.ComicChapterApi(api_client)
    comic_code = 'comic_code_example' # str | 
    chapter_nv = 'chapter_nv_example' # str | Number[+Version]
    ulid = 'ulid_example' # str | 
    set_comic_chapter_provider = comicbagi_openapi.SetComicChapterProvider() # SetComicChapterProvider | 

    try:
        # Update comic chapter provider.
        api_response = api_instance.update_comic_chapter_provider(comic_code, chapter_nv, ulid, set_comic_chapter_provider)
        print("The response of ComicChapterApi->update_comic_chapter_provider:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ComicChapterApi->update_comic_chapter_provider: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **comic_code** | **str**|  | 
 **chapter_nv** | **str**| Number[+Version] | 
 **ulid** | **str**|  | 
 **set_comic_chapter_provider** | [**SetComicChapterProvider**](SetComicChapterProvider.md)|  | 

### Return type

[**ComicChapterProvider**](ComicChapterProvider.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Comic chapter provider updated. |  * Location -  <br>  |
**204** | Comic chapter provider unmodified. |  -  |
**0** | Unexpected error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

