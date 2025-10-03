# RagieRubySdk::SearchStep

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  | [optional][default to &#39;base_search&#39;] |
| **think** | **String** |  |  |
| **current_question** | **String** |  |  |
| **search** | [**Search**](Search.md) | The search request to be made. |  |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::SearchStep.new(
  type: null,
  think: null,
  current_question: null,
  search: null
)
```

