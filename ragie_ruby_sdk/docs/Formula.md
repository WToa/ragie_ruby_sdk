# RagieRubySdk::Formula

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  | [optional][default to &#39;Formula&#39;] |
| **content** | **String** | The formula as plain text. |  |
| **latex** | **String** | The LaTeX representation of the formula. | [optional] |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::Formula.new(
  type: null,
  content: null,
  latex: null
)
```

