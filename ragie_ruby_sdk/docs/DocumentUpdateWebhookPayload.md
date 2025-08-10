# OpenapiClient::DocumentUpdateWebhookPayload

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_id** | **String** |  |  |
| **status** | [**Status**](Status.md) |  |  |
| **partition** | **String** |  |  |
| **metadata** | **Hash&lt;String, Object&gt;** |  |  |
| **external_id** | **String** |  |  |
| **name** | **String** |  |  |
| **connection_id** | **String** |  |  |
| **sync_id** | **String** |  |  |
| **error** | **String** |  |  |

## Example

```ruby
require 'openapi_client'

instance = OpenapiClient::DocumentUpdateWebhookPayload.new(
  document_id: null,
  status: null,
  partition: null,
  metadata: null,
  external_id: null,
  name: null,
  connection_id: null,
  sync_id: null,
  error: null
)
```

