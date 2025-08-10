# RagieRubySdk::AuthenticatorSlackConnection

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **provider** | **String** |  |  |
| **data** | [**SlackData**](SlackData.md) |  |  |
| **user_email** | **String** | The email of the Slack account this is for |  |
| **credentials** | [**AccessTokenCredentials**](AccessTokenCredentials.md) |  |  |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::AuthenticatorSlackConnection.new(
  provider: null,
  data: null,
  user_email: null,
  credentials: null
)
```

