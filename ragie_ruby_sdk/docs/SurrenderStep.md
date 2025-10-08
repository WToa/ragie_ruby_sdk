# RagieRubySdk::SurrenderStep

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  | [optional][default to &#39;surrender&#39;] |
| **think** | **String** |  |  |
| **current_question** | **String** |  |  |
| **errored** | **Boolean** |  | [optional][default to false] |
| **partial_answer** | [**Answer**](Answer.md) | The a potential partial answer when a full answer was not possible. |  |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::SurrenderStep.new(
  type: null,
  think: null,
  current_question: null,
  errored: null,
  partial_answer: null
)
```

