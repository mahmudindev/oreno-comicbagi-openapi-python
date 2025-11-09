# SetComicProvider


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**link_website_host** | **str** |  | [optional] 
**link_relative_reference** | **str** |  | [optional] 
**language_lang** | **str** |  | [optional] 
**released_at** | **datetime** |  | [optional] 

## Example

```python
from comicbagi_openapi.models.set_comic_provider import SetComicProvider

# TODO update the JSON string below
json = "{}"
# create an instance of SetComicProvider from a JSON string
set_comic_provider_instance = SetComicProvider.from_json(json)
# print the JSON string representation of the object
print(SetComicProvider.to_json())

# convert the object into a dict
set_comic_provider_dict = set_comic_provider_instance.to_dict()
# create an instance of SetComicProvider from a dict
set_comic_provider_form_dict = set_comic_provider.from_dict(set_comic_provider_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


