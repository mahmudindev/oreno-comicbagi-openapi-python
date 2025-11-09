# SetComicChapterProvider


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**link_website_host** | **str** |  | [optional] 
**link_relative_reference** | **str** |  | [optional] 
**language_lang** | **str** |  | [optional] 
**released_at** | **datetime** |  | [optional] 

## Example

```python
from comicbagi_openapi.models.set_comic_chapter_provider import SetComicChapterProvider

# TODO update the JSON string below
json = "{}"
# create an instance of SetComicChapterProvider from a JSON string
set_comic_chapter_provider_instance = SetComicChapterProvider.from_json(json)
# print the JSON string representation of the object
print(SetComicChapterProvider.to_json())

# convert the object into a dict
set_comic_chapter_provider_dict = set_comic_chapter_provider_instance.to_dict()
# create an instance of SetComicChapterProvider from a dict
set_comic_chapter_provider_form_dict = set_comic_chapter_provider.from_dict(set_comic_chapter_provider_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


