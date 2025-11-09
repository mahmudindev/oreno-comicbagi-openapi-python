# NewWebsite


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**host** | **str** |  | 
**name** | **str** |  | [optional] 
**redacted** | **bool** |  | [optional] 

## Example

```python
from comicbagi_openapi.models.new_website import NewWebsite

# TODO update the JSON string below
json = "{}"
# create an instance of NewWebsite from a JSON string
new_website_instance = NewWebsite.from_json(json)
# print the JSON string representation of the object
print(NewWebsite.to_json())

# convert the object into a dict
new_website_dict = new_website_instance.to_dict()
# create an instance of NewWebsite from a dict
new_website_form_dict = new_website.from_dict(new_website_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


