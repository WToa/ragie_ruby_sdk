# RagieRubySdk::ReasoningOutput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique ID of the reasoning output. |  |
| **summary** | [**Array&lt;ReasoningSummary&gt;**](ReasoningSummary.md) | The summary of the reasoning. |  |
| **type** | **String** |  | [optional][default to &#39;reasoning&#39;] |
| **content** | [**Array&lt;ReasoningText&gt;**](ReasoningText.md) | The content of the reasoning. |  |
| **encrypted_content** | **String** | The encrypted content of the reasoning output. |  |
| **status** | **String** |  | [optional][default to &#39;completed&#39;] |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::ReasoningOutput.new(
  id: null,
  summary: null,
  type: null,
  content: null,
  encrypted_content: null,
  status: null
)
```

