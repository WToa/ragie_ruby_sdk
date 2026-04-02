# RagieRubySdk::PartitionLimitParams

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **pages_hosted_limit_monthly** | **Integer** | Monthly limit of hosted pages added in the current month in the partition. | [optional] |
| **pages_processed_limit_monthly** | **Integer** | Monthly limit, in pages, for processed documents in the partition. | [optional] |
| **pages_hosted_limit_max** | **Integer** | Maximum limit, in pages, for hosted documents in the partition. | [optional] |
| **pages_processed_limit_max** | **Integer** | Maximum limit, in pages, for processed documents in the partition. | [optional] |
| **video_processed_limit_monthly** | **Integer** | Monthly limit, in minutes, for video processing in the partition. | [optional] |
| **video_processed_limit_max** | **Integer** | Maximum limit, in minutes, for video processing in the partition. | [optional] |
| **audio_processed_limit_monthly** | **Integer** | Monthly limit, in minutes, for audio processing in the partition. | [optional] |
| **audio_processed_limit_max** | **Integer** | Maximum limit, in minutes, for audio processing in the partition. | [optional] |
| **media_streamed_limit_monthly** | **Integer** | Monthly limit, in MBs, for media streamed from the partition. | [optional] |
| **media_streamed_limit_max** | **Integer** | Maximum limit, in MBs, for media streamed from the partition. | [optional] |
| **media_hosted_limit_monthly** | **Integer** | Monthly limit, in MBs, for media hosted in the partition. | [optional] |
| **media_hosted_limit_max** | **Integer** | Maximum limit, in MBs, for media hosted in the partition. | [optional] |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::PartitionLimitParams.new(
  pages_hosted_limit_monthly: null,
  pages_processed_limit_monthly: null,
  pages_hosted_limit_max: null,
  pages_processed_limit_max: null,
  video_processed_limit_monthly: null,
  video_processed_limit_max: null,
  audio_processed_limit_monthly: null,
  audio_processed_limit_max: null,
  media_streamed_limit_monthly: null,
  media_streamed_limit_max: null,
  media_hosted_limit_monthly: null,
  media_hosted_limit_max: null
)
```

