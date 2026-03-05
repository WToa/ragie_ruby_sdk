# RagieRubySdk::BoundingBoxLocation

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **location_type** | **String** |  | [optional][default to &#39;bounding_box&#39;] |
| **left** | **Float** | Left coordinate (0.0 to 1.0) |  |
| **top** | **Float** | Top coordinate (0.0 to 1.0) |  |
| **width** | **Float** | Width of the element (0.0 to 1.0) |  |
| **height** | **Float** | Height of the element (0.0 to 1.0) |  |
| **page_number** | **Integer** | Page number |  |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::BoundingBoxLocation.new(
  location_type: null,
  left: null,
  top: null,
  width: null,
  height: null,
  page_number: null
)
```

