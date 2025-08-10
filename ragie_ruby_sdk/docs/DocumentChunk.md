# RagieRubySdk::DocumentChunk

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **index** | **Integer** |  | [optional][default to -1] |
| **text** | **String** |  |  |
| **metadata** | **Hash&lt;String, Object&gt;** |  | [optional] |
| **links** | [**Hash&lt;String, Link&gt;**](Link.md) |  |  |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::DocumentChunk.new(
  id: null,
  index: null,
  text: null,
  metadata: null,
  links: null
)
```

