# RagieRubySdk::Connection1

## Class instance methods

### `openapi_one_of`

Returns the list of classes defined in oneOf.

#### Example

```ruby
require 'ragie-ruby-sdk'

RagieRubySdk::Connection1.openapi_one_of
# =>
# [
#   :'AuthenticatorConfluenceConnection',
#   :'AuthenticatorDropboxConnection',
#   :'AuthenticatorGmailConnection',
#   :'AuthenticatorGoogleDriveConnection',
#   :'AuthenticatorHubspotConnection',
#   :'AuthenticatorJiraConnection',
#   :'AuthenticatorNotionConnection',
#   :'AuthenticatorOnedriveConnection',
#   :'AuthenticatorSalesforceConnection',
#   :'AuthenticatorSharepointConnection',
#   :'AuthenticatorSlackConnection'
# ]
```

### `openapi_discriminator_name`

Returns the discriminator's property name.

#### Example

```ruby
require 'ragie-ruby-sdk'

RagieRubySdk::Connection1.openapi_discriminator_name
# => :'provider'
```

### `openapi_discriminator_name`

Returns the discriminator's mapping.

#### Example

```ruby
require 'ragie-ruby-sdk'

RagieRubySdk::Connection1.openapi_discriminator_mapping
# =>
# {
#   :'confluence' => :'AuthenticatorConfluenceConnection',
#   :'dropbox' => :'AuthenticatorDropboxConnection',
#   :'gmail' => :'AuthenticatorGmailConnection',
#   :'google_drive' => :'AuthenticatorGoogleDriveConnection',
#   :'hubspot' => :'AuthenticatorHubspotConnection',
#   :'jira' => :'AuthenticatorJiraConnection',
#   :'notion' => :'AuthenticatorNotionConnection',
#   :'onedrive' => :'AuthenticatorOnedriveConnection',
#   :'salesforce' => :'AuthenticatorSalesforceConnection',
#   :'sharepoint' => :'AuthenticatorSharepointConnection',
#   :'slack' => :'AuthenticatorSlackConnection'
# }
```

### build

Find the appropriate object from the `openapi_one_of` list and casts the data into it.

#### Example

```ruby
require 'ragie-ruby-sdk'

RagieRubySdk::Connection1.build(data)
# => #<AuthenticatorConfluenceConnection:0x00007fdd4aab02a0>

RagieRubySdk::Connection1.build(data_that_doesnt_match)
# => nil
```

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| **data** | **Mixed** | data to be matched against the list of oneOf items |

#### Return type

- `AuthenticatorConfluenceConnection`
- `AuthenticatorDropboxConnection`
- `AuthenticatorGmailConnection`
- `AuthenticatorGoogleDriveConnection`
- `AuthenticatorHubspotConnection`
- `AuthenticatorJiraConnection`
- `AuthenticatorNotionConnection`
- `AuthenticatorOnedriveConnection`
- `AuthenticatorSalesforceConnection`
- `AuthenticatorSharepointConnection`
- `AuthenticatorSlackConnection`
- `nil` (if no type matches)

