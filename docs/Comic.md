# Comic


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**created_at** | **datetime** |  | 
**updated_at** | **datetime** |  | 
**code** | **str** |  | 
**provider_count** | **int** |  | 
**chapter_count** | **int** |  | 

## Example

```python
from comicbagi_openapi.models.comic import Comic

# TODO update the JSON string below
json = "{}"
# create an instance of Comic from a JSON string
comic_instance = Comic.from_json(json)
# print the JSON string representation of the object
print(Comic.to_json())

# convert the object into a dict
comic_dict = comic_instance.to_dict()
# create an instance of Comic from a dict
comic_form_dict = comic.from_dict(comic_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


