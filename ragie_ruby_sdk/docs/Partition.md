# OpenapiClient::Partition

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  |  |
| **is_default** | **Boolean** |  |  |
| **limit_exceeded_at** | **Time** |  | [optional] |
| **limits** | [**PartitionLimits**](PartitionLimits.md) |  |  |

## Example

```ruby
require 'openapi_client'

instance = OpenapiClient::Partition.new(
  name: null,
  is_default: null,
  limit_exceeded_at: null,
  limits: null
)
```

