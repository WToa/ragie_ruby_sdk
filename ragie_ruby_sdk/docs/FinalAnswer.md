# RagieRubySdk::FinalAnswer

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **text** | **String** | The final answer to the question. |  |
| **evidence** | [**Array&lt;EvidenceInner&gt;**](EvidenceInner.md) | The evidence used to derive the answer. | [optional] |
| **steps** | [**Array&lt;StepsInner&gt;**](StepsInner.md) | The steps that led to the answer. | [optional] |
| **usage** | [**AgentHoppsModelsModelsUsage**](AgentHoppsModelsModelsUsage.md) | The usage of the models. | [optional] |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::FinalAnswer.new(
  text: null,
  evidence: null,
  steps: null,
  usage: null
)
```

