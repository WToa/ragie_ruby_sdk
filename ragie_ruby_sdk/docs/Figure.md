# RagieRubySdk::Figure

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  | [optional][default to &#39;Figure&#39;] |
| **content** | **String** | The text visible inside the visual (OCR) |  |
| **description** | **String** | A detailed description of what the visual depicts. |  |
| **base64_data** | **String** |  | [optional] |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::Figure.new(
  type: null,
  content: null,
  description: null,
  base64_data: null
)
```

