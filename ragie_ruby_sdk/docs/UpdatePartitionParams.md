# RagieRubySdk::UpdatePartitionParams

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **context_aware** | **Boolean** | Enable context-aware descriptions for the partition. | [optional] |
| **description** | **String** | Description of the partition. | [optional] |
| **metadata_schema** | [**Hash&lt;String, CreatePartitionParamsMetadataSchemaValue&gt;**](CreatePartitionParamsMetadataSchemaValue.md) | Metadata schema for the partition. This is an optional subset of the metadata of documents in the partition, defined as JSON Schema, that can be used in filter generatation. Providing detailed descriptions of the fields in the schema can be helpful for LLMs generating filters dynamically. | [optional] |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::UpdatePartitionParams.new(
  context_aware: null,
  description: null,
  metadata_schema: null
)
```

