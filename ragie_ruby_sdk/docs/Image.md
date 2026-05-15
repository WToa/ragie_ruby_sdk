# RagieRubySdk::Image

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  | [optional][default to &#39;Image&#39;] |
| **content** | **String** | The text visible inside the visual (OCR) |  |
| **description** | **String** | A detailed description of what the visual depicts. |  |
| **base64_data** | **String** | Base64 encoded image data, when available. | [optional] |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::Image.new(
  type: null,
  content: null,
  description: null,
  base64_data: null
)
```

