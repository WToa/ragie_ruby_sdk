# OpenapiClient::ConnectionSyncStartedWebhookPayload

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **connection_id** | **String** |  |  |
| **sync_id** | **String** |  |  |
| **partition** | **String** |  |  |
| **connection_metadata** | **Hash&lt;String, Object&gt;** |  |  |
| **create_count** | **Integer** |  |  |
| **update_content_count** | **Integer** |  |  |
| **update_metadata_count** | **Integer** |  |  |
| **delete_count** | **Integer** |  |  |

## Example

```ruby
require 'openapi_client'

instance = OpenapiClient::ConnectionSyncStartedWebhookPayload.new(
  connection_id: null,
  sync_id: null,
  partition: null,
  connection_metadata: null,
  create_count: null,
  update_content_count: null,
  update_metadata_count: null,
  delete_count: null
)
```

