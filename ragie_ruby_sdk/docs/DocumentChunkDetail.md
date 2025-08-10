# RagieRubySdk::DocumentChunkDetail

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **index** | **Integer** |  | [optional][default to -1] |
| **text** | **String** |  |  |
| **metadata** | **Hash&lt;String, Object&gt;** |  | [optional] |
| **links** | [**Hash&lt;String, Link&gt;**](Link.md) |  |  |
| **modality_data** | [**DocumentChunkDetailModalityData**](DocumentChunkDetailModalityData.md) |  | [optional] |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::DocumentChunkDetail.new(
  id: null,
  index: null,
  text: null,
  metadata: null,
  links: null,
  modality_data: null
)
```

