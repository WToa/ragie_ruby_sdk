# RagieRubySdk::ConnectionLimitParams

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page_limit** | **Integer** | The maximum number of pages a connection will sync. The connection will be disabled after this limit is reached. Some in process documents may continue processing. Remove the limit by setting to &#x60;null&#x60;. | [optional] |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::ConnectionLimitParams.new(
  page_limit: null
)
```

