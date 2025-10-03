# RagieRubySdk::FinalAnswerStepsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  | [optional][default to &#39;answer&#39;] |
| **think** | **String** |  |  |
| **current_question** | **String** |  |  |
| **other_resolved_question_ids** | **Array&lt;String&gt;** | A list of questions ids that are no longer relevant to the current answer referenced by their IDs. | [optional] |
| **answer** | [**Answer**](Answer.md) |  |  |
| **search** | [**Search**](Search.md) | The search request to be made. |  |
| **query_details** | [**Array&lt;QueryDetails&gt;**](QueryDetails.md) |  | [optional] |
| **search_log** | **String** | A log of the search results you found. | [optional][default to &#39;&#39;] |
| **questions_to_answer** | **Array&lt;String&gt;** | The questions that need to be answered to answer the original question. | [optional] |
| **code_issue** | **String** | The natural language description of the code issue you need to solve. |  |
| **code** | **String** | The code you generated to solve the code issue. | [optional][default to &#39;&#39;] |
| **code_result** | **String** | The result of the code you generated after executing it. | [optional][default to &#39;&#39;] |
| **partial_answer** | [**Answer**](Answer.md) | The a potential partial answer when a full answer was not possible. |  |
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
  query_details: null,
  search_log: null,
  questions_to_answer: null,
  code_issue: null,
  code: null,
  code_result: null,
  partial_answer: null,
  eval_passed: null,
  eval_reason: null
)
```

