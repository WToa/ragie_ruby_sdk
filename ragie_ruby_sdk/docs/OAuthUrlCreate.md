# RagieRubySdk::OAuthUrlCreate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **redirect_uri** | **String** |  |  |
| **partition** | **String** |  | [optional] |
| **source_type** | [**ConnectorSource**](ConnectorSource.md) | The type of connector you want to create, such as google_drive, notion, hubspot, etc. | [optional] |
| **metadata** | [**Hash&lt;String, MetadataValue&gt;**](MetadataValue.md) | Metadata for the document. Keys must be strings. Values may be strings, numbers, booleans, or lists of strings. Numbers may be integers or floating point and will be converted to 64 bit floating point. 1000 total values are allowed. Each item in an array counts towards the total. The following keys are reserved for internal use: &#x60;document_id&#x60;, &#x60;document_type&#x60;, &#x60;document_source&#x60;, &#x60;document_name&#x60;, &#x60;document_uploaded_at&#x60;, &#x60;start_time&#x60;, &#x60;end_time&#x60;, &#x60;chunk_content_type&#x60;. | [optional] |
| **mode** | [**Mode1**](Mode1.md) |  | [optional] |
| **theme** | **String** | Sets the theme of the Ragie Web UI when the user lands there. Can be light, dark, or system to use whatever the system value is. If omitted, system is used. | [optional] |
| **page_limit** | **Integer** | The maximum number of pages a connection will sync. The connection will be disabled after this limit is reached. Some in progress documents may continue processing after the limit is reached. The limit will be enforced at the start of the next document sync. Remove the limit by setting to null. | [optional] |
| **config** | **Hash&lt;String, Object&gt;** | Optional config per connector | [optional] |
| **authenticator_id** | **String** |  | [optional] |
| **workflow** | [**DocumentWorkflow**](DocumentWorkflow.md) |  | [optional] |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::OAuthUrlCreate.new(
  redirect_uri: null,
  partition: null,
  source_type: null,
  metadata: null,
  mode: null,
  theme: null,
  page_limit: null,
  config: null,
  authenticator_id: null,
  workflow: null
)
```

