# RagieRubySdk::AuthenticatorGmailConnection

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **provider** | **String** |  |  |
| **data** | [**GmailData**](GmailData.md) |  |  |
| **email** | **String** | The email of the Google Drive account this is for |  |
| **credentials** | [**OAuthRefreshTokenCredentials**](OAuthRefreshTokenCredentials.md) |  |  |

## Example

```ruby
require 'ragie-ruby-sdk'

instance = RagieRubySdk::AuthenticatorGmailConnection.new(
  provider: null,
  data: null,
  email: null,
  credentials: null
)
```

