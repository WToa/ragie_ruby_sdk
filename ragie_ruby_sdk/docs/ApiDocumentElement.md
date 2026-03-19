# RagieRubySdk::ApiDocumentElement

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **created_at** | **Time** |  |  |
| **index** | **Integer** |  |  |
| **metadata** | **Hash&lt;String, Object&gt;** |  |  |
| **type** | [**DocumentElementType**](DocumentElementType.md) |  |  |
| **text** | **String** |  |  |
| **markdown** | **String** |  |  |
| **location** | [**ApiDocumentElementLocation**](ApiDocumentElementLocation.md) |  | [optional] |
| **data** | [**ApiElement**](ApiElement.md) |  |  |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::ApiDocumentElement.new(
  id: null,
  created_at: null,
  index: null,
  metadata: null,
  type: null,
  text: null,
  markdown: null,
  location: null,
  data: null
)
```

