# RagieRubySdk::InstructionEntityExtractionLog

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **created_at** | **Time** |  |  |
| **updated_at** | **Time** |  |  |
| **instruction_id** | **String** | The ID of the instruction which generated the entity. |  |
| **document_id** | **String** | The ID of the document which the entity was produced from. |  |
| **scope** | **String** | Whether extraction was attempted at document scope or chunk scope. |  |
| **chunk_index** | **Integer** | Chunk index when scope is &#x60;chunk&#x60;; null when scope is &#x60;document&#x60;. | [optional] |
| **status** | **String** | Extraction status for this attempt. |  |
| **reason_code** | **String** | Machine-readable reason code when available. Values: &#x60;NO_MATCH&#x60;, &#x60;AMBIGUOUS&#x60;, &#x60;OUT_OF_SCOPE&#x60;, &#x60;SCHEMA_INVALID&#x60;, &#x60;MODEL_ERROR&#x60;. | [optional] |
| **reason** | **String** | Optional debug text for this attempt. Usually model-provided; may be system-generated when normalization/parsing fails. | [optional] |
| **errors** | **Array&lt;String&gt;** | Machine-readable extraction error identifiers. Public responses map internal entity-shape validation failures to &#x60;unexpected_error&#x60;. Common values include &#x60;unexpected_error&#x60;, &#x60;invalid_instruction_schema&#x60;, and &#x60;empty_completion_content&#x60;. Raw provider/runtime error strings may also appear. | [optional] |
| **page_count** | **Float** | Input pages for this extraction attempt. |  |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::InstructionEntityExtractionLog.new(
  id: null,
  created_at: null,
  updated_at: null,
  instruction_id: null,
  document_id: null,
  scope: null,
  chunk_index: null,
  status: null,
  reason_code: null,
  reason: null,
  errors: null,
  page_count: null
)
```

