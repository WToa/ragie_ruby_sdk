# RagieRubySdk::FinalAnswerEvidenceInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  | [optional][default to &#39;code_interpreter&#39;] |
| **text** | **String** |  |  |
| **code** | **String** |  |  |
| **code_issue** | **String** |  |  |
| **code_result** | **String** |  |  |
| **id** | **String** |  |  |
| **index** | **Integer** |  |  |
| **document_id** | **String** |  |  |
| **document_name** | **String** |  |  |
| **metadata** | **Hash&lt;String, Object&gt;** |  | [optional] |
| **document_metadata** | **Hash&lt;String, Object&gt;** |  | [optional] |
| **links** | [**Hash&lt;String, SearchResultLink&gt;**](SearchResultLink.md) |  | [optional] |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::FinalAnswerEvidenceInner.new(
  type: null,
  text: null,
  code: null,
  code_issue: null,
  code_result: null,
  id: null,
  index: null,
  document_id: null,
  document_name: null,
  metadata: null,
  document_metadata: null,
  links: null
)
```

