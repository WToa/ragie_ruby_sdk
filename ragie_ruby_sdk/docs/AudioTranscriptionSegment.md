# RagieRubySdk::AudioTranscriptionSegment

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **content** | **String** |  | [optional] |
| **modality_data** | [**Array&lt;WordModality&gt;**](WordModality.md) | A list of information per word that shows the word, start time, and end time |  |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::AudioTranscriptionSegment.new(
  content: null,
  modality_data: null
)
```

