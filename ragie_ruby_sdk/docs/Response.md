# RagieRubySdk::Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **object** | **String** |  | [optional][default to &#39;response&#39;] |
| **created_at** | **Integer** |  |  |
| **status** | **String** |  |  |
| **error** | **String** |  | [optional] |
| **incomplete_details** | [**Null**](Null.md) |  | [optional] |
| **instructions** | **String** |  | [optional] |
| **max_output_tokens** | [**Null**](Null.md) |  | [optional] |
| **model** | **String** |  | [optional][default to &#39;deep-search&#39;] |
| **output** | [**Array&lt;OutputInner&gt;**](OutputInner.md) |  |  |
| **output_parsed** | [**FinalAnswer**](FinalAnswer.md) |  | [optional] |
| **tools** | [**Array&lt;Tool&gt;**](Tool.md) |  |  |
| **reasoning** | [**Reasoning**](Reasoning.md) |  |  |
| **parallel_tool_calls** | **Boolean** |  | [optional][default to false] |
| **store** | **Boolean** |  | [optional][default to false] |
| **temperature** | **Float** |  | [optional][default to 1.0] |
| **previous_response_id** | **String** |  | [optional] |
| **tool_choice** | **String** |  | [optional][default to &#39;auto&#39;] |
| **top_p** | **Float** |  | [optional][default to 1.0] |
| **truncation** | **String** |  | [optional][default to &#39;disabled&#39;] |
| **usage** | [**RagieApiSchemaResponseUsage**](RagieApiSchemaResponseUsage.md) |  |  |
| **user** | [**Null**](Null.md) |  | [optional] |
| **metadata** | **Hash&lt;String, Object&gt;** |  | [optional] |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::Response.new(
  id: null,
  object: null,
  created_at: null,
  status: null,
  error: null,
  incomplete_details: null,
  instructions: null,
  max_output_tokens: null,
  model: null,
  output: null,
  output_parsed: null,
  tools: null,
  reasoning: null,
  parallel_tool_calls: null,
  store: null,
  temperature: null,
  previous_response_id: null,
  tool_choice: null,
  top_p: null,
  truncation: null,
  usage: null,
  user: null,
  metadata: null
)
```

