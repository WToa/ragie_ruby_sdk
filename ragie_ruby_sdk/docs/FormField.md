# RagieRubySdk::FormField

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  | [optional][default to &#39;FormField&#39;] |
| **content** | **String** | The text content of the form field, including both the label and the value |  |
| **input_type** | **String** | Type of input. |  |
| **label** | **String** | The main question/label for the field. |  |
| **value** | **String** |  | [optional] |
| **options** | [**Array&lt;FormOption&gt;**](FormOption.md) |  | [optional] |
| **selected_values** | **Array&lt;String&gt;** |  | [optional] |
| **help_text** | **String** |  | [optional] |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::FormField.new(
  type: null,
  content: null,
  input_type: null,
  label: null,
  value: null,
  options: null,
  selected_values: null,
  help_text: null
)
```

