# OpenapiClient::PartitionDetail

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  |  |
| **is_default** | **Boolean** |  |  |
| **limit_exceeded_at** | **Time** |  | [optional] |
| **limits** | [**PartitionLimits**](PartitionLimits.md) |  |  |
| **stats** | [**PartitionStats**](PartitionStats.md) |  |  |

## Example

```ruby
require 'openapi_client'

instance = OpenapiClient::PartitionDetail.new(
  name: null,
  is_default: null,
  limit_exceeded_at: null,
  limits: null,
  stats: null
)
```

