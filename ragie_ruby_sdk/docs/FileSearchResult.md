# RagieRubySdk::FileSearchResult

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **file_id** | **String** | The unique ID of the document. |  |
| **filename** | **String** | The name of the document. |  |
| **score** | **Float** | The relevance score of the chunk - a value between 0 and 1. |  |
| **text** | **String** | The text content of the chunk. |  |
| **attributes** | **Hash&lt;String, Object&gt;** | The attributes of the chunk. |  |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::FileSearchResult.new(
  file_id: null,
  filename: null,
  score: null,
  text: null,
  attributes: null
)
```

