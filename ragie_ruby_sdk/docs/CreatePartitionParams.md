# RagieRubySdk::CreatePartitionParams

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  |  |
| **description** | **String** |  | [optional] |
| **pages_hosted_limit_monthly** | **Integer** |  | [optional] |
| **pages_processed_limit_monthly** | **Integer** |  | [optional] |
| **pages_hosted_limit_max** | **Integer** |  | [optional] |
| **pages_processed_limit_max** | **Integer** |  | [optional] |
| **audio_processed_limit_monthly** | **Integer** |  | [optional] |
| **audio_processed_limit_max** | **Integer** |  | [optional] |
| **video_processed_limit_monthly** | **Integer** |  | [optional] |
| **video_processed_limit_max** | **Integer** |  | [optional] |
| **media_streamed_limit_monthly** | **Integer** |  | [optional] |
| **media_streamed_limit_max** | **Integer** |  | [optional] |
| **media_hosted_limit_monthly** | **Integer** |  | [optional] |
| **media_hosted_limit_max** | **Integer** |  | [optional] |
| **metadata_schema** | [**Hash&lt;String, CreatePartitionParamsMetadataSchemaValue&gt;**](CreatePartitionParamsMetadataSchemaValue.md) |  | [optional] |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::CreatePartitionParams.new(
  name: null,
  description: null,
  pages_hosted_limit_monthly: null,
  pages_processed_limit_monthly: null,
  pages_hosted_limit_max: null,
  pages_processed_limit_max: null,
  audio_processed_limit_monthly: null,
  audio_processed_limit_max: null,
  video_processed_limit_monthly: null,
  video_processed_limit_max: null,
  media_streamed_limit_monthly: null,
  media_streamed_limit_max: null,
  media_hosted_limit_monthly: null,
  media_hosted_limit_max: null,
  metadata_schema: null
)
```

