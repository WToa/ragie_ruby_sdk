# RagieRubySdk::FailedStep

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  | [optional][default to &#39;failed&#39;] |
| **think** | **String** |  |  |
| **current_question** | **String** |  |  |
| **errored** | **Boolean** |  | [optional][default to false] |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::FailedStep.new(
  type: null,
  think: null,
  current_question: null,
  errored: null
)
```

