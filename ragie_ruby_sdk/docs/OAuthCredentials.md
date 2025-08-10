# RagieRubySdk::OAuthCredentials

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **provider** | **String** |  |  |
| **name** | **String** | The unique name of your authenticator, used to identify it and distinguish it from others. This name must be unique. Attempting to reuse the same name will result in an error. |  |
| **client_id** | **String** |  |  |
| **client_secret** | **String** |  |  |
| **domain** | **String** |  | [optional] |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::OAuthCredentials.new(
  provider: null,
  name: null,
  client_id: null,
  client_secret: null,
  domain: null
)
```

