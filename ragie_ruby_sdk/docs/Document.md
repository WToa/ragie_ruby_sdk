# RagieRubySdk::Document

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **status** | **String** |  |  |
| **id** | **String** |  |  |
| **created_at** | **Time** |  |  |
| **updated_at** | **Time** |  |  |
| **name** | **String** |  |  |
| **metadata** | [**Hash&lt;String, MetadataValue&gt;**](MetadataValue.md) |  |  |
| **partition** | **String** |  |  |
| **chunk_count** | **Integer** |  | [optional] |
| **external_id** | **String** |  | [optional] |
| **page_count** | **Float** |  | [optional] |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::Document.new(
  status: null,
  id: null,
  created_at: null,
  updated_at: null,
  name: null,
  metadata: null,
  partition: null,
  chunk_count: null,
  external_id: null,
  page_count: null
)
```

