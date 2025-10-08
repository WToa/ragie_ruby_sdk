# RagieRubySdk::SearchStepWithQueryDetails

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  | [optional][default to &#39;search&#39;] |
| **think** | **String** |  |  |
| **current_question** | **String** |  |  |
| **errored** | **Boolean** |  | [optional][default to false] |
| **search** | [**Search**](Search.md) | The search request to be made. |  |
| **query_details** | [**Array&lt;QueryDetails&gt;**](QueryDetails.md) |  | [optional] |
| **search_log** | **String** | A log of the search results you found. | [optional][default to &#39;&#39;] |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::SearchStepWithQueryDetails.new(
  type: null,
  think: null,
  current_question: null,
  errored: null,
  search: null,
  query_details: null,
  search_log: null
)
```

