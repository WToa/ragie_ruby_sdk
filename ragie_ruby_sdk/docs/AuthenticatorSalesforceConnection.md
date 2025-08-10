# RagieRubySdk::AuthenticatorSalesforceConnection

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **provider** | **String** |  |  |
| **user_email** | **String** | The email of the Salesforce account this is for |  |
| **url** | **String** | The url of your Salesforce instance, where you go to login. |  |
| **credentials** | [**OAuthRefreshTokenCredentials**](OAuthRefreshTokenCredentials.md) |  |  |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::AuthenticatorSalesforceConnection.new(
  provider: null,
  user_email: null,
  url: null,
  credentials: null
)
```

