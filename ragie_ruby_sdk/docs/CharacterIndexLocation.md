# RagieRubySdk::CharacterIndexLocation

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **location_type** | **String** |  | [optional][default to &#39;character_index&#39;] |
| **start_char_index** | **Integer** | Start character index (inclusive) |  |
| **end_char_index** | **Integer** | End character index (exclusive) |  |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::CharacterIndexLocation.new(
  location_type: null,
  start_char_index: null,
  end_char_index: null
)
```

