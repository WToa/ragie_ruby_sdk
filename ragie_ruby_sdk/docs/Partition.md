# RagieRubySdk::Partition

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  |  |
| **is_default** | **Boolean** |  |  |
| **limit_exceeded_at** | **Time** |  | [optional] |
| **limits** | [**PartitionLimits**](PartitionLimits.md) |  |  |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::Partition.new(
  name: null,
  is_default: null,
  limit_exceeded_at: null,
  limits: null
)
```

