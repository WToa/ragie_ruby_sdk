# RagieRubySdk::CreatePartitionParams

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  |  |
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

## Example

```ruby
require 'ragie-ruby-sdk'

instance = RagieRubySdk::CreatePartitionParams.new(
  name: null,
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
  media_hosted_limit_max: null
)
```

