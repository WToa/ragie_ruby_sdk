# RagieRubySdk::EvaluatedAnswerStep

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  | [optional][default to &#39;evaluated_answer&#39;] |
| **think** | **String** |  |  |
| **current_question** | **String** |  |  |
| **answer** | [**Answer**](Answer.md) |  |  |
| **other_resolved_question_ids** | **Array&lt;String&gt;** | A list of questions ids that are no longer relevant to the current answer referenced by their IDs. | [optional] |
| **eval_passed** | **Boolean** |  |  |
| **eval_reason** | **String** |  |  |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::EvaluatedAnswerStep.new(
  type: null,
  think: null,
  current_question: null,
  answer: null,
  other_resolved_question_ids: null,
  eval_passed: null,
  eval_reason: null
)
```

