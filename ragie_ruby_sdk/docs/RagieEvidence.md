# RagieRubySdk::RagieEvidence

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  | [optional][default to &#39;ragie&#39;] |
| **text** | **String** |  |  |
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

instance = RagieRubySdk::RagieEvidence.new(
  type: null,
  text: null,
  id: null,
  index: null,
  document_id: null,
  document_name: null,
  metadata: null,
  document_metadata: null,
  links: null
)
```

