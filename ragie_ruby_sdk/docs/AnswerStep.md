# RagieRubySdk::AnswerStep

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  | [optional][default to &#39;answer&#39;] |
| **think** | **String** |  |  |
| **current_question** | **String** |  |  |
| **errored** | **Boolean** |  | [optional][default to false] |
| **other_resolved_question_ids** | **Array&lt;String&gt;** | A list of question ids that are no longer relevant to the current answer referenced by their IDs. | [optional] |
| **answer** | [**Answer**](Answer.md) |  |  |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::AnswerStep.new(
  type: null,
  think: null,
  current_question: null,
  errored: null,
  other_resolved_question_ids: null,
  answer: null
)
```

