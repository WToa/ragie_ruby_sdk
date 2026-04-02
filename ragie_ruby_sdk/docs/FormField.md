# RagieRubySdk::FormField

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  | [optional][default to &#39;FormField&#39;] |
| **content** | **String** | The text content of the form field, including both the label and the value |  |
| **input_type** | **String** | Type of input. |  |
| **label** | **String** | The main question/label for the field. |  |
| **value** | **String** | The filled text. For single checkbox: &#39;true&#39;/&#39;false&#39;. | [optional] |
| **options** | [**Array&lt;FormOption&gt;**](FormOption.md) | List of available options. | [optional] |
| **selected_values** | **Array&lt;String&gt;** | The &#39;label&#39; of the selected option(s). | [optional] |
| **help_text** | **String** | The help text for the form field. | [optional] |

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

