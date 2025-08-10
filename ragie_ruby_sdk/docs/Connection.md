# OpenapiClient::Connection

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **created_at** | **Time** |  |  |
| **updated_at** | **Time** |  |  |
| **metadata** | [**Hash&lt;String, MetadataValue&gt;**](MetadataValue.md) |  |  |
| **type** | **String** |  |  |
| **name** | **String** |  |  |
| **source** | [**Source**](Source.md) |  |  |
| **enabled** | **Boolean** |  |  |
| **disabled_by_system_reason** | **String** |  |  |
| **last_synced_at** | **Time** |  | [optional] |
| **syncing** | **Boolean** |  | [optional] |
| **partition** | **String** |  | [optional] |
| **page_limit** | **Integer** |  |  |
| **disabled_by_system** | **Boolean** |  | [readonly] |

## Example

```ruby
require 'openapi_client'

instance = OpenapiClient::Connection.new(
  id: null,
  created_at: null,
  updated_at: null,
  metadata: null,
  type: null,
  name: null,
  source: null,
  enabled: null,
  disabled_by_system_reason: null,
  last_synced_at: null,
  syncing: null,
  partition: null,
  page_limit: null,
  disabled_by_system: null
)
```

