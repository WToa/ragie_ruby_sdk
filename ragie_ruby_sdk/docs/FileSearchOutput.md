# RagieRubySdk::FileSearchOutput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **queries** | **Array&lt;String&gt;** | The queries used to search for files. |  |
| **status** | **String** |  | [optional][default to &#39;searching&#39;] |
| **type** | **String** |  |  |
| **results** | [**Array&lt;FileSearchResult&gt;**](FileSearchResult.md) | The results of the file search tool call. |  |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::FileSearchOutput.new(
  id: null,
  queries: null,
  status: null,
  type: null,
  results: null
)
```

