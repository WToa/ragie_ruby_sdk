# RagieRubySdk::RetrieveParams

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | The query to search with when retrieving document chunks. |  |
| **top_k** | **Integer** | The maximum number of chunks to return. Defaults to 8. | [optional][default to 8] |
| **filter** | **Hash&lt;String, Object&gt;** | The metadata search filter on documents. Returns chunks only from documents which match the filter. The following filter operators are supported: $eq - Equal to (number, string, boolean), $ne - Not equal to (number, string, boolean), $gt - Greater than (number), $gte - Greater than or equal to (number), $lt - Less than (number), $lte - Less than or equal to (number), $in - In array (string or number), $nin - Not in array (string or number). The operators can be combined with AND and OR. Read [Metadata &amp; Filters guide](https://docs.ragie.ai/docs/metadata-filters) for more details and examples. | [optional] |
| **rerank** | **Boolean** | Reranks the chunks for semantic relevancy post cosine similarity. Will be slower but returns a subset of highly relevant chunks. Best for reducing hallucinations and improving accuracy for LLM generation. | [optional][default to false] |
| **max_chunks_per_document** | **Integer** | Maximum number of chunks to retrieve per document. Use this to increase the number of documents the final chunks are retrieved from. This feature is in beta and may change in the future. | [optional] |
| **partition** | **String** | The partition to scope a retrieval to. If omitted, the retrieval will be scoped to the default partition, which includes any documents that have not been created in a partition. | [optional] |
| **recency_bias** | **Boolean** | Enables recency bias which will favor more recent documents vs older documents. https://docs.ragie.ai/docs/retrievals-recency-bias | [optional][default to false] |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::RetrieveParams.new(
  query: null,
  top_k: null,
  filter: null,
  rerank: null,
  max_chunks_per_document: null,
  partition: null,
  recency_bias: null
)
```

