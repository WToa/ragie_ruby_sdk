# RagieRubySdk::AuthenticatorSharepointConnection

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **provider** | **String** |  |  |
| **data** | [**SharepointData**](SharepointData.md) |  |  |
| **user_email** | **String** | The email of the Sharepoint account this is for |  |
| **credentials** | [**OAuthRefreshTokenCredentials**](OAuthRefreshTokenCredentials.md) |  |  |

## Example

```ruby
require 'ragie-ruby-sdk'

instance = RagieRubySdk::AuthenticatorSharepointConnection.new(
  provider: null,
  data: null,
  user_email: null,
  credentials: null
)
```

