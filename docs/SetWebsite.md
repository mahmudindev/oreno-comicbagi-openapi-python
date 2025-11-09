# SetWebsite


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**host** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**redacted** | **bool** |  | [optional] 

## Example

```python
from comicbagi_openapi.models.set_website import SetWebsite

# TODO update the JSON string below
json = "{}"
# create an instance of SetWebsite from a JSON string
set_website_instance = SetWebsite.from_json(json)
# print the JSON string representation of the object
print(SetWebsite.to_json())

# convert the object into a dict
set_website_dict = set_website_instance.to_dict()
# create an instance of SetWebsite from a dict
set_website_form_dict = set_website.from_dict(set_website_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


