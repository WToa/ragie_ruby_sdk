# RagieRubySdk::ApiElement

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  | [optional][default to &#39;Text&#39;] |
| **content** | **String** |  |  |
| **handwritten** | **Boolean** | True if handwritten, false otherwise | [optional][default to false] |
| **latex** | **String** |  | [optional] |
| **description** | **String** | A detailed description of what the visual depicts. |  |
| **header_range** | **String** |  | [optional] |
| **base64_data** | **String** |  | [optional] |
| **label** | **String** | The main question/label for the field. |  |
| **is_signed** | **Boolean** | True if a handwritten signature, digital signature, or stamp is present. False if blank. |  |
| **signer_name** | **String** |  | [optional] |
| **date** | **String** |  | [optional] |
| **key** | **String** | The label/attribute name (e.g. &#39;Date&#39;, &#39;Invoice #&#39;). |  |
| **value** | **String** |  |  |
| **input_type** | **String** | Type of input. |  |
| **options** | [**Array&lt;FormOption&gt;**](FormOption.md) |  | [optional] |
| **selected_values** | **Array&lt;String&gt;** |  | [optional] |
| **help_text** | **String** |  | [optional] |
| **language** | **String** | The language the code is written in | [optional][default to &#39;&#39;] |
| **modality_data** | [**Array&lt;WordModality&gt;**](WordModality.md) | A list of information per word that shows the word, start time, and end time |  |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::ApiElement.new(
  type: null,
  content: null,
  handwritten: null,
  latex: null,
  description: null,
  header_range: null,
  base64_data: null,
  label: null,
  is_signed: null,
  signer_name: null,
  date: null,
  key: null,
  value: null,
  input_type: null,
  options: null,
  selected_values: null,
  help_text: null,
  language: null,
  modality_data: null
)
```

