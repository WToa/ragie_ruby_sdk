# RagieRubySdk::SpreadsheetLocation

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **location_type** | **String** |  | [optional][default to &#39;spreadsheet&#39;] |
| **range** | **String** |  | [optional] |
| **sheet_name** | **String** |  | [optional] |
| **sheet_index** | **Integer** |  | [optional] |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::SpreadsheetLocation.new(
  location_type: null,
  range: null,
  sheet_name: null,
  sheet_index: null
)
```

