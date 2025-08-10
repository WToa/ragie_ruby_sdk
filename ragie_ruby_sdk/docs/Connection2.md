# RagieRubySdk::Connection2

## Class instance methods

### `openapi_one_of`

Returns the list of classes defined in oneOf.

#### Example

```ruby
require 'ragie_ruby_sdk'

RagieRubySdk::Connection2.openapi_one_of
# =>
# [
#   :'PublicBackblazeConnection',
#   :'PublicFreshdeskConnection',
#   :'PublicGCSConnection',
#   :'PublicIntercomConnection',
#   :'PublicS3CompatibleConnection',
#   :'PublicZendeskConnection'
# ]
```

### `openapi_discriminator_name`

Returns the discriminator's property name.

#### Example

```ruby
require 'ragie_ruby_sdk'

RagieRubySdk::Connection2.openapi_discriminator_name
# => :'provider'
```

### `openapi_discriminator_name`

Returns the discriminator's mapping.

#### Example

```ruby
require 'ragie_ruby_sdk'

RagieRubySdk::Connection2.openapi_discriminator_mapping
# =>
# {
#   :'backblaze' => :'PublicBackblazeConnection',
#   :'freshdesk' => :'PublicFreshdeskConnection',
#   :'gcs' => :'PublicGCSConnection',
#   :'intercom' => :'PublicIntercomConnection',
#   :'s3' => :'PublicS3CompatibleConnection',
#   :'zendesk' => :'PublicZendeskConnection'
# }
```

### build

Find the appropriate object from the `openapi_one_of` list and casts the data into it.

#### Example

```ruby
require 'ragie_ruby_sdk'

RagieRubySdk::Connection2.build(data)
# => #<PublicBackblazeConnection:0x00007fdd4aab02a0>

RagieRubySdk::Connection2.build(data_that_doesnt_match)
# => nil
```

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| **data** | **Mixed** | data to be matched against the list of oneOf items |

#### Return type

- `PublicBackblazeConnection`
- `PublicFreshdeskConnection`
- `PublicGCSConnection`
- `PublicIntercomConnection`
- `PublicS3CompatibleConnection`
- `PublicZendeskConnection`
- `nil` (if no type matches)

