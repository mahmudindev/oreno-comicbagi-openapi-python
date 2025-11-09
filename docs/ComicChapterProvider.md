# ComicChapterProvider


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**created_at** | **datetime** |  | 
**updated_at** | **datetime** |  | 
**ulid** | **str** |  | 
**link_website_host** | **str** |  | 
**link_website_name** | **str** |  | 
**link_website_redacted** | **bool** |  | 
**link_relative_reference** | **str** |  | 
**language_lang** | **str** |  | 
**released_at** | **datetime** |  | 

## Example

```python
from comicbagi_openapi.models.comic_chapter_provider import ComicChapterProvider

# TODO update the JSON string below
json = "{}"
# create an instance of ComicChapterProvider from a JSON string
comic_chapter_provider_instance = ComicChapterProvider.from_json(json)
# print the JSON string representation of the object
print(ComicChapterProvider.to_json())

# convert the object into a dict
comic_chapter_provider_dict = comic_chapter_provider_instance.to_dict()
# create an instance of ComicChapterProvider from a dict
comic_chapter_provider_form_dict = comic_chapter_provider.from_dict(comic_chapter_provider_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


