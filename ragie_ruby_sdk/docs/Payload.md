# OpenapiClient::Payload

## Class instance methods

### `openapi_one_of`

Returns the list of classes defined in oneOf.

#### Example

```ruby
require 'openapi_client'

OpenapiClient::Payload.openapi_one_of
# =>
# [
#   :'CreateGoogleAuthenticator',
#   :'OAuthCredentials'
# ]
```

### `openapi_discriminator_name`

Returns the discriminator's property name.

#### Example

```ruby
require 'openapi_client'

OpenapiClient::Payload.openapi_discriminator_name
# => :'provider'
```

### `openapi_discriminator_name`

Returns the discriminator's mapping.

#### Example

```ruby
require 'openapi_client'

OpenapiClient::Payload.openapi_discriminator_mapping
# =>
# {
#   :'atlassian' => :'OAuthCredentials',
#   :'dropbox' => :'OAuthCredentials',
#   :'google' => :'CreateGoogleAuthenticator',
#   :'hubspot' => :'OAuthCredentials',
#   :'microsoft' => :'OAuthCredentials',
#   :'salesforce' => :'OAuthCredentials',
#   :'slack' => :'OAuthCredentials'
# }
```

### build

Find the appropriate object from the `openapi_one_of` list and casts the data into it.

#### Example

```ruby
require 'openapi_client'

OpenapiClient::Payload.build(data)
# => #<CreateGoogleAuthenticator:0x00007fdd4aab02a0>

OpenapiClient::Payload.build(data_that_doesnt_match)
# => nil
```

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| **data** | **Mixed** | data to be matched against the list of oneOf items |

#### Return type

- `CreateGoogleAuthenticator`
- `OAuthCredentials`
- `nil` (if no type matches)

