# RagieRubySdk::Entity

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **created_at** | **Time** |  |  |
| **updated_at** | **Time** |  |  |
| **instruction_id** | **String** | The ID of the instruction which generated the entity. |  |
| **document_id** | **String** | The ID of the document which the entity was produced from. |  |
| **chunk_id** | **String** |  | [optional] |
| **data** | **Hash&lt;String, Object&gt;** |  |  |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::Entity.new(
  id: null,
  created_at: null,
  updated_at: null,
  instruction_id: null,
  document_id: null,
  chunk_id: null,
  data: null
)
```

