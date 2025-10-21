# RagieRubySdk::UpdatePartitionParams

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **context_aware** | **Boolean** |  | [optional] |
| **description** | **String** |  | [optional] |
| **metadata_schema** | [**Hash&lt;String, CreatePartitionParamsMetadataSchemaValue&gt;**](CreatePartitionParamsMetadataSchemaValue.md) |  | [optional] |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::UpdatePartitionParams.new(
  context_aware: null,
  description: null,
  metadata_schema: null
)
```

