# RagieRubySdk::ResponseOutputMessage

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  | [optional][default to &#39;message&#39;] |
| **id** | **String** |  |  |
| **role** | **String** |  | [optional][default to &#39;assistant&#39;] |
| **content** | [**Array&lt;ResponseContent&gt;**](ResponseContent.md) |  |  |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::ResponseOutputMessage.new(
  type: null,
  id: null,
  role: null,
  content: null
)
```

