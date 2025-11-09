# NewComicChapterProvider


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**link_website_host** | **str** |  | 
**link_relative_reference** | **str** |  | [optional] 
**language_lang** | **str** |  | [optional] 
**released_at** | **datetime** |  | [optional] 

## Example

```python
from comicbagi_openapi.models.new_comic_chapter_provider import NewComicChapterProvider

# TODO update the JSON string below
json = "{}"
# create an instance of NewComicChapterProvider from a JSON string
new_comic_chapter_provider_instance = NewComicChapterProvider.from_json(json)
# print the JSON string representation of the object
print(NewComicChapterProvider.to_json())

# convert the object into a dict
new_comic_chapter_provider_dict = new_comic_chapter_provider_instance.to_dict()
# create an instance of NewComicChapterProvider from a dict
new_comic_chapter_provider_form_dict = new_comic_chapter_provider.from_dict(new_comic_chapter_provider_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


