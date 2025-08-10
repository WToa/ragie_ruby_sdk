# RagieRubySdk::AuthenticatorOnedriveConnection

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **provider** | **String** |  |  |
| **data** | [**OnedriveData**](OnedriveData.md) |  |  |
| **user_email** | **String** | The email of the Onedrive account this is for |  |
| **credentials** | [**OAuthRefreshTokenCredentials**](OAuthRefreshTokenCredentials.md) |  |  |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::AuthenticatorOnedriveConnection.new(
  provider: null,
  data: null,
  user_email: null,
  credentials: null
)
```

