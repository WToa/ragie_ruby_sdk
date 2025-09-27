# RagieRubySdk::FinalAnswerStepsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  | [optional][default to &#39;answer&#39;] |
| **think** | **String** |  |  |
| **current_question** | **String** |  |  |
| **other_resolved_question_ids** | **Array&lt;String&gt;** | A list of questions ids that are no longer relevant to the current answer referenced by their IDs. | [optional] |
| **answer** | [**Answer**](Answer.md) |  |  |
| **search** | [**Search**](Search.md) |  |  |
| **questions_to_answer** | **Array&lt;String&gt;** |  |  |
| **code_issue** | **String** | The natural language description of the code issue you need to solve. |  |
| **code** | **String** | The code you generated to solve the code issue. | [optional][default to &#39;&#39;] |
| **code_result** | **String** | The result of the code you generated after executing it. | [optional][default to &#39;&#39;] |
| **partial_answer** | [**Answer**](Answer.md) |  |  |
| **eval_passed** | **Boolean** |  |  |
| **eval_reason** | **String** |  |  |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::FinalAnswerStepsInner.new(
  type: null,
  think: null,
  current_question: null,
  other_resolved_question_ids: null,
  answer: null,
  search: null,
  questions_to_answer: null,
  code_issue: null,
  code: null,
  code_result: null,
  partial_answer: null,
  eval_passed: null,
  eval_reason: null
)
```

