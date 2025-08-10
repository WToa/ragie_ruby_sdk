# RagieRubySdk::AuthenticatorDropboxConnection

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **provider** | **String** |  |  |
| **data** | [**FolderData**](FolderData.md) |  |  |
| **email** | **String** | The email of the Dropbox account this is for |  |
| **credentials** | [**OAuthRefreshTokenCredentials**](OAuthRefreshTokenCredentials.md) |  |  |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::AuthenticatorDropboxConnection.new(
  provider: null,
  data: null,
  email: null,
  credentials: null
)
```

