# RagieRubySdk::Table

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  | [optional][default to &#39;Table&#39;] |
| **content** | **String** | The Table in HTML. |  |
| **description** | **String** | A brief summary of the content in the table. |  |
| **header_range** | **String** | Optional normalized header rows range used for &lt;thead&gt; construction. | [optional] |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::Table.new(
  type: null,
  content: null,
  description: null,
  header_range: null
)
```

