# RagieRubySdk::CodeStep

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  | [optional][default to &#39;code&#39;] |
| **think** | **String** |  |  |
| **current_question** | **String** |  |  |
| **errored** | **Boolean** |  | [optional][default to false] |
| **code_issue** | **String** | The natural language description of the code issue you need to solve. |  |
| **code** | **String** | The code you generated to solve the code issue. | [optional][default to &#39;&#39;] |
| **code_result** | **String** | The result of the code you generated after executing it. | [optional][default to &#39;&#39;] |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::CodeStep.new(
  type: null,
  think: null,
  current_question: null,
  errored: null,
  code_issue: null,
  code: null,
  code_result: null
)
```

