# RagieRubySdk::ApiDocumentElementLocation

## Class instance methods

### `openapi_one_of`

Returns the list of classes defined in oneOf.

#### Example

```ruby
require 'ragie_ruby_sdk'

RagieRubySdk::ApiDocumentElementLocation.openapi_one_of
# =>
# [
#   :'BoundingBoxLocation',
#   :'CharacterIndexLocation',
#   :'DurationLocation',
#   :'SpreadsheetLocation'
# ]
```

### `openapi_discriminator_name`

Returns the discriminator's property name.

#### Example

```ruby
require 'ragie_ruby_sdk'

RagieRubySdk::ApiDocumentElementLocation.openapi_discriminator_name
# => :'location_type'
```

### `openapi_discriminator_name`

Returns the discriminator's mapping.

#### Example

```ruby
require 'ragie_ruby_sdk'

RagieRubySdk::ApiDocumentElementLocation.openapi_discriminator_mapping
# =>
# {
#   :'bounding_box' => :'BoundingBoxLocation',
#   :'character_index' => :'CharacterIndexLocation',
#   :'duration' => :'DurationLocation',
#   :'spreadsheet' => :'SpreadsheetLocation'
# }
```

### build

Find the appropriate object from the `openapi_one_of` list and casts the data into it.

#### Example

```ruby
require 'ragie_ruby_sdk'

RagieRubySdk::ApiDocumentElementLocation.build(data)
# => #<BoundingBoxLocation:0x00007fdd4aab02a0>

RagieRubySdk::ApiDocumentElementLocation.build(data_that_doesnt_match)
# => nil
```

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| **data** | **Mixed** | data to be matched against the list of oneOf items |

#### Return type

- `BoundingBoxLocation`
- `CharacterIndexLocation`
- `DurationLocation`
- `SpreadsheetLocation`
- `nil` (if no type matches)

