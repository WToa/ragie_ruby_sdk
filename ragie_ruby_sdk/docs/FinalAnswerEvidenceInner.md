# RagieRubySdk::FinalAnswerEvidenceInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  | [optional][default to &#39;code_interpreter&#39;] |
| **text** | **String** |  |  |
| **code** | **String** | The code that was executed. |  |
| **code_issue** | **String** | The issue that the code was written to solve. |  |
| **code_result** | **String** | The result of the code that was executed. |  |
| **id** | **String** | The chunk id of the evidence. |  |
| **index** | **Integer** | The index of the chunk in the document. |  |
| **document_id** | **String** | The document id of the document containing the chunk being used as evidence. |  |
| **document_name** | **String** | The name of the document that contains the chunk being used as evidence. |  |
| **metadata** | **Hash&lt;String, Object&gt;** | The metadata of the chunk being used as evidence. | [optional] |
| **document_metadata** | **Hash&lt;String, Object&gt;** | The metadata of the document that contains the evidence. | [optional] |
| **links** | [**Hash&lt;String, SearchResultLink&gt;**](SearchResultLink.md) | The links to the evidence. | [optional] |

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

