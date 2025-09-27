# RagieRubySdk::Request

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **input** | **String** | The text used to generate the response. Generally a question or a query. |  |
| **instructions** | **String** |  | [optional] |
| **tools** | [**Array&lt;Tool&gt;**](Tool.md) | The tools available to the agent. Currently the only tool is retrieve. The &#x60;default&#x60; partition is used by default unless an other partition is specified. | [optional] |
| **model** | **String** | The model to use for the agent. Currently the only model is deep-search. | [optional][default to &#39;deep-search&#39;] |
| **reasoning** | [**Reasoning**](Reasoning.md) | The reasoning to use for the agent. The default effort level is medium. | [optional] |
| **stream** | **Boolean** | Whether to stream the response | [optional][default to false] |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::Request.new(
  input: null,
  instructions: null,
  tools: null,
  model: null,
  reasoning: null,
  stream: null
)
```

