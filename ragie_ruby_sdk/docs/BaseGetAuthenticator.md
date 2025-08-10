# OpenapiClient::BaseGetAuthenticator

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **provider** | **String** |  |  |
| **name** | **String** | The unique name of your authenticator, used to identify it and distinguish it from others. This name must be unique. Attempting to reuse the same name will result in an error. |  |
| **id** | **String** |  |  |

## Example

```ruby
require 'openapi_client'

instance = OpenapiClient::BaseGetAuthenticator.new(
  provider: null,
  name: null,
  id: null
)
```

