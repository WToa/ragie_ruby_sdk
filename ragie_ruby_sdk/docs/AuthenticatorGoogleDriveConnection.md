# OpenapiClient::AuthenticatorGoogleDriveConnection

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **provider** | **String** |  |  |
| **data** | [**Array&lt;GoogleFolderData&gt;**](GoogleFolderData.md) |  |  |
| **email** | **String** | The email of the Google Drive account this is for |  |
| **credentials** | [**OAuthRefreshTokenCredentials**](OAuthRefreshTokenCredentials.md) |  |  |

## Example

```ruby
require 'openapi_client'

instance = OpenapiClient::AuthenticatorGoogleDriveConnection.new(
  provider: null,
  data: null,
  email: null,
  credentials: null
)
```

