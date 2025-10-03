# RagieRubySdk::QueryDetails

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** |  |  |
| **search_effort** | [**SearchEffort**](SearchEffort.md) |  |  |
| **metadata_filter** | **Hash&lt;String, Object&gt;** |  |  |
| **search_results** | [**Array&lt;RagieEvidence&gt;**](RagieEvidence.md) |  |  |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::QueryDetails.new(
  query: null,
  search_effort: null,
  metadata_filter: null,
  search_results: null
)
```

