# RagieRubySdk::PlanStep

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  | [optional][default to &#39;plan&#39;] |
| **think** | **String** |  |  |
| **current_question** | **String** |  |  |
| **questions_to_answer** | **Array&lt;String&gt;** |  |  |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::PlanStep.new(
  type: null,
  think: null,
  current_question: null,
  questions_to_answer: null
)
```

