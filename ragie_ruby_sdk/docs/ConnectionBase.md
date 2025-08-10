# RagieRubySdk::ConnectionBase

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **partition_strategy** | [**PartitionStrategy**](PartitionStrategy.md) |  |  |
| **metadata** | [**Hash&lt;String, MetadataValue&gt;**](MetadataValue.md) | Metadata for the document. Keys must be strings. Values may be strings, numbers, booleans, or lists of strings. Numbers may be integers or floating point and will be converted to 64 bit floating point. 1000 total values are allowed. Each item in an array counts towards the total. The following keys are reserved for internal use: &#x60;document_id&#x60;, &#x60;document_type&#x60;, &#x60;document_source&#x60;, &#x60;document_name&#x60;, &#x60;document_uploaded_at&#x60;, &#x60;start_time&#x60;, &#x60;end_time&#x60;. | [optional] |
| **page_limit** | **Integer** |  | [optional] |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::ConnectionBase.new(
  partition_strategy: null,
  metadata: null,
  page_limit: null
)
```

