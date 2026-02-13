# RagieRubySdk::WebcrawlerData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **url** | **String** |  |  |
| **restrict_domain** | **Boolean** |  | [optional][default to true] |
| **max_depth** | **Integer** |  | [optional] |
| **max_pages** | **Integer** |  | [optional] |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::WebcrawlerData.new(
  url: null,
  restrict_domain: null,
  max_depth: null,
  max_pages: null
)
```

