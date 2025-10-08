# RagieRubySdk::PlanStep

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  | [optional][default to &#39;plan&#39;] |
| **think** | **String** |  |  |
| **current_question** | **String** |  |  |
| **errored** | **Boolean** |  | [optional][default to false] |
| **questions_to_answer** | **Array&lt;String&gt;** | The questions that need to be answered to answer the original question. | [optional] |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::PlanStep.new(
  type: null,
  think: null,
  current_question: null,
  errored: null,
  questions_to_answer: null
)
```

