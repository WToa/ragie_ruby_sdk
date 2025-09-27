# RagieRubySdk::SurrenderStep

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  | [optional][default to &#39;surrender&#39;] |
| **think** | **String** |  |  |
| **current_question** | **String** |  |  |
| **partial_answer** | [**Answer**](Answer.md) |  |  |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::SurrenderStep.new(
  type: null,
  think: null,
  current_question: null,
  partial_answer: null
)
```

