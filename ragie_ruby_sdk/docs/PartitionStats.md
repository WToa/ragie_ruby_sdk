# OpenapiClient::PartitionStats

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **pages_processed_monthly** | **Float** | Number of pages processed in the current month in this partition. |  |
| **pages_hosted_monthly** | **Float** | Number of hosted pages added in the current month in this partition. |  |
| **pages_processed_total** | **Float** | Total number of pages processed in this partition. |  |
| **pages_hosted_total** | **Float** | Total number of hosted pages in this partition. |  |
| **document_count** | **Integer** | Total number of documents, inclusive of all files types, in this partition. |  |
| **video_processed_monthly** | **Float** | Total number of seconds of video processed in the current month in this partition. |  |
| **video_processed_total** | **Float** | Total number of seconds of video processed in this partition. |  |
| **audio_processed_monthly** | **Float** | Total number of seconds of audio processed in the current month in this partition. |  |
| **audio_processed_total** | **Float** | Total number of seconds of audio processed in this partition. |  |
| **media_streamed_monthly** | **Float** | Total number of MBs streamed in the current month in this partition. |  |
| **media_streamed_total** | **Float** | Total number of MBs streamed in this partition. |  |
| **media_hosted_monthly** | **Float** | Total number of MBs hosted in the current month in this partition. |  |
| **media_hosted_total** | **Float** | Total number of MBs hosted in this partition. |  |

## Example

```ruby
require 'openapi_client'

instance = OpenapiClient::PartitionStats.new(
  pages_processed_monthly: null,
  pages_hosted_monthly: null,
  pages_processed_total: null,
  pages_hosted_total: null,
  document_count: null,
  video_processed_monthly: null,
  video_processed_total: null,
  audio_processed_monthly: null,
  audio_processed_total: null,
  media_streamed_monthly: null,
  media_streamed_total: null,
  media_hosted_monthly: null,
  media_hosted_total: null
)
```

