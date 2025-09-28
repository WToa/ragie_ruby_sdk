# RagieRubySdk::CodeInterpreterEvidence

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  | [optional][default to &#39;code_interpreter&#39;] |
| **text** | **String** |  |  |
| **code** | **String** | The code that was executed. |  |
| **code_issue** | **String** | The issue that the code was written to solve. |  |
| **code_result** | **String** | The result of the code that was executed. |  |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::CodeInterpreterEvidence.new(
  type: null,
  text: null,
  code: null,
  code_issue: null,
  code_result: null
)
```

