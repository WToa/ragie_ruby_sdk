# RagieRubySdk::Mode2

## Class instance methods

### `openapi_one_of`

Returns the list of classes defined in oneOf.

#### Example

```ruby
require 'ragie-ruby-sdk'

RagieRubySdk::Mode2.openapi_one_of
# =>
# [
#   :'Mode2OneOf',
#   :'String'
# ]
```

### build

Find the appropriate object from the `openapi_one_of` list and casts the data into it.

#### Example

```ruby
require 'ragie-ruby-sdk'

RagieRubySdk::Mode2.build(data)
# => #<Mode2OneOf:0x00007fdd4aab02a0>

RagieRubySdk::Mode2.build(data_that_doesnt_match)
# => nil
```

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| **data** | **Mixed** | data to be matched against the list of oneOf items |

#### Return type

- `Mode2OneOf`
- `String`
- `nil` (if no type matches)

