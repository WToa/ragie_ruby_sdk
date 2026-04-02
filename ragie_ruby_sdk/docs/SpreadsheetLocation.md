# RagieRubySdk::SpreadsheetLocation

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **location_type** | **String** |  | [optional][default to &#39;spreadsheet&#39;] |
| **range** | **String** | Excel-style range like &#39;A1:C10&#39; | [optional] |
| **sheet_name** | **String** | Name of the sheet | [optional] |
| **sheet_index** | **Integer** | 0-based index of the sheet | [optional] |

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

