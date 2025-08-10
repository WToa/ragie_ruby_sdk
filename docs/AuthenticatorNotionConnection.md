# RagieRubySdk::AuthenticatorNotionConnection

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **provider** | **String** |  |  |
| **workspace_id** | **String** |  |  |
| **workspace_name** | **String** |  |  |
| **user_email** | **String** | The email of the Notion account this is for |  |
| **credentials** | [**AccessTokenCredentials**](AccessTokenCredentials.md) |  |  |

## Example

```ruby
require 'ragie-ruby-sdk'

instance = RagieRubySdk::AuthenticatorNotionConnection.new(
  provider: null,
  workspace_id: null,
  workspace_name: null,
  user_email: null,
  credentials: null
)
```

