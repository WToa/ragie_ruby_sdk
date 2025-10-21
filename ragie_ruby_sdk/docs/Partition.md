# RagieRubySdk::Partition

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  |  |
| **is_default** | **Boolean** |  |  |
| **limit_exceeded_at** | **Time** |  | [optional] |
| **description** | **String** |  |  |
| **context_aware** | **Boolean** |  |  |
| **metadata_schema** | [**Hash&lt;String, CreatePartitionParamsMetadataSchemaValue&gt;**](CreatePartitionParamsMetadataSchemaValue.md) |  |  |
| **limits** | [**PartitionLimits**](PartitionLimits.md) |  |  |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::Partition.new(
  name: null,
  is_default: null,
  limit_exceeded_at: null,
  description: null,
  context_aware: null,
  metadata_schema: null,
  limits: null
)
```

